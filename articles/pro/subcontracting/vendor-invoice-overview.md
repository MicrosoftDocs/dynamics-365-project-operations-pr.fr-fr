---
title: Facturation fournisseur - Concept et réalisation
description: Cet article décrit le concept de factures fournisseur, les scénarios d’utilisation et la façon de créer des factures fournisseur dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261931"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Facturation fournisseur - Concept et réalisation

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

La facturation fournisseur dans Microsoft Dynamics 365 Project Operations peut être utilisée pour enregistrer les coûts des livraisons de services et/ou de matériaux sur un projet par les fournisseurs.

Lorsque des services et/ou des matériaux sont sous-traités à un fournisseur, un contrat de sous-traitance représente l’accord contractuel avec ce fournisseur. Au fur et à mesure que le fournisseur fournit les services ou que les matériaux sont reçus et utilisés pour les tâches du projet, les coûts sont enregistrés sur le projet. Périodiquement, le fournisseur envoie des factures qui sont vérifiées et mises en correspondance avec les coûts enregistrés sur le projet. Une fois le processus de vérification terminé, la facture fournisseur est confirmée et validée pour paiement.

## <a name="scenarios-for-use"></a>Scénarios d’utilisation

Les factures fournisseur dans Project Operations peuvent être utilisées pour prendre en charge deux scénarios distincts.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Les clients utilisent les expériences complètes de sous-traitance

Les expériences de facturation fournisseur permettent de vérifier et de faire correspondre les entrées de temps, l’utilisation des matériaux et les entrées de dépenses qui font référence aux composants sous-traités avec les lignes de facture fournisseur. Ce processus peut être utilisé pour vérifier l’exactitude des lignes de facture fournisseur. Une fois le processus de vérification terminé et la facture fournisseur confirmée, l’application contrepassera les chiffres réels qui ont été enregistrés par les journaux de temps, de dépense et d’utilisation des matériaux approuvés, et créera des chiffres réels du coût à l’aide des lignes de facture fournisseur.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Les clients n’utilisent pas les expériences de sous-traitance complètes, mais souhaitent avoir une vue unifiée des coûts des projets dans Project Operations

Si vous suivez le processus de sous-traitance dans un système tiers, vous pouvez enregistrer les coûts de ce système tiers dans Project Operations en créant des factures fournisseur qui ne font pas référence aux contrats de sous-traitance. De cette façon, vos chefs de projet peuvent avoir une vue unique et unifiée de tous les coûts d’un projet donné.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Création de factures fournisseurs dans Project Operations

Les factures fournisseur peuvent être créées de deux manières :

- À partir de la page de liste des factures fournisseur ou de la page de détails d’une seule facture fournisseur
- Depuis la page de liste des sous-traitants ou la page de détails d’un seul contrat de sous-traitance

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Création à partir de la page de liste des factures fournisseur ou de la page de détails

1. Accédez à **Achat** \> **Factures fournisseurs**.
2. Sur la page de liste des factures fournisseur ou sur la page de détails d’une facture fournisseur unique, sélectionnez **Nouveau** pour créer une nouvelle facture fournisseur.

Les factures fournisseur ainsi créées peuvent également faire référence à un contrat de sous-traitance.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Création à partir de la page de liste des contrats de sous-traitance ou de la page de détails

1. Accédez à **Achat** \> **Sous-traitance**.
2. Sélectionner un ou plusieurs contrats de sous-traitance.
3. Sur la page de liste des contrats de sous-traitance ou sur la page de détails d’un contrat de sous-traitance unique, sélectionnez **Créer une facture fournisseur** pour créer une nouvelle facture fournisseur.

Une nouvelle facture fournisseur dans **Brouillon** est créée pour chaque contrat de sous-traitance que vous avez sélectionné.

Les factures fournisseur que vous créez de cette manière font toujours référence au contrat de sous-traitance dans l’en-tête de la facture fournisseur. Chaque ligne du contrat de sous-traitance avec un mode de facturation Temps et Matériel entraînera la création d’une ligne sur la facture fournisseur. Chaque ligne du contrat de sous-traitance ayant un mode de facturation à prix fixe entraînera la création d’une ligne sur la facture fournisseur pour chaque jalon de ligne de contrat de sous-traitance dont le statut est **Prêt à facturer**.

Les champs suivants et les enregistrements associés seront copiés du contrat de sous-traitance vers l’en-tête de la facture fournisseur :

- Fournisseur.
- Les listes de prix associées seront copiées sur la facture fournisseur en tant que listes de prix.
- Devise.
- Unité contractante.
- Modalités de paiement.

Pour les lignes de sous-traitance Temps et Matériel, les champs suivants et les enregistrements associés seront copiés de la ligne de sous-traitance vers la ligne de facture fournisseur :

- Références de sous-traitance et de ligne de sous-traitance
- Classe de transaction
- Role
- Catégorie de transaction
- Champs du produit
- Project
- Task
- Ressource pouvant être réservée

Pour les lignes de sous-traitance Prix fixe, les champs suivants seront copiés de la ligne de sous-traitance et du jalon de la ligne de sous-traitance vers la ligne de facture fournisseur :

- Références de sous-traitance et de ligne de sous-traitance.
- Classe de transaction. Par défaut, la valeur sera **Jalon**.
- Le nom et le montant de l’étape seront copiés à partir de l’étape de la ligne de sous-traitance associée.
- L’utilisateur pourra sélectionner un projet et une tâche sur la ligne de facture fournisseur.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
