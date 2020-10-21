---
title: Appliquer la configuration de la démonstration et les données de configuration
description: Cette rubrique fournit des informations sur l’application de la configuration de démonstration et des données de configuration dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948847"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Appliquer la configuration de démonstration et les données de configuration pour le déploiement simplifié de Project Operations – Traiter la facturation pro forma

_**Déploiement simplifié – traiter la facturation pro forma_

1. Téléchargez le [package de données principal](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Accédez au dossier *ProjOpsDemoDataSetupAndMaster - Integrated CMT* et exécutez le fichier exécutable, *DataMigrationUtility*.
3. Sur la page 1 de l’Assistant de migration de configuration (CMT) Common Data Service, sélectionnez **Importer des données**, puis **Continuer**.

![Migration de la configuration](./media/1ConfigurationMigration.png)

4. Sur la page 2 de l’Assistant CMT, sélectionnez **Office 365** comme le **Type de déploiement**.
5. Cochez les cases **Afficher une liste des organisations disponibles** et **Afficher les paramètres avancés**.
6. Sélectionnez la région de votre client, entrez vos informations d’identification, puis sélectionnez **Connexion**.

![Connexion de configuration](./media/2ConfigurationSignin.png)

7. Sur la page 3, dans la liste des Organisations sur le Client, sélectionnez l’organisation dans laquelle vous souhaitez importer les données de démonstration et sélectionnez **Connexion**.
8. Sur la page 4, sélectionnez le fichier compressé, *MasterAndSetupData* à partir du dossier décompressé *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Fichier compressé](./media/3ZipFile.png)

![Sélectionnez un fichier](./media/4SelectAFile.png)

9. Une fois le fichier zip sélectionné, sélectionnez **Importer des données**.

![Importer les données](./media/5ImportData.png)

10. L’importation durera environ deux à dix minutes en fonction de la vitesse de votre réseau. Une fois terminé, quittez l’Assistant CMT. 
11. Vérifiez votre organisation pour les données dans les 20 entités suivantes :

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
- Détail de la fréquence de facture
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
