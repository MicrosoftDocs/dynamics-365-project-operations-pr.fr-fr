---
title: Transitions d’état dans un contrat de sous-traitance
description: Cette rubrique explique les transitions d’état sur un contrat de sous-traitance dans Microsoft Dynamics 365 Project Operations à mesure que le contrat de sous-traitance est créé, exécuté et clôturé.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903409"
---
# <a name="state-transitions-on-a-subcontract"></a>Transitions d’état dans un contrat de sous-traitance 

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique explique les transitions d’état sur un sous-contrat dans Microsoft Dynamics 365 Project Operations. Chaque état est représenté comme brouillon, confirmé, fermé ou annulé. L’image suivante représente les transitions d’état.

![Modèle d’état d’un contrat de sous-traitance](../media/SubconStates.png)  

Le tableau suivant fournit une description de ce que chaque état représente dans le cycle de vie d’un contrat de sous-traitance dans Project Operations.

| State | Description | Transitions autorisées |
| --- | --- | --- |
| Brouillon | Cela représente l’état initial d’un contrat de sous-traitance. Des négociations avec le fournisseur sont en cours. Les lignes et les tarifs sont susceptibles d’être modifiés. Un contrat de sous-traitance dans cet état peut être utilisé pour estimer et pourvoir les besoins du projet en ressources et en matériel. Il peut également être référencé sur le temps, les dépenses et l’utilisation des matériels pour un projet. Un contrat de sous-traitance dans cet état peut être modifié et supprimé. | Confirmé |
| Confirmé | Cela représente l’étape d’un contrat de sous-traitance après que les négociations avec le fournisseur sur les tarifs et les articles achetés sont terminées. Cependant, la livraison effective des matériels et/ou des travaux par des ressources sous-traitées est toujours en cours. Un contrat de sous-traitance dans cet état peut être utilisé pour estimer et pourvoir les besoins du projet en ressources et en matériel. Il peut également être référencé sur le temps, les dépenses et l’utilisation des matériels pour un projet. Un contrat de sous-traitance dans cet état ne peut être ni modifié, ni supprimé. Le bouton **Annuler** vous permet d’annuler un contrat de sous-traitance confirmé. Le bouton **Rouvrir** permet de rouvrir le contrat de sous-traitance pour le remettre au statut de **Brouillon**. Utilisez le bouton **Fermer** pour fermer un contrat de sous-traitance confirmé. | Fermée <br> Annulée <br> Brouillon |
| Fermée | Cela représente l’étape d’un contrat de sous-traitance lorsque la livraison effective des matériaux et/ou des travaux par des ressources sous-traitées est terminée. Un contrat de sous-traitance dans cet état ne peut plus être utilisé pour estimer et pourvoir les besoins du projet en ressources et en matériel. En outre, il ne peut plus être référencé sur le temps, les dépenses et l’utilisation des matériels pour un projet. Un contrat de sous-traitance dans cet état ne peut être ni modifié, ni supprimé. | None |
| Annulée | Cela représente l’étape d’un contrat de sous-traitance lorsque la livraison effective des matériaux et/ou des travaux par des ressources sous-traitées n’est plus nécessaire. Un contrat de sous-traitance dans cet état ne peut pas être utilisé pour estimer et doter les besoins du projet en ressources et en matériels, ni être référencé sur le temps, les dépenses et l’utilisation des matériels sur un projet. Un contrat de sous-traitance dans cet état ne peut être ni modifié, ni supprimé. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
