---
title: Gérer plusieurs clients sur les lignes de contrat basées sur un projet
description: Cette rubrique fournit des informations sur l’utilisation des lignes de contrat et des contrats comprenant plusieurs clients.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 71081775ab45167bc1bff1979f7856a2a2a91385
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181899"
---
# <a name="manage-multiple-customers-on-project-based-contract-lines"></a>Gérer plusieurs clients sur les lignes de contrat basées sur un projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les lignes de contrat basées sur un projet peuvent inclure une liste de clients responsables du paiement. Cette liste de clients sur la ligne de contrat basée sur un projet peut être identique à la liste de clients du contrat, mais cela n’est pas obligatoire. Lorsqu’un devis de projet est remporté et qu’un contrat de projet est créé, la liste des clients de la ligne de devis est copiée dans la ligne de contrat correspondante. Les clients figurant sur le devis sont copiés dans le contrat.

Lorsque le contrat de projet est facturé, la liste de clients sur la ligne de contrat basée sur un projet est prioritaire par rapport à la liste de clients figurant sur le contrat. La liste des clients du contrat de projet est uniquement utilisée pour la création de lignes de contrat par défaut.

Tous les clients du contrat figurant sur l’onglet **Clients** du contrat de projet sont créés par défaut en tant que clients de ligne de contrat sur toutes les lignes de contrat créées pour le contrat de projet. Une fois créées, les lignes de contrat existantes n’hériteront pas des nouveaux enregistrements de clients de contrat.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Créer, mettre à jour ou supprimer un enregistrement de client de ligne de contrat

Vous pouvez créer, mettre à jour ou supprimer un client de ligne de contrat sous l’onglet **Clients de la ligne de contrat** sur la page **Ligne de contrat basée sur un projet**. Lorsqu’un nouveau client est ajouté à la ligne de contrat basée sur un projet, il est également ajouté au contrat d’ensemble en tant que client de contrat avec un pourcentage de fractionnement de facturation par défaut de 0 %. Le pourcentage de fractionnement de la facturation sur le contrat d’ensemble est copié dans les nouvelles lignes de contrat et dans le contrat de projet éventuel. Cependant, lors de la facturation à partir du contrat, c’est le pourcentage de fractionnement de la facturation au niveau de la ligne de contrat qui est utilisé et non celui au niveau du contrat d’ensemble. 

Vous trouverez ci-dessous les champs de l’enregistrement de client de la ligne de contrat d’une ligne de contrat basée sur un projet à prendre en considération lorsque vous travaillez avec :

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| Compte | Grille modifiable sous l’onglet **Clients de la ligne de contrat** et formulaires principaux et de création rapide pour un client de ligne de contrat | Tous les comptes actifs. Ce champ est verrouillé après la création de l’enregistrement. Pour mettre à jour le champ, supprimez l’enregistrement et créez un nouvel enregistrement. Si des chiffres réels ont été enregistrés, vous ne pouvez pas supprimer cet enregistrement. Cependant, vous pouvez marquer le pourcentage de fractionnement de la facturation à 0 pour ce compte. Lorsque l’enregistrement est marqué à 0, tous les coûts et revenus réels futurs attribués ou fractionnés pour ce client sont affectés. | Lorsque vous sélectionnez un compte dans la liste principale des comptes pour les ajouter et les enregistrer, le client de ligne de contrat est également ajouté comme client du contrat. Les clients de ligne de contrat sont utilisés lors de la génération des factures. |
| Pourcentage de facturation fractionnée | Grille modifiable sous l’onglet **Clients de la ligne de contrat** et formulaires principaux et de création rapide pour un client de ligne de contrat | Ce champ comprend le pourcentage de chaque transaction commerciale non facturée qui sera attribuée à ce client de ligne de contrat. | Les clients de ligne de contrat et les pourcentages de fractionnement de la facturation sont utilisés lorsque les chiffres réels sont créés après approbation et lorsque la facture est générée. |
| Limite à ne pas dépasser | Grille modifiable sous l’onglet **Clients de la ligne de contrat** et formulaires principaux et de création rapide pour un client de ligne de contrat | Indique s’il existe une limite négociée ou un plafond du montant global qui sera facturé à ce client pour la ligne de contrat. | La limite à ne pas dépasser pour le client de la ligne de contrat est utilisée lorsque les chiffres réels sont créés et que les factures sont générées. |
| Société propriétaire | Grille modifiable sous l’onglet **Clients de la ligne de devis** et formulaires principaux et de création rapide pour un client de ligne de devis | L’entité juridique pour laquelle ce client est configuré. Ce champ est en lecture seule et est défini sur la société propriétaire du devis. La liste des clients à ajouter dans le champ **Compte** est déjà filtrée à partir de cette société propriétaire. | Le concept d’une société propriétaire équivaut au concept d’entité juridique. Tous les coûts et revenus générés par ce projet sont comptabilisés dans la Comptabilité de la société propriétaire. |
| Est arrondi | Grille modifiable sous l’onglet **Clients de la ligne de contrat** et formulaires principaux et de création rapide pour un client de ligne de contrat | Ce champ indique si ce client est un client d’arrondi par défaut pour cette ligne de contrat basée sur un projet. | Lorsque vous générez un chiffre réel en appliquant le pourcentage de fractionnement de la facturation, il peut y avoir des différences d’arrondi. Ce client se voit attribuer les différences d’arrondi dans ce cas. |

## <a name="edit-billing-split-percentages"></a>Modifier des pourcentages de facturation fractionnée

Les pourcentages de fractionnement de facturation peuvent être modifiés dans la grille. Si le total des pourcentages de fractionnement de la facturation n’est pas égal à 100 %, une erreur se produit. Après avoir modifié les pourcentages de fractionnement de la facturation, actualisez la page pour supprimer l’erreur.

Vous pouvez également essayer de sélectionner **Répartition homogène** dans la sous-grille du client de la ligne de contrat. Cette action répartit les fractionnements de la facturation de façon homogène entre tous les clients de la ligne de contrat. S’il existe une valeur d’arrondi, elle sera ajoutée au client d’arrondi. Un client de ligne de contrat est toujours identifié comme client d’**Arrondi** avec l’indicateur d’**Arrondi** défini sur **Oui**.
