---
title: Résolution des prix de revient pour les estimations et les chiffres réels
description: Cette rubrique fournit des informations sur la façon dont les prix de revient des estimations et des chiffres réels sont résolus.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bad8f4b95ac5803d3f334e1b306d2a9d27a6645d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075650"
---
# <a name="resolving-cost-prices-on-estimates-and-actuals"></a>Résolution des prix de revient pour les estimations et les chiffres réels

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Pour résoudre les prix de revient et le tarif de revient pour les estimations et les chiffres réels, le système utilise les informations des champs **Date** , **Devise** et **Unité contractante** du projet concerné. Une fois la liste de prix de revient résolue, l'application résout le taux de coût.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Résolution des taux de coût sur les lignes réelles et estimées pour le temps

Les lignes d'estimation pour le temps font référence aux détails de la ligne de devis et de contrat pour les affectations de temps et de ressources sur un projet.

Une fois la liste de prix de revient résolue, le système utilise les champs **Rôle** et **Unité d’allocation de ressources** sur la ligne d'estimation pour Temps de correspondance avec les lignes de prix de rôle dans la liste de prix. Cette correspondance suppose que vous utilisiez des dimensions de tarification prêtes à l'emploi pour le coût de la main-d'œuvre. Si vous avez configuré le système pour qu'il corresponde aux champs au lieu ou en plus des champs **Rôle** et **Unité d’allocation des ressources** , puis une combinaison différente sera utilisée pour récupérer une ligne de prix de rôle correspondante. Si l'application trouve une ligne de prix de rôle qui a un taux de coût pour la combinaison **Rôle** et **Unité d’allocation des ressources** , c'est le taux de coût par défaut. Si l'application ne correspond pas aux valeurs **Rôle** et **Unité d'allocation de ressources** , alors elle récupère les lignes de prix de rôle avec un rôle correspondant, sauf les valeurs nulles de l' **unité d'allocation de ressources**. Une fois qu'il a un enregistrement de prix de rôle correspondant, le taux de coût est par défaut de cet enregistrement. 

> [!NOTE]
> Si vous configurez une hiérarchisation différente des valeurs **Rôle** et **Unité d'allocation de ressources** , ou si vous avez d'autres dimensions qui ont une priorité plus élevée, ce comportement changera en conséquence. Le système récupère les enregistrements de prix de rôle avec des valeurs qui correspondent à chacune des valeurs de dimension de tarification par ordre de priorité avec les lignes qui ont des valeurs nulles pour ces dimensions venant en dernier.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Résolution des taux de coût sur les lignes réelles et estimées pour les dépenses

Les lignes d'estimation pour les dépenses font référence aux détails de la ligne de contrat pour les dépenses et les lignes d'estimation des dépenses sur un projet.

Une fois la liste de prix de revient résolue, le système utilise une combinaison des champs **Catégorie** et **Unités** sur la ligne d'estimation pour qu'une dépense corresponde aux lignes **Prix de la catégorie** sur le tarif résolu. Si le système trouve une ligne de prix de catégorie qui a un taux de coût pour la combinaison de champs **Catégorie** et **Unité** , le taux de coût est défini par défaut. Si le système ne correspond pas aux valeurs **Catégorie** et **Unité** , ou s'il est capable de trouver une ligne de prix de catégorie correspondante mais que la méthode de tarification n'est pas **Prix par unité** , le taux de coût est défini par défaut sur zéro (0).
