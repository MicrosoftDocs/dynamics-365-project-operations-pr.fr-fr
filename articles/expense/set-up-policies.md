---
title: Définir des politiques de dépenses
description: Vous pouvez définir des politiques de dépenses que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 30b3a0e1547ca7043b1433da2b4ebf02f2b473a1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075810"
---
# <a name="define-expense-policies"></a>Définir des politiques de dépenses

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez définir les politiques que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.         
La mise en œuvre de politiques de dépenses peut vous aider à gérer efficacement les dépenses.         

Par exemple, vous pouvez définir une politique pour les dépenses d'hôtel à New York, qui stipule que les dépenses par nuit ne peuvent pas dépasser 250 USD.       
Si un employé soumet une note de frais ou une demande de voyage où le tarif de la chambre dépasse ce montant, le système informera         
l'employé que le montant de la dépense a été dépassé, conformément à la politique. Vous pouvez configurer le message que l'employé recevra lorsque vous        
définissez la politique.      
        
Vous pouvez définir trois types de politiques :         
        
- **Avertissement**  : Permet à l'employé de soumettre une note de frais ou une demande de voyage, mais la dépense sera marquée pour tous les approbateurs et         
  pour un rapport ultérieur.        

- **Erreur**  : Oblige l'employé à réviser la dépense pour se conformer à la politique avant de soumettre la note de frais ou la demande de voyage.        
 
 - **Justification**  : Oblige l'employé ou un gestionnaire à saisir une justification pour le dépassement du montant, conformément à la politique, avant de soumettre la note de frais ou la demande de déplacement.        

## <a name="policy-tips"></a>Conseils en matière de politique
Voici quelques suggestions qui peuvent vous aider lors de la création de nouvelles politiques de gestion des dépenses : 

- Les politiques sont à date d'entrée en vigueur, ce qui signifie qu'une politique ne prendra pas effet si elle est créée avec une date postérieure à la date à laquelle la dépense a eu lieu. Par exemple, vous pouvez créer une nouvelle politique afin d'appliquer une dépense de repas maximale de 50 USD. Toutes les dépenses existantes saisies avant ne seront pas comparées à cette politique.
- Lors de la création d'une politique pour une catégorie de dépenses pouvant être détaillée, pensez à ajouter une condition pour le type de ligne de dépenses. Certaines politiques, telles que l'exigence d'un reçu, peuvent ne pas avoir de sens pour les lignes détaillées. Dans ce cas, la politique est appliquée uniquement à la ligne d'en-tête ou à une ligne non détaillée. 
- Les politiques de gestion des dépenses sont évaluées par défaut par rapport à l'entité source. Pour les scénarios intersociétés, vous pouvez définir la stratégie à évaluer par rapport à l'entité de destination (entité emprunteuse) à la place. Pour exécuter les politiques sur l'entité de destination, activez la fonctionnalité **Évaluer la politique de dépenses par rapport à l'entité juridique emprunteuse** dans l'espace de travail **Gestion des fonctionnalités**.

## <a name="when-to-evaluate-policies"></a>Quand évaluer les politiques

Dans les paramètres de gestion des dépenses, vous pouvez choisir d'évaluer les politiques de gestion des dépenses lorsqu'une ligne est enregistrée ou lorsqu'une note de frais est soumise. Si vous choisissez d'évaluer le moment où une ligne est enregistrée, les utilisateurs auront une meilleure visibilité sur ce qu'ils doivent faire pour compléter leur note de frais en une seule fois. Sinon, vous pouvez retarder l'évaluation de la politique et gagner du temps en validant à la fin, lors de la soumission au workflow.
