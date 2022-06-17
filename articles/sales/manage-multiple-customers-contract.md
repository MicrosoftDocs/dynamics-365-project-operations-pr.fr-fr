---
title: Gérer plusieurs clients sur des contrats de projets
description: Cet article fournit des informations sur la gestion de plusieurs clients sur un contrat de projet.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 78ee117c1068e7af4674cc3b21e1055fd05bb43a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928337"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Gérer plusieurs clients sur des contrats de projets

Cet article fournit des informations sur la gestion de plusieurs clients sur un contrat de projet. Vous pouvez utiliser un contrat de projet lorsqu’un accord contractuel pour plusieurs clients est nécessaire pour financer une transaction. Sur la page **Contrat de projet**, l’onglet **Récapitulatif** contient des informations sur le client principal d’une transaction. D’autres clients qui participent à l’offre peuvent être ajoutés sur l’onglet **Clients**.

Tous les clients du contrat figurant sur l’onglet **Clients** du contrat de projet sont créés par défaut en tant que clients de ligne de contrat sur toutes les lignes de contrat basées sur un projet créées pour le contrat de projet. Les lignes de contrat basées un projet existantes n’héritent pas des nouveaux enregistrements de clients de contrat qui sont créés ultérieurement.

Vous pouvez ajouter, mettre à jour ou supprimer un contrat et des clients de ligne de contrat à tout moment avant que le contrat ne soit remporté. Un client sur le contrat de projet doit être configuré en tant que client dans la société propriétaire ou l’entité juridique sur la page **Clients**. Les entités juridiques sont créées dans le module **Gestion et comptabilité des projets** de Dynamics 365 Project Operations et sont disponibles en tant que sociétés dans les modules **Ventes de projets** et **Livraison** de Project Operations.

## <a name="primary-customers"></a>Clients principaux

Le client potentiel dans l’onglet **Récapitulatif** du contrat de projet est le client principal du contrat. Vous ne pouvez pas mettre à jour le client principal à partir de la liste des clients du contrat. Si vous essayez de supprimer le client principal d’une liste des clients du contrat, une erreur se produit et indique qu’un enregistrement de client principal ne peut pas être supprimé. Au lieu de cela, vous devez modifier le client dans le champ **Client potentiel** de l’onglet **Récapitulatif** du contrat de projet. Lorsque vous mettez à jour ce champ, le nouveau client sélectionné est ajouté en tant que nouveau client du contrat, avec l’indicateur **Principal** défini sur **Oui**. Le client principal précédent est toujours un client sur le contrat, mais il n’est plus le client principal.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Créer, mettre à jour ou supprimer un enregistrement de client de contrat

Vous pouvez créer, mettre à jour ou supprimer un client de contrat depuis l’onglet **Clients de contrat** sur la page **Contrat**. Les champs suivants se trouvent dans l’enregistrement de client de contrat d’un contrat de projet.

| **Champ** | **Emplacement** | **Description** | 
| --- | --- | --- | 
| Compte | Grille modifiable sous l’onglet **Clients du contrat** et formulaires Principal et Création rapide pour le client d’un contrat. | Répertorie tous les comptes actifs. Ce champ est verrouillé après la création de l’enregistrement. Pour mettre à jour l’enregistrement, vous devez le supprimer, puis le récréer. Si vous avez enregistré des chiffres réels ou si l’enregistrement de client du contrat est un client principal, vous ne pouvez pas supprimer l’enregistrement. Lorsqu’une ligne de contrat est créée, les clients de contrat sont copiés comme clients de ligne de contrat. |
| Pourcentage de facturation fractionnée | Grille modifiable sous l’onglet **Clients du contrat** et formulaires Principal et Création rapide pour le client d’un contrat. | Comprend le pourcentage de chaque transaction commerciale non facturée attribuée au client de contrat. Lorsque de nouvelles lignes de contrat de projet sont créées, le pourcentage de facturation fractionnée est copié dans les nouvelles lignes de contrat créées et dans les clients de la ligne de contrat de projet. |
| Nom du contact de facturation | Grille modifiable sous l’onglet **Clients du contrat** et formulaires Principal et Création rapide pour le client d’un contrat. | Ce champ de texte doit être utilisé pour identifier la personne à contacter pour la facturation du client. La valeur par défaut provient de l’enregistrement de compte associé. Le nom de contact est copié dans **Nom du contrat de facturation** sur la facture générée pour le client. |
| Nom de facturation | Grille modifiable sous l’onglet **Clients du contrat** et formulaires Principal et Création rapide pour le client d’un contrat. | Utilisez ce champ pour identifier la personne à contacter pour la facturation du client. La valeur par défaut provient de l’enregistrement de compte associé. Le nom est copié dans le champ **Nom du contrat de facturation** sur la facture générée pour le client. |
| Modalités de paiement | Grille modifiable sous l’onglet **Clients du contrat** et formulaires Principal et Création rapide pour le client d’un contrat. | La valeur par défaut provient de l’enregistrement de compte associé. Les termes sont copiés dans **Nom du contrat de facturation** sur la facture générée pour le client. |
| Société propriétaire | Grille modifiable sous l’onglet **Clients du contrat de projet** et formulaires Principal et Création rapide pour le client d’un contrat de projet. | Entité juridique dans laquelle le client est configuré dans le module **Gestion de projet et comptabilité**. Ce champ est en lecture seule et est défini sur la société propriétaire du contrat de projet.</br>La liste des clients à ajouter dans le champ **Compte** est déjà filtré dans la liste de la société propriétaire dans le module **Gestion de projet et comptabilité** de Project Operations. La société propriétaire est égale à l’entité juridique du module **Gestion de projet et comptabilité** de Project Operations. Tous les coûts et revenus générés par le projet sont comptabilisés dans la Comptabilité de la société propriétaire. |
| Est arrondi | Grille modifiable sous l’onglet **Clients du contrat** et formulaires Principal et Création rapide pour le client d’un contrat. | Indique si le client est un client arrondi par défaut pour l’opération. Il ne peut y avoir qu’un seul client d’arrondi sur un contrat de projet. Lorsque le fractionnement des coûts et des ventes non facturées entraînent une différence d’arrondi, cette différence est appliquée au chiffre réel correspondant au client. |
| Limite à ne pas dépasser | Grille modifiable sous l’onglet **Clients du contrat** et formulaires Principal et Création rapide pour le client d’un contrat. | Indique s’il existe une limite négociée ou un plafond du montant global qui sera facturé au client pour l’engagement. La Limite à ne pas dépasser définie au niveau du client du contrat est évaluée selon les Chiffres de vente réels non facturés qui font référence au client de contrat. |

## <a name="edit-billing-split-percentages"></a>Modifier des pourcentages de facturation fractionnée

Vous pouvez modifier les pourcentages de fractionnement de facturation dans la grille. Si le total des pourcentages de fractionnement de la facturation n’est pas égal à 100 %%, une erreur se produit. Après avoir modifié les pourcentages de fractionnement d’une facturation, actualisez la page **Contrat de projet** pour supprimer l’erreur.

Vous pouvez également sélectionner **Répartition homogène** dans la sous-grille des clients du contrat de projet. Les pourcentages de facturation sont répartis de manière homogène sur tous les clients du contrat du projet. S’il existe une valeur d’arrondi, elle sera ajoutée au client d’arrondi. L’un des clients du contrat a toujours l’indicateur **Arrondi** défini sur **Oui**. Ce client est le client arrondi. En règle générale, le client arrondi est également le client principal du contrat, mais ce n’est pas obligatoire.


[!INCLUDE[footer-include](../includes/footer-banner.md)]