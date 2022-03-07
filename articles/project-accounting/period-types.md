---
title: Types de période
description: Cette rubrique fournit des informations sur la manière de configurer des types de période pour une estimation de revenus.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 487e3de7895ca0752e6c9033c7bb7007ba89301c01e6205b3bc8a7d750724bc9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998773"
---
# <a name="period-types"></a>Types de période

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Un type de période définit la fréquence à laquelle les revenus d’un projet sont estimés. Cette rubrique fournit des informations sur la manière de configurer des types de période pour une estimation de revenus. 

## <a name="create-and-work-with-period-types"></a>Créer et utiliser des types de période
Pour créer et utiliser des types de période, procédez comme suit :

1. Dans votre environnement Dynamics 365 Finance, accédez à **Gestion et comptabilité des projets** > **Configurer** > **Estimations** > **Types de période**.
2. Sélectionnez **Nouveau** pour créer un nouveau type de période. Entrez un nom et une description.
3. Dans le champ **Fréquence**, sélectionnez une valeur :

    - Si vous sélectionnez **Semaine**, **Bihebdomadaire**, **Semi-mensuelle**, **Mois**, **Jour**, **Trimestre** ou **Année**, le calendrier sera utilisé pour générer les périodes. 
    - Si vous sélectionnez **Période comptable**, les périodes comptables de la configuration de comptabilité seront utilisées pour générer des périodes.
    - Si vous sélectionnez **Illimité**, vous pouvez spécifier des périodes personnalisées.
4. Sélectionnez l’enregistrement de type de période, puis sélectionnez **Générer des périodes** pour créer des périodes pour le type de période. En fonction de la fréquence de période que vous avez sélectionnée, vous avez la possibilité de spécifier une date de début ou le nombre de périodes à générer.
5. Sélectionnez **Périodes** pour revoir les périodes générées.



[!INCLUDE[footer-include](../includes/footer-banner.md)]