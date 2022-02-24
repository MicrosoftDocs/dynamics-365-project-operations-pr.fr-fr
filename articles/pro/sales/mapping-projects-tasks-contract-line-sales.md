---
title: Mapper les projets et les tâches à une ligne de contrat basée sur un projet – Simplifié
description: Cette rubrique fournit des informations sur l’ajout et la suppression de projets et de tâches à une ligne de contrat.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4737f9870904bfc7adac11b8e2aa13bb8c610ca3
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858084"
---
# <a name="map-projects-and-tasks-to-a-project-based-contract-line"></a>Mapper les projets et les tâches sur une ligne de contrat basée sur un projet 

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_

Dans les lignes de contrat basées sur un projet, vous pouvez mapper des tâches spécifiques d’un projet à la ligne de contrat.

Lorsque vous mappez des tâches spécifiques à une ligne de contrat, le mode de facturation, les options d’exigibilité, les limites à ne pas dépasser et les clients définis sur la ligne de contrat s’appliquent uniquement à ces tâches spécifiques.

Si vous vous trouvez dans un scénario dans lequel une seule phase de projet, par exemple la phase Prototype, est à prix fixe et toutes les autres phases sont Temps et Matériel, vous pourrez associer la phase Prototype et toutes les tâches enfants associées à la ligne de contrat de cette phase avec un mode de facturation à prix fixe.

Toutes les autres phases de la structure de répartition du travail (WBS) de votre projet peuvent être associées à la ligne de contrat basée sur le temps et le matériel.

## <a name="associate-tasks-to-project-based-contract-lines"></a>Associer des tâches à des lignes de contrat basées sur un projet

Les tâches peuvent être associées aux lignes de contrat à partir de l’onglet **Tâches facturables** sur la page **Ligne de contrat** ou depuis l’onglet **Facturation de la tâche** sur la page **Projet**.

### <a name="from-the-contract-line-page"></a>À partir de la page Ligne de contrat

Effectuez les étapes suivantes pour associer des tâches de projet à la ligne de contrat à partir de l’onglet **Tâches facturables** de la page **Ligne de contrat**.

1. Sous l’onglet **Général** d’une ligne de contrat basée sur un projet, vérifiez que le champ **Projet** est renseigné.
2. Dans le champ **Tâches incluses**, sélectionnez **Tâches sélectionnées uniquement**.
3. Enregistrez vos modifications. Après actualisation du formulaire, l’onglet **Tâches facturables** devient visible.
4. Sélectionnez l’onglet **Tâches facturables** et dans la sous-grille, sélectionne **Ajouter une tâche de ligne de contrat**.
5. Sur la page **Tâches de ligne de contrat**, dans la liste déroulante **Tâches**, sélectionnez la tâche. 
6. Saisissez les informations dans le champ **Type de facturation**, puis sélectionnez **Enregistrer et fermer**. La tâche sélectionnée est associée à la ligne de contrat.

> [!NOTE]
> Cette méthode n’est pas le meilleur moyen d’associer des tâches de projet à des lignes de contrat. En effet, chaque projet devra être associé manuellement. Le meilleur moyen est de passer par l’onglet **Facturation de la tâche** dans la page **Projet**.

### <a name="from-the-project-page"></a>À partir de la page du projet

Il s’agit de la meilleure méthode pour associer des tâches à des lignes de contrat. Vous pouvez sélectionner plusieurs tâches et associer toutes celles-ci et leurs tâches enfants à la ligne de contrat sélectionnée. Effectuez les étapes suivantes pour associer des tâches à la ligne de contrat à partir de la page **Projet**.

1. Sous l’onglet **Général** d’une ligne de contrat basée sur un projet, vérifiez que le champ **Projet** est renseigné.
2. Dans le champ **Tâches incluses**, sélectionnez **Tâches sélectionnées uniquement**.
3. Enregistrez la ligne de contrat basée sur le projet. Après actualisation du formulaire, l’onglet **Tâches facturables** devient visible. Cette étape n’est réalisée qu’à des fins de vérification.
4. Sous l’onglet **Général** de la ligne de contrat basée sur un projet, dans le champ **Projet**, sélectionnez le lien du projet.
5. Sur la page **Projet**, sélectionnez l’onglet **Configuration de la facturation de la tâche**.
6. Il y a deux grilles. Une grille concerne les lignes de contrat qui s’appliquent à l’ensemble du projet. La deuxième grille s’applique à la configuration spécifique de la facturation à la tâche. Dans la deuxième grille, sélectionnez une ou plusieurs tâches, puis sélectionnez **Associer des lignes de contrat**.
7. Dans la page de dialogue qui s’ouvre, sélectionnez une ligne de contrat dans la liste déroulante.
8. Utilisez le menu déroulant **Type de facturation** pour marquer les tâches comme facturables ou non facturables.
9. Cochez la case pour indiquer si l’association doit également inclure les tâches enfants des tâches sélectionnées. Le fait de cocher la case associera également les tâches enfants des tâches sélectionnées à la ligne de contrat.
10. Sélectionnez **OK** pour fermer la boîte de dialogue.

## <a name="unassociate-tasks-from-project-based-contract-lines"></a>Dissocier des tâches de lignes de contrat basées sur un projet

### <a name="from-the-contract-line-page"></a>À partir de la page Ligne de contrat

Effectuez les étapes suivantes pour dissocier des tâches de projet de la ligne de contrat sur l’onglet **Tâches facturables** de la page **Ligne de contrat**.

1. Sous l’onglet **Tâches facturables**, sélectionnez **Supprimer une tâche de ligne de contrat**.
2. Un message d’avertissement indique que la suppression de cette association pourrait entraîner la contrepassation de tous les chiffres réels enregistrés précédemment sur la tâche. Sélectionnez **OK** dans la boîte de dialogue pour supprimer l’association entre la tâche et la ligne de contrat basée sur un projet. 

> [!NOTE]
> Cela ne supprime pas la tâche du projet. En revanche, cette action supprime l’association de tâches à la ligne de contrat basée sur un projet.

### <a name="from-the-project-page"></a>À partir de la page du projet

Cette méthode est le meilleur moyen de dissocier des tâches des lignes de contrat. Vous pouvez sélectionner plusieurs tâches et dissocier toutes celles-ci et leurs tâches enfants de la ligne de contrat sélectionnée. Effectuez les étapes suivantes pour dissocier des tâches de la ligne de contrat.

1. Sous l’onglet **Général** de la ligne de contrat basée sur un projet, dans le champ **Projet**, cliquez sur le lien du projet.
2. Sur la page **Projet**, sélectionnez l’onglet **Configuration de la facturation de la tâche**.
3. Il y a deux grilles sur la page. Une grille concerne les lignes de contrat qui s’appliquent à l’ensemble du projet et la seconde s’applique à la configuration de la facturation spécifique à la tâche. Dans la deuxième grille, sélectionnez une ou plusieurs tâches, puis sélectionnez **Dissocier des lignes de contrat**.
4. Dans la page de dialogue qui s’ouvre, sélectionnez une ligne de contrat dans la liste déroulante.
5. Cochez la case pour indiquer si l’association doit également être supprimée des tâches enfants des tâches sélectionnées. Le fait de cocher la case dissociera également les tâches enfants des tâches sélectionnées de la ligne de contrat.
6. Cliquez sur **OK**. Un message d’avertissement indique que la suppression de cette association pourrait entraîner la contrepassation de tous les chiffres réels enregistrés précédemment sur la tâche. Sélectionnez **OK** dans la boîte de dialogue d’avertissement pour supprimer l’association entre la tâche et la ligne de contrat basée sur un projet.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
