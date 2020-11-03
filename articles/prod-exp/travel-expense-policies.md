---
title: Configurer des politiques de dépenses
description: Vous pouvez configurer des politiques de dépenses que vos collaborateurs devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement dans Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f74f6906cc1137b9645a830360a546432dc5207f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075887"
---
# <a name="set-up-expense-policies"></a>Configurer des politiques de dépenses

[!include [banner](../includes/banner.md)]

Vous pouvez définir les politiques que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.         
La mise en œuvre de politiques de dépenses peut vous aider à gérer efficacement les dépenses.         

Par exemple, vous pouvez définir une politique pour les dépenses d'hôtel à New York, qui stipule que les dépenses par nuit ne peuvent pas dépasser 250 USD.       
Si un collaborateur soumet une note de frais ou une demande de voyage dans laquelle le tarif de la chambre dépasse ce montant, le système informera        
l'employé que le montant de la dépense a été dépassé, conformément à la politique. Vous pouvez configurer le message que l'employé recevra lorsque vous        
définissez la politique.      
        
Vous pouvez définir trois types de politiques :         
        
- Avertissement – Permet à l'employé de soumettre une note de frais ou une demande de voyage, mais la dépense sera marquée pour tous les approbateurs et        
  pour un rapport ultérieur.        

- Erreur – Oblige l'employé à réviser la dépense pour se conformer à la politique avant de soumettre la note de frais ou la demande de voyage.       
 
 - Justification – Oblige l'employé ou un gestionnaire à saisir une justification pour le dépassement du montant, conformément à la politique, avant de soumettre la note de frais ou la demande de déplacement.        

## <a name="policy-tips"></a>Conseils en matière de politique
Voici quelques suggestions qui peuvent vous aider lors de la création de nouvelles politiques de gestion des dépenses. 
* Les politiques prennent effet à une date et ne prennent pas effet si la politique est créée avec une date postérieure à la date à laquelle la dépense a eu lieu. Par exemple, si vous créez une politique aujourd'hui pour appliquer une dépense de repas maximale de 50 USD, toutes les dépenses existantes saisies avant aujourd'hui ne seront pas comparées à cette politique.
* Lors de la création d'une politique pour une catégorie de dépenses pouvant être détaillée, pensez à ajouter une condition pour le type de ligne de dépenses. Certaines politiques, telles que l'exigence d'un reçu, peuvent ne pas avoir de sens pour les lignes détaillées et ne doivent être appliquées qu'à la ligne d'en-tête ou à une ligne non détaillée. 
* Les politiques de gestion des dépenses sont évaluées par défaut par rapport à l'entité source. Pour les scénarios intersociétés, vous pouvez définir la stratégie à évaluer par rapport à l'entité de destination (entité emprunteuse) à la place. Pour exécuter les politiques sur l'entité de destination, activez la fonctionnalité « Évaluer la politique de dépenses par rapport à l'entité juridique emprunteuse » dans l'espace de travail **Gestion des fonctionnalités**.

## <a name="when-to-evaluate-policies"></a>Quand évaluer les politiques

Dans les paramètres de gestion des dépenses, vous disposez d'une option pour évaluer les politiques de gestion des dépenses lorsqu'une ligne est enregistrée ou lorsqu'une note de frais est soumise. Si vous choisissez d'évaluer lorsqu'une ligne est enregistrée, cela permet de garantir que les utilisateurs ont une meilleure visibilité sur ce qu'ils doivent faire pour compléter leur note de frais en une seule fois. Sinon, vous pouvez retarder l'évaluation de la politique et gagner du temps si la validation a lieu à la fin, lors de la soumission au flux de travail.
