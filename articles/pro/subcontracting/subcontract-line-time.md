---
title: Lignes du contrat de sous-traitance pour le temps
description: Cette rubrique explique comment enregistrer des lignes du contrat de sous-traitance pour le temps et enregistrer l’achat de temps auprès des fournisseurs.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547241"
---
# <a name="subcontract-lines-for-time"></a>Lignes du contrat de sous-traitance pour le temps

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Un contrat de sous-traitance dans Dynamics 365 Project Operations peut avoir une ligne pour le temps. Les lignes du contrat de sous-traitance pour le temps permettent à un chef de projet d’acheter du temps pour une ressource fournisseur pour répondre aux besoins des tâches du projet et des ressources.

Dans Project Operations, pour créer une ligne pour le temps dans le contrat de sous-traitance, procédez comme suit :

1. Dans le volet de navigation, sélectionnez **Contrats de sous-traitance** et ouvrez un contrat de sous-traitance.
2. Sur l’onglet **Lignes du contrat de sous-traitance**, sélectionnez **Nouveau** pour créer une nouvelle ligne.
3. Sur la page **Création rapide**, dans le champ **Classe de transaction**, sélectionnez **Temps**.
4. Indiquez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

  Le tableau suivant fournit des informations sur les champs de la page **Ligne du contrat de sous-traitance** et de la page **Création rapide**.

| **Champ** | **Description** | **Impact fonctionnel** |
| --- | --- | --- |
| Nom  | Le nom de la ligne du contrat de sous-traitance pour aider à l’identification. | Il apparaît dans la première colonne de toutes les recherches basées sur les lignes du contrat de sous-traitance. |
| Description | Une brève description des services qui sont achetés sur la ligne du contrat de sous-traitance. |Aucun(e) |
| Type de ligne |   Ce champ contient la valeur par défaut **Basé sur la quantité**.| Aucun(e) |
| Mode de facturation | Ce groupe d’options représente les deux principaux modèles contractuels pris en charge par Project Operations : **Prix fixe** et **Temps et matériel**. | En fonction du mode de facturation sélectionné, une planification de facturation basée sur des jalons est mise à disposition pour les lignes du contrat de sous-traitance avec le mode de facturation à prix fixe. |
| Classe de transaction | La valeur par défaut est **Temps**. | Elle indique que la ligne du contrat de sous-traitance sert à enregistrer un achat de temps de sous-traitant. |
| Rôle | Sélectionnez le rôle des ressources de sous-traitance dont le temps est acheté. | Le rôle associé aux ressources de sous-traitance détermine le coût de l’achat. |
| Début demandé | Entrez la date à laquelle les ressources de sous-traitance doivent commencer à travailler. | Elle permet de choisir un tarif du projet dans les tarifs du projet associés au contrat de sous-traitance. Le coût du rôle sur la ligne du contrat de sous-traitance provient de ce tarif. |
| Fin demandée | Entrez la date de fin de l’affectation de la ressource de sous-traitance. | Elle permet d’afficher des avertissements si un chef de projet puise dans la capacité pour les besoins en ressources après cette date. |
| Quantité commandée | Entrez le nombre d’heures du rôle acheté auprès du fournisseur. | Il permet d’afficher des avertissements si un chef de projet puise excessivement dans cette capacité pour les besoins en ressources. |
| Groupe d'unités | La valeur par défaut est le **groupe d’unités Temps**, valeur qui ne peut pas être modifiée. | Aucun(e)|
| Unité | La valeur par défaut de ce champ est l’unité de base en heures à partir du **groupe d’unités Temps**. Vous pouvez modifier cette valeur pour acheter toute unité du **groupe d’unités Temps**, comme un jour ou une semaine. | L’association **Rôle** et **Unité** est utilisée par défaut ou calculée pour le prix unitaire de la ligne du contrat de sous-traitance. |
| Prix unitaire | Le prix unitaire par défaut utilise l’association **Rôle** et **Unité** du tarif du projet applicable pour la date **Début demandé** de la ligne du contrat de sous-traitance. | Si le tarif du projet applicable est configuré dans une unité différente de celle sur la ligne du contrat de sous-traitance, le système utilise la conversion d’unité pour calculer le prix unitaire. |
| Sous-total |    Ce champ en lecture seule est calculé de la façon suivante : Quantité x Prix unitaire, si les valeurs de quantité et de prix unitaire sont entrées. Si la quantité, le prix unitaire ou les deux sont vides, vous pouvez saisir une valeur dans le champ. | Aucun(e)|
| Taxe de ventes |   Entrez le montant de la taxe de ventes. |Aucun(e) |
| Montant total | Le montant total de la ligne de sous-traitance, taxes incluses. Ce champ est calculé de la façon suivante : Sous-total + Taxe de vente.|Aucun(e) |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
