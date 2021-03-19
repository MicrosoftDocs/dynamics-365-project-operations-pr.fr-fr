---
title: Vue d’ensemble de l’utilisation des ressources
description: Cette rubrique fournit des informations sur l’utilisation des ressources dans Project Operations.
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279315"
---
# <a name="resource-utilization-overview"></a>Vue d’ensemble de l’utilisation des ressources

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les ressources peuvent avoir une utilisation facturable cible. Cette utilisation cible est définie soit comme un attribut dans le rôle par défaut d’une ressource, soit sur l’enregistrement de la ressource réservable individuelle. Les calculs de l’utilisation sont basés sur les heures réelles que les ressources ont signalées à l’aide des entrées de temps approuvées.

Les formules suivantes sont utilisées pour calculer l’utilisation :

  - Utilisation facturable = Heures réelles facturables ÷ Capacité ressource
  - Utilisation non facturable = Temps réel avec ID du type de facturation = Non facturable, Gratuit ou Non disponible ÷ Capacité ressource
  - Interne = Temps réel sans contrat de vente ÷ Capacité ressource
  - Capacité ressource = Heures de travail de la ressource – Absence du bureau – Jours non ouvrables

Vous trouverez la vue **Utilisation des ressources** dans le volet **Ressources**.

Chaque cellule dans la grille représente le pourcentage total d’utilisation de la ressource à une période, par exemple un jour, une semaine ou un mois. Les formules suivantes sont utilisées pour colorer les cellules :

  - **Vert** : utilisation facturable >= utilisation cible de la ressource
  - **Jaune** : utilisation cible – 20 <= utilisation facturable <= utilisation cible
  - **Rouge** : utilisation facturable < utilisation cible - 20

Comme la vue **Utilisation des ressources** est basée sur le Tableau de planification, vous pouvez utiliser les fonctionnalités de filtrage du Tableau de planification pour filtrer vos résultats.

La grille nécessite que vous définissiez une utilisation cible du rôle ou de la ressource individuelle. Pour effectuer cette configuration, accédez à **Ressources** > **Rôles des ressources**.

En outre, un rôle par défaut doit être affecté à chaque ressource réservable. Accédez à **Ressources** > **Ressources**. Dans l’onglet **Project Service**, vérifiez qu’un rôle de ressource est défini, et que le champ **Est la valeur par défaut** est défini sur **Oui**. Vous pouvez ajouter des rôles supplémentaires où **Est la valeur par défaut** = **Non**. Le rôle où **Est la valeur par défaut** = **Oui** est utilisé pour évaluer l’utilisation de la ressource par rapport à la cible de ce rôle.

Dans l’onglet **Project Service**, vous pouvez également définir une utilisation cible individuelle pour la ressource. Le calcul de l’utilisation utilise ensuite cette utilisation cible pour évaluer la cible de la ressource au lieu de la cible du rôle par défaut de la ressource.

L’utilisation s’affiche uniquement pour une ressource si cette ressource est approuvée, temps facturable pendant la période affichée dans la grille.


[!INCLUDE[footer-include](../includes/footer-banner.md)]