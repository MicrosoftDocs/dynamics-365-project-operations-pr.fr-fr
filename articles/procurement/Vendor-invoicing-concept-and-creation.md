---
title: Créer des factures fournisseur
description: Cet article décrit le concept de factures fournisseur, les scénarios d’utilisation et la façon de créer des factures fournisseur dans Microsoft Dynamics 365 Project Operations.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475417"
---
# <a name="create-vendor-invoices"></a>Créer des factures fournisseur

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Pour utiliser la fonctionnalité décrite dans cet article, vous devez activer la fonctionnalité **Activer le traitement des chiffres réels de sous-contrat avec Project Operations pour les scénarios basés sur les ressources** dans l’espace de travail **Gestion des fonctionnalités**.

La facturation fournisseur dans Microsoft Dynamics 365 Project Operations peut être utilisée pour enregistrer les coûts des livraisons de services et/ou de matériaux sur un projet par les fournisseurs.

Lorsque des services et/ou des matériaux sont sous-traités à un fournisseur, un contrat de sous-traitance représente l’accord contractuel avec ce fournisseur. Au fur et à mesure que le fournisseur fournit les services ou que les matériaux sont reçus et utilisés pour les tâches du projet, les coûts sont enregistrés sur le projet. Le vendeur envoie alors périodiquement des factures. Ces factures qui sont vérifiées et mises en correspondance avec les coûts enregistrés sur le projet. Une fois le processus de vérification terminé, la facture fournisseur est confirmée et validée pour paiement.

## <a name="scenarios-for-use"></a>Scénarios d’utilisation

Les factures fournisseur dans Project Operations peuvent être utilisées pour prendre en charge deux scénarios distincts :

- Les clients utilisent les expériences complètes de sous-traitance.
- Les clients n’utilisent pas les expériences de sous-traitance complètes, mais souhaitent avoir une vue unifiée des coûts des projets dans Project Operations.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Les clients utilisent les expériences complètes de sous-traitance

Les expériences de facturation fournisseur permettent de vérifier et de faire correspondre les entrées de temps, l’utilisation des matériaux et les entrées de dépenses qui font référence aux composants sous-traités avec les lignes de facture fournisseur. Ce processus peut être utilisé pour vérifier l’exactitude des lignes de facture fournisseur. Une fois le processus de vérification terminé et la facture fournisseur confirmée, l’application contrepassera les chiffres réels qui ont été enregistrés par les journaux de temps, de dépense et d’utilisation des matériaux approuvés, et créera des chiffres réels du coût à l’aide des lignes de facture fournisseur.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Les clients n’utilisent pas les expériences de sous-traitance complètes, mais souhaitent avoir une vue unifiée des coûts des projets dans Project Operations

Si vous suivez le processus de sous-traitance dans un système tiers, vous pouvez enregistrer les coûts de ce système tiers dans Project Operations en créant des factures fournisseur qui ne font pas référence aux contrats de sous-traitance. De cette façon, vos chefs de projet peuvent avoir une vue unique et unifiée de tous les coûts d’un projet donné.

## <a name="create-vendor-invoices-in-project-operations"></a>Créer des factures fournisseurs dans Project Operations

Les factures fournisseur sont créées dans Dynamics 365 Finance, en utilisant le module **Comptabilité fournisseur**. Vous ne pouvez pas créer de factures fournisseur directement dans Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Paramétrer la vérification des factures fournisseur

Si la facture fournisseur est destinée à un contrat de sous-traitance dans Dataverse, vous devez activer le paramètre **Vérification manuelle par PM requise**. Le paramétrage de l’option détermine si la facture fournisseur doit être automatiquement confirmée dans Dataverse, ou si elle nécessite une confirmation manuelle. L’en-tête de chaque facture fournisseur de projet inclut une option du même nom. Par défaut, l’option sur l’en-tête de toutes les factures fournisseur de projet est définie sur la valeur que vous définissez ici. Cependant, vous pouvez mettre à jour la valeur selon les besoins sur l’en-tête des factures fournisseur individuelles.

Si l’option est définie sur **Oui**, la facture fournisseur créée dans Finance et synchronisée avec Dataverse a son statut défini sur **Brouillon**. La facture doit ensuite être validée et vérifiée par le chef de projet, puis confirmée, avant d’être traitée et enregistrée sur les comptes spécifiques du projet et du grand livre dans Finance.

Si l’option est définie sur **Non**, la facture fournisseur est automatiquement confirmée. Aucune autre action n’est requise.

Pour paramétrer la vérification de factures fournisseur, procédez comme suit.

1. Dans Finance, accédez à **Gestion et comptabilité des projets** \> **Configuration** \> **Paramètres de gestion et comptabilité des projets**.
1. Sur l’onglet **Finance**, définissez l’option **Vérification manuelle par PM requise** sur **Oui** si la politique de l’entreprise exige la vérification des factures des sous-traitants. Si la vérification par le chef de projet n’est pas requise dans Dataverse, laissez le groupe d’options sur **Non**. Par défaut, le paramètre est utilisé sur la page **Facture fournisseur en attente**.

> [!NOTE]
> Les factures fournisseur créées pour les sous-contrats dans Dataverse ne peut être traité correctement que si l’option **Vérification manuelle par PM requise** est définie sur **Oui**. Les coûts réels de temps, de matériel et de dépenses créés par les sous-traitants peuvent être mis en correspondance manuellement avec les lignes de facture fournisseur par le chef de projet uniquement si cette option est définie sur **Oui**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Configurer un compte d’intégration d’approvisionnement pour les factures fournisseur

Lorsqu’une facture fournisseur est validée dans Finance for Project Operations - Environnement intégré (hors stock), les données financières sont validées sur le compte d’intégration des achats. Le système génère les réels dans Dataverse pour la facture enregistrée. Ces chiffres réels sont validés dans Finance à l’aide du journal d’intégration de projet. La validation de cette feuille d’intégration de Project valide le coût réel et contrepasse le compte d’intégration.

Pour configurer un compte d’intégration d’approvisionnement pour les factures fournisseur, procédez comme suit.

1. Dans Finance, accédez à **Gestion et comptabilité des projets** \> **Configuration** \> **Paramètres de gestion et comptabilité des projets**.
1. Sur l’onglet **Project Operations sur Dynamics 365 Customer Engagement**, sélectionnez **Matériaux** \> **Compte d’intégration des achats**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Créer et valider des factures fournisseurs sous-traitants

Lorsqu’un commis à la comptabilité fournisseur reçoit une facture du sous-traitant, une nouvelle facture est créée dans Finance.

1. Dans Finance, accédez à **Comptabilité fournisseur** \> **Factures** \> **Factures fournisseur en attente**.
1. Dans le **volet Actions**, sélectionnez **Nouveau** pour créer une facture fournisseur.
1. Sur l’en-tête de la facture, dans le champ **Compte de facturation**, sélectionnez **Sous-traitant**.
1. Sélectionnez la date de la facture.
1. Sur l’onglet **En-tête**, définissez l’option **Vérification manuelle par PM requise** sur **Oui**. Le paramètre par défaut de cette option provient de la page **Gestion de projet et paramètres de comptabilité**. Cependant, il peut être modifié au niveau de la facture fournisseur.
1. Sur le raccourci **Ligne de facture**, sélectionnez **Ajouter une ligne** pour créer une ligne de facture fournisseur.
1. Sélectionnez la catégorie d’approvisionnement qui a été créée pour les lignes de sous-traitance et entrez le prix unitaire, l’unité de mesure et la quantité.
1. Dans la section Lignes de facture fournisseur, sur l’onglet **Projet**, sélectionnez le projet pour lequel le sous-traitant partage la facture de sous-traitance.
1. Sélectionnez la catégorie de projet. Il peut s’agir de tout type d’**Article**, de **Dépense**, de **Matériaux** ou d’**Heures**.
1. Sélectionnez le rôle uniquement si la catégorie de projet sélectionnée est de type **Heure**.
1. Sélectionnez **Valider** pour valider la facture fournisseur.

Vous pouvez également créer une facture fournisseur en accédant à **Comptabilité fournisseur** \> **Factures**\>**Factures fournisseur en cours** et en sélectionnant **Nouveau**.

Lorsque la facture fournisseur est comptabilisée, elle devient disponible dans Dataverse pour la vérification et le traitement du chef de projet.

## <a name="vendor-invoice-processing-in-dataverse"></a>Traitement des factures fournisseur dans Dataverse

Dans la facture fournisseur créée dans Dataverse, certaines valeurs de champ proviennent de la facture fournisseur enregistrée dans Finance. Les autres valeurs sont des valeurs par défaut issues du contrat de sous-traitance.

Les champs suivants et les enregistrements associés seront copiés du contrat de sous-traitance vers l’en-tête de la facture fournisseur :

- Devise
- Unité contractante
- Modalités de paiement

Sur les lignes de facture fournisseur, Project Operations utilise les valeurs de champ suivantes pour saisir le sous-contrat par défaut et la référence de ligne de sous-contrat :

- Classe de transaction
- Role
- Catégorie de transaction
- Champs du produit
- Project
- Task

> [!NOTE]
> Les lignes de sous-contrat de prix fixe ne sont pas prises en charge dans Project Operations.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
