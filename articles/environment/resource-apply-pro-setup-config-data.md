---
title: Configurer et appliquer les données de configuration dans Common Data Service
description: Cette rubrique fournit des informations sur la configuration et l’application des données de configuration dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401125"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Configurer et appliquer les données de configuration dans Common Data Service 

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

## <a name="prerequisites"></a>Conditions préalables

Avant de commencer à configurer les données dans Common Data Service (CDS), les conditions préalables suivantes doivent être respectées :

1.  Configurer un environnement CDS et un environnement Dynamics 365 Finance pour Project Operations.
2.  Les informations sur l’entité juridique de Dynamics 365 Finance sont partagées avec l’environnement CDS. Cela signifie que l’entité **Société** dans CDS possède les enregistrement de société suivants :
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Installer la configuration de la démonstration et les données de configuration

1. Téléchargez, débloquez et décompressez le [Package de données d’installation et de configuration](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Accédez au dossier décompressé et exécutez le fichier exécutable, *DataMigrationUtility*.
3. Sur la page 1 de l’Assistant de migration de configuration (CMT) Common Data Service, sélectionnez **Importer des données**, puis **Continuer**.

![Migration de la configuration](./media/1ConfigurationMigration.png)

4. Sur la page 2 de l’Assistant CMT, sélectionnez **Microsoft 365** comme **Type de déploiement**.
5. Cochez les cases **Afficher une liste des organisations disponibles** et **Afficher les paramètres avancés**.
6. Sélectionnez la région de votre client, entrez vos informations d’identification et sélectionnez **Connexion**.

![Connexion de configuration](./media/2ConfigurationSignin.png)

7. Sur la page 3, dans la liste des organisations sur le client, sélectionnez l’organisation dans laquelle vous souhaitez importer les données de démonstration et sélectionnez **Connexion**.
8. Sur la page 4, sélectionnez le fichier zip, *SampleSetupAndConfigData* à partir du dossier décompressé.

![Sélection de fichier zip](./media/3ZipFile.png)

![Sélectionnez un fichier](./media/4SelectAFile.png)

9. Une fois le fichier zip sélectionné, sélectionnez **Importer des données**.

![Importer des données](./media/5ImportData.png)

10. L’importation durera environ deux à dix minutes en fonction de la vitesse de votre réseau. Une fois l’importation terminée, quittez l’Assistant CMT. 
11. Vérifiez votre organisation pour les données dans les 19 entités suivantes :

  - Devise
  - Unité d’organisation
  - Contact
  - Groupe fiscal
  - Groupe de clients
  - Unité
  - Groupe d’unités
  - Tarifs
  - Tarifs du paramètre du projet
  - Fréquence de facture
  - Catégorie de ressources pouvant être réservées
  - Catégorie de transaction
  - Catégorie de dépense
  - Prix du rôle
  - Prix de la catégorie de transaction
  - Caractéristique
  - Ressource pouvant être réservée
  - Association de catégories de ressources pouvant être réservées
  - Caractéristique des ressources pouvant être réservées

![Importation terminée](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>Mettre à jour les configurations Project Operations

1. Accéder à l’environnement CE. Vous pouvez le trouver en ouvrant le [Centre d’administration Power Platform](https://admin.powerplatform.microsoft.com/environments), en sélectionnant l’environnement, puis en sélectionnant **Ouvrir l’environnement**. 

![Ouvrir l’environnement](./media/7OpenEnvironment.png)

2. Accédez à **Projets** > **Ressources**, puis sélectionnez **Nouveau** pour créer une ressource réservable pour votre utilisateur.

![Ressources pouvant être réservées](./media/8BookableResources.png)

3. Sur l’onglet **Général**, sélectionnez votre utilisateur administrateur. Vérifiez que le fuseau horaire correspond à celui dans lequel vous vous trouvez. 

![Nouvelle ressource pouvant être réservée](./media/9NewBookableResource.png)

4. Sur l’onglet **Planification**, dans le champ **Société**, choisissez la société **USPM**, puis **Enregistrer**. 

![Onglet Planification](./media/10SchedulingTab.png)

5. Cliquez sur l’onglet **Heures de travail**.  

![Heures de travail](./media/11WorkHours.png)

6. Double-cliquez sur n’importe quelle valeur du calendrier et sélectionnez **Modifier** > **Tous les événements de la série**. 

![Calendrier de travail](./media/12WorkCalendar.png)

7. Remplacez les heures de travail par une journée de travail de huit (8) heures, marquez les week-ends comme jours non travaillés et assurez-vous que le fuseau horaire correspond au vôtre. 
8. Sélectionnez **Enregistrer et fermer**.

![Mettre à jour un calendrier](./media/13UpdateCalendar.png)

9. Accédez à **Paramètres** > **Modèles de calendrier** et sélectionnez **Nouveau**.
 
 ![Modèles de calendrier](./media/14CalendarTemplates.png)
 
 10. Entrez un nom, sélectionnez la ressource de modèle que vous avez créée, puis sélectionnez **Enregistrer**. 
 
 ![Enregistrer un modèle de calendrier](./media/15SaveCalendarTemplate.png)
 
 11. Accédez à **Paramètres** et double-cliquez sur l’enregistrement. 
 
 ![Paramètres du projet](./media/16ProjectParameters.png)
 
12. Mettez à jour les champs suivants :

 - **Société par défaut** : USPM
 - **Unité d’organisation par défaut** : Contoso Robotics Global
 - **Fréquence de facturation** : Septième et dernier jour
 - **Modèle d’heure de travail** : Passez au modèle que vous avez créé.

13. Sélectionnez **Enregistrer**. 

![Paramètres du projet mis à jour](./media/17UpdatedProjectParameters.png)
