---
title: Appliquer les données de démonstration à un environnement hébergé par le cloud Finance
description: Cette rubrique explique comment appliquer les données de démonstration de Project Operations à un environnement hébergé par Dynamics 365 Finance Cloud.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e4ccc7eb02fabdc0476fe454f33bff637ab8b835
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588963"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a>Appliquer les données de démonstration à un environnement hébergé par le cloud Finance

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

> [!IMPORTANT]
> Cette rubrique n’est applicable qu’à Microsoft Dynamics 365 Finance version 10.0.13 et ne peut être effectuée que sur un environnement hébergé dans le Cloud. Suivez les étapes de cette rubrique **AVANT** d’appliquer des mises à jour de qualité à l’environnement.

1. Dans votre projet LCS, ouvrez la page **Détails de l’environnement**. Notez qu’elle inclut les détails nécessaires pour se connecter à l’environnement à l’aide du protocole RDP (Remote Desktop Protocol).

![Détails de l’environnement.](./media/1EnvironmentDetails.png)

Le premier ensemble d’informations d’identification mises en évidence sont les informations d’identification du compte local et contiennent un lien hypertexte vers la connexion Bureau à distance. Les informations d’identification incluent le nom d’utilisateur et le mot de passe de l’administrateur de l’environnement. Le deuxième ensemble d’informations d’identification est utilisé pour se connecter à SQL Server dans cet environnement.

2. Connectez-vous à l’environnement à distance par le lien hypertexte dans **Comptes locaux** et utilisez les **Informations d’identification du compte local** pour vous authentifier.
3. Accédez à **IIS (Internet Information Services)** > **Pools d’applications** > **AOSService** et arrêtez le service. Vous arrêtez le service à ce stade afin de pouvoir continuer à remplacer la base de données SQL.

![Arrêtez le service AOS.](./media/2StopAOS.png)

4. Accédez à **Services** et arrêtez les deux éléments suivants :

- Microsoft Dynamics 365 Unified Operations : Service de gestion des lots
- Microsoft Dynamics 365 Unified Operations : Cadre d’importation et d’exportation des données

![Arrêtez les services.](./media/3StopServices.png)

5. Ouvrez Microsoft SQL Server Management Studio. Connectez-vous avec les informations d’identification SQL Server et utilisez l’utilisateur et le mot de passe axdbadmin de la page **Détails des environnements** de LCS.

![SQL Server Management Studio.](./media/4SSMS.png)

6. Dans l’Explorateur d’objets, **Bases de données** et localisez **AXDB**. Vous allez remplacer la base de données par une nouvelle base de données située dans le [centre de téléchargement](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip). 
7. Copiez le fichier zip sur la machine virtuelle dans laquelle vous êtes distant et extrayez le contenu du zip.
8. Dans SQL Server Management Studio, cliquez avec le bouton droit sur **AxDB**, puis sélectionnez **Tâches** > **Restaurer** > **Base de données**.

![Restaurez la base de données.](./media/5RestoreDatabase.png)

9. Sélectionnez **Périphérique source** et accédez au fichier extrait du zip que vous avez copié.

![Périphériques source.](./media/6SourceDevice.png)

10. Sélectionnez **Options**, puis **Remplacer la base de données existante** et **Fermer les connexions existantes à la base de données de destination**. 
11. Cliquez sur **OK**.

![Restaurez les paramètres.](./media/7RestoreSetting.png)

Vous recevrez la confirmation que la restauration AXDB a réussi. Après avoir reçu cette confirmation, vous pouvez fermer SQL Services Management Studio.

12. Revenez à **IIS (Internet Information Services)** > **Pools d’applications** > **AOSService** et démarrez AOSService.
13. Accédez à **Services** et démarrez les deux services que vous avez arrêtés précédemment.

14. Localisez l’outil AdminUserProvisioning sur cette machine virtuelle. Regardez sous K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.
15. Exécutez le fichier .ext en utilisant votre adresse utilisateur dans le champ **Adresse électronique**. 
16. Cliquez sur **Envoyer**.

![Attribution d’utilisateurs administrateurs.](./media/8AdminUserProvisioning.png)

Ce processus peut prendre quelques minutes. Vous devriez recevoir un message de confirmation indiquant que l’utilisateur administrateur a été mis à jour avec succès.

17. Enfin, exécutez l’invite de commande en tant qu’administrateur et exécutez iisreset

![Réinitialisez IIS.](./media/9IISReset.png)

18. Fermez la session de bureau à distance et utilisez la page **Détails de l’environnement** de LCS pour vous connecter à l’environnement pour confirmer qu’il fonctionne comme prévu.

![Finance and Operations.](./media/10FinanceAndOperations.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]