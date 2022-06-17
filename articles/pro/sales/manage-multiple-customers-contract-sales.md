---
title: Gérer plusieurs clients sur des contrats de projets – Simplifié
description: Cet article fournit des informations sur la gestion de plusieurs clients sur les contrats de projets.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 17cd464bad81a01f5f334524a542104d6f25717b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917202"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Gérer plusieurs clients sur des contrats de projets – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Les contrats de projet dans Dynamics 365 Project Operations prennent en charge les scénarios dans lesquels un accord contractuel implique plusieurs clients qui financent une transaction. L’onglet **Synthèse** de la page **Contrat du projet** comprend le champ **Client**. Ce champ identifie le client principal de la transaction. D’autres clients de la transaction peuvent être définis sous l’onglet **Clients** de la page **Contrat du projet**.

Tous les clients du contrat répertoriés sur le contrat de projet sont créés par défaut en tant que clients de ligne de contrat sur toutes les lignes de contrat basées sur un projet créées pour le contrat du projet. Une fois leur enregistrement créé, les lignes de contrat basées un projet existantes n’héritent pas des nouveaux clients de contrat.

Les lignes de contrat basées sur les produits sont automatiquement associées au client principal.

Les clients de contrat et les clients de ligne de contrat peuvent être ajoutés, mis à jour ou supprimés à tout moment avant que le contrat ne soit remporté.

## <a name="primary-customer"></a>Client principal

Le client figurant dans l’onglet **Synthèse** du contrat de projet comme client potentiel est le client principal du contrat. Si vous essayez de supprimer le client principal de la liste des clients du contrat, un message d’erreur indiquera qu’un enregistrement de client principal d’un contrat ne peut pas être supprimé.

Le client principal ne peut pas être mis à jour à partir de la liste des clients du contrat. En revanche, vous pouvez modifier le client potentiel sous l’onglet **Synthèse** du contrat. Lorsque ce champ est mis à jour sur la page **Synthèse du contrat**, le nouveau client est ajouté en tant que nouveau client du contrat, marqué de l’indicateur **Principal**. Le client principal précédent demeure client du contrat.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Créer, mettre à jour ou supprimer un enregistrement de client de contrat

Un client de contrat peut être créé, mis à jour ou supprimé depuis l’onglet **Clients** sur la page **Contrat du projet**. Les champs du tableau suivant traitent de l’enregistrement de client du contrat d’un contrat de projet et doivent être pris en considération lorsque vous travaillez avec le contrat.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| **Compte** | La grille est modifiable sous l’onglet **Clients du contrat** et les formulaires **Principal** et **Création rapide** pour le client d’un contrat. | Répertorie tous les comptes actifs. Ce champ est verrouillé après la création de l’enregistrement. Pour mettre à jour le compte, supprimez l’enregistrement et créez un nouvel enregistrement. Si vous avez enregistré des chiffres réels ou si l’enregistrement de client du contrat est un client principal, vous ne pouvez pas supprimer l’enregistrement. | Les clients de contrat sont copiés comme clients de ligne de contrat lorsqu’une ligne de contrat est créée. |
| **Pourcentage de facturation fractionnée** | La grille est modifiable sous l’onglet **Clients du contrat** et les formulaires **Principal** et **Création rapide** pour le client d’un contrat. | Comprend le pourcentage de chaque transaction commerciale non facturée qui est attribuée à ce client de contrat. | Copié dans de nouvelles lignes de contrat et permettant de projeter les clients de ligne de contrat sur de nouvelles lignes de contrat de projet. |
| **Nom du contact de facturation** | La grille est modifiable sous l’onglet **Clients du contrat** et les formulaires **Principal** et **Création rapide** pour le client d’un contrat. | Ce champ de texte doit être utilisé pour identifier la personne à contacter pour la facture de ce client. Ce champ est créé par défaut à partir de l’enregistrement de compte associé. | Copié dans le champ **Nom du contrat de facturation** sur la facture générée pour ce client. |
| **Nom de facturation** | La grille est modifiable sous l’onglet **Clients du contrat** et les formulaires **Principal** et **Création rapide** pour le client d’un contrat | Ce champ de texte doit être utilisé pour identifier la personne à contacter pour la facture de ce client. Ce champ est créé par défaut à partir de l’enregistrement de compte associé. | Copié dans le champ **Nom du contrat de facturation** sur la facture générée pour ce client. |
| **Conditions de paiement** | La grille est modifiable sous l’onglet **Clients du contrat** et les formulaires **Principal** et **Création rapide** pour le client d’un contrat. | Les valeurs sont créées par défaut à partir de l’enregistrement de compte associé. | Copié dans le champ **Nom du contrat de facturation** sur la facture générée pour ce client. |
| **Est arrondi** | La grille est modifiable sous l’onglet **Clients du contrat** et les formulaires **Principal** et **Création rapide** pour le client d’un contrat. | Indique si ce client est un client arrondi par défaut pour cette transaction. Il ne peut y avoir qu’un seul client d’arrondi sur un contrat de projet. | Lorsque le fractionnement des coûts et des ventes non facturées entraînent une différence d’arrondi, cette différence est appliquée au chiffre réel correspondant à ce client. |
| **Limite à ne pas dépasser** | La grille est modifiable sous l’onglet **Clients du contrat** et les formulaires **Principal** et **Création rapide** pour le client d’un contrat | Indique s’il existe une limite négociée ou un plafond du montant global qui sera facturé au client pour cet engagement. | La **Limite à ne pas dépasser** définie au niveau du client du contrat sera évaluée selon les **Chiffres de vente réels non facturés** qui font référence à ce client de contrat. |

## <a name="edit-billing-split-percentages"></a>Modifier des pourcentages de facturation fractionnée

Les pourcentages de fractionnement de la facturation peuvent être modifiés en utilisant la modification de la grille en ligne. Si le total des pourcentages de fractionnement de la facturation n’est pas égal à 100 %%, vous recevrez un message d’erreur. Après avoir modifié les pourcentages de fractionnement de la facturation, actualisez la page pour annuler l’erreur.

Vous pouvez également sélectionner **Répartition homogène** dans la sous-grille **Clients du contrat** pour répartir les fractionnements de la facturation de façon homogène entre tous les clients du contrat. S’il existe une valeur d’arrondi, elle sera ajoutée au client d’arrondi. Un des clients de contrat est toujours identifié comme client d’**arrondi**, ce qui signifie que l’enregistrement de ce client du contrat est marqué de l’indicateur d’arrondi défini sur **Oui**. En règle générale, il s’agit du client principal du contrat, mais cela peut également être modifié.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]