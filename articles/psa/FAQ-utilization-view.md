---
title: Afficher l’utilisation facturable des ressources
description: Cette rubrique fournit des informations sur la vue d’utilisation des ressources.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 32dba5acd95c1d192556153240ebd51343112be53aa3db93e5e6f127c2d960e9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007143"
---
# <a name="view-chargeable-utilization-for-resources"></a>Afficher l’utilisation facturable des ressources

[!include [banner](../includes/psa-now-project-operations.md)]
 
La **Vue d’utilisation** sur la page **Utilisation des ressources Project Service** affiche l’utilisation imputable de chaque ressource réservable. Comme la vue est basée sur le tableau de planification, vous trouverez plusieurs fonctions identiques.

> ![Capture d’écran de vue Utilisation.](media/FAQ-utilization-1.png)
 

Le calcul de l’utilisation facturable fonctionne comme suit :

   Utilisation facturable = (Heures réelles facturables) / (Capacité ressource).

Les cellules représentent l’utilisation facturable calculée pour la période sélectionnée (jours, semaines ou mois).

Les couleurs de chaque cellule affichent l’utilisation facturable d’une ressource comparée à son utilisation facturable cible. 

L’utilisation cible peut être définie sur le rôle par défaut de la ressource ou sur la ressource individuelle elle-même. Le calcul prend en compte la ressource individuelle pour la première cible, puis le rôle par défaut de la ressource.

## <a name="set-target-on-a-resource"></a>Définir la cible sur une ressource

1. Accédez à **Ressources** \> **Ressources**. 
2. Sélectionnez une ressource pour ouvrir l’enregistrement. 
3. Dans l’onglet **Project Service**, vous pouvez définir l’utilisation cible de la ressource.

> ![Capture d’écran de l’utilisation de l’onglet Project Service pour définir l’utilisation cible.](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a>Définir l’utilisation cible sur un rôle

1. Accédez à **Ressources** \> **Rôles des ressources**. 
2. Sélectionnez un rôle et ouvrez l’enregistrement. 
3. Définissez l’utilisation cible du rôle.

> ![Capture d’écran de l’utilisation Rôles des ressources pour définir l’utilisation cible.](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a>Calculer l’utilisation facturable d’une ressource

Pour calculer l’utilisation facturable d’une ressource, vous devez satisfaire certaines conditions préalables. 

### <a name="set-default-role-for-individual-resource"></a>Définir le rôle par défaut d’une ressource individuelle

D’abord, l’utilisation cible doit être définie sur la ressource individuelle ou les rôles de la ressource. Si vous utilisez des rôles de ressource pour les cibles, chaque ressource individuelle doit avoir un rôle par défaut. 

1. Pour définir cela, accédez à **Ressources** \> **Ressources**. 
2. Sélectionnez une ressource, ouvrez l’enregistrement, puis sélectionnez l’onglet **Project Service**. 
3. Dans la grille **Rôle de la ressource**, vérifiez qu’il existe un rôle pour la ressource et que **Est la valeur par défaut** est défini sur **Oui**.
 
### <a name="change-billing-type-for-resource-role"></a>Modifier le type de facturation pour le rôle de ressource

Les rôles de la ressource doivent être définis pour avec un type facturation **Facturable**. 

1. Accédez à **Ressources** \> **Rôles des ressources**. 
2. Ouvrez l’enregistrement à mettre à jour, puis définissez la valeur par défaut du type de facturation sur **Facturable**.

### <a name="set-working-hours-for-resource-role"></a>Définir des heures de travail pour le rôle de la ressource
 
La ressource doit avoir des heures ouvrées pour le calcul de la capacité. 

1. Accédez à **Ressources** \> **Ressources**. 
2. Sélectionnez une ressource pour ouvrir l’enregistrement, puis **Afficher les heures de travail**. 
3. Vous pouvez effectuer une mise à jour en bloc de la liste des ressources en appliquant un **Modèle d’heures de travail** de la vue **Liste des ressources**.

## <a name="troubleshooting-chargeable-actual-hours"></a>Dépannage des heures réelles facturables

Les heures réelles facturables sont extraites de l’entité **Chiffres réels**. Les chiffres réels avec un type de facturation **Facturable** sont inclus dans le calcul et pour cette raison, vous devez disposer de projets où les chiffres réels sont facturables.

Si vous ne voyez pas d’utilisation facturable, voici ce que vous pouvez vérifier :

- La ressource dispose d’heures de travail définies pour la capacité.
- La ressource a une cible d’utilisation définie individuellement ou un rôle par défaut qui lui est attribué. Le rôle a une cible d’utilisation qui lui est définie.
- Les chiffres réels ont un type de facturation **Facturable** pour la période pour laquelle vous prévoyez le calcul de l’utilisation. Vérificiez ce qui suit si vous voyez des chiffres réels avec des types de facturation autres que facturables :

  - Le rôle utilisé sur le chiffre réel possède un type de facturation par défaut autre que facturable.
  - Le rôle sur la ligne de contrat du projet soutenant le projet a été défini sur non facturable.
  - Le projet ne dispose pas de ligne de contrat associée.



[!INCLUDE[footer-include](../includes/footer-banner.md)]