---
title: Résoudre des prix de revient pour les estimations et les chiffres réels – Simplifié
description: Cette rubrique fournit des informations sur la façon dont les prix de revient des estimations et des chiffres réels sont résolus.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2afaa2231f4044dbcbfa24b91aec39289275a91
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764583"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Résoudre des prix de revient pour les estimations et les chiffres réels – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Pour résoudre les prix de revient et le tarif de revient pour les estimations et les chiffres réels, le système utilise les informations des champs **Date**, **Devise** et **Unité contractante** du projet concerné. Une fois la liste de prix de revient résolue, l’application résout le taux de coût.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Résolution des taux de coût sur les lignes réelles et estimées pour le temps

Les lignes d’estimation pour le temps font référence aux détails de la ligne de devis et de contrat pour les affectations de temps et de ressources sur un projet.

Une fois la liste de prix de revient résolue, les champs **Rôle** et **Unité d’allocation des ressources** de la ligne d'estimation pour le temps sont comparés aux lignes de prix du rôle dans la liste de prix. Cette correspondance suppose que vous utilisez les dimensions de tarification standard pour le coût de la main-d'œuvre. Si vous avez configuré le système pour qu’il corresponde aux champs au lieu ou en plus des champs **Rôle** et **Unité d’allocation des ressources**, puis une combinaison différente sera utilisée pour récupérer une ligne de prix de rôle correspondante. Si l’application trouve une ligne de prix de rôle qui a un taux de coût pour la combinaison **Rôle** et **Unité d’allocation des ressources**, c’est le taux de coût par défaut. Si l’application ne correspond pas aux valeurs **Rôle** et **Unité d’allocation de ressources**, alors elle récupère les lignes de prix de rôle avec un rôle correspondant, sauf les valeurs nulles de l’**unité d’allocation de ressources**. Une fois qu’il a un enregistrement de prix de rôle correspondant, le taux de coût est par défaut de cet enregistrement. 

> [!NOTE]
> Si vous configurez une hiérarchisation différente des valeurs **Rôle** et **Unité d’allocation de ressources**, ou si vous avez d’autres dimensions qui ont une priorité plus élevée, ce comportement changera en conséquence. Le système récupère les enregistrements de prix de rôle avec des valeurs qui correspondent à chacune des valeurs de dimension de tarification par ordre de priorité avec les lignes qui ont des valeurs nulles pour ces dimensions venant en dernier.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Résolution des taux de coût sur les lignes réelles et estimées pour les dépenses

Les lignes d’estimation pour les dépenses font référence aux détails de la ligne de contrat pour les dépenses et les lignes d’estimation des dépenses sur un projet.

Une fois la liste de prix de revient résolue, le système utilise une combinaison des champs **Catégorie** et **Unité** sur la ligne d'estimation des dépenses pour faire correspondre les lignes **Prix de la catégorie** sur la liste de prix résolue. Si le système trouve une ligne de prix de catégorie qui a un taux de coût pour la combinaison de champs **Catégorie** et **Unité**, le taux de coût est défini par défaut. Si le système ne correspond pas aux valeurs de **Catégorie** et **Unité**, ou s'il est en mesure de trouver une ligne de prix de catégorie correspondante mais que la méthode de tarification n'est pas **Prix unitaire**, le taux de coût par défaut est zéro (0).
