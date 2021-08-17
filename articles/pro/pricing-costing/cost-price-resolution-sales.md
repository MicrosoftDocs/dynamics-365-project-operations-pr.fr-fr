---
title: Résoudre les prix de revient pour les estimations de projet et les chiffres réels
description: Cette rubrique fournit des informations sur la résolution des prix de revient sur les estimations et les chiffres réels de projet.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997558"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Résoudre les prix de revient pour les estimations de projet et les chiffres réels 

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Pour résoudre les prix de revient et le tarif de revient pour les estimations et les chiffres réels, le système utilise les informations des champs **Date**, **Devise** et **Unité contractante** du projet concerné. Une fois la liste de prix de revient résolue, l’application résout le taux de coût.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Résolution des taux de coût sur les lignes réelles et estimées pour le temps

Les lignes d’estimation pour le temps font référence aux détails de la ligne de devis et de contrat pour les affectations de temps et de ressources sur un projet.

Une fois la liste de prix de revient résolue, les champs **Rôle** et **Unité d’allocation des ressources** de la ligne d’estimation pour le temps sont comparés aux lignes de prix du rôle dans la liste de prix. Cette correspondance suppose que vous utilisez les dimensions de tarification standard pour le coût de la main-d’œuvre. Si vous avez configuré le système pour qu’il corresponde aux champs au lieu ou en plus des champs **Rôle** et **Unité d’allocation des ressources**, puis une combinaison différente sera utilisée pour récupérer une ligne de prix de rôle correspondante. Si l’application trouve une ligne de prix de rôle qui a un taux de coût pour la combinaison **Rôle** et **Unité d’allocation des ressources**, c’est le taux de coût par défaut. Si l’application ne correspond pas aux valeurs **Rôle** et **Unité d’allocation de ressources**, alors elle récupère les lignes de prix de rôle avec un rôle correspondant, sauf les valeurs nulles de l’**unité d’allocation de ressources**. Une fois qu’il a un enregistrement de prix de rôle correspondant, le taux de coût est par défaut de cet enregistrement. 

> [!NOTE]
> Si vous configurez une hiérarchisation différente des valeurs **Rôle** et **Unité d’allocation de ressources**, ou si vous avez d’autres dimensions qui ont une priorité plus élevée, ce comportement changera en conséquence. Le système récupère les enregistrements de prix de rôle avec des valeurs qui correspondent à chacune des valeurs de dimension de tarification par ordre de priorité avec les lignes qui ont des valeurs nulles pour ces dimensions venant en dernier.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Résolution des taux de coût sur les lignes réelles et estimées pour les dépenses

Les lignes d’estimation pour les dépenses font référence aux détails de la ligne de contrat pour les dépenses et les lignes d’estimation des dépenses sur un projet.

Une fois la liste de prix de revient résolue, le système utilise une combinaison des champs **Catégorie** et **Unité** sur la ligne d’estimation des dépenses pour faire correspondre les lignes **Prix de la catégorie** sur la liste de prix résolue. Si le système trouve une ligne de prix de catégorie qui a un taux de coût pour la combinaison de champs **Catégorie** et **Unité**, le taux de coût est défini par défaut. Si le système ne correspond pas aux valeurs de **Catégorie** et **Unité**, ou s’il est en mesure de trouver une ligne de prix de catégorie correspondante mais que la méthode de tarification n’est pas **Prix unitaire**, le taux de coût par défaut est zéro (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Résolution des taux de coûts sur les lignes de chiffres réels et d’estimation pour le matériel

Les lignes d’estimation pour le matériel font référence aux détails de la ligne de devis et de contrat pour le matériel et les lignes d’estimation de matériel d’un projet.

Une fois que la liste de prix de revient est résolue, le système utilise une combinaison des champs **Produit** et **Unité** sur la ligne d’estimation d’une estimation de matériel pour les mettre en correspondance avec les lignes **Éléments tarifaires** du tarif résolu. Si le système trouve une ligne de prix de produit ayant un taux de coûts pour la combinaison de champs **Produit** et **Unité**, le taux de coûts est défini par défaut. Si le système ne correspond pas aux valeurs **Produit** et **Unité**, ou s’il est en mesure de trouver une ligne d’élément tarifaire correspondante mais que la méthode de tarification est basée sur le coût standard ou le coût actuel et que ces derniers ne sont pas définis sur le produit, le coût unitaire est par défaut égal à zéro.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
