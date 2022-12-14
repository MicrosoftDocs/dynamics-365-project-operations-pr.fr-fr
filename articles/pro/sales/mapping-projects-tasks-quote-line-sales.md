---
title: Mapper les projets et les tâches sur des lignes de devis de projet
description: Cet article fournit des informations sur la façon de mapper les projets et les tâches à des lignes de devis de projet.
author: rumant
ms.date: 10/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b276e7fb6ec8b98188c9396aca5092d19848afcc
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824265"
---
# <a name="map-projects-and-tasks-to-project-quote-lines"></a>Mapper les projets et les tâches sur des lignes de devis de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Sur les lignes de devis de projet, vous pouvez mapper les tâches spécifiques d’un projet déjà associé à une ligne de devis.

Lorsque vous mappez des tâches à une ligne de devis, les éléments suivants que vous avez définis sur la ligne de devis ne s’appliqueront qu’à ces tâches :

- Mode de facturation
- Options d’exigibilité
- Limites à ne pas dépasser
- Clients

Par exemple, vous pourriez avoir un projet où une phase est un prix fixe et toutes les autres phases sont le temps et les matériaux. Dans ce cas, vous pouvez associer la première phase, et toutes ses tâches enfants, à la ligne de devis pour cette phase avec un mode de facturation à prix fixe. Vous pouvez ensuite associer toutes les autres phases à la ligne de devis basée sur le temps et les matériaux.

## <a name="associate-tasks-to-project-based-quote-lines"></a>Associer des tâches à une ligne de devis selon un projet

Vous pouvez associer des tâches à des lignes de devis à partir des emplacements suivants :

- Page **Projet** > onglet **Facturation des tâches** (optimal)
- Page **Ligne de devis** > onglet **Tâches payantes** 

### <a name="from-the-project-page"></a>À partir de la page du projet

La page **Projet** offre une expérience optimale pour associer des tâches à des lignes de devis. Vous pouvez utiliser cette page pour sélectionner plusieurs tâches et les associer toutes, ainsi que leurs tâches enfants, à la ligne de devis sélectionnée.

1. Sur l’onglet **Général** d’une ligne de devis basée sur un projet, vérifiez que le champ **Projet** est rempli.
2. Dans le champ **Tâches incluses**, sélectionnez **Tâches sélectionnées uniquement**.
3. Enregistrez la ligne du devis selon les projets. Lorsque le formulaire est actualisé, l’onglet **Tâches payantes** s’affiche.
4. Sur l’onglet **Général**, sélectionnez le lien du projet dans le champ **Projet**.
5. Sur la page **Projet**, sélectionnez l’onglet **Facturation des tâches**.
6. Dans la deuxième grille, qui s’applique à la configuration de la facturation spécifique aux tâches, sélectionnez une ou plusieurs tâches, puis sélectionnez **Associer des lignes de devis**.
7. Dans la page de dialogue qui apparaît, sélectionnez une ligne de devis qui affiche les lignes de devis basées sur le projet sur le devis.
8. Dans le champ **Type de facturation**, indiquez si ces tâches sont facturables ou non.
9. Cochez la case pour indiquer si l’association doit inclure les tâches enfants des tâches sélectionnées. Cochez la case pour associer les tâches enfants des tâches sélectionnées à la ligne de devis.
10. Sélectionnez **OK** pour fermer la boîte de dialogue.

### <a name="from-the-quote-line-page"></a>À partir de la page de la ligne de devis

Vous pouvez associer des tâches de projet aux lignes de devis de l’onglet **Tâches payantes** sur la page **Ligne de devis**.

>[!NOTE]
>L’emplacement optimal pour associer des tâches de projet à des lignes de devis est l’onglet **Facturation des tâches** sur la page **Projet**. Si vous associez des tâches de l’onglet **Tâches payantes** sur la page **Ligne de devis**, vous devez associer manuellement chaque projet.

1. Sur l’onglet **Général** d’une ligne de devis basée sur un projet, vérifiez qu’un projet est sélectionné dans le champ **Projet**.
2. Dans le champ **Tâches incluses**, sélectionnez **Tâches sélectionnées uniquement**.
3. Enregistrez la ligne du devis selon les projets. Lorsque le formulaire est actualisé, l’onglet **Tâches payantes** s’affiche.
4. Sur l’onglet **Tâches payantes**, sélectionnez **Ajouter une tâche de ligne de devis**.
5. Sur la page **Tâche de ligne de devis**, dans le champ **Tâches**, sélectionnez la tâche et dans le champ **Type de facturation**, sélectionnez **Enregistrer**. 
6. Fermez la page. La tâche sélectionnée est maintenant associée à la ligne de devis.

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a>Dissocier des tâches de lignes de devis selon un projet

### <a name="from-the-project-page"></a>À partir de la page du projet

Cette méthode offre l’expérience la plus optimale pour dissocier des tâches des lignes de devis. Vous sélectionner plusieurs tâches et les dissocier toutes, ainsi que leurs tâches enfants, de la ligne de devis sélectionnée.

1. Sur l’onglet **Général** d’une ligne de devis basée sur un projet, dans le champ **Projet**, sélectionnez le lien du projet.
2. Sur la page **Projet**, sélectionnez l’onglet **Facturation des tâches**.
3. Dans la deuxième grille, qui s’applique à la configuration de la facturation spécifique aux tâches, sélectionnez une ou plusieurs tâches, puis sélectionnez **Dissocier des lignes de devis**.
4. Dans la page de dialogue qui apparaît, sélectionnez une ligne de devis.
5. Cochez la case pour indiquer si l’association doit également être supprimée des tâches enfants des tâches sélectionnées. Cochez la case pour dissocier également les tâches enfants des tâches sélectionnées à la ligne de devis.
6. Cliquez sur **OK**. Un message d’avertissement vous informe que si vous supprimez cette association, tout chiffre réel précédemment enregistré sur la tâche pourrait être annulé. 
7. Sélectionnez **OK** pour continuer et supprimer l’association entre la tâche et la ligne de devis basée sur le projet.

### <a name="from-the-quote-line-page"></a>À partir de la page de la ligne de devis

Vous pouvez également dissocier des tâches de projet aux lignes de devis de l’onglet **Tâches payantes** sur la page **Ligne de devis**.

1. Sur l’onglet **Tâches payantes**, sélectionnez **Supprimer une tâche de ligne de devis**.
2. Cliquez sur **OK**. Un message d’avertissement vous informe que si vous supprimez cette association, tout chiffre réel précédemment enregistré sur la tâche pourrait être annulé. 
3. Sélectionnez **OK** pour continuer et supprimer l’association entre la tâche et la ligne de devis basée sur le projet.

>[!NOTE]
> Cette procédure ne supprime pas la tâche du projet. Elle supprime uniquement l’association de tâche de la ligne de devis basée sur le projet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
