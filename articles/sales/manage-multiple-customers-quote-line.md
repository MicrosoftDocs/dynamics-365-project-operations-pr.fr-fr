---
title: Gérer plusieurs clients sur les lignes de devis selon les projets
description: Cette rubrique fournit des informations sur la manière de gérer plusieurs clients sur des lignes de devis basées sur des projets.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf3d10cc4a742f7247586d09f5b209cbfdbbd790bdf97e09da06d9db583e61a5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992023"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Gérer plusieurs clients sur les lignes de devis selon les projets

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les lignes de devis basées sur des projets prennent en charge des scénarios où chaque ligne de devis a une liste de clients qui paient pour cela. Cette liste de clients sur la ligne de devis basée sur le projet peut être la même que la liste de clients sur le devis. Vous pouvez également modifier la liste des clients pour qu’elle soit différente. Pour créer le contrat de projet potentiel lorsqu’un devis de projet est remporté, la liste des clients de la ligne de devis basée sur le projet est copiée dans la ligne de contrat basée sur le projet correspondante. Les clients du devis basé sur le projet sont copiés dans le contrat de projet.

Lorsque vous facturez l’éventuel contrat de projet, la liste de clients de la ligne de contrat de projet est prioritaire sur la liste du contrat de projet. La liste des clients du contrat de projet n’est utilisée que pour les valeurs par défaut sur les nouvelles lignes de contrat de projet.

Tous les clients du devis sur l’onglet **Clients** du devis de projet par défaut en tant que clients de la ligne de devis sur toutes les nouvelles lignes de devis selon le projet créées pour le devis de projet. Les lignes de devis existantes selon un projet n’héritent pas des enregistrements client de devis créés après elles.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Créer, mettre à jour ou supprimer un enregistrement client de ligne de devis

Vous pouvez créer, mettre à jour ou supprimer un client de ligne de devis sur l’onglet **Clients de la ligne de devis** sur la page **Ligne de devis basée sur le projet**. Lorsque vous ajoutez un nouveau client sur la ligne de devis basée sur le projet, le client est également ajouté au devis global en tant que client du devis, avec un pourcentage de répartition de facturation par défaut sur le devis global de 0 %%. Le pourcentage de facturation fractionnée sur le devis global est copié dans les nouvelles lignes de devis et dans l’éventuel contrat de projet. Cependant, lorsque vous facturez à partir du contrat, le pourcentage de facturation fractionnée au niveau de la ligne de devis est utilisé, et non le pourcentage de facturation fractionnée au niveau du contrat global. 

Le tableau suivant affiche les champs sur l’enregistrement de client de la ligne de devis d’une ligne de devis selon un projet.

| Champ | Emplacement | Description et conseils | Impact en aval |
| --- | --- | --- | --- |
| **Compte** | Grille modifiable sur l’onglet **Clients de ligne du devis**, le formulaire principal et le formulaire de création rapide pour un client de ligne de devis. | Répertorie tous les comptes actifs. Ce champ est verrouillé après la création de l’enregistrement. Si vous devez mettre à jour le champ, supprimez et recréez l’enregistrement. Si vous avez enregistré des chiffres réels, vous ne pouvez pas supprimer l’enregistrement. | Lorsque vous sélectionnez un compte dans la liste principale des comptes à ajouter, le client de la ligne de devis est également ajouté en tant que client de devis. Les clients de la ligne de devis sont également copiés vers les clients de la ligne du contrat de projet lorsqu’un devis est conclu. |
| **Pourcentage de facturation fractionnée** | Grille modifiable sur l’onglet **Clients de ligne du devis**, le formulaire principal et le formulaire de création rapide pour un client de ligne de devis. | Représente le pourcentage de chaque transaction de vente non facturée qui sera attribuée à ce client de ligne de devis. | Copié vers les clients de la ligne du contrat du projet. |
| **Limite à ne pas dépasser** | Grille modifiable sur l’onglet **Clients de ligne du devis**, le formulaire principal et le formulaire de création rapide pour un client de ligne de devis. | Indique s’il existe une limite ou un plafond négocié au montant global qui sera facturé à ce client pour cette ligne de devis. | Copié vers les clients de la ligne du contrat de projet lorsqu’un devis est remporté. |
| **Société propriétaire** | Grille modifiable sur l’onglet **Clients de ligne du devis**, le formulaire principal et le formulaire de création rapide pour un client de ligne de devis, | L’entité juridique dans laquelle ce client est installé dans le module **Gestion de projet et comptabilité**. Ce champ est en lecture seule et est défini sur la société propriétaire du devis lui-même. La liste des clients à ajouter dans le champ **Compte** est déjà filtré dans la liste de la société propriétaire dans le module **Gestion de projet et comptabilité** de Project Operations. | La société propriétaire équivaut au concept d’entité juridique. Tous les coûts et revenus générés par ce projet sont comptabilisés dans la comptabilité de la société propriétaire. |
| **Est arrondi** | Grille modifiable sur l’onglet **Clients de ligne du devis**, le formulaire principal et le formulaire de création rapide pour un client de ligne de devis. | Indique si ce client est un client arrondi par défaut pour cette ligne de devis basée sur un projet. | Copié vers les clients du contrat de projet lorsqu’un devis est remporté. |

## <a name="edit-billing-split-percentages"></a>Modifier des pourcentages de facturation fractionnée

Vous pouvez modifier les pourcentages de facturation fractionnée en ligne. Lorsque les pourcentages de facturation fractionnée ne totalisent pas 100 %%, une erreur se produit. Après avoir modifié les pourcentages de facturation fractionnée, actualisez la page de ligne de devis pour supprimer l’erreur.

Utilisez l’action de répartition homogène sur la sous-grille des clients de la ligne de devis pour attribuer des facturations fractionnées à tous les clients de la ligne de devis. S’il y a un facteur d’arrondi, il sera ajouté au client d’arrondi. L’un des clients de la ligne de devis est toujours marqué comme client d’arrondi, ce qui signifie que l’enregistrement de client de la ligne de devis a l’indicateur d’arrondi défini sur **Oui**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]