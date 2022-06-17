---
title: Vérification des factures fournisseurs avec les chiffres réels approuvés
description: Cet article explique comment Microsoft Dynamics 365 Project Operations permet aux chefs de projet de vérifier les factures des fournisseurs avec les chiffres réels qui ont été approuvés au fur et à mesure que les sous-traitants ont effectué le travail et enregistré le temps, ainsi que les dépenses et les matériaux utilisés par les membres de l’équipe de projet.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 43f47a44260d1a47437846f2764b56f680d4b682
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914215"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Vérification des factures fournisseurs avec les chiffres réels approuvés

[!include [banner](../../includes/dataverse-preview.md)]

**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma

Microsoft Dynamics 365 Project Operations permet aux chefs de projet de vérifier les lignes de facture fournisseur de la manière suivante :

- Utilisez le champ **Statut de vérification** sur les lignes de facture fournisseur.
- Si les lignes de facture fournisseur font référence à une ligne de sous-traitance, liez les chiffres réels du coût de l’activité du sous-traitant à ces lignes de facture fournisseur. Le lien est créé en faisant correspondre les chiffres réels du coût aux lignes de facture fournisseur.

    > [!NOTE]
    > Bien que le statut de vérification puisse être suivi pour les lignes de facture fournisseur qui ne font pas référence à un contrat de sous-traitance, les chiffres réels du coût ne peuvent pas être associés à ces lignes de facture fournisseur.

## <a name="verification-status"></a>Statut de vérification

Le champ **Statut de la vérification** sur une ligne de facture fournisseur indique le statut de la vérification. Les statuts suivants sont pris en charge :

1. Non démarré(e)(s)
2. En cours
3. Terminée

Les lignes de facture fournisseur ayant un statut de vérification **Non démarré** peuvent être modifiées.

Les lignes de facture fournisseur ayant un statut de vérification **En cours** ne peuvent plus être modifiées. Pour une ligne de facture fournisseur faisant référence à un contrat de sous-traitance, le statut de vérification est automatiquement défini sur **En cours** dès que le premier chiffre réel du coût est mis en correspondance avec la ligne de facture fournisseur.

Les lignes de facture fournisseur ayant un statut de vérification **Terminé** ne peuvent plus être modifiées. Lorsque toutes les lignes d’une facture fournisseur ont ce statut de vérification, la facture fournisseur ne peut pas être confirmée.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Faire correspondre les chiffres réels du coût aux lignes de facture fournisseur

La correspondance des chiffres réels du coût facilite le processus de vérification sur une ligne de facture fournisseur. Pour faire correspondre les chiffres réels du coût à une ligne de facture fournisseur, procédez comme suit.

1. Ouvrez la ligne de facture fournisseur et sélectionnez l’onglet **Chiffres réels de coût sans correspondance**. Une grille affiche une liste des chiffres réels du coût qui font référence à la même ligne de contrat de sous-traitance que la ligne de facture fournisseur.
2. Sélectionnez un ou plusieurs chiffres réels du coût, puis sélectionnez **Mettre en correspondance** dans la barre d’outils au-dessus de la grille. Le système valide que les chiffres réels du coût sélectionnés peuvent être rapprochés. Une fois la validation réussie, les chiffres réels du coût sont associés à la ligne de facture fournisseur.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Critères de validation utilisés pour associer les chiffres réels du coût aux lignes de facture fournisseur

Lors du processus de mise en correspondance, un lien entre un chiffre réel du coût et une ligne de facture fournisseur ne peut être établi que si les deux conditions suivantes sont remplies :

- Le champ **Statut d’ajustement** pour chaque chiffre réel du coût sélectionné doit être vide. En d’autres termes, les chiffres réels du coût ne doivent pas avoir été remplacés par d’autres chiffres réels du coût lors d’un processus de journal de rappel, d’annulation d’approbation ou de correction.
- Les valeurs des champs suivants sont mises en correspondance entre la ligne de facture fournisseur et le chiffre réel du coût sélectionné. Si un champ n’est pas défini sur la ligne de facture fournisseur, il n’est pas pris en compte pour la correspondance.

    - Contrat du projet
    - Ligne de contrat du projet
    - Classe de transaction
    - Project
    - Task
    - Catégorie des ressources
    - Catégorie de transaction
    - Produit
    - Ligne de sous-traitance
    - Ressource pouvant être réservée

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Dissocier les chiffres réels de coût d’une ligne de facture fournisseur

La dissociation des chiffres réels du coût peut également faciliter le processus de vérification sur une facture fournisseur en permettant la suppression des liens précédemment établis. Les chiffres réels du coût peuvent être dissociés uniquement des lignes de facture fournisseur ayant un statut de vérification **En cours**. Pour dissocier les chiffres réels du coût depuis une ligne de facture fournisseur, procédez comme suit.

1. Ouvrez la ligne de facture fournisseur et sélectionnez l’onglet **Chiffres réels de coût avec correspondance**. Une grille affiche une liste des chiffres réels du coût qui font référence à la ligne de facture fournisseur.
2. Sélectionnez un ou plusieurs chiffres réels du coût, puis sélectionnez **Dissocier** dans la barre d’outils au-dessus de la grille.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
