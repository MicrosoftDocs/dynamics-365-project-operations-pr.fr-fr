---
title: Gestion de plusieurs clients sur les devis de projet
description: Cette rubrique fournit des informations sur le travail sur les devis avec plusieurs clients qui financeront le projet. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075640"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Gestion de plusieurs clients sur les devis de projet (Ventes)

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Les devis de projet prennent en charge le scénario où la proposition implique plusieurs clients qui financeront la transaction. L’onglet **Synthèse** du devis a le champ **Client potentiel** qui identifie le client principal de l’opération. D’autres clients pour l’offre peuvent être configurés sur l’onglet **Clients** du devis du projet.

Tous les clients du devis sur l’onglet **Clients** du devis de projet par défaut en tant que clients de la ligne de devis sur toutes les **nouvelles** lignes de devis selon le projet créées pour le devis. Les lignes de devis existantes selon un projet n’hériteront pas des enregistrements client de devis créés après elles.

Les lignes de devis basées sur le produit sont automatiquement associées au client principal qui est également le client dans le champ **Client potentiel** sur l’onglet **Résumé** du devis.

Les clients de devis et les clients de ligne de devis peuvent être ajoutés, mis à jour ou supprimés à tout moment avant que le devis ne soit conclu.

## <a name="concept-of-a-primary-customer"></a>Concept de client principal

Le client qui se trouve sur l’onglet Résumé du devis de projet en tant que client potentiel est le client principal du devis. Lorsque vous essayez de supprimer le client principal de la liste des clients sur le devis, une erreur s’affiche indiquant qu’un enregistrement de client principal sur un devis ne peut pas être supprimé.

Le client principal ne doit pas être mis à jour à partir de la liste des clients sur le devis. Cependant, vous pouvez influencer le client principal en modifiant le client potentiel sur l’onglet **Résumé** du devis. Lorsque ce champ est mis à jour sur le **Résumé du devis** , le client potentiel nouvellement sélectionné est ajouté en tant que nouveau client de devis avec l’indicateur **Primaire** défini. L’ancien client potentiel sera toujours un client sur le devis.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Créer, mettre à jour ou supprimer un enregistrement client de devis

Un client de devis peut être créé, mis à jour ou supprimé de l’onglet **Clients du devis** sur la page **Devis**. Les champs répertoriés dans le tableau suivant se trouvent sur la fiche client de devis d’un devis de projet.

| **Champ** | **Emplacement** | **Pertinence, objectif et conseils** | **Impact en aval** |
| --- | --- | --- | --- |
| Compte | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Répertorie tous les comptes actifs. Ce champ est verrouillé après la création de l’enregistrement. Si vous souhaitez le mettre à jour, supprimez l’enregistrement et recréez-le. Si vous avez enregistré des chiffres réels ou si l’enregistrement client du devis est un client principal, vous serez autorisé à supprimer l’enregistrement. | Les clients de devis sont copiés en tant que clients de ligne de devis lorsqu’une ligne de devis est créée. Les clients de devis sont également copiés vers les clients du contrat de projet lorsqu’un devis est remporté. |
| Pourcentage de facturation fractionnée | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Représente le pourcentage de chaque transaction de vente non facturée qui sera attribuée à ce client de devis. | Copié sur les nouvelles lignes de devis et sur les clients contractuels du projet. |
| Nom du contact de facturation | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Il s’agit d’un champ de texte qui doit être utilisé pour identifier la personne à contacter pour la facture de ce client. Celle-ci est définie par défaut à partir de l’enregistrement de compte associé | Copié vers les clients du contrat de projet lorsqu’un devis est conclu et ensuite dans le champ Nom de la facture au contrat sur la facture générée pour ce client. |
| Nom de facturation | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Ce champ de texte doit être utilisé pour identifier la personne à contacter pour la facture de ce client. | Copié vers les clients du contrat de projet lorsqu’un devis est conclu et ensuite dans le champ **Nom du contrat à facturer** sur la facture générée pour ce client. |
| Modalités de paiement | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Il s’agit d’un groupe d’options avec des valeurs par défaut de l’enregistrement de compte associé. | Copié vers les clients du contrat de projet lorsqu’un devis est conclu et ensuite dans le champ **Nom du contrat à facturer** sur la facture générée pour ce client. |
| Est arrondi | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Indique si ce client est un client arrondi par défaut pour cette transaction. | Copié vers les clients du contrat de projet lorsqu’un devis est remporté. |
| Limite à ne pas dépasser | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Indique s’il existe une limite ou un plafond négocié au montant global qui sera facturé à ce client pour cet engagement | Copié vers les clients du contrat de projet lorsqu’un devis est remporté. |

## <a name="editing-billing-split-percentages"></a>Modification des pourcentages de facturation fractionnée

Vous pouvez modifier les pourcentages de facturation fractionnée à l’aide de l’expérience de modification de grille en ligne. Lorsque les pourcentages de facturation fractionnée ne totalisent pas 100 %, une erreur se produit. Après avoir mis à jour les pourcentages de facturation fractionnée, actualisez la page pour supprimer l’erreur.

Vous pouvez également essayer de sélectionner **Répartition homogène** sur la sous-grille des clients de devis. Cette action attribue des fractionnements de facturation à tous les clients de devis. S’il y a un facteur d’arrondi, il sera ajouté au client d’arrondi. L’un des clients du devis est toujours identifié comme le client arrondi. cela signifie que l’enregistrement client du devis a l’indicateur **Arrondi** défini sur **Oui**. Il s’agit généralement du client principal du devis, mais cela peut être modifié.
