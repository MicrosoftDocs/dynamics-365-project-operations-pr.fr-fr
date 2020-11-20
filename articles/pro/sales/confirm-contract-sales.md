---
title: Confirmer un contrat de projet
description: Cette rubrique fournit des informations sur le mode de confirmation d’un contrat dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128280"
---
# <a name="confirm-a-project-contract"></a>Confirmer un contrat de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Un contrat de projet dans Dynamics 365 Project Operations peut être actif avec la raison **Confirmé** ou fermé avec la raison **Perdu**. Lorsque vous confirmez un contrat de projet, le statut est mis à jour en passant du statut de **Brouillon** au statut **Actif** et avec la raison de statut **Confirmé**. Un contrat actif ou fermé ne peut pas être modifié ni rouvert. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Impact financier de la confirmation d’un contrat de projet

Une fois qu’un contrat de projet est confirmé, l’application recalcule les coûts en inversant les anciens chiffres réels de coûts et en créant les chiffres réels de coûts. Les nouveaux coûts réels sont ensuite traités en fonction de la méthode de facturation de la ligne de contrat de projet associée. Si les coûts réels font référence à une ligne de contrat Temps et matériel, l’application recrée automatiquement les chiffres réels des ventes non facturées correspondants. Si les coûts réels font référence à une ligne de contrat à prix fixe, l’application arrête de retraiter les coûts réels.

Les limites à ne pas dépasser, la configuration de la chargeabilité, la tarification et le calcul des coûts réels sont évalués puis mis à jour dans le cadre du processus de confirmation.

## <a name="close-a-project-contract-as-lost"></a>Fermer un contrat de projet considéré Perdu

Lorsque vous fermez un contrat de projet considéré perdu, le statut du contrat est mis à jour avec les statut **Fermé** et la raison du statut est **Perdu**. Le contrat de projet passe en lecture seule. Une boîte de dialogue de confirmation est fournie avant la fin des modifications, car vous ne pouvez pas rouvrir un contrat de projet fermé.

Si le contrat de projet qui est fermé parce que considéré perdu fait référence à un projet sur ses lignes, ce projet est également marqué comme fermé. Toutes les réservations de ressources à partir de ce jour sont annulées. Les ventes réelles non facturées sur le contrat de projet qui ne figurent pas déjà sur une facture seront annulées.

> [!NOTE]
> Dans Dynamics 365 Project Operations, la clôture d’un contrat de projet comme perdu n’aura pas d’impact sur ce statut de l’opportunité associée. L’opportunité restera ouverte et doit être fermée manuellement.
