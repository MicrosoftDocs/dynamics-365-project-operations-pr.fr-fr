---
title: Configurer les tarifs
description: Cet article fournit des informations sur la manière de configurer des tarifs de prix de revient et de vente.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8a6d96f4a5a8d97e86bbd00413e21f69255a48c5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917665"
---
# <a name="set-up-price-lists"></a>Configurer les tarifs

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les tarifs dans Dynamics 365 Project Operations représentent un catalogue de tarifs. Les tarifs expriment les tarifs de coût, de ventes et de facturation. Selon que le tarif exprime des tarifs de coût ou des tarifs de ventes et de facturation, le contexte du tarif est **Ventes** ou **Coût**.

Les extensions suivantes sont spécifiques à Project Operations et sont appliquées aux tarifs de Dynamics 365 Sales.

- **Contexte** : Ce champ contient les valeurs prises en charge, **Coût** et **Ventes**. La valeur **Achat** n’est pas prise en charge. Définissez le contexte sur **Coût** pour créer un tarif de prix de revient ou définissez le contexte sur **Ventes** pour un tarif de vente. Les prix de revient déterminent le prix du type de coût sur les enregistrements des chiffres estimés et réels. Les tarifs de vente résolvent le prix sur des estimations et des chiffres réels de types de vente non facturés et facturés.
- **Unité de temps** : Unité de temps par défaut pour laquelle le prix est défini dans le tableau **Prix du rôle** pour ce tarif.
- **Entité Tarifs** : Ce champ est masqué par Project Operations pour différencier les tarifs spécifiques à un devis ou à un contrat des tarifs standard et applicables globalement.

## <a name="price-list-header"></a>En-tête de tarif

Le tableau suivant comprend les champs de l’onglet **Général** d’un tarif qui sont propres à Project Operations ou qui présentent des changements de comportement importants par rapport aux tarifs dans Sales.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| Nom | Onglet **Général** et formulaires **Création rapide** | Identité du tarif. | Le tarif est affiché avec cette valeur sur toutes les pages de liste et options de liste déroulante.|
| Contexte | Onglet **Général** et formulaires **Création rapide** | Ce champ peut être défini sur **Coût** ou sur **Ventes**. | Un tarif défini sur **Coût** est utilisé pour rechercher le prix des estimations de coûts et des chiffres réels des coûts. Un tarif défini sur **Ventes** est utilisé pour rechercher le prix des estimations de ventes et des chiffres réels de vente. Seuls les tarifs dont le contexte est défini sur **Ventes** peuvent être attachés aux tarifs de projet pour les clients, aux devis de projet et aux contrats de projet. |
| Date de début | Onglet **Général** et formulaires **Création rapide** | La date de début de la période au cours de laquelle le tarif est effectif. | Avec le champ **Date de fin**, ce champ est utilisé pour déterminer quel tarif est applicable pour une certaine ligne d’estimation ou de chiffres réels. |
| Date de fin | Onglet **Général** et formulaires **Création rapide** | La date de fin de la période au cours de laquelle le tarif est effectif. | Avec le champ **Date de début**, ce champ est utilisé pour déterminer quel tarif est applicable pour une certaine ligne d’estimation ou de chiffres réels. |
| Devise | Onglet **Général** et formulaires **Création rapide** | Ce champ est utilisé pour définir la devise par défaut de chaque rôle, catégorie ou ligne d’élément tarifaire associée à ce tarif. | Sur les tarifs **Ventes**, les rôles, les catégories ou les lignes d’éléments tarifaires ne peuvent pas être créés dans une devise autre que cette devise. Sur les tarifs **Coût**, vous pouvez créer une ligne de prix de rôle dans n’importe quelle devise. La devise définie ici est utilisée par défaut. La configuration utilisateur associée aux prix de rôle peut remplacer cette valeur pour permettre la configuration du taux de coût de la main-d’œuvre dans n’importe quelle devise. Les tarifs de coûts des catégories et les coûts des éléments tarifaires ne peuvent être configurés que dans la devise définie ici. |
| Unité de temps | Onglet **Général** et formulaires **Création rapide** | Ce champ est utilisé pour définir l’unité de temps par défaut de chaque rôle associée à ce tarif. | Cette valeur de champ n’est utilisée que pour la configuration du prix du rôle associé. Sur les tarifs **Coût** et **Ventes**, vous pouvez créer une ligne de prix de rôle dans n’importe quelle unité de temps. L’unité de temps définie ici est utilisée par défaut. La configuration utilisateur associée aux prix de rôle peut remplacer cette valeur pour permettre la configuration du taux de coût de la main-d’œuvre et du taux de facturation dans n’importe quelle unité de temps. |
| Description | Onglet **Général** et formulaires **Création rapide** | Ce champ de texte vous permet de fournir une description sur plusieurs lignes du tarif. | Ce champ est affiché dans les vues **Associé(e)** sur le tarif dans diverses entités qui ont des tarifs associés. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]