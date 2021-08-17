---
title: Estimations financières pour le matériel des projets
description: Cette sujet fournit des informations sur la définition ou l’estimation du matériel basé sur le projet.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1717abb8f37acb7ab5f4e24b9323b3d958b40b13d7da44c0bbfa88eea28b99ef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992608"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimations financières pour le matériel des projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations permet aux chefs de projet de définir des coûts de matériel basés sur un projet pour chaque projet ou tâche. Chaque estimation de matériaux peut être associée à une tâche de projet spécifique. Les dépenses sont classées en différentes catégories de dépenses définies au niveau organisationnel. La tarification et l’évaluation des coûts pour chaque catégorie de dépense sont définis dans la liste de prix. 

Pour afficher, ajouter ou supprimer une estimation de matériaux de projet, procédez comme suit :

1. Accédez à **Projets**, puis sélectionnez le projet que vous souhaitez mettre à jour.
2. Dans l’onglet **Estimations des matériaux**, affichez la liste des estimations des matériaux de projet.
3. Cliquez sur **Nouvelle estimation de matériaux** pour créer une estimation de matériaux. Ou sélectionnez une estimation de matériel à supprimer, puis sélectionnez **Supprimer l’estimation de matériel**.

Le tableau suivant fournit des informations sur les champs de la **Ligne d’estimation de matériel** sur un projet. 

| **Champ** | **Description** | **Impact en aval** |
| --- | --- | --- |
| Tâche | Une liste des tâches du projet. Inclut les tâches récapitulatives et les tâches de nœud terminal. | Lorsque vous sélectionnez une tâche pour une ligne d’estimation de matériel, cela a un impact sur le coût de matériel estimé et les ventes de matériel estimées pour une tâche. Si ce champ est vide, l’estimation de matériel est suivie et résumée uniquement au niveau du projet. |
| Sélectionner un produit |  Vous pouvez spécifier si cette ligne d’estimation s’applique à un produit existant (catalogue) ou à un produit hors catalogue. | Ce champ détermine si vous sélectionnez un produit dans le catalogue ou un produit hors catalogue. |
| Produit | L’ID du produit du catalogue de produits. Lorsque vous sélectionnez un ID de produit, la valeur du champ **Sélectionner un produit** est automatiquement mise à jour sur **Produit existant**. L’ID est utilisé pour récupérer les coûts et prix de vente à partir des tarifs. | Il n’y a pas d’impact en aval pour ce champ. |
| Description du produit hors catalogue | Un champ de texte pour écrire le nom du produit. Ce champ doit être utilisé lorsque **Produit hors catalogue** est sélectionné dans le champ **Sélectionner un produit**.| Il n’y a pas d’impact en aval pour ce champ. |
| Date de début | La date prévue à laquelle le matériel devrait être utilisé. | Il n’y a pas d’impact en aval pour ce champ. |
| Groupe d’unités | La valeur par défaut de ce champ provient du groupe d’unités par défaut du produit du catalogue. Vous pouvez mettre à jour ce champ pour sélectionner un autre groupe d’unités. | Il n’y a pas d’impact en aval pour ce champ. |
| Unité | Par défaut, la valeur de ce champ correspond à l’unité par défaut du produit sélectionné. Vous pouvez mettre à jour ce champ pour sélectionner une autre unité. | La modification de l’unité entraîne un prix et un coût unitaire par défaut différents. |
| Quantité | La quantité estimée du produit qui sera utilisée pour le projet. | Il n’y a pas d’impact en aval pour ce champ. |
| Coût unitaire | Le coût unitaire de la combinaison du produit et de l’unité sélectionnée, tel que défini dans la liste de prix de revient applicable. | Le coût unitaire est toujours affiché dans la devise de coût du projet. S’il n’existe pas de configuration du coût unitaire pour la combinaison du produit et la configuration de l’unité dans le tarif, le coût unitaire sera de 0,00 par défaut. |
| Prix unitaire | Le prix de la combinaison du produit et de l’unité sélectionnée, tel que défini dans le tarif de vente applicable. | Le prix unitaire est toujours affiché dans la devise de vente du projet. S’il n’existe pas de configuration du prix unitaire pour la combinaison du produit et la configuration de l’unité dans le tarif, le prix unitaire sera de 0,00 par défaut.|
| Coût total | Le montant du coût qui est calculé comme suit : quantité \* coût unitaire.| Le montant unitaire est toujours affiché dans la devise de coût du projet. |
| Total des ventes | Le montant des ventes qui est calculé comme suit : quantité \* prix unitaire. | Le montant des ventes est toujours affiché dans la devise de vente du projet. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
