---
title: Configuration des tarifs de vente
description: Cette rubrique fournit des informations sur les tarifs de ventes associés pour la tarification de projet.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d2c797b72666123eb0a18d2d0c1df9fe3d207f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075795"
---
# <a name="sales-price-list-setup"></a>Configuration des tarifs de vente

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Pour les devis et les contrats du projet, les tarifs du projet ont un autre modèle de remplacement de prix qu'une liste de prix de produits. Dans une ligne de devis basée sur un catalogue de produits, vous pouvez remplacer le prix des rôles et des catégories directement sur la ligne de devis, car chaque ligne de devis pointe exactement vers un article du catalogue. Toutefois, sur une ligne de devis basée sur un projet, vous ne pouvez pas remplacer le tarif des rôles et des catégories directement sur la ligne de devis. Vous pouvez utiliser le tarif du projet pour prendre en charge les deux modèles de remplacement distincts.

> [!NOTE]
> Il est recommandé d'avoir des tarifs distincts pour vos ressources de projet et vos articles de catalogue, en raison des différences de comportement entre les deux lors du remplacement de la tarification.

Chacune des entités suivantes peut contenir un ou plusieurs tarifs de ventes associés pour la tarification de projet :

- Client (compte) 
- Opportunité 
- Devis 
- Contrat du projet

L'association de ces entités avec des tarifs est indiquée par les tarifs du projet. Vous pouvez associer un ou plusieurs tarifs avec les entités de vente Client, Opportunité, Devis et Contrat du projet.

Des tarifs par défaut de projet ne sont pas automatiquement entrés sur un enregistrement client. Cependant, vous pouvez manuellement joindre des tarifs de projet à l'enregistrement de client. Toutefois, vous devez manuellement joindre des tarifs de projet uniquement si vous avez un contrat de tarification personnalisé avec le client. 

Lorsque des tarifs de projet sont attachés à une entité de ventes, les informations suivantes sont validées :

- Le tarif a un contexte de **Ventes**. 
- La devise des tarifs correspond à la devise client. 

Sur un contrat de projet, l'ordre suivant de priorité est utilisé pour définir automatiquement les tarifs associés de projet :

1. Devis
2. Opportunité
3. Client 
4. Paramètres globaux 

Lorsque des tarifs de projet sont entrés par défaut, le système valide le fait que la devise corresponde à la devise client, et que les tarifs par défaut entrés ont un contexte de **Ventes**.

Vous pouvez associer plusieurs tarifs de projet aux entités Client, Opportunité, Devis et Contrat du projet. Cette fonctionnalité prend en charge les prix par défaut spécifiques à une date dans un contrat de projet à long terme, où vous pouvez nécessiter plusieurs tarifs pour tenir compte des mises à jour des prix qui se produisent en raison de l'inflation. Toutefois, si les tarifs que vous associez à l'entité Client, Opportunité, Devis ou Contrat du projet ont une validité de date se chevauchant, les prix par défaut peuvent être incorrects. Par conséquent, vous devez vous assurer que les tarifs de projet qui ont une validité de dates se chevauchant ne sont pas associés à ces entités.
