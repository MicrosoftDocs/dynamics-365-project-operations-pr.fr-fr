---
title: Types de période
description: Cet article fournit des informations sur la configuration des types de périodes pour l’estimation des revenus.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bbf2dcb4758611aa9d0591ddfec42869f4438c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930959"
---
# <a name="period-types"></a>Types de période

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Un type de période définit la fréquence à laquelle les revenus d’un projet sont estimés. Cet article fournit des informations sur la configuration des types de périodes pour l’estimation des revenus. 

## <a name="create-and-work-with-period-types"></a>Créer et utiliser des types de période
Pour créer et utiliser des types de période, procédez comme suit :

1. Dans votre environnement Dynamics 365 Finance, accédez à **Gestion de projet et comptabilité** > **Configurer** > **Estimations** > **Types de période**.
2. Sélectionnez **Nouveau** pour créer un nouveau type de période. Entrez un nom et une description.
3. Dans le champ **Fréquence**, sélectionnez une valeur :

    - Si vous sélectionnez **Semaine**, **Bihebdomadaire**, **Semi-mensuelle**, **Mois**, **Jour**, **Trimestre** ou **Année**, le calendrier sera utilisé pour générer les périodes. 
    - Si vous sélectionnez **Période comptable**, les périodes comptables de la configuration de comptabilité seront utilisées pour générer des périodes.
    - Si vous sélectionnez **Illimité**, vous pouvez spécifier des périodes personnalisées.
4. Sélectionnez l’enregistrement de type de période, puis sélectionnez **Générer des périodes** pour créer des périodes pour le type de période. En fonction de la fréquence de période que vous avez sélectionnée, vous avez la possibilité de spécifier une date de début ou le nombre de périodes à générer.
5. Sélectionnez **Périodes** pour revoir les périodes générées.



[!INCLUDE[footer-include](../includes/footer-banner.md)]