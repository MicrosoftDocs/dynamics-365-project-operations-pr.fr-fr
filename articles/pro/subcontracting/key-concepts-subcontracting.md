---
title: Concepts clés de la sous-traitance
description: Cette rubrique explique certains concepts clés qui s′appliquent à la sous-traitance dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 159eeca3aa9ed0c490be5ce3a8f46c7d7206aebe
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578108"
---
# <a name="key-concepts-in-subcontracting"></a>Concepts clés de la sous-traitance

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

La rubrique explique certains concepts clés que vous devez connaître avant de commencer à utiliser la fonctionnalité de sous-traitance dans Microsoft Dynamics 365 Project Operations.

## <a name="contracting-unit-on-the-subcontract"></a>Unité contractante sur le contrat de sous-traitance

L’unité contractante représente la division ou le cabinet responsable de la livraison du projet éventuel. L′unité contractante est également la division qui entre en relation contractuelle avec le fournisseur.

## <a name="purchase-currency"></a>Devise d′achat

Dans Project Operations, la devise d′achat correspond à la devise dans laquelle le contrat de sous-traitance est créé. Il s′agit également de la devise dans laquelle les coûts de sous-traitance sur un projet sont enregistrés. La devise d′achat peut être différente de la devise du projet et la devise du projet peut, à son tour, être différente de la devise de vente.

## <a name="billing-methods-on-subcontract-lines"></a>Modes de facturation sur les lignes du contrat de sous-traitance

Pour les projets, il existe en général les modèles de contrats forfaitaires et facturés à l’utilisation. Project Operations prend en charge ces méthodes de facturation dans les contextes de vente et d′achat. Pour un achat, les méthodes de facturation fonctionnent de la manière suivante :

- **Temps et matériel** : si une ligne de sous-traitance utilise la méthode de facturation **Temps et matériel**, le coût du temps est enregistré sur le projet au fur et à mesure que les sous-traitants travaillent sur ce projet et enregistrent le temps. Ces transactions des coûts de sous-traitance sont ensuite rapprochées des éléments de ligne sur les factures fournisseur. Dans ce modèle, les chefs de projet qui utilisent Project Operations peuvent faire correspondre et vérifier les lignes des factures fournisseur avec le temps de sous-traitance enregistré et approuvé. Une fois la vérification terminée, les chiffres réels de coût antérieurs enregistrés après l′approbation sont annulés et les nouveaux chiffres réels de coût basés sur la facture fournisseur sont créés sur le projet.
- **Prix fixe** : dans ce modèle de contrat forfaitaire, les factures fournisseur sont basées sur des jalons fixes. Cependant, les sous-traitants peuvent également indiquer le temps. Ce temps est ensuite revu et validé par le chef de projet. Une fois approuvé, Project Operations crée des chiffres réels de coût temporaires sur le projet. Dès que le fournisseur envoie une facture pour un jalon, le chef de projet peut comparer les chiffres réels de coût enregistrés précédemment avec le jalon. Une fois la vérification terminée, les chiffres réels de coût sont annulés et le coût basé sur le jalon est enregistré.

## <a name="project-price-lists-on-subcontracts"></a>Tarifs du projet sur des contrats de sous-traitance

Les tarifs de projet servent à configurer les prix d′achat pour le temps, les dépenses et les autres composants liés au projet. Il peut y avoir plusieurs listes de prix, chacune pouvant avoir son propre contrat de sous-traitance avec date d′effet dans Project Operations. Project Operations ne prend pas en charge le chevauchement des dates d′effet sur les listes de prix de projet pour un contrat de sous-traitance.

## <a name="transaction-classes-on-subcontracts"></a>Classes de transactions sur les contrats de sous-traitance

Project Operations prend en charge quatre types de classes de transactions :

- Temps
- Dépense
- Matériel
- Frais

Les coûts d′achat peuvent être estimés et engagés dans les classes de transactions **Temps**, **Dépense** et **Matériel** uniquement. **Frais** est une classe de transaction de revenus uniquement et n′est pas disponible dans les achats.

## <a name="purchase-pricing-dimensions"></a>Dimensions de tarification d′achat

Les dimensions de tarification permettent de décider quels attributs sont utilisés pour la configuration du prix d′achat et les transactions par défaut en temps. En ce qui concerne les achats, Project Operations ne prend en charge que les ensembles de dimensions fixes pour la configuration et la valeur par défaut du prix d′achat. Pour la configuration et la valeur par défaut du prix d′achat sur les lignes des contrats de sous-traitance et les transactions de temps de sous-traitance, les attributs sont **Rôle** et **Ressource réservable**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
