---
title: Gestion de la sous-traitance dans Project Operations
description: Cette rubrique présente le processus de gestion de la sous-traitance de bout en bout dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6ffceb0886fdc841ea01a099243cf4eeb43e5374a18414576f3639a3e50857fd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994228"
---
# <a name="subcontract-management-in-project-operations"></a>Gestion de la sous-traitance dans Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

La sous-traitance dans Microsoft Dynamics 365 Project Operations prend en charge le flux des processus d′entreprise suivants.

![Flux de processus de sous-traitance](../media/SubcontractingProcessFlow.png)

Voici une description étape par étape du processus de sous-traitance.

1. Le chef de projet crée un contrat de sous-traitance avec un fournisseur. Par défaut, les tarifs joints à l′enregistrement fournisseur sont utilisés pour le contrat de sous-traitance. Le compte fournisseur a un type de relation **Vendeur** ou **Fournisseur**.
2. Le chef de projet peut ventiler tous les achats sous forme d′éléments de ligne dans le contrat de sous-traitance. Les lignes du contrat de sous-traitance peuvent concerner le temps, les dépenses ou les produits. La classe de transaction sélectionnée sur chaque ligne du contrat de sous-traitance détermine l′objet de la ligne.
3. Le gestionnaire de compte fournisseur et le chef de projet peuvent itérer sur le contrat de sous-traitance. La tarification peut être ajustée au niveau des tarifs d′achat joints au contrat de sous-traitance.
4. À ce stade ou plus tard dans le processus, si la ligne du contrat de sous-traitance concerne le temps, le gestionnaire de compte fournisseur associe des contacts à chaque ligne du contrat de sous-traitance. Cette association fournit des informations au chef de projet qui travaille sur le contrat de sous-traitance. Si un contact est associé à une ligne d′un contrat de sous-traitance, le système crée automatiquement une ressource réservable à partir du contact, si une ressource réservable n′existe pas déjà.
5. Le mode de facturation sur chaque ligne du contrat de sous-traitance peut être **Prix fixe** ou **Temps et matériel**. Pour les lignes de contrat de sous-traitance à prix fixe, vous pouvez configurer un échéancier de facturation basé sur des jalons.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
