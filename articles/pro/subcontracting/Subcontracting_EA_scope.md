---
title: Version en accès anticipé à la sous-traitance en octobre 2021
description: Cette rubrique donne un aperçu des capacités de sous-traitance de Project Operations qui font partie de la version en accès anticipé d’octobre 2021.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 21ec8355487b5e69fc5b68b11dca029e6dc04f3c
ms.sourcegitcommit: c7f891adb5c81654c01d00c6b39beed403058eb1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/14/2021
ms.locfileid: "7383692"
---
# <a name="subcontracting-in-october-2021-early-access-release"></a>Version en accès anticipé à la sous-traitance en octobre 2021

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique donne un aperçu des capacités de sous-traitance de Dynamics 365 Project Operations qui font partie de la version en accès anticipé d’octobre 2021. Cet ensemble de fonctionnalités n’est pas prêt pour les environnements de production ou en direct. Ces fonctionnalités resteront donc dans la version en accès anticipé jusqu’à ce que l’ensemble de fonctionnalités complet soit publié. Nous vous recommandons vivement de ne pas utiliser l’ensemble de fonctionnalités de sous-traitance pour les scénarios de production en direct tant que la bannière Version préliminaire n’est pas supprimée. 

La liste suivante donne un aperçu de ce qui est actuellement disponible dans la version en accès anticipé d’octobre 2021 :

1. Le chef de projet crée un contrat de sous-traitance avec un fournisseur. Par défaut, les tarifs joints à l′enregistrement fournisseur sont utilisés pour le contrat de sous-traitance. Le compte fournisseur a un type de relation **Vendeur** ou **Fournisseur**.

2. Le chef de projet peut ventiler tous les achats sous forme d′éléments de ligne dans le contrat de sous-traitance. Les lignes du contrat de sous-traitance peuvent concerner le temps, les dépenses ou les produits. La classe de transaction de la ligne du contrat de sous-traitance détermine l’objet de la ligne.

3. Le gestionnaire de compte fournisseur et le chef de projet peuvent itérer sur le contrat de sous-traitance. La tarification peut être ajustée au niveau des tarifs d′achat joints au contrat de sous-traitance.

4. À ce stade ou plus tard dans le processus, si la ligne du contrat de sous-traitance concerne le temps, le gestionnaire de compte fournisseur associe des contacts fournisseur à chaque ligne du contrat de sous-traitance. Cette association fournit des informations au chef de projet qui travaille sur le contrat de sous-traitance. Si un fournisseur est associé à une ligne d’un contrat de sous-traitance, le système crée automatiquement une ressource réservable à partir du contact, si une ressource réservable n’existe pas déjà.

5. Le mode de facturation sur chaque ligne du contrat de sous-traitance peut être **Prix fixe** ou **Temps et matériel**. Pour les lignes de contrat de sous-traitance à prix fixe, il est possible de configurer un échéancier de facturation basé sur des jalons.

Les étapes restantes du flux des processus d’entreprise pour la sous-traitance qui sont décrites dans la présentation ne sont actuellement pas disponibles. Cette rubrique sera mise à jour au fur et à mesure de l’ajout de nouvelles fonctionnalités. 

L’illustration suivante représente la version en accès anticipé de la sous-traitance par opposition au processus d’entreprise complet de bout en bout.

![Flux de processus de sous-traitance](../media/SubcontractingEAFlow.png)  


## <a name="quantity-based-and-work-based-subcontract-lines-early-access-release"></a>Version en accès anticipé des lignes du contrat de sous-traitance basées sur la quantité et des lignes du contrat de sous-traitance basées sur le travail
Dans la version en accès anticipé d’octobre 2021, seules les lignes de sous-traitance basées sur la quantité sont prises en charge. Cela signifie qu’une ligne de sous-traitance peut être utilisée pour acheter du temps, des dépenses ou des matériaux auprès d’un fournisseur, mais pas pour tout un ensemble de travaux. Cela signifie également que la quantité achetée (unités de temps, dépenses ou quantité de matériaux) sur une ligne de sous-traitance peut être utilisée sur n’importe quel projet du système.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
