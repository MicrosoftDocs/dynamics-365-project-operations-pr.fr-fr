---
title: Gérer plusieurs clients sur le devis d’un projet
description: Cet article fournit des informations sur le travail sur des devis qui impliquent plusieurs clients qui financeront le projet.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b9c82ababdb9a588a0d28cae60a49d0594378d9
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825145"
---
# <a name="manage-multiple-customers-on-a-project-based-quote"></a>Gérer plusieurs clients sur le devis d’un projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Les devis basés sur un projet prennent en charge le scénario où la proposition implique plusieurs clients qui financeront la transaction. L’onglet **Synthèse** du devis a le champ **Client potentiel** qui identifie le client principal de l’opération. D’autres clients pour l’offre peuvent être configurés sur l’onglet **Clients** du devis du projet.

Tous les clients du devis sur l’onglet **Clients** du devis de projet par défaut en tant que clients de la ligne de devis sur toutes les **nouvelles** lignes de devis selon le projet créées pour le devis. Les lignes de devis existantes selon un projet n’hériteront pas des enregistrements client de devis créés après elles.

Les clients de devis et les clients de ligne de devis peuvent être ajoutés, mis à jour ou supprimés à tout moment avant que le devis ne soit conclu. Un client valide sur le devis doit être configuré en tant que client dans la société propriétaire ou l’entité juridique sur la page **Clients**. Les entités juridiques sont créées dans le module **Gestion et comptabilité des projets** de Dynamics 365 Project Operations et sont disponibles en tant que sociétés dans les modules **Ventes de projets et Livraison** de Project Operations.

## <a name="concept-of-a-primary-customer"></a>Concept de client principal

Le client répertorié sur l’onglet **Résumé** du devis de projet en tant que client potentiel est le client principal du devis. Si vous essayez de supprimer le client principal de la liste des clients sur le devis, une erreur s’affiche indiquant qu’un enregistrement de client principal sur un devis ne peut pas être supprimé.

Le client principal ne doit pas être mis à jour à partir de la liste des clients sur le devis. Cependant, vous pouvez influencer le client principal en modifiant le client potentiel sur l’onglet **Résumé** du devis. Lorsque ce champ est mis à jour sur le **Résumé du devis**, le client potentiel nouvellement sélectionné est ajouté en tant que nouveau client de devis avec l’indicateur **Primaire** défini. L’ancien client potentiel sera toujours un client sur le devis.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Créer, mettre à jour ou supprimer un enregistrement client de devis

Un client de devis peut être créé, mis à jour ou supprimé de l’onglet **Clients du devis** sur la page **Devis**. Les champs répertoriés dans le tableau suivant se trouvent sur la fiche client de devis d’un devis de projet.

| **Champ** | **Emplacement** | **Description** | **Impact en aval** |
| --- | --- | --- | --- |
| Compte | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Répertorie tous les comptes actifs. Ce champ est verrouillé après la création de l’enregistrement. Si vous souhaitez le mettre à jour, supprimez l’enregistrement et recréez-le. Si vous avez enregistré des chiffres réels ou si l’enregistrement client du devis est un client principal, vous serez autorisé à supprimer l’enregistrement. | Les clients de devis sont copiés en tant que clients de ligne de devis lorsqu’une ligne de devis est créée. Les clients de devis sont également copiés vers les clients du contrat de projet lorsqu’un devis est remporté. |
| Pourcentage de facturation fractionnée | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Représente le pourcentage de chaque transaction de vente non facturée qui sera attribuée à ce client de devis. | Copié sur les nouvelles lignes de devis créées et sur les clients contractuels du projet. |
| Nom du contact de facturation | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Il s’agit d’un champ de texte qui doit être utilisé pour identifier la personne à contacter pour la facture de ce client. Celle-ci est définie par défaut à partir de l’enregistrement de compte associé | Copié vers les clients du contrat de projet lorsqu’un devis est conclu et ensuite dans le champ Nom de la facture au contrat sur la facture générée pour ce client. |
| Nom de facturation | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Ce champ de texte doit être utilisé pour identifier la personne à contacter pour la facture de ce client. | Copié vers les clients du contrat de projet lorsqu’un devis est conclu et ensuite dans le champ **Nom du contrat à facturer** sur la facture générée pour ce client. |
| Modalités de paiement | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Il s’agit d’un groupe d’options avec des valeurs par défaut de l’enregistrement de compte associé. | Copié vers les clients du contrat de projet lorsqu’un devis est conclu et ensuite dans le champ **Nom du contrat à facturer** sur la facture générée pour ce client. |
| Est arrondi | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Indique si ce client est un client arrondi par défaut pour cette transaction. | Copié vers les clients du contrat de projet lorsqu’un devis est remporté. |
| Société propriétaire | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | L’entité juridique dans laquelle ce client est configuré avec le module **Gestion de projet et comptabilité**. Ce champ est en lecture seule et est défini sur la société propriétaire du devis lui-même. La liste des clients à ajouter dans le champ **Compte** est déjà filtré dans la liste de cette société propriétaire dans le module **Gestion de projet et comptabilité** de Project Operations. | La société propriétaire équivaut au concept d’entité juridique dans le module **Gestion de projet et comptabilité** Project Operations. Tous les coûts et revenus accumulés par ce projet sont comptabilisés dans la comptabilité de la société propriétaire, |
| Limite à ne pas dépasser | Grille modifiable sur l’onglet **Clients du devis** et les formulaires **Principal** et **Création rapide** pour un client de devis. | Indique s’il existe une limite ou un plafond négocié au montant global qui sera facturé à ce client pour cet engagement. | Copié vers les clients du contrat de projet lorsqu’un devis est remporté. |

## <a name="editing-billing-split-percentages"></a>Modification des pourcentages de facturation fractionnée

Vous pouvez modifier les pourcentages de facturation fractionnée à l’aide de l’expérience de modification de grille en ligne. Lorsque les pourcentages de facturation fractionnée ne totalisent pas 100 %%, une erreur se produit. Après avoir mis à jour les pourcentages de facturation fractionnée, actualisez la page pour supprimer l’erreur.

Vous pouvez également essayer de sélectionner **Répartition homogène** dans la sous-grille des clients de devis. Cette action attribue des fractionnements de facturation à tous les clients de devis. S’il y a un facteur d’arrondi, il sera ajouté au client d’arrondi. L’un des clients du devis est toujours identifié comme le client arrondi. cela signifie que l’enregistrement client du devis a l’indicateur **Arrondi** défini sur **Oui**. Il s’agit généralement du client principal du devis, mais cela peut être modifié.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
