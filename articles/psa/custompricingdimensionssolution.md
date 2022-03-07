---
title: Création de solutions personnalisées pour les dimensions Tarification
description: Cette rubrique explique comment créer une solution personnalisée lors de la création de dimensions Tarification personnalisées.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 4dea80d8e4645675d3e89e846532ca7c0f292faa328c45938941c50dc15486fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995263"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>Création de solutions personnalisées pour les dimensions Tarification

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> Tous les changements de dimension Tarification personnalisée doivent se faire dans une solution distincte. Cette meilleure pratique importante procure la flexibilité nécessaire à l’avenir pour mettre à jour ou supprimer des modifications si nécessaire, permet une réutilisation de votre travail, et facilite le déplacement de ces modifications vers une autre instance. Après avoir apporté toutes les modifications requises, exportez cette solution en tant que **Solution gérée** et importez-la dans d’autres instances pour réutiliser votre configuration de tarification.

1. Sélectionnez **Paramètres** > **Solutions**, puis sélectionnez **Nouveau**. 
2. Nommez la solution, **\<your organization name> dimensions tarification**, entrez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

> ![Création d’une solution personnalisée pour les dimensions de tarification.](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Ajouter tous les entités requises et les composants associés à la solution Dimension Tarification
Vous devrez ajouter les entités Project Service suivantes à votre solution de tarification. Exécutez la procédure ci-dessous pour apporter quelques modifications importantes au schéma dans la solution de tarification de sorte que les entités soient informées des nouvelles dimensions de tarification.

1. Sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **\<your organization name> dimensions de tarification**. 
2. Dans l’Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Ajouter** > **Entités**.
3. Dans la boîte de dialogue **Composants de solution**, sélectionnez les entités suivantes :

- Réel
- Ressource pouvant être réservée
- Ligne d’estimation
- Tâche du projet
- Détail de la ligne de facture
- Ligne de journal
- Détail de la ligne de contrat du projet
- Membre de l’équipe du projet
- Détail de la ligne de devis
- Majoration du prix du rôle
- Prix du rôle 
- Entrée de temps 

> ![Ajouter des entités existantes à la solution des dimensions de tarification.](media/Existing-entities-to-PD-solution.png)

> ![Sélectionner les composants de solution.](media/Dimension-Components.png)

> [!NOTE]
> Veillez à inclure tous les formulaires et vues pour chacune des entités sélectionnées.

4. Lorsque vous êtes invité à inclure toutes les entités dépendantes des entités sélectionnées, cliquez sur **Non**.

> ![Ne pas inclure tous les composants associés.](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]