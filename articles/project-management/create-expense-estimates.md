---
title: Estimations financières des dépenses des projets
description: Cette rubrique fournit des informations sur la définition ou l’estimation des dépenses liées au projet.
author: rumant
manager: Annbe
ms.date: 03/19/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad4901b1264289f1da881154bc147fc3f8da698f
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701779"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Estimations financières des dépenses des projets
_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations permet aux chefs de projet de définir des dépenses basées sur un projet pour chaque projet ou tâche. Chaque poste de dépense peut être associé à une tâche de projet spécifique. Les dépenses sont classées en différentes catégories de dépenses, qui sont définies au niveau de l’organisation. La tarification et le calcul des coûts pour chaque catégorie de dépenses sont définis dans le tarif. 

Effectuez les étapes suivantes pour afficher, ajouter ou supprimer une dépense de projet.

1. Accédez à **Projets** et sélectionnez le projet auquel vous souhaitez travailler.
2. Sélectionnez l’onglet **Estimations du projet** et affichez la liste des dépenses du projet.
3. Sélectionnez **Nouvelle dépense** pour ajouter une dépense. Sinon, sélectionnez une dépense à supprimer, puis sélectionnez **Supprimer la dépense**.

Le tableau suivant fournit des informations sur les champs de la **Ligne d’estimation des dépenses** sur un projet. 

| **Champ** | **Description** | **Impact en aval** |
| --- | --- | --- |
| Tâche | Une liste des tâches du projet. Inclut les tâches récapitulatives et les tâches de nœud terminal. | La sélection d’une tâche pour une ligne d’estimation des dépenses aura un impact sur le coût des dépenses estimé et les ventes de dépenses estimées pour une tâche. Si ce champ est laissé vide, l’estimation des dépenses est suivie et résumée uniquement au niveau du projet. |
| Catégorie | Une liste des catégories de transaction qui ont des catégories de dépenses liées dans l’application. | La sélection d’une catégorie détermine la tarification et l’évaluation des coûts sur la ligne d’estimation des dépenses. |
| Date de début | La date prévue à laquelle la dépense se produira. | Il n’y a pas d’impact en aval pour ce champ. |
| Groupe d’unités | La valeur par défaut de ce champ provient du groupe d’unités configuré par défaut sur la catégorie sélectionnée. Vous pouvez mettre à jour ce champ pour sélectionner un autre groupe d’unités. | Il n’y a pas d’impact en aval pour ce champ. |
| Unité | Par défaut, la valeur de ce champ correspond à l’unité par défaut de la catégorie sélectionnée. Vous pouvez mettre à jour ce champ pour sélectionner une autre unité. | La modification de l’unité entraîne un prix et un coût unitaire par défaut différents. |
| Quantité | Le montant de la dépense estimée que vous engagerez. | Il n’y a pas d’impact en aval pour ce champ. |
| Coût unitaire | Le coût de la combinaison de la catégorie et de l’unité sélectionnée, tel que défini dans la liste de prix de revient applicable | Le coût unitaire est toujours affiché dans la devise de coût du projet. |
| Prix unitaire | Le prix de la combinaison de la catégorie et de l’unité sélectionnée, tel que défini dans le tarif de vente applicable. | Le prix unitaire est toujours affiché dans la devise de vente du projet. |
| Coût total | Le montant du coût qui est calculé comme suit : quantité \* coût unitaire.| Le montant unitaire est toujours affiché dans la devise de coût du projet. |
| Total des ventes | Le montant des ventes qui est calculé comme suit : quantité \* prix unitaire. | Le montant des ventes est toujours affiché dans la devise de vente du projet. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
