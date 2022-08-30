---
title: Gestion des tarifs fournisseur et achat dans Project Operations
description: Cet article fournit des informations qui vous aideront à créer et à gérer les données des fournisseurs et les tarifs d’achat pour la sous-traitance.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3cd883fed8a59f1c54c39e2d051b9748833ba692
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261884"
---
# <a name="vendor-and-purchase-price-list-management-in-project-operations"></a>Gestion des tarifs fournisseur et achat dans Project Operations


_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

## <a name="vendors-in-project-operations"></a>Fournisseurs dans Project Operations

Dans Microsoft Dynamics 365 Project Operations, les comptes fournisseurs ont un type de relation **Fournisseur** ou **Fournisseur**. Vous ne pouvez pas sélectionner un enregistrement de compte d′un autre type de relation que fournisseur sur un contrat de sous-traitance.

Vous pouvez associer un ou plusieurs tarifs achat à un enregistrement fournisseur. Toutefois, chaque tarif achat associé à un enregistrement fournisseur doit avoir une date donnée effective différente. Le chevauchement des dates données effectives n’est pas pris en charge pour les tarifs achat dans Project Operations.

Par défaut, les champs et concepts suivants dans un enregistrement fournisseur sont utilisés pour tout contrat de sous-traitance créé pour le fournisseur :

- Modalités de paiement
- Contact de facturation
- Contact principal

    > [!NOTE]
    > Par défaut, le contact principal du fournisseur est utilisé comme gestionnaire de compte fournisseur du contrat de sous-traitance.

- Devise
- Tarifs achat actuels

## <a name="purchase-price-lists-in-project-operations"></a>Tarifs achat dans Project Operations

Les tarifs pour lesquels le champ **Contexte** est défini sur **Achat** sont considérés comme des tarifs achat. Les tarifs achat peuvent être définis pour représenter un catalogue de tarifs achat pour le temps, les dépenses et les matériaux. Les tarifs achat ressemblent aux tarifs de revient et de vente dans Project Operations. Les concepts suivants s′appliquent aux tarifs achat de la même manière qu′ils s′appliquent aux tarfis de revient et de vente :

- **Date donnée effective** : les tarifs achat ont une date donnée effective. Cette date données effective est représentée par les champs de date de début et de date de fin de chaque tarif. Le temps entre la date de début et la date de fin est la période de date donnée effective.
- **Devise** : devise dans l′en-tête des tarifs utilisée pour exprimer les prix d′achat pour la main-d′œuvre, les catégories de dépenses et les produits du catalogue.
- **Unité de temps par défaut** : exprime les prix de la main-d′œuvre pour les achats. Le champ d′unité de temps sur des tarifs est utilisé uniquement pour fournir une valeur par défaut. Cette valeur peut être modifiée au niveau de chaque ligne de prix du rôle.

Les tarifs achat peuvent être joints aux enregistrements fournisseur en tant qu′associations appelées tarifs du projet. Ces tarifs permettent de saisir les prix par défaut sur les lignes de sous-traitance. Par défaut, si plusieurs tarifs achat sont joints à un enregistrement fournisseur, les tarifs les plus récents sont utilisés pour les sous-contrats créés pour le fournisseur. Seuls les tarifs pour lesquels le champ **Contexte** est défini sur **Achat** peuvent être joints aux enregistrements fournisseur.

### <a name="subcontract-specific-purchase-price-lists"></a>Tarifs achat spécifiques à la sous-traitance

Des tarifs achat peuvent également être joints aux contrats de sous-traitance en tant qu′associations appelées tarifs du projet. Ces tarifs permettent de saisir les prix par défaut sur les lignes de sous-traitance. Par défaut, si plusieurs tarifs achat sont joints à un contrat de sous-traitance, chacun doit avoir une date donnée effective différente. Le chevauchement des dates données effectives n’est pas pris en charge pour les tarifs achat dans Project Operations. Seuls les tarifs pour lesquels le champ **Contexte** est défini sur **Achat** peuvent être joints aux contrats de sous-traitance.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
