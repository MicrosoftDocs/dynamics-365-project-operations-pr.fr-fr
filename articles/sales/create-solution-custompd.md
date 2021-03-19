---
title: Créer une solution pour les dimensions de tarification personnalisées
description: Cette rubrique donne des informations sur la manière de créer des solutions pour les dimensions de tarification personnalisées.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278415"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>Créer une solution pour les dimensions de tarification personnalisées

 _**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_ 

>[!IMPORTANT]
>Tous les changements de dimension Tarification personnalisée doivent se faire dans une solution distincte. Cette meilleure pratique importante procure la flexibilité nécessaire pour mettre à jour ou supprimer des modifications si nécessaire, elle permet une réutilisation de votre travail, et facilite le déplacement des modifications vers d'autres instances. Après avoir apporté toutes les modifications requises, exportez cette solution en tant que solution **Gérée** et importez-la dans d’autres instances en vue d'une réutilisation.

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>Créer une solution pour les dimensions de tarification personnalisées

1.  Sélectionnez **Paramètres** > **Solutions**, puis sélectionnez **Nouveau**.
2.  Nommez la solution,*dimensions de tarification <your organization name>*.
3. Tapez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

  ![Création d'une solution de dimension de tarification personnalisée](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>Ajouter tous les entités requises et les composants associés à la solution Dimension Tarification

Ajoutez les entités Project Service suivantes à votre solution de tarification pour apporter des modifications de schéma importantes à la solution de tarification. Une fois cette procédure terminée, les entités reconnaissent les nouvelles dimensions de tarification.

1.  Sélectionnez **Paramètres** > **Solutions**, puis double-cliquez sur **<*nom de votre organisation*> dimensions de tarification**.
2.  Dans l'Explorateur de solutions, sur le volet de navigation de gauche, sélectionnez **Ajouter** > **Entités**.
3.  Dans la boîte de dialogue **Composants de solution**, sélectionnez les entités suivantes :
 
   - **Réel**
   - **Ressource pouvant être réservée**
   - **Ligne d'estimation**
   - **Tâche du projet**
   - **Détail de la ligne de facture**
   - **Ligne de journal**
   - **Détail de la ligne de contrat du projet**
   - **Membre de l'équipe du projet**
   - **Détail de la ligne de devis**
   - **Majoration du prix du rôle**
   - **Prix du rôle**
   - **Entrée de temps**
 
   ![Ajouter des entités existantes à la solution de dimensions de tarification personnalisée](./media/Existing-entities-to-PD-solution.png)
 
 4. Pour chaque entité, examinez les composants ajoutés et la liste finale des actifs d'entité pour chaque entité. 

   >[!NOTE]
   > Incluez tous les formulaires et toutes les vues pour chacune des entités sélectionnées.

  ![Entités ajoutées](./media/solution-component-selection.png)


5.  Lorsque vous êtes invité à inclure des entités dépendantes pour les entités sélectionnées, sélectionnez **Non, ne pas inclure les composants requis.**

    ![Inclure des entités dépendantes](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]