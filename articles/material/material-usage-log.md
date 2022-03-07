---
title: Enregistrer l’utilisation du matériel sur les projets et les tâches du projet
description: Cette rubrique fournit des informations sur la façon de consigner l’utilisation du matériel par rapport aux projets et aux tâches de projet.
author: rumant
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c739d7fabb96a845eaf139fcc9eab21247b0860
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001558"
---
# <a name="record-material-usage-on-projects-and-project-tasks"></a>Enregistrer l’utilisation du matériel sur les projets et les tâches du projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Lorsqu’une équipe de projet exécute des tâches d’un projet, elle consomme ou utilise du matériel. Un journal de l’utilisation du matériel permet d’enregistrer cette utilisation afin qu’elle puisse être approuvée par le chef de projet et éventuellement facturée au client. 

Pour enregistrer l’utilisation du matériel du catalogue ou hors catalogue et la soumettre à approbation, procédez comme suit : 

1. Dans le volet de navigation de gauche, sélectionnez **Utilisation du matériel**, puis **Nouveau**.
2. Sur la page **Nouvelle utilisation du matériel**, entrez les informations requises sur l’utilisation du matériel, puis sélectionnez **Enregistrer**.

Le tableau suivant fournit des informations sur les champs de la page **Journal d’utilisation du matériel**. 

| **Champ** | **Description** | **Impact en aval** |
| --- | --- | --- |
| Description | Une description de l’utilisation du matériel spécifique. | Il n’y a pas d’impact en aval pour ce champ. |
| Date | La date à laquelle le matériel devrait être utilisé. | Il n’y a pas d’impact en aval pour ce champ. |
| Project | Une liste des projets actifs. | La sélection d’un projet pour un journal d’utilisation du matériel a un impact sur le champ **Tâche**, car seules les tâches du projet sont affichées. |
| Tâche | Une liste de tâches pour le projet, y compris les tâches récapitulatives et de nœud terminal. | La sélection d’une tâche pour un journal d’utilisation du matériel a un impact sur le coût réel du matériel et les ventes de matériel réelles pour une tâche. Si ce champ est vide, le coût d’utilisation et les ventes de matériel correspondant sont suivis et résumés uniquement au niveau du projet. |
| Sélectionner un produit | Spécifiez si cette utilisation du matériel s’applique à un produit **Existant** (catalogue) ou à un produit **Hors catalogue**. | Ce champ détermine le type de produit. |
| Produit | L’ID du produit du catalogue de produits. Lorsque vous sélectionnez un ID de produit, la valeur du champ **Sélectionner un produit** est automatiquement mise à jour sur **Produit existant**. L’ID est utilisé pour récupérer les coûts et prix de vente à partir des tarifs. | Il n’y a pas d’impact en aval pour ce champ. |
| Description du produit hors catalogue | Un champ de texte pour écrire le nom du produit. Ce champ est disponible lorsque vous sélectionnez **Produit hors catalogue** dans le champ **Sélectionner un produit**.| Il n’y a pas d’impact en aval pour ce champ. |
| Ressource réservable| Ressource qui a utilisé ce matériel sur le projet. La valeur par défaut de ce champ est la ressource pouvant être réservée de l’utilisateur connecté, mais elle peut être modifiée pour enregistrer l’utilisation au nom des autres membres de l’équipe de projet. | Il n’y a pas d’impact en aval pour ce champ. |
| Groupe d’unités | La valeur par défaut de ce champ provient du groupe d’unités configuré par défaut sur le produit du catalogue. Vous pouvez mettre à jour ce champ pour sélectionner un autre groupe d’unités. | Il n’y a pas d’impact en aval pour ce champ. |
| Unité | Par défaut, la valeur de ce champ est l’unité par défaut du produit sélectionné. Vous pouvez mettre à jour ce champ pour sélectionner une autre unité. | La modification de l’unité entraîne un prix et un coût unitaire par défaut différents. |
| Quantité | La quantité du produit qui a été utilisé sur le projet ou la tâche de projet. | Il n’y a pas d’impact en aval pour ce champ. |
| Coût unitaire | Le coût unitaire de la combinaison du produit et de l’unité sélectionnée, tel que défini dans la liste de prix de revient applicable. | Le coût unitaire est toujours affiché dans la devise de coût du projet. S’il n’existe pas de coût unitaire pour la combinaison du produit et de l’unité dans le tarif, le coût unitaire sera de 0,00 par défaut. |
| Coût total | Le montant du coût qui est calculé comme suit : quantité \* coût unitaire.| Le montant unitaire est toujours affiché dans la devise de coût du projet. |


## <a name="submit-material-usage-for-review-and-approval"></a>Soumettre l’utilisation du matériel à examen et approbation 
Une fois que vous avez capturé toute votre utilisation du matériel et que vous êtes prêt à la faire approuver, vous devez soumettre les informations d’utilisation afin qu’elles soient examinées.

1. Accédez à **Journal d’utilisation du matériel** et sélectionnez une ou plusieurs entrées. Ou sélectionnez tous les enregistrements d’utilisation du matériel en utilisant la case à cocher sur l’en-tête.
2. Sélectionnez **Soumettre**. Le système traite les entrées sélectionnées, puis crée des demandes d’approbation de l’utilisation du matériel.

## <a name="recall-a-material-usage-log"></a>Rappeler un journal d’utilisation du matériel

Si nécessaire, vous pouvez rappeler une utilisation de matériel soumise. Le temps nécessaire pour rappeler une entrée d’utilisation de matériel dépend de l’étape d’approbation.  Si l’approbateur n’a pas encore approuvé l’entrée, le rappel peut avoir lieu immédiatement. Cependant, si l’entrée a déjà été approuvée, l’approbateur est invité à approuver le rappel et à annuler les transactions.

1. Accédez à **Utilisation du matériel** et, dans la liste des journaux d’utilisation du matériel, sélectionnez l’utilisation du matériel à rappeler.
2. Sélectionnez **Rappeler**. Si l’entrée d’utilisation du matériel n’a pas encore été approuvée, le système la rappelle immédiatement. Si l’entrée du matériel a déjà été approuvée, une demande de rappel est créée pour informer l’approbateur que vous souhaitez rappeler l’utilisation du matériel. L’approbateur confirmera alors que l’annulation peut être effectuée et l’entrée sera renvoyée.

## <a name="delete-a-material-usage-log"></a>Supprimer un journal d’utilisation du matériel

Vous pouvez supprimer les journaux d’utilisation du matériel qui n’ont pas été soumis. Pour supprimer un journal d’utilisation du matériel qui a déjà été soumis, vous devez d’abord le rappeler.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
