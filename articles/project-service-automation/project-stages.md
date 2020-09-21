---
title: Phases du projet
description: Cette rubrique fournit des informations sur les phases du projet.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168021"
---
# <a name="project-stages"></a>Phases du projet 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les phases d'un projet sont mises à jour pour refléter l'état du projet à mesure qu'il progresse. Les flux des processus d'entreprise par défaut mettent automatiquement à jour certaines phases du projet pendant que d'autres sont mises à jour manuellement par le chef de projet. 

Les phases suivantes sont définies dans le flux des processus d'entreprise par défaut :

- Nouveau
- Devis
- Planifier
- Livrer
- Fin
- Fermer 

## <a name="new"></a>Nouveau

Lorsque vous créez un projet, la phase de projet est définie sur **Nouveau**. Si le projet a été créé à partir d'un modèle, il peut posséder des données de planification, d'estimation ou d'équipe. Sinon, il s'agit simplement d'un plan du projet, et les autres composants doivent être entrés.

## <a name="quote"></a>Devis

Lorsque vous associez un projet à un devis ou que vous créez un projet depuis un devis, la phase de projet est définie sur **Devis**, et les dates de début et de fin estimées sont mises à jour. Lorsque le projet est dans la phase **Devis**, l'onglet **Ventes** de la page **Entité du projet** affiche les détails du devis.

## <a name="plan"></a>Planifier

Lorsque vous ayez conclu un devis associé à un projet, et que le projet passe à la phase **Contrat**, la phase du projet est mise à jour sur **Planifier**. Lorsque le projet est dans la phase **Planifier**, la page **Entité du projet** affiche les détails du contrat.

## <a name="deliver"></a>Livrer

Lorsque le plan du projet est terminé, et que vous êtes prêt à lancer le projet, le chef de projet doit mettre à jour la phase du projet sur **Livrer** pour vous indiquer que le projet a démarré.

## <a name="complete"></a>Fin 

Lorsque le travail du projet est terminé, le chef de projet peut mettre à jour la phase sur **Terminer**. En mettant à jour la phase du projet sur **Terminer**, le chef de projet indique que le travail est terminé à 100 pourcent, mais que le projet est maintenu ouvert afin que toutes les entrées de temps ou de dépenses en attente puissent être enregistrées.

## <a name="close"></a>Fermer

Lorsque toutes les transactions sont enregistrées pour le projet, le chef de projet peut mettre à jour la phase sur **Fermer**. À ce stade, aucune transaction ne peut être enregistrée, et le projet passe en lecture seule.
