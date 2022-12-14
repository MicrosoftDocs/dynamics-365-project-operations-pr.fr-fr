---
title: Gérer plusieurs clients sur des lignes de contrats de projets
description: Cet article fournit des informations sur la gestion de plusieurs clients sur les lignes de contrat basées sur un projet.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ec8457fd32a5c215bbc2056b02b2ab3527c4ab1f
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825937"
---
# <a name="manage-multiple-customers-on-project-contract-lines"></a>Gérer plusieurs clients sur des lignes de contrats de projets

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Les lignes de contrat basées sur un projet peuvent inclure une liste de clients responsables du paiement. Cette liste de clients sur la ligne de contrat basée sur un projet peut être identique à la liste de clients du contrat, mais cela n’est pas obligatoire. Lorsqu’un devis de projet est remporté et qu’un contrat de projet est créé, la liste des clients de la ligne de devis est copiée dans la ligne de contrat correspondante. Les clients figurant sur le devis sont copiés dans le contrat.

Lorsque le contrat de projet est facturé, la liste de clients sur la ligne de contrat basée sur un projet est prioritaire par rapport à la liste de clients figurant sur le contrat. La liste des clients du contrat de projet est uniquement utilisée pour la création de lignes de contrat par défaut.

Tous les clients du contrat figurant sur l’onglet **Clients** du contrat de projet sont créés par défaut en tant que clients de ligne de contrat sur toutes les lignes de contrat créées pour le contrat de projet. Une fois créées, les lignes de contrat existantes n’hériteront pas des nouveaux enregistrements de clients de contrat.

## <a name="create-update-or-delete-a-contract-line-customer-record"></a>Créer, mettre à jour ou supprimer un enregistrement de client de ligne de contrat

Vous pouvez créer, mettre à jour ou supprimer un client de ligne de contrat sous l’onglet Clients de la ligne de contrat sur la page Ligne de contrat basée sur un projet. Lorsqu’un nouveau client est ajouté à la ligne de contrat basée sur un projet, il est également ajouté au contrat d’ensemble en tant que client de contrat avec un pourcentage de fractionnement de facturation par défaut de 0 %%. Le pourcentage de fractionnement de la facturation sur le contrat d’ensemble est copié dans les nouvelles lignes de contrat et dans le contrat de projet éventuel. Cependant, lors de la facturation à partir du contrat, c’est le pourcentage de fractionnement de la facturation au niveau de la ligne de contrat qui est utilisé et non celui au niveau du contrat d’ensemble.

Vous trouverez ci-dessous les champs figurant sur la ligne **Contrat** de l’enregistrement de client d’une ligne de contrat basée sur un projet à prendre en considération lorsque vous travaillez avec :

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| **Compte** | Grille modifiable sous l’onglet **Clients du contrat** et formulaires **Principal** et **Création rapide** pour le client d’un contrat. | Tous les comptes actifs. Ce champ est verrouillé après la création de l’enregistrement. Pour mettre à jour le champ, supprimez l’enregistrement et créez un nouvel enregistrement. Si des chiffres réels ont été enregistrés, vous ne pouvez pas supprimer cet enregistrement. Cependant, vous pouvez marquer le pourcentage de fractionnement de la facturation à 0 pour ce compte. Lorsque l’enregistrement est marqué à 0, tous les coûts et revenus réels futurs attribués ou fractionnés pour ce client sont affectés. | Lorsque vous sélectionnez un compte dans la liste principale des comptes pour les ajouter et les enregistrer, le client de ligne de contrat est également ajouté comme client du contrat. Les clients de ligne de contrat sont utilisés lors de la génération des factures. |
| **Pourcentage de facturation fractionnée** | Grille modifiable sous l’onglet **Clients du contrat** et formulaires **Principal** et **Création rapide** pour le client d’un contrat. | Ce champ comprend le pourcentage de chaque transaction commerciale non facturée qui sera attribuée à ce client de ligne de contrat. | Les clients de ligne de contrat et les pourcentages de fractionnement de la facturation sont utilisés lorsque les chiffres réels sont créés après approbation et lorsque la facture est générée. |
| **Limite à ne pas dépasser** | Grille modifiable sous l’onglet **Clients du contrat** et formulaires **Principal** et **Création rapide** pour le client d’un contrat. | Indique s’il existe une limite négociée ou un plafond du montant global qui sera facturé à ce client pour la ligne de contrat. | La limite à ne pas dépasser pour le client de la ligne de contrat est utilisée lorsque les chiffres réels sont créés et que les factures sont générées. |
| **Est arrondi** | Grille modifiable sous l’onglet **Clients du contrat** et formulaires **Principal** et **Création rapide** pour un client de ligne de contrat. | Ce champ indique si ce client est un client d’arrondi par défaut pour cette ligne de contrat basée sur un projet. | Lorsque vous générez un chiffre réel en appliquant le pourcentage de fractionnement de la facturation, il peut y avoir des différences d’arrondi. Ce client se voit attribuer les différences d’arrondi dans ce cas. |

## <a name="edit-billing-split-percentages"></a>Modifier des pourcentages de facturation fractionnée

Les pourcentages de fractionnement de facturation peuvent être modifiés dans la grille. Si le total des pourcentages de fractionnement de la facturation n’est pas égal à 100 %%, une erreur se produit. Après avoir modifié les pourcentages de fractionnement de la facturation, actualisez la page pour supprimer l’erreur.

Vous pouvez également sélectionner **Répartition homogène** dans la sous-grille du client de la ligne de contrat. Cette action répartit les fractionnements de la facturation de façon homogène entre tous les clients de la ligne de contrat. S’il existe une valeur d’arrondi, elle sera ajoutée au client d’arrondi. Un client de ligne de contrat est toujours identifié comme client d’**Arrondi** avec l’indicateur d’**Arrondi** défini sur **Oui**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
