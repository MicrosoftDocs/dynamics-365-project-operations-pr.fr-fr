---
title: Appliquer la configuration de la démonstration et les données de configuration – Simplifié
description: Cette rubrique fournit des informations sur l’application de la configuration de démonstration et des données de configuration dans Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997148"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Appliquer la configuration de la démonstration et les données de configuration pour Project Operations – Simplifié 

_**Déploiement simplifié – traiter la facturation pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a>Conditions préalables

Avant de commencer la configuration, vous devez disposer d’un environnement Common Data Service (CDS) mis en service pour Dynamics 365 Project Operations.


## <a name="instructions"></a>Instructions

1. Téléchargez le [package de données principal](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Accédez au dossier *ProjOpsSampleSetupData - CE only CMT* et lancez le fichier exécutable *DataMigrationUtility*.
3. Sur la page 1 de l’Assistant de migration de configuration (CMT) Common Data Service, sélectionnez **Importer des données**, puis **Continuer**.

    ![Migration de la configuration](./media/1ConfigurationMigration.png)

4. Sur la page 2 de l’Assistant CMT, sélectionnez **Microsoft 365** comme **Type de déploiement**.
5. Cochez les cases **Afficher une liste des organisations disponibles** et **Afficher les paramètres avancés**.
6. Sélectionnez la région de votre client, entrez vos informations d’identification, puis sélectionnez **Connexion**.

   ![Connexion de configuration](./media/2ConfigurationSignin.png)

7. Sur la page 3, dans la liste des Organisations sur le Client, sélectionnez l’organisation dans laquelle vous souhaitez importer les données de démonstration et sélectionnez **Connexion**.
8. À la page 4, sélectionnez le fichier zip *ExempleSetupAndConfigData* dans le dossier décompressé *ProjOpsSampleSetupData - CE only CMT*.

   ![Fichier compressé](./media/3ZipFile.png)

   ![Sélectionner un fichier](./media/4SelectAFile.png)

9. Une fois le fichier zip sélectionné, sélectionnez **Importer des données**.

   ![Importer les données](./media/5ImportData.png)

10. L’importation durera environ deux à dix minutes en fonction de la vitesse de votre réseau. Une fois terminé, quittez l’Assistant CMT. 
11. Vérifiez votre organisation pour les données dans les 18 entités suivantes :

    -   Devise
    -   Compte
    -   Unité d’organisation
    -   Contact
    -   Unité
    -   Groupe d’unités
    -   Tarifs
    -   Tarifs du paramètre du projet 
    -   Fréquence de facture
    -   Catégorie de ressources pouvant être réservées
    -   Catégorie de transaction
    -   Catégorie de dépense
    -   Prix du rôle
    -   Prix de la catégorie de transaction
    -   Caractéristique
    -   Ressource pouvant être réservée
    -   Association de catégories de ressources pouvant être réservées
    -   Caractéristique des ressources pouvant être réservées

    ![Importation terminée](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
