---
title: Gérer les tarifs des projets sur les devis de projet
description: Cette rubrique fournit des informations sur l’utilisation de tarifs de projet sur les devis. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075663"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Gérer les tarifs des projets sur les devis de projet (Ventes)

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Les devis de projet sont conçus pour prendre en charge des tarifs de vente effectifs à plusieurs dates. Avec Dynamics 365 Project Operations, une nouvelle entité associée appelée **Tarifs des projets** est ajoutée. Cette entité a une relation 1 à plusieurs avec un devis de projet.

Les tarifs de projet sont utilisés pour évaluer les transactions de temps et de dépenses sur un projet. Lorsqu’un devis comporte un ou plusieurs tarifs de projet, ces tarifs sont utilisés pour évaluer les estimations de temps et de dépenses et les chiffres réels sur les projets associés au devis via la ligne de devis.

Lorsqu’il n’y a pas de tarifs de projet sur un devis de projet, vous recevez un message d’avertissement. Le message indique qu’en l’absence de tarifs de projet, le travail et les dépenses estimés et réels de votre projet ne seront pas facturés. Au lieu de cela, ils auront un prix de zéro (0) pour les valeurs de vente.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Associer ou dissocier un tarif de projet sur un devis de projet

Pour créer ou sélectionner des tarifs spécifiques pour estimer le travail et les dépenses liés au projet, procédez comme suit.

1. Sur le devis, sélectionnez l’onglet **Prix du projet** et dans la sous-grille, sélectionnez **+ Ajouter un nouveau tarif de projet**.
2. Sur la page de création rapide, sélectionnez un tarif. La liste déroulante affiche tous les tarifs dont le contexte est défini sur **Ventes** et la devise correspond à la devise sur le devis.
4. Entrez une description pour l’association de tarif du projet et sélectionnez **Enregistrer et fermer**.

Une association de tarif du projet est créée.

Vous pouvez répéter ce processus si vous devez associer plusieurs tarifs de projet au devis de projet. Ne créez plusieurs tarifs de projet que si vous avez des dates de validité différentes pour chacun des tarifs de projet associées.

> [!NOTE]
> Project Operations ne prend pas en charge le chevauchement des dates de validité des tarifs du projet. S’il existe plusieurs tarifs de projet pour une transaction avec une date donnée, le prix de cette transaction sera défini par défaut sur zéro (0).
Pour supprimer une association de tarifs de projet, sélectionnez le tarif de projet, puis **Supprimer le tarif du projet de devis**. Le tarif est supprimé des tarifs du projet du devis, mais le tarif lui-même n’est pas supprimé. Seule l’association au devis est supprimée.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Configurer des tarifs de projet par défaut sur un devis

Les tarifs de projet peuvent être définis par défaut sur un devis de projet. Cette configuration garantit que tous les devis de votre organisation commencent toujours par un tarif standard pour cette période de prix.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Configurer une valeur d’organisation par défaut pour un tarif de projet

1. Accédez à **Paramètres** > **Général** > **Paramètres**.
2. Sur la page de liste **Paramètres actifs** , recherchez l’enregistrement et double-cliquez pour l’ouvrir. 
3. Sur la page **Paramètres** , sélectionnez l’onglet **Tarifs**. Vous pouvez voir que la liste des tarifs par défaut est affichée. Il s’agit de tarifs standard de coûts et de prix de vente de liste. Le fait d’associer ici un tarif de vente pour chaque devise dans laquelle vous vendez garantit que ce tarif de vente est défini par défaut sur tout devis que vous créez pour les clients qui effectuent des transactions dans cette devise.

### <a name="set-up-customer-specific-project-price-lists"></a>Configurer des tarifs de projet spécifiques au client

Des tarifs de projet spécifiques au client peuvent également être configurés lorsque vous avez négocié un accord de tarification principal avec vos clients.

Pour configurer un tarif de projet spécifique au client, procédez comme suit.

1. Dans la zone **Ventes** , sélectionnez **Clients**.
2. Dans la liste de vos comptes actifs, sélectionnez et ouvrez la fiche client pour laquelle vous avez un tarif spécial.
3. Sur l’onglet **Tarifs des projets** , vous pouvez créer une association de tarifs pour avoir le tarif du projet qui est spécifique à ce client.

## <a name="create-custom-pricing-on-a-project-quote"></a>Créer une tarification personnalisée sur un devis de projet

Une fois que vous disposez de tarifs de projet par défaut pour l’organisation et le client, vos devis de projet seront automatiquement créés avec ces associations de tarifs de projet. Cependant, dans certains cas, vous devrez peut-être créer une tarification personnalisée pour un devis de projet spécifique. 

1. Sur le **Devis de projet** , sur l’onglet **Tarif du projet** , vérifiez dans la sous-grille qu’aucun enregistrement de tarif spécifique n’est sélectionné.
2. Sélectionnez **Créer des tarifs personnalisés**. Cela fera des copies de tous les tarifs standard actuellement associés au devis et associera ces copies au devis. Les associations existantes avec les tarifs standard seront supprimées. Le vendeur peut alors commencer à modifier les prix de ces copies. Ces prix modifiés seront applicables à ce devis de projet uniquement.
