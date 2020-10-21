---
title: Mettre en service un nouvel environnement
description: Cette rubrique fournit des informations sur la mise en service d’un nouvel environnement Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949359"
---
# <a name="provision-a-new-environment"></a>Mettre en service un nouvel environnement

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique fournit des informations sur la façon de mettre en service un nouvel environnement Dynamics 365 Project Operations pour les scénarios basés sur les ressources/non stockés.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Activer la mise en service automatisée de Project Operations dans un projet LCS

Utilisez les étapes suivantes pour activer le flux de mise en service automatisé de Project Operations pour votre projet LCS.

1. Accédez à [LCS](https://lcs.dynamics.com/v2) et sélectionnez la vignette **Gestion des fonctionnalités d’évaluation**.
2. Dans la liste **Fonctionnalité d’évaluation**, sélectionnez **Project Operations** et sélectionnez **Fonctionnalité d’évaluation activée** pour activer Project Operations.

> [!NOTE]
> Cette étape n’est effectuée qu’une seule fois par projet LCS.

## <a name="provision-a-project-operations-environment"></a>Mettre en service un environnement Project Operations

1. Ouvrez un nouveau déploiement [d’environnement de démonstration](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance ou [d’environnement bac à sable/de production](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Parcourez l’Assistant **Mise en service d’environnement**. 

> [!IMPORTANT]
> Assurez-vous que la version de l’application sélectionnée est 10.0.13 ou supérieure.

3. Pour mettre en service Project Operations, sous **Paramètres avancés**, sélectionnez **Common Data Service**. 
4. Activez le **paramètre Common Data Service** en sélectionnant **Oui**, puis entrez les informations dans les champs obligatoires :

  - Nom
  - Région
  - Langage
  - Devise
 
5. Dans le champ **Modèle Common Data Service**, sélectionnez **Project Operations** 

6. Sélectionnez le type d’environnement pour votre déploiement. Un essai basé sur un abonnement vous permettra de déployer un environnement CDS pendant 30 jours. 

![Paramètres de déploiement](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Sélectionnez **J’accepte** pour accepter les conditions d’utilisation, puis sélectionnez **Terminé** pour revenir aux paramètres de déploiement.

![Consentement au déploiement](./media/2DeploymentConsent.png)

7. Renseignez les champs obligatoires restants dans l’Assistant et confirmez le déploiement. Le délai de mise en service de l’environnement varie en fonction du type d’environnement. La mise en service peut prendre jusqu’à six heures.

  Une fois le déploiement terminé, l’environnement apparaîtra comme **Déployé**.

8. Pour confirmer que l’environnement a été déployé avec succès, sélectionnez **Connexion** et connectez-vous à l’environnement pour confirmer.

![Détails de l’environnement](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Appliquer des données de démonstration Finance à Project Operations (étape facultative)

Appliquez des données de démonstration de Finance Project Operations à l’environnement hébergé par le cloud, version de service 10.0.13 comme décrit dans [cet article](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Appliquer des mises à jour à l’environnement Finance

Project Operations nécessite un environnement Finance avec la version de l’application **10.0.13 (10.0.569.20009)** ou ultérieures.

Vous devrez peut-être appliquer des mises à jour de qualité à votre environnement Finance pour recevoir cette version.

1. Dans LCS, sur la page **Détails de l’environnement**, dans la section **Mises à jour disponibles**, sélectionnez **Afficher la mise à jour**.

![Afficher les mises à jour](./media/5ViewUpdates.png)

2. Sur la page **Mises à jour binaires**, cliquez sur **Enregistrer le package.**

![Enregistrer le package](./media/6SavePackage.png)

3. Cliquez sur **Sélectionner tout** et **Enregistrer le package**.

![Relire et enregistrer les mises à jour](./media/7ReviewAndSaveUpdates.png)

4. Saisissez un nom et une description du package, puis sélectionnez **Enregistrer**. Selon la connexion Internet, ce processus peut prendre un certain temps.

![Charger le package dans la Bibliothèque d’actifs](./media/8UploadPackageToAssetsLibrary.png)

5. Une fois le package enregistré, sélectionnez **Terminé** et enregistrez ce package dans la Bibliothèque d’actifs de votre projet LCS.

L’enregistrement et la validation du package peuvent prendre environ 15 minutes.

6. Pour appliquer la mise à jour, accédez à la page **Détails de l’environnement** dans LCS, sélectionnez **Gérer** > **Appliquer les mises à jour**.

![Gérer des environnements](./media/9MaintainEnvironment.png)

7. Dans la liste des mises à jour, sélectionnez le package que vous avez créé et sélectionnez **Appliquer**.

![Appliquez les mises à jour](./media/10ApplyUpdates.png)

La maintenance de l’environnement prendra un certain temps. Une fois terminé, l’environnement retournera à un état déployé.

![Environnement déployé](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Établir une connexion en double écriture 

1. Dans votre projet LCS, accédez à la page **Détails de l’environnement**.
2. Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps**.
3. Une fois le lien créé, sélectionnez à nouveau **Lien vers CDS for Apps**. Vous serez redirigé vers Double écriture dans Finance.

![Lien vers CDS](./media/12LinktoCDS.png)

4. Sélectionnez **Appliquer la solution** pour accéder aux entités qui seront mappées dans l’intégration.

![Appliquer des solutions](./media/13ApplySolutions.png)

5. Sélectionnez les deux solutions, **Mappage d’entités de double écriture Dynamics 365 Finance and Operations** et **Mappage d’entités de double écriture Dynamics 365 Project Operations**, puis sélectionnez **Appliquer**.

![Confirmer des solutions](./media/14ConfirmSolutions.png)

Une fois les solutions appliquées, les entités Double écriture sont appliquées à l’environnement.

![Application des solutions](./media/15ApplyingSolutions.png)

Une fois les entités appliquées, tous les mappages disponibles sont répertoriés dans l’environnement.

![Mappages de double écriture](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Actualiser les entités de données après la mise à jour

1. Dans Finance, accédez à l’espace de travail **Gestion des données**.

![Espace de travail de la gestion de données](./media/16DataManagement.png)

2. Sélectionnez la vignette **Paramètres du cadre**.

![Paramètres du cadre](./media/17FrameworkParameters.png)

3. Sur la page **Paramètres d’entité**, sélectionnez **Actualiser la liste des entités**.

![Actualiser la liste des entités](./media/18RefreshEntityList.png)

L’actualisation prendra environ 20 minutes. Vous recevrez une alerte lorsqu’elle sera terminée.

![Confirmer l’actualisation](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Exécuter les mappages d’écriture double Project Operations

1. Dans votre projet LCS, accédez à la page **Détails de l’environnement**.
2. Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps.** Après avoir sélectionné le lien, vous serez redirigé vers la liste des entités dans les mappages.
3. Démarrez les mappages comme décrit dans le tableau suivant. Assurez-vous de suivre la séquence indiquée.

| **Mappage d’entité** | **Actualiser l’entité** | **Synchronisation initiale** | **Sélection principale pour la synchronisation initiale** | **Exécuter la configuration requise** | **Synchronisation initiale de la configuration requise** |
| --- | --- | --- | --- | --- | --- |
| **Rôles des ressources de projet pour toutes les entreprises (bookableresourcecategories)** | Non | Oui | Common Data Service | Non | S. O. |
| **Entités juridiques (cdm\_entreprises)** | Non | Oui | Applications Finance and Operations | Non | S. O. |
| **Intégration des chiffres réels Project Operations (msdyn\_chiffres réels)** | Non | Non | S. O. | Oui | Non |
| **Lignes du contrat de projet (salesorderdetails)** | Non | Non | S. O. | Non | Non |
| **Entité d’intégration pour les relations de transaction du projet (msdyn\_transactionconnections)** | Non | Non | S. O. | Non | S. O. |
| **Jalons de la ligne de contrat d’intégration de Project Operations (msdyn\_contractlinesscheduleofvalues)** | Non | Non | S. O. | Non | S. O. |
| **Entité d’intégration de Project Operations pour les estimations de dépenses (msdyn\_estimateslines)** | Non | Non | S. O. | Non | S. O. |
| **Entité d’intégration de Project Operations pour les estimations d’heures (msdyn\_resourceassignments)** | Non | Non | S. O. | Non | S. O. |
| **Entité d’exportation des dépenses de projet d’intégration de Project Operations (msdyn\_expenses)** | Oui | Non | S. O. | Non | S. O. |
| **Entité d’intégration de Project Operations pour les estimations d’heures (msdyn\_resourceassignments)** | Oui | Non | S. O. | Non | S. O. |

4. Pour actualiser l’entité, sélectionnez le nom du mappage, puis sélectionnez **Actualiser les entités**. 
5. Continuez à exécuter le mappage une fois l’actualisation terminée.

![Actualiser le mappage](./media/20RefreshMapping.png)

Avant d’activer le mappage suivant, vérifiez que le mappage du tableau est dans un état de **En cours d’exécution**. L’exécution des mappages avec un plus grand nombre de prérequis peut prendre un certain temps.

Pour exécuter un mappage avec des prérequis, activez le bouton de basculement **Afficher les mappages d’entités associés**. Si le tableau indique que **Synchronisation initiale préalable** est **Non**, vérifiez que l’indicateur **Synchronisation initiale** est **Désactivé** dans tous les mappages de prérequises avant de l’exécuter.

![Exécuter le mappage](./media/21RunMap.png)

6. Validez que tous les mappages liés au projet sont en cours d’exécution.

![Toutes les mappages en cours d’exécution](./media/22AllMapsRunning.png)

Votre environnement Project Operations est désormais mis en service et configuré.
