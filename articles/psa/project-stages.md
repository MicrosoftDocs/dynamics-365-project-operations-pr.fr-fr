---
title: Types de phase du projet
description: Cette rubrique fournit des informations sur les phases du projet.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e4f50d12b4f0bf1586d0a5702bcd38b891590bffe0d3f9661d7f5d170877b54e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996883"
---
# <a name="project-stage-types"></a>Types de phase du projet 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les phases d’un projet sont conçues pour refléter l’état du projet à mesure qu’il progresse. Les personnalisations permettent de mettre à jour automatiquement les phases avec les flux des processus d’entreprise, Power Automate ou des extensions de plug-in.

Les phases suivantes sont définies dans le flux des processus d’entreprise par défaut :

- Nouveau
- Devis
- Planifier
- Livrer
- Fin
- Fermer 

## <a name="new"></a>Nouveau

Lorsque vous créez un projet, la phase de projet est définie sur **Nouveau**. Si le projet a été créé à partir d’un modèle, il peut posséder des données de planification, d’estimation ou d’équipe. Sinon, il s’agit simplement d’un plan du projet, et les autres composants doivent être entrés.

## <a name="quote"></a>Devis

Lorsque vous associez un projet à un devis ou que vous créez un projet depuis un devis, la phase de projet est définie sur **Devis**, et les dates de début et de fin estimées sont mises à jour. Lorsque le projet est dans la phase **Devis**, l’onglet **Ventes** de la page **Entité du projet** affiche les détails du devis.

## <a name="plan"></a>Planifier

Lorsque vous ayez conclu un devis associé à un projet, et que le projet passe à la phase **Contrat**, la phase du projet est mise à jour sur **Planifier**. Lorsque le projet est dans la phase **Planifier**, la page **Entité du projet** affiche les détails du contrat.

## <a name="deliver"></a>Livrer

Lorsque le plan du projet est terminé, et que vous êtes prêt à lancer le projet, le chef de projet doit mettre à jour la phase du projet sur **Livrer** pour vous indiquer que le projet a démarré.

## <a name="complete"></a>Fin 

Lorsque le travail du projet est terminé, le chef de projet peut mettre à jour la phase sur **Terminer**. En mettant à jour la phase du projet sur **Terminer**, le chef de projet indique que le travail est terminé à 100 pourcent, mais que le projet est maintenu ouvert afin que toutes les entrées de temps ou de dépenses en attente puissent être enregistrées.

## <a name="close"></a>Fermer

Lorsque toutes les transactions sont enregistrées pour le projet, le chef de projet peut mettre à jour la phase sur **Fermer**. À ce stade, aucune transaction ne peut être enregistrée, et le projet passe en lecture seule.


[!INCLUDE[footer-include](../includes/footer-banner.md)]