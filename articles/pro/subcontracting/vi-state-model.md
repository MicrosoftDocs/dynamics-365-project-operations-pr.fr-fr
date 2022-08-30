---
title: Transitions d’état sur une facture fournisseur
description: Cet article explique les transitions d’état sur une facture fournisseur dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261013"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Transitions d’état sur une facture fournisseur

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cet article explique les transitions d’état sur une facture fournisseur dans Microsoft Dynamics 365 Project Operations. Les états suivants sont utilisés : **Brouillon**, **En cours de révision**, **Confirmé**, **En attente** et **Annulé**.

Les illustrations suivantes présentent les transitions d’état.

![Modèle de transition de l’état du contrat de sous-traitance.](../media/VI_State_Model.jpg)

Le tableau suivant explique une description de ce que chaque état représente dans le cycle de vie d’une facture fournisseur dans Project Operations.

| State | Description | Transitions autorisées |
| --- | --- | --- |
| Brouillon | Cet état est l’état initial d’une facture fournisseur. Les lignes et les tarifs sont susceptibles d’être modifiés. Une facture fournisseur définie à cet état peut être modifiée et supprimée. | En cours de traitement |
| En cours de révision | Cet état représente l’état de traitement d’une facture fournisseur. Au moins une ligne de facture fournisseur a un statut de vérification définie sur **En cours**. | Confirmé, En attente |
| Confirmé | Cet état représente l’étape d’une facture fournisseur où l’application a créé des chiffres réels du coût pour chaque ligne de facture fournisseur. Tous les chiffres réels du coût liés qui ont été rapprochés des lignes de facture fournisseur ont été annulés et remplacés par les chiffres réels du coût de ces lignes de facture fournisseur. Impossible de modifier ou de supprimer une facture fournisseur dont l’état est celui-ci. Vous pouvez utiliser le bouton **Annuler** pour annuler une facture fournisseur confirmée. L’action Annuler annule l’impact de l’action Confirmer. | Annulée |
| En attente | <p>Cet état représente une étape d’une facture fournisseur où la facture fournisseur ne peut pas être déplacée en raison d’un problème avec la facture ou le statut du fournisseur. Impossible de confirmer, de modifier ou de supprimer une facture fournisseur dont l’état est celui-ci.</p><p>Vous pouvez utiliser l’action Rouvrir pour déplacer la facture fournisseur vers l’état **Brouillon** ou **En cours de révision**. Si au moins une ligne de la facture fournisseur a un statut de vérification défini sur **En cours** ou **Terminé**, la facture fournisseur sera rouverte dans l’état **En cours de révision**. Si toutes les lignes de la facture fournisseur ont un statut de vérification défini sur **Pas commencé**, la facture fournisseur sera rouverte à l’état **Brouillon**.</p> | Brouillon, En cours de révision |
| Annulée | Cela représente l’étape d’un contrat de sous-traitance lorsque la livraison effective des matériaux et/ou des travaux par des ressources sous-traitées n’est plus nécessaire. Un contrat de sous-traitance dans cet état ne peut pas être utilisé pour estimer et doter les besoins du projet en ressources et en matériels, ni être référencé sur le temps, les dépenses et l’utilisation des matériels sur un projet. Un contrat de sous-traitance dans cet état ne peut être ni modifié, ni supprimé. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
