---
title: Confirmer un contrat de projet
description: Cet article explique comment confirmer un contrat dans Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e92dc42c4ff6bdc40c479511c80d3e500df781a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929993"
---
# <a name="confirm-a-project-contract"></a>Confirmer un contrat de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Un contrat de projet dans Dynamics 365 Project Operations peut être actif avec la raison **Confirmé** ou fermé avec la raison **Perdu**. Lorsque vous confirmez un contrat de projet, le statut est mis à jour en passant du statut de **Brouillon** au statut **Actif** et avec la raison de statut **Confirmé**. Un contrat actif ou fermé ne peut pas être modifié ni rouvert. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impact financier de la confirmation d’un contrat de projet

Après la confirmation d’un contrat de projet, l’application recalcule les coûts en contrepassant les anciens chiffres réels des coûts et en créant des chiffres réels des coûts. Les nouveaux chiffres réels des coûts sont ensuite traités en fonction du mode de facturation de la ligne de contrat de projet associée. Si les coûts réels font référence à une ligne de contrat Temps et matériel, l’application recrée automatiquement les chiffres réels des ventes non facturées correspondants. Si les coûts réels font référence à une ligne de contrat à prix fixe, l’application arrête de retraiter les coûts réels.

Les limites à ne pas dépasser, la configuration de la chargeabilité, la tarification et le calcul des coûts réels sont évalués puis mis à jour dans le cadre du processus de confirmation.

## <a name="close-a-project-contract-as-lost"></a>Fermer un contrat de projet considéré Perdu

Lorsque vous fermez un contrat de projet considéré perdu, le statut du contrat est mis à jour avec les statut **Fermé** et la raison du statut est **Perdu**. Le contrat de projet passe en lecture seule. Une boîte de dialogue de confirmation est fournie avant la fin des modifications, car vous ne pouvez pas rouvrir un contrat de projet fermé.

Si le contrat de projet qui est fermé parce que considéré perdu fait référence à un projet sur ses lignes, ce projet est également marqué comme fermé. Toutes les réservations de ressources à partir de ce jour sont annulées. Les ventes réelles non facturées sur le contrat de projet qui ne figurent pas déjà sur une facture seront annulées.

> [!NOTE]
> Dans Dynamics 365 Project Operations, la fermeture d’un contrat de projet comme perdu n’affectera le statut de l’opportunité associée. L’opportunité restera ouverte et doit être fermée manuellement.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]