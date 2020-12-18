---
title: Vue d'ensemble de la constatation du produit
description: Cette rubrique fournit des informations sur la constatation du produit dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531416"
---
# <a name="revenue-recognition-overview"></a>Vue d'ensemble de la constatation du produit

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Dans Dynamics 365 Project Operations, les principes de constatation du produit varient en fonction de la méthode de facturation choisie pour un projet ou une partie du projet. Cette rubrique fournit des informations sur la constatation du produit dans Project Operations.

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>Transactions comptabilisées utilisant une méthode de facturation des temps et matières

- La constatation des coûts et des revenus est liée. Le coût de transaction et les ventes non facturées sont enregistrés à l'aide du [Journal d'intégration Project Operations](../project-accounting/project-operations-integration-journal.md).
- Le profil de coût et de revenu du projet détermine si les transactions de vente non facturées sont validées dans la comptabilité. Si **Régulariser revenus** est sélectionné, le système utilise les comptes **Valeur des ventes TEC** et **Valeur des ventes des revenus régularisés** lors de la validation. Voici un exemple de cette méthode.  

  | Type de transaction | Débit/crédit | Montant |
  | --- | --- | --- |
  | Valeur des ventes TEC | Débit | 100 |
  | Valeur des ventes des revenus régularisés | Crédit | 100 |

- Le produit est constaté lors de la facturation. Le système utilise le compte **Revenu facturé** lors de la validation. Voici un exemple de cette méthode.  

  | Type de transaction | Débit/crédit | Montant |
  | --- | --- | --- |
  | Solde client | Débit | 120 |
  | Taxe due | Crédit | 20 |
  | Revenu facturé | Crédit | 100 |

- Si des revenus ont été régularisés lors de la validation des ventes non facturées, le système annulera les revenus régularisés lors de la facturation.

  | Type de transaction | Débit/crédit | Montant |
  | --- | --- | --- |
  | Valeur des ventes TEC | Crédit | 100 |
  | Valeur des ventes des revenus régularisés | Débit | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>Transactions comptabilisées utilisant une méthode de facturation à prix fixe

- La constatation des coûts et des revenus est séparée. Le coût de transaction est validé à l'aide du [Journal d'intégration Project Operations](../project-accounting/project-operations-integration-journal.md). Les transactions de vente non facturées ne sont pas créées.
- Le revenu peut être reconnu lors de la facturation si le profil de coût et de revenu du projet **Principe utilisé pour les calculs d'achèvement de projet** est défini sur **Pas de TEC**. N'utilisez cette méthode que pour des projets simples à court terme.
- Le produit peut être constaté à l'aide d'estimations de revenus à prix fixe, avec la méthode **Contrat complété** ou **Reconnaissance des revenus en pourcentage d'achèvement**.

## <a name="additional-resources"></a>Ressources complémentaires
[Configurer la comptabilité des projets facturables](../project-accounting/configure-accounting-billable-projects.md)

[Projets d’estimation de revenus à prix fixe](rev-rec-percentage-completion-method.md)

[Gérer les estimations de revenus](rev-rec-completed-contract-method.md)

[Coût pour compléter les méthodes](cost-complete-methods.md)
