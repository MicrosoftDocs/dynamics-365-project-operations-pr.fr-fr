---
title: Configurer des politiques de dépenses
description: Vous pouvez définir des stratégies de dépenses que vos travailleurs sont tenus de suivre lorsqu’ils entrent et soumettent des états de dépenses et des demandes de voyage dans Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3dc5d1768b57baa68f134af318dd9d2d7cdd756
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684731"
---
# <a name="set-up-expense-policies"></a>Configurer des politiques de dépenses

Vous pouvez définir les politiques que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.         
L’implémentation de stratégies de gestion des dépenses vous permet de gérer efficacement les dépenses.         

Par exemple, vous pouvez définir une politique pour les dépenses d’hôtel à New York, qui stipule que les dépenses par nuit ne peuvent pas dépasser 250 USD.       
Si un collaborateur soumet une note de frais ou une demande de voyage dans laquelle le tarif de la chambre dépasse ce montant, le système informera        
l’employé que le montant de la dépense a été dépassé, conformément à la politique. Vous pouvez configurer le message que l’employé recevra lorsque vous        
définissez la politique.      
        
Vous pouvez définir trois types de politiques :         
        
- Avertissement – Permet à l’employé de soumettre une note de frais ou une demande de voyage, mais la dépense sera marquée pour tous les approbateurs et        
  pour un rapport ultérieur.        

- Erreur – Oblige l’employé à réviser la dépense pour se conformer à la politique avant de soumettre la note de frais ou la demande de voyage.       
 
 - Justification – Oblige l’employé ou un gestionnaire à saisir une justification pour le dépassement du montant, conformément à la politique, avant de soumettre la note de frais ou la demande de déplacement.        

## <a name="policy-tips"></a>Conseils relatifs aux stratégies
Voici quelques suggestions qui peuvent vous aider lors de la création de nouvelles politiques de gestion des dépenses. 
* Les politiques prennent effet à une date et ne prennent pas effet si la politique est créée avec une date postérieure à la date à laquelle la dépense a eu lieu. Par exemple, si vous créez une politique aujourd’hui pour appliquer une dépense de repas maximale de 50 USD, toutes les dépenses existantes saisies avant aujourd’hui ne seront pas comparées à cette politique.
* Lors de la création d’une politique pour une catégorie de dépenses pouvant être détaillée, pensez à ajouter une condition pour le type de ligne de dépenses. Certaines politiques, telles que l’exigence d’un reçu, peuvent ne pas avoir de sens pour les lignes détaillées et ne doivent être appliquées qu’à la ligne d’en-tête ou à une ligne non détaillée. 
* Les politiques de gestion des dépenses sont évaluées par défaut par rapport à l’entité source. Pour les scénarios intersociétés, vous pouvez définir la stratégie de manière à l’évaluer par rapport à l’entité de destination (entité emprunteuse) à la place. Pour exécuter les politiques sur l’entité de destination, activez la fonctionnalité « Évaluer la politique de dépenses par rapport à l’entité juridique emprunteuse » dans l’espace de travail **Gestion des fonctionnalités**.

## <a name="when-to-evaluate-policies"></a>Quand évaluer les politiques

Dans les paramètres de gestion des dépenses, vous disposez d’une option pour évaluer les politiques de gestion des dépenses lorsqu’une ligne est enregistrée ou lorsqu’une note de frais est soumise. Si vous choisissez d’évaluer lorsqu’une ligne est enregistrée, cela permet de garantir que les utilisateurs ont une meilleure visibilité sur ce qu’ils doivent faire pour compléter leur note de frais en une seule fois. Sinon, vous pouvez retarder l’évaluation de la politique et gagner du temps si la validation a lieu à la fin, lors de la soumission au flux de travail.


[!INCLUDE[footer-include](../includes/footer-banner.md)]