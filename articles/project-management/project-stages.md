---
title: Phases du projet
description: Cet article fournit des informations sur les étapes de projet disponibles dans Microsoft Dynamics Project Operations.
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a8c8e63a2d8c238f582b67348f88b7285a0b1e12
ms.sourcegitcommit: 278740b352f1ed9618ee5c79597c8f449984d6f4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/19/2022
ms.locfileid: "9177376"
---
# <a name="project-stages"></a>Phases du projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les phases d’un projet sont conçues pour refléter l’état du projet à mesure qu’il progresse. Les personnalisations permettent de mettre à jour automatiquement les phases avec les flux des processus d’entreprise, Power Automate ou des extensions de plug-in.

Les phases suivantes sont définies dans le flux des processus d’entreprise par défaut :

- Nouveau
- Devis
- Plan
- Livrer
- Fin
- Fermer 

## <a name="new"></a>Nouveau

Lorsque vous créez un projet, la phase de projet est définie sur **Nouveau**. Si le projet a été créé à partir d’un modèle, il peut posséder des données de planification, d’estimation ou d’équipe. Sinon, il s’agit d’un plan du projet, et les autres composants doivent être entrés.

## <a name="quote"></a>Devis

Lorsque vous associez un projet à un devis ou que vous créez un projet depuis un devis, la phase de projet est définie sur **Devis**, et les dates de début et de fin estimées sont mises à jour. Lorsque le projet est dans la phase **Devis**, l’onglet **Ventes** de la page **Entité du projet** affiche les détails du devis.

## <a name="plan"></a>Planifier

Lorsque vous ayez conclu un devis associé à un projet, et que le projet passe à la phase **Contrat**, la phase du projet est mise à jour sur **Planifier**. Lorsque le projet est dans la phase **Plan**, l’onglet **Ventes** de la page **Entité du projet** affiche les détails du contrat.

## <a name="deliver"></a>Livrer

Lorsque le plan du projet est terminé, et que vous êtes prêt à lancer le projet, le chef de projet doit mettre à jour la phase du projet sur **Livrer** pour vous indiquer que le projet a démarré.

## <a name="complete"></a>Fin 

Lorsque le travail du projet est terminé, le chef de projet peut mettre à jour la phase sur **Terminer**. En mettant à jour la phase du projet sur **Terminer**, le chef de projet indique que le travail est terminé à 100 pourcent, mais que le projet est maintenu ouvert afin que toutes les entrées de temps ou de dépenses en attente puissent être enregistrées.

## <a name="close"></a>Fermer

Lorsque toutes les transactions sont enregistrées pour le projet, le chef de projet peut mettre à jour la phase sur **Fermer**. À ce stade, aucune transaction ne peut être enregistrée, et le projet passe en lecture seule.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
