---
title: Définir des politiques de dépenses
description: Vous pouvez définir des politiques de dépenses que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d29b1a9c1a935b933f403f78279b74577d11089007ce1d1090c361075822263a
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986353"
---
# <a name="define-expense-policies"></a>Définir des politiques de dépenses

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez définir les politiques que vos employés devront suivre lors de la saisie et de la soumission des notes de frais et des demandes de déplacement.         
L’implémentation de stratégies de gestion des dépenses vous permet de gérer efficacement les dépenses.         

Par exemple, vous pouvez définir une stratégie pour les frais d’hébergement à New York, qui stipule que le budget par nuit est plafonné à 250 USD.       
Si un employé soumet une note de frais ou une demande de voyage où le tarif de la chambre dépasse ce montant, le système informera         
l’employé que le montant de la dépense a été dépassé, conformément à la politique. Vous pouvez configurer le message que l’employé recevra lorsque vous        
définissez la politique.      
        
Vous pouvez définir trois types de politiques :         
        
- **Avertissement** : Permet à l’employé de soumettre une note de frais ou une demande de voyage, mais la dépense sera marquée pour tous les approbateurs et         
  pour un rapport ultérieur.        

- **Erreur** : Oblige l’employé à réviser la dépense pour se conformer à la politique avant de soumettre la note de frais ou la demande de voyage.        
 
 - **Justification** : Oblige l’employé ou un gestionnaire à saisir une justification pour le dépassement du montant, conformément à la politique, avant de soumettre la note de frais ou la demande de déplacement.        

## <a name="policy-tips"></a>Conseils relatifs aux stratégies
Voici quelques suggestions utiles lors de la création de stratégies de gestion des dépenses : 

- Les stratégies ont une date d’effet. Autrement dit, une stratégie ne prend pas effet si elle est créée avec une date postérieure à celle à laquelle la dépense a eu lieu. Par exemple, vous créez une stratégie aujourd’hui pour plafonner les frais de repas à 50 $. Toutes les dépenses existantes saisies jusqu’à hier ne sont pas comparées à cette stratégie.
- Lors de la création d’une stratégie pour une catégorie de dépense pouvant être détaillée, envisagez d’ajouter une condition pour le type de ligne de dépense. Certaines stratégies telles que l’exigence d’un reçu peuvent n’avoir aucun sens pour les lignes détaillées. Dans ce cas, la stratégie est appliquée uniquement à la ligne d’en-tête ou à une ligne non détaillée. 
- Les stratégies de gestion des dépenses sont évaluées par défaut par rapport à l’entité d’origine. Pour les scénarios intersociétés, vous pouvez définir la stratégie de manière à l’évaluer par rapport à l’entité de destination (entité emprunteuse) à la place. Pour exécuter les politiques sur l’entité de destination, activez la fonctionnalité **Évaluer la politique de dépenses par rapport à l’entité juridique emprunteuse** dans l’espace de travail **Gestion des fonctionnalités**.

## <a name="when-to-evaluate-policies"></a>Quand évaluer les politiques

Dans les paramètres de gestion des dépenses, vous pouvez choisir d’évaluer les politiques de gestion des dépenses lorsqu’une ligne est enregistrée ou lorsqu’une note de frais est soumise. Si vous choisissez d’évaluer le moment où une ligne est enregistrée, les utilisateurs auront une meilleure visibilité sur ce qu’ils doivent faire pour compléter leur note de frais en une seule fois. Sinon, vous pouvez retarder l’évaluation de la politique et gagner du temps en validant à la fin, lors de la soumission au workflow.


[!INCLUDE[footer-include](../includes/footer-banner.md)]