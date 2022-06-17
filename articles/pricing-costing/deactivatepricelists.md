---
title: Désactiver les tarifs
description: Cet article explique comment désactiver ou supprimer des tarifs inutilisés ou anciens.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 56bd498d2cb892bdf0c7514d0918e3873098b8d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924381"
---
# <a name="deactivate-price-lists"></a>Désactiver les tarifs 

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Pour supprimer des tarifs anciens ou inutilisés de Dynamics 365 Project Operations, vous devez effectuer deux étapes. 

1. Supprimez ou effacez le tarif de pages spécifiques.
2. Désactivez ou supprimez le tarif des tarifs actifs sur la page **Tarifs**.

>[!IMPORTANT]
> Vous devez effectuer les deux étapes pour supprimer complètement un tarif. Il n’est pas suffisant d’effectuer seulement l’étape 2, qui consiste à supprimer ou désactiver directement le tarif de la vue Tarifs actifs. Vous devez également supprimer l’association de ce tarif de tous les endroits mentionnés à l’étape 1.

## <a name="delete-the-price-list-from-specific-pages"></a>Supprimer le tarif de pages spécifiques
1. Pour supprimer un tarif de Project Operations, accédez aux pages suivantes :  

      - Page **Paramètres du projet** > Onglet **Tarifs**
      - Page **Unité d’organisation** > Grille **Tarifs**
      - Page **Compte** > Grille **Tarifs du projet**
      - Page **Devis de projet** > Grille **Tarifs du projet** : s’applique à tous les devis de projet actifs.
      - Page **Contrats de projets** > Grille **Tarifs du projet** : s’applique à tous les contrats de projets actifs.

 2. Pour chaque page, vous devez sélectionner le tarif que vous souhaitez supprimer, puis sélectionner **Supprimer**. 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a>Supprimer ou désactiver le tarif de la page Tarifs
 
1. Pour supprimer un tarif des tarifs actifs, accédez à **Ventes** > **Clients** > **Tarifs**. 
2. Sélectionnez le tarif que vous souhaitez supprimer, puis sélectionnez **Supprimer**. Si le tarif est référencé sur des transactions existantes, vous ne pourrez pas le supprimer. Dans ce cas, vous pouvez désactiver le tarif pour qu’il n’apparaisse dans aucune vue. 
3. Pour désactiver le tarif, sélectionnez-le à nouveau, puis sélectionnez **Désactiver**.   
