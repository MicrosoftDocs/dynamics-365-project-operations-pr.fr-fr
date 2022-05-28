---
title: Mettre en service un nouvel environnement
description: Cette rubrique fournit des informations sur la mise en service d’un nouvel environnement Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 03626cb1579fad7f8d8eb501905056cd13092754
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594805"
---
# <a name="provision-a-new-environment"></a>Mettre en service un nouvel environnement

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_



Cette rubrique fournit des informations sur la manière d’approvisionner un nouvel environnement Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Activer la mise en service automatisée de Project Operations dans un projet LCS

Utilisez les étapes suivantes pour activer le flux de mise en service automatisé de Project Operations pour votre projet LCS.

1. Accédez à [LCS](https://lcs.dynamics.com/v2) et sélectionnez la vignette **Gestion des fonctionnalités d’évaluation**.
2. Dans la liste **Fonctionnalité d’évaluation**, sélectionnez **Fonctionnalité Project Operations**, puis sélectionnez **Fonctionnalité d’évaluation activée** pour activer Project Operations.

   > [!NOTE]
   > Cette étape n’est effectuée qu’une seule fois par projet LCS.

## <a name="provision-a-project-operations-environment"></a>Mettre en service un environnement Project Operations

1. Ouvrez un nouveau déploiement d’[environnement de démonstration](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) Dynamics 365 Finance ou d’[environnement de production/bac à sable](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
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

     ![Paramètres de déploiement.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Sélectionnez **J’accepte** pour accepter les conditions d’utilisation, puis sélectionnez **Terminé** pour revenir aux paramètres de déploiement.
    >
    >![Consentement au déploiement.](./media/2DeploymentConsent.png)

7. Facultatif – Appliquez les données de démonstration à l’environnement. Aller à **Réglages avancés**, sélectionnez **Personnaliser la configuration de SQL Database**, et définissez **Spécifier un jeu de données pour la base de données d’application** sur **Démo**.
8. Renseignez les champs obligatoires restants dans l’Assistant et confirmez le déploiement. Le délai d’approvisionnement de l’environnement varie en fonction du type d’environnement. La mise en service peut prendre jusqu’à six heures.

   Une fois le déploiement terminé, l’environnement apparaîtra comme **Déployé**.

9. Pour confirmer que l’environnement s’est déployé avec succès, sélectionnez **Connexion** et connectez-vous à l’environnement pour confirmer.

    ![Détails de l’environnement.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Appliquer des mises à jour à l’environnement Finance

Project Operations nécessite un environnement Finance avec la version de l’application **10.0.13 (10.0.569.20009)** ou ultérieures.

Vous devrez peut-être appliquer des mises à jour de qualité à votre environnement Finance pour recevoir cette version.

1. Dans LCS, sur la page **Détails de l’environnement**, dans la section **Mises à jour disponibles**, sélectionnez **Afficher la mise à jour**.

    ![Affichez les mises à jour.](./media/5ViewUpdates.png)

2. Sur la page **Mises à jour binaires**, cliquez sur **Enregistrer le package.**

    ![Enregistrez le package.](./media/6SavePackage.png)

3. Cliquez sur **Sélectionner tout** et **Enregistrer le package**.

    ![Relisez et enregistrez les mises à jour.](./media/7ReviewAndSaveUpdates.png)

4. Saisissez un nom et une description du package, puis sélectionnez **Enregistrer**. Selon la connexion Internet, ce processus peut prendre un certain temps.

    ![Chargez le package dans la Bibliothèque d’actifs.](./media/8UploadPackageToAssetsLibrary.png)

5. Une fois le package enregistré, sélectionnez **Terminé** et enregistrez ce package dans la Bibliothèque d’actifs de votre projet LCS.

   L’enregistrement et la validation du package peuvent prendre environ 15 minutes.

6. Pour appliquer la mise à jour, accédez à la page **Détails de l’environnement** dans LCS, sélectionnez **Gérer** > **Appliquer les mises à jour**.

    ![Gérez les environnements.](./media/9MaintainEnvironment.png)

7. Dans la liste des mises à jour, sélectionnez le package que vous avez créé et sélectionnez **Appliquer**.

    ![Appliquez les mises à jour.](./media/10ApplyUpdates.png)

   La maintenance de l’environnement prendra un certain temps. Une fois terminé, l’environnement retournera à un état déployé.

    ![Environnement déployé.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Établir une connexion en double écriture 

1. Dans votre projet LCS, accédez à la page **Détails de l’environnement**.
2. Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps**.
3. Une fois le lien créé, sélectionnez à nouveau **Lien vers CDS for Apps**. Vous serez redirigé vers Double écriture dans Finance.

    ![Liez vers CDS.](./media/12LinktoCDS.png)

4. Sélectionnez **Appliquer la solution** pour accéder aux entités qui seront mappées dans l’intégration.

    ![Appliquez les solutions.](./media/13ApplySolutions.png)

5. Sélectionnez les deux solutions, **Mappage d’entité en double écriture de Dynamics 365 Finance and Operations** et **Mappages d’entité en double écriture Dynamics 365 Project Operations**, puis sélectionnez **Appliquer**.

    ![Confirmez les solutions.](./media/14ConfirmSolutions.png)

    Une fois les solutions appliquées, les entités Double écriture sont appliquées à l’environnement.

    ![Application des solutions.](./media/15ApplyingSolutions.png)

    Une fois les entités appliquées, tous les mappages disponibles sont répertoriés dans l’environnement.

    ![Mappages de double écriture.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Actualiser les entités de données après la mise à jour

1. Dans Finance, accédez à l’espace de travail **Gestion des données**.

    ![Espace de travail Gestion des données.](./media/16DataManagement.png)

2. Sélectionnez la vignette **Paramètres du cadre**.

    ![Paramètres du cadre.](./media/17FrameworkParameters.png)

3. Sur la page **Paramètres d’entité**, sélectionnez **Actualiser la liste des entités**.

    ![Actualisez la liste des entités.](./media/18RefreshEntityList.png)

L’actualisation prendra environ 20 minutes. Vous recevrez une alerte lorsqu’elle sera terminée.

  ![Confirmez l’actualisation.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Mettre à jour les paramètres de sécurité sur Project Operations sur Dataverse

1. Accédez à Project Operations sur votre environnement Dataverse. 
2. Accédez à **Paramètres** > **Sécurité** > **Rôles de sécurité**. 
3. Sur la page **Rôles de sécurité**, dans la liste des rôles, sélectionnez **Utilisateur d’application à double écriture** et sélectionnez l’onglet **Entités personnalisées**.  
4. Vérifiez que le rôle est associé aux autorisations **Lire** et **Ajouter à** pour les entités suivantes :
      
      - **Type de taux de change devise**
      - **Plan comptable**
      - **Calendrier fiscal**
      - **Registre**
      - **Société**
      - **Dépense**

5. Une fois le rôle de sécurité mis à jour, accédez à **Paramètres** > **Sécurité** > **Équipes** et sélectionnez l’équipe par défaut dans la vue d’équipe **Propriétaire d’entreprise locale**.
6. Sélectionnez **Gérer les rôles** et vérifiez que le privilège de sécurité **Utilisateur d’application à double écriture** est appliqué à cette équipe.

## <a name="run-project-operations-dual-write-maps"></a>Exécuter les mappages d’écriture double Project Operations

1. Dans votre projet LCS, accédez à la page **Détails de l’environnement**.
2. Sous **Informations sur l’environnement Common Data Service**, sélectionnez **Lien vers CDS for Apps.** Après avoir sélectionné le lien, vous serez redirigé vers la liste des entités dans les mappages.
3. Démarrez les mappages. Pour plus d’informations, voir [Versions du mappage à double écriture Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps).
4. Validez que tous les mappages liés au projet sont en cours d’exécution.

    ![Tous les mappages en cours d’exécution.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Appliquer les données de configuration dans CDS pour Project Operations (facultatif)

Si vous avez appliqué des données de démonstration à l’environnement Finance, consultez [Configurer et appliquer les données de configuration dans Common Data Service pour Project Operations](resource-apply-pro-setup-config-data.md) pour appliquer les données de démonstration à l’environnement CDS.


Votre environnement Project Operations est désormais mis en service et configuré. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
