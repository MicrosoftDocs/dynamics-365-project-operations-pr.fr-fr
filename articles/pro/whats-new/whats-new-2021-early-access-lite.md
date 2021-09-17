---
title: Nouveautés de l’accès anticipé à la 2e vague de lancement 2021 de Project Operations - Déploiement simplifié de Project Operations
description: Cette rubrique fournit des informations sur les fonctionnalités disponibles dans la version en accès anticipé à la 2e vague de lancement 2021 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 08/10/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a201e3e4333b8892eea72387222d64e18b74d71b
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323908"
---
# <a name="whats-new-2021-wave-2-early-access---project-operations-lite-deployment"></a>Nouveautés de l’accès anticipé à la 2e vague de lancement 2021 de Project Operations - Déploiement simplifié de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique s’applique aux composants et versions suivants de Dynamics 365 Project Operations :

  - Version 4.23.0.4 de Project Operations dans l’environnement Dataverse

La version n’est appliquée que lorsqu’un environnement est [activé en accès anticipé](/power-platform/admin/opt-in-early-access-updates#how-to-enable-early-access-updates).

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

[Gestion de la sous-traitance](../subcontracting/subcontracting_EA_scope.md) - Cette fonctionnalité offre une meilleure visibilité et un meilleur contrôle sur tous les aspects du travail sur un projet. La gestion de la sous-traitance en version préliminaire comprend les fonctionnalités suivantes :

  - Un chef de projet peut créer un contrat de sous-traitance avec un fournisseur. Par défaut, les tarifs joints à l′enregistrement fournisseur sont utilisés pour le contrat de sous-traitance. Le compte fournisseur a un type de relation **Vendeur** ou **Fournisseur**.
  - Un chef de projet peut ventiler tous les achats sous forme d’éléments de ligne dans le contrat de sous-traitance. Les lignes du contrat de sous-traitance peuvent concerner le temps, les dépenses ou les produits. La classe de transaction de la ligne du contrat de sous-traitance détermine l’objet de la ligne.
  - Le gestionnaire de compte fournisseur et le chef de projet peuvent itérer sur le contrat de sous-traitance. La tarification peut être ajustée au niveau des tarifs d′achat joints au contrat de sous-traitance.
  - Durant le processus, si la ligne du contrat de sous-traitance concerne le temps, le gestionnaire de compte fournisseur peut associer des contacts fournisseur à chaque ligne du contrat de sous-traitance. Cette association fournit des informations au chef de projet qui travaille sur le contrat de sous-traitance. Si un fournisseur est associé à une ligne d’un contrat de sous-traitance, le système crée automatiquement une ressource réservable à partir du contact, si une ressource réservable n’existe pas déjà.
  - Le mode de facturation sur chaque ligne du contrat de sous-traitance peut être Prix fixe ou Temps et matériel. Pour les lignes de contrat de sous-traitance à prix fixe, il est possible de configurer un échéancier de facturation basé sur des jalons.
