---
title: Résolution des prix de revient pour les estimations et les chiffres réels
description: Cette rubrique fournit des informations sur la façon dont les prix de revient des estimations et des chiffres réels sont résolus.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d81b521acbfd97127cf056bd41a3249c01108374
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001378"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Résolution des prix de revient pour les estimations et les chiffres réels

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Pour résoudre les prix de revient et le tarif de revient pour les estimations et les chiffres réels, le système utilise les informations des champs **Date**, **Devise** et **Unité contractante** du projet concerné. Une fois la liste de prix de revient résolue, l’application résout le taux de coût.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Résolution des taux de coût sur les lignes réelles et estimées pour le temps

Les lignes d’estimation pour le temps font référence aux détails de la ligne de devis et de contrat pour les affectations de temps et de ressources sur un projet.

Une fois la liste de prix de revient résolue, le système utilise les champs **Rôle**, **Société d’allocation de ressources** et **Unité d’allocation des ressources** sur la ligne d’estimation pour Temps de correspondance avec les lignes de prix de rôle dans la liste de prix. Cette correspondance suppose que vous utilisiez des dimensions de tarification prêtes à l’emploi pour le coût de la main-d’œuvre. Si vous avez configuré le système pour qu’il corresponde aux champs au lieu ou en plus des champs **Rôle**, **Unité d’allocation des ressources** et **Unité d’allocation des ressources**, puis une combinaison différente sera utilisée pour récupérer une ligne de prix de rôle correspondante. Si l’application trouve une ligne de prix de rôle qui a un taux de coût pour la combinaison **Rôle**, **Société d’allocation de ressources** et **Unité d’allocation des ressources**, c’est le taux de coût par défaut. Si l’application ne peut pas correspondre exactement à la combinaison des valeurs **Rôle**, **Société d’allocation de ressources** et **Unité d’allocation des ressources**, elle récupérera les lignes de prix de rôle avec une valeur de rôle correspondante, mais aura des valeurs Null pour **Unité d’allocation des ressources** et **Société d’allocation de ressources**. Une fois qu’un enregistrement de prix de rôle correspondant avec une valeur de prix de rôle correspondante est trouvé, le taux de coût par défaut est celui de cet enregistrement. 

> [!NOTE]
> Si vous configurez une hiérarchisation différente des valeurs **Rôle**, **Société d’allocation de ressources** et **Unité d’allocation de ressources**, ou si vous avez d’autres dimensions qui ont une priorité plus élevée, ce comportement changera en conséquence. Le système récupère les enregistrements de prix de rôle avec des valeurs qui correspondent à chacune des valeurs de dimension de tarification par ordre de priorité avec des lignes qui ont des valeurs nulles pour les dimensions qui viennent en dernier dans l’ordre de priorité.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Résolution des taux de coût sur les lignes réelles et estimées pour les dépenses

Les lignes d’estimation pour les dépenses font référence aux détails de la ligne de contrat pour les dépenses et les lignes d’estimation des dépenses sur un projet.

Une fois la liste de prix de revient résolue, le système utilise une combinaison des champs **Catégorie** et **Unités** sur la ligne d’estimation pour qu’une dépense corresponde aux lignes **Prix de la catégorie** sur le tarif résolu. Si le système trouve une ligne de prix de catégorie qui a un taux de coût pour la combinaison de champs **Catégorie** et **Unité**, le taux de coût est défini par défaut. Si le système ne correspond pas aux valeurs **Catégorie** et **Unité**, ou s’il est capable de trouver une ligne de prix de catégorie correspondante mais que la méthode de tarification n’est pas **Prix par unité**, le taux de coût est défini par défaut sur zéro (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Résolution des taux de coûts sur les lignes de chiffres réels et d’estimation pour le matériel

Les lignes d’estimation pour le matériel font référence aux détails de la ligne de devis et de contrat pour le matériel et les lignes d’estimation de matériel d’un projet.

Une fois que la liste de prix de revient est résolue, le système utilise une combinaison des champs **Produit** et **Unité** sur la ligne d’estimation d’une estimation de matériel pour les mettre en correspondance avec les lignes **Éléments tarifaires** du tarif résolu. Si le système trouve une ligne de prix de produit ayant un taux de coûts pour la combinaison de champs **Produit** et **Unité**, le taux de coûts est défini par défaut. Si le système ne correspond pas aux valeurs **Produit** et **Unité**, le coût unitaire par défaut est égal à zéro. Cette valeur par défaut se produit également s’il existe une ligne d’élément tarifaire correspondante, mais que la méthode de tarification est basée sur un coût standard ou un coût actuel qui n’est pas défini dans le produit.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
