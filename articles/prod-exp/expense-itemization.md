---
title: Détail des dépenses
description: Cet article explique comment détailler les dépenses à l’aide de l’espace de travail repensé Dépenses.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920931"
---
# <a name="expense-itemization"></a>Détail des dépenses

[!include [banner](../includes/banner.md)]

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Les organisations exigent souvent que les employés fournissent une ventilation détaillée des dépenses engagées pendant leur voyage. Par exemple, un folio d’hôtel peut contenir plusieurs lignes détaillées pour le tarif de la chambre, les taxes, le stationnement et d’autres dépenses diverses engagées chaque jour pendant la durée du séjour. Ou les dépenses de repas peuvent nécessiter que vous indiquiez de manière plus détaillée leur répartition, pour le petit-déjeuner, le déjeuner ou le dîner. Quels que soient les besoins de l’organisation, chaque catégorie de dépenses peut être configurée pour refléter les sous-catégories ou les postes qui composent une dépense. Bien que le détail ait toujours été pris en charge dans la **Gestion des dépenses**, l’espace de travail rénové **Dépenses** permet une ventilation plus efficace lorsque la fonctionnalité **Capacité à détailler rapidement les dépenses récurrentes** est activée.  

## <a name="enable-quick-itemization"></a>Activer la ventilation rapide 

Vous pouvez utiliser la fonction **Capacité à détailler rapidement les dépenses récurrentes** pour détailler rapidement les dépenses récurrentes tout en évitant d’avoir à saisir à chaque fois les dépenses quotidiennes pendant la durée du séjour. Effectuez les étapes suivantes pour activer la ventilation rapide.

1. Accédez à l’espace de travail **Gestion des fonctionnalités** et, dans la liste des fonctionnalités, localisez et sélectionnez **Notes de frais réinventées**. 
2. Sélectionnez **Activer maintenant**. 
3. Dans la liste des fonctionnalités, recherchez et sélectionnez **Capacité à détailler rapidement les dépenses récurrentes**.
4. Sélectionnez **Activer maintenant**. 

## <a name="itemization-grid"></a>Grille de ventilation 

Si une catégorie de dépenses comporte des sous-catégories ou des composants différents qui composent cette dépense, elle peut être détaillée. Pour détailler une dépense, sélectionnez la ligne de dépense dans la note de frais et, dans le volet **Détails des dépenses**, sélectionnez **Actions** > **Détailler**. Le curseur **Détailler** révèle une grille avec des champs. Le tableau suivant fournit un exemple de chaque champ de la grille et de la façon dont le champ est rendu dans la note de frais. 

|     Champ          |     Description                                                                                  |     Exemple              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Sous-catégorie    |     La liste des sous-catégories configurées sous le type de catégorie de dépenses, **Hôtel**.             |     Tarif journalier de la chambre      |
|     Date de début     |     La date à laquelle le poste de dépense a été engagé pour la première fois.                                           |     13/09/2021           |
|     Taux journalier     |     Montant déboursé pour le poste de dépense.                                                    |     200                  |
|     Quantité       |     Le nombre de fois que le frais est répété sur une période continue.                       |     3                    |

![Détailler la dépense.](media/Itemization%20screen%201.png)

Lorsque vous enregistrez une ventilation, vous voyez une ligne détaillée pour la quantité spécifiée dans la grille de détail. Chaque ligne commence à la date spécifiée dans la grille.

![Rapport détaillé.](media/Itemization%20screen%202.png)

