---
title: Coût pour compléter les méthodes
description: Cette rubrique fournit des informations sur les méthodes utilisées pour calculer le coût de réalisation d'un projet.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531418"
---
# <a name="cost-to-complete-methods"></a>Coût pour compléter les méthodes

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique fournit des informations sur les méthodes utilisées pour calculer le coût de réalisation d'un projet. Il existe plusieurs méthodes que vous pouvez utiliser pour calculer le coût de réalisation d'un projet. 

Lorsque vous créez une estimation pour un projet, sur la page **Créer une estimation**, dans le champ **Coût pour compléter les méthodes**, vous pouvez sélectionner l'un des coûts suivants pour compléter les méthodes.

| Coût pour compléter la méthode    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Coût total - réel            | Saisissez les coûts estimés manuellement dans les champs **Coût total** ou **Quantité totale** à l'aide du bouton **Estimation du coût** sur la page **Estimation**. Le système soustrait les coûts réels des totaux que vous avez saisis. Le total correspond au coût de réalisation du projet. Cette méthode n'utilise pas les estimations de dépenses et les affectations de ressources saisies dans Project Operations au sein de Microsoft Dataverse. Le coût total ou la quantité totale peut être mis à jour manuellement si nécessaire.  |
| Prévision totales-chiffre réel        | Les affectations de ressources et les estimations de dépenses sont utilisées pour déterminer le montant total des prévisions du projet. Les coûts réels sont comparés à cette prévision pour calculer le coût pour terminer.                                                                                                                                                                                                                                                                          |
| Comme estimation précédente         | Les mêmes méthodes d'estimation utilisées dans la période précédente sont utilisées ici. Cette méthode nécessite un modèle de prévision si la période précédente nécessitait un modèle de prévision.                                                                                                                                                                                                                                                                                                                           |
| Définir le coût pour terminer à zéro | Généralement utilisée avant l'élimination du projet d'estimation, cette méthode fait correspondre les estimations totales aux transactions réelles enregistrées et efface la colonne **Coût pour compléter**. Une fois terminé, le résultat est toujours de 100 %. Pour chaque ligne de coût que vous créez, la case à cocher **Prévision** est désactivée et l'estimation totale est copiée à partir de l'estimation des coûts précédente. La consommation réelle pour la période estimée est déduite du coût de réalisation du projet.              |
| À partir du modèle de coût           | Méthode de coût à terminer qui est configurée dans le modèle de coût associé au projet d'estimation sélectionné.                                                                                                                                                                                                                                                                                                                                                                          |
