---
title: Réviser l'arriéré de facturation sur les projets et les contrats de projet
description: Cette rubrique explique comment vérifier les arriérés de temps, de dépenses, et de produits, et comment les marquer comme prêts pour la facturation.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168102"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a>Réviser l'arriéré de facturation sur les projets et les contrats de projet

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Lorsqu'une transaction est prête pour qu'une facture soit créée et traitée, la transaction doit être marquée comme **Prêt pour la facturation**. Cette rubrique décrit les types de transactions qui peuvent être créés.

## <a name="review-the-time-and-material-billing-backlog"></a>Réviser les arriérés de facturation du temps et des matériaux

Lorsqu'une entrée de temps ou de dépenses est envoyée et approuvée pour un projet, PSA crée un chiffre réel de projet. Si la combinaison du projet et de la classe de transaction sont mappés à une ligne de contrat pour le projet temps et matériaux, deux chiffres réels sont créés lorsque l'entrée est approuvée :

- Coût réel 
- Chiffre réel de ventes non facturées

Les chiffres réels de ventes non facturées représentent l'arriéré de facturation, et leur statut de facturation doit être défini sur **Prêt pour la facturation**. Lorsqu'une facture de projet est créée, les chiffres réels de ventes non facturées marqués comme **Prêt pour la facturation** sont copiés comme des détails de ligne de facture.

Pour vérifier les arriérés de facturation pour le temps et les matériaux, accédez à **Ventes** \> **Facturation** \> **Arriéré de facturation de temps et de matériaux**. Sélectionnez tous les chiffres réels de ventes non facturés prêts à être facturés, puis sélectionnez **Prêt pour la facturation**. Le statut de facturation de ces chiffres réels passe à **Prêt pour la facturation**.

![Arriérés de facturation pour le temps et le matériel](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a>Vérifier l'arriéré de facturation pour les produits

Dans PSA, lorsqu'un contrat de projet contient des lignes de contrat basées sur les produits, ces lignes sont considérées pour la facturation chaque fois qu'une facture est créée pour le contrat du projet. Tout produit qui possède des lignes de contrat marquées comme **Prêt pour la facturation** est copié sur une facture de projet sous forme de lignes de facture de projet.

Pour vérifier les arriérés de facturation pour les produits, accédez à **Ventes** \> **Facturation** \> **Arriéré de facturation de produit**. Sélectionnez toutes les lignes de contrat basées sur des produits prêtes à être facturées, puis sélectionnez **Prêt pour la facturation**. Le statut de facturation de ces lignes passe à **Prêt pour la facturation**.

![Arriéré de facturation pour les produits](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a>Vérifiez les jalons de facturation sur les contrats à prix fixe

Chaque ligne de contrat de projet avec une méthode de facturation à prix fixe doit définir des jalons de contrat. Ces jalons de contrat peuvent être facturés uniquement s'ils sont marqués comme **Prêt pour la facturation**. 

Pour vérifier les jalons de facturation, accédez à **Ventes** \> **Facturation** \> **Jalons de forfait**. Sélectionnez les jalons prêts à être facturés, puis sélectionnez **Prêt pour la facturation**. Le statut de facturation de ces jalons passe à **Prêt pour la facturation**.

![Jalons à prix fixe](media/FPBacklog.png)
