---
title: Appliquer les données de démonstration Project Operations à un environnement hébergé par le cloud Finance
description: Ce sujet explique comment appliquer les données de démonstration entre Project Operations et un environnement hébergé dans le cloud Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096619"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a>Appliquer les données de démonstration Project Operations à un environnement hébergé par le cloud Finance

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

> [!IMPORTANT]
> Cette rubrique ne s'applique qu'à Microsoft Dynamics 365 Finance version 10.0.13 et ne peut être effectuée que sur un environnement hébergé dans le cloud. Suivez les étapes de cette rubrique **AVANT** d’appliquer des mises à jour de qualité à l’environnement.

1. Dans votre projet LCS, ouvrez la page **Détails de l’environnement**. Notez qu’elle inclut les détails nécessaires pour se connecter à l’environnement à l’aide du protocole RDP (Remote Desktop Protocol).

![Détails de l’environnement](./media/1EnvironmentDetails.png)

Le premier ensemble d’informations d’identification mises en évidence sont les informations d’identification du compte local et contiennent un lien hypertexte vers la connexion Bureau à distance. Les informations d’identification incluent le nom d’utilisateur et le mot de passe de l’administrateur de l’environnement. Le deuxième ensemble d’informations d’identification est utilisé pour se connecter à SQL Server dans cet environnement.

2. Connectez-vous à l’environnement à distance par le lien hypertexte dans **Comptes locaux** et utilisez les **Informations d’identification du compte local** pour vous authentifier.
3. Accédez à **IIS (Internet Information Services)** > **Pools d’applications** > **AOSService** et arrêtez le service. Vous arrêtez le service à ce stade afin de pouvoir continuer à remplacer la base de données SQL.

![Arrêter AOS](./media/2StopAOS.png)

4. Accédez à **Services** et arrêtez les deux éléments suivants :

- Microsoft Dynamics 365 Unified Operations : Service de gestion des lots
- Microsoft Dynamics 365 Unified Operations : Cadre d’importation et d’exportation des données

![Arrêter les services](./media/3StopServices.png)

5. Ouvrez Microsoft SQL Server Management Studio. Connectez-vous avec les informations d’identification SQL Server et utilisez l’utilisateur et le mot de passe axdbadmin de la page **Détails des environnements** de LCS.

![SQL Server Management Studio](./media/4SSMS.png)

6. Dans l’Explorateur d’objets, **Bases de données** et localisez **AXDB**. Vous allez remplacer la base de données par une nouvelle base de données située dans le [centre de téléchargement](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copiez le fichier zip sur la machine virtuelle dans laquelle vous êtes distant et extrayez le contenu du zip.
8. Dans SQL Server Management Studio, cliquez avec le bouton droit sur **AxDB** , puis sélectionnez **Tâches** > **Restaurer** > **Base de données**.

![Restaurer la base de données](./media/5RestoreDatabase.png)

9. Sélectionnez **Périphérique source** et accédez au fichier extrait du zip que vous avez copié.

![Périphériques sources](./media/6SourceDevice.png)

10. Sélectionnez **Options** , puis **Remplacer la base de données existante** et **Fermer les connexions existantes à la base de données de destination**. 
11. Cliquez sur **OK**.

![Restaurer les paramètres](./media/7RestoreSetting.png)

Vous recevrez la confirmation que la restauration AXDB a réussi. Après avoir reçu cette confirmation, vous pouvez fermer SQL Services Management Studio.

12. Revenez à **IIS (Internet Information Services)** > **Pools d’applications** > **AOSService** et démarrez AOSService.
13. Accédez à **Services** et démarrez les deux services que vous avez arrêtés précédemment.

14. Localisez l’outil AdminUserProvisioning sur cette machine virtuelle. Regardez sous K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Exécutez le fichier .ext en utilisant votre adresse utilisateur dans le champ **Adresse électronique**. 
16. Sélectionnez **Soumettre**.

![Attribution d’utilisateur administrateur](./media/8AdminUserProvisioning.png)

Ce processus peut prendre quelques minutes. Vous devriez recevoir un message de confirmation indiquant que l’utilisateur administrateur a été mis à jour avec succès.

17. Enfin, exécutez l’invite de commande en tant qu’administrateur et exécutez iisreset

![IIS Reset](./media/9IISReset.png)

18. Fermez la session de bureau à distance et utilisez la page **Détails de l’environnement** de LCS pour vous connecter à l’environnement pour confirmer qu’il fonctionne comme prévu.

![Finance and Operations](./media/10FinanceAndOperations.png)
