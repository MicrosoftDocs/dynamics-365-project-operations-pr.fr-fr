---
title: Déterminer les taux de coût pour les estimations et les réels du projet
description: Cet article fournit des informations sur la façon dont les taux de revient sur les estimations de projet et les chiffres réels sont déterminés.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475270"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Déterminer les taux de coût pour les estimations et les réels du projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Pour déterminer les prix de vente dans les estimations et les chiffres réels dans Microsoft Dynamics 365 Project Operations, le système utilise d’abord la date et la devise du devis entrant ou du contexte des chiffres réels pour déterminer les tarifs de vente. Dans le contexte des chiffres réels en particulier, le système utilise le champ **Date de la transaction** pour déterminer quels tarifs sont applicables. La valeur **Date de la transaction** de l’estimation entrante ou réelle est comparée aux valeurs **Date de début effective (sans fuseau horaire)** et **Date de fin effective (sans fuseau horaire)** sur la liste de prix. Une fois la liste de prix de revient déterminée, le système détermine le taux de coût.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Détermination des taux de revient dans les contextes d’estimation et de chiffres réels pour Temps

Contexte de devis pour **Temps** fait référence à :

- Détails de la ligne de devis pour **Temps**.
- Détails de la ligne de contrat pour **Temps**.
- Attributions de ressources sur un projet.

Le contexte de chiffres réels pour **Temps** fait référence à :

- Lignes de journal de saisie et de correction pour **Temps**.
- Lignes de journal créées lorsqu’une entrée de temps est soumise.

Une fois les tarifs de prix de revient déterminés, le système exécute les étapes suivantes pour saisir le taux de revient par défaut.

1. Le système associe la combinaison des champs **Rôle**, **Société d’allocation de ressources** et **Unité d’allocation des ressources** dans le contexte d’estimation ou réel pour que **Temps** corresponde aux lignes de prix du rôle sur le tarif. Cette correspondance suppose que vous utilisez les dimensions de tarification standard pour le coût de la main-d’œuvre. Si vous avez configuré le système pour qu’il corresponde aux champs au lieu ou en plus des champs **Rôle**, **Unité d’allocation des ressources** et **Unité d’allocation des ressources**, puis une combinaison différente sera utilisée pour récupérer une ligne de prix de rôle correspondante.
1. Si le système trouve une ligne de prix de rôle qui a un taux de coût pour la combinaison **Rôle**, **Société d’allocation de ressources** et **Unité d’allocation des ressources**, c’est le taux de coût par défaut.
1. Si le système ne peut pas correspondre aux valeurs **Rôle**, **Société d’allocation de ressources** et **Unité d’allocation de ressources**, il supprime la dimension qui a la priorité la plus basse, recherche les lignes de prix de rôle qui ont des correspondances pour les deux autres valeurs de dimension et continue à supprimer progressivement les dimensions jusqu’à ce qu’une ligne de prix de rôle correspondante soit trouvée. Le taux de coût de cet enregistrement sera utilisé comme taux de coût par défaut. Si le système ne trouve pas de ligne de prix de rôle correspondante, le prix est défini sur **0** (zéro) par défaut.

> [!NOTE]
> Si vous configurez une hiérarchisation différente des champs **Rôle** et **Unité d’allocation de ressources**, ou si vous avez d’autres dimensions qui ont une priorité plus élevée, ce comportement changera en conséquence. Le système récupère les enregistrements de prix de rôle dont les valeurs correspondent à chaque valeur de dimension de prix par ordre de priorité. Les lignes qui ont des valeurs nulles pour ces dimensions viennent en dernier.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Détermination des taux de revient sur les lignes réelles et estimées pour les dépenses

Contexte de devis pour **Dépense** fait référence à :

- Détails de la ligne de devis pour **Dépense**.
- Détails de la ligne de contrat pour **Dépense**.
- Estimations de dépense sur un projet.

Le contexte de chiffres réels pour **Dépense** fait référence à :

- Lignes de journal de saisie et de correction pour **Dépense**.
- Lignes de journal créées lorsqu’une entrée de dépense est soumise.

Une fois les tarifs de prix de revient déterminés, le système exécute les étapes suivantes pour saisir le taux de revient par défaut.

1. Le système associe la combinaison des champs **Catégorie** et **Unité** dans le contexte d’estimation ou de chiffres réels pour que **Dépense** corresponde aux lignes de prix de la catégorie sur les tarifs.
1. Si le système trouve une ligne de prix de catégorie qui a un taux de coût pour la combinaison de champs **Catégorie** et **Unité**, le taux de revient utilisé est le taux de revient par défaut.
1. Si le système ne correspond pas aux valeurs **Catégorie** et **Unité**, le prix est défini sur **0** (zéro) par défaut.
1. Dans le contexte de l’estimation, si le système est en mesure de trouver une ligne de prix de catégorie correspondante, mais que la méthode de tarification n’est pas **Prix unitaire**, le taux de revient par défaut est **0** (zéro).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Détermination des coûts sur les lignes de chiffres réels et d’estimation pour le matériel

Contexte de devis pour **Matériel** fait référence à :

- Détails de la ligne de devis pour **Matériel**.
- Détails de la ligne de contrat pour **Matériel**.
- Estimations du matériel du projet.

Le contexte de chiffres réels pour **Matériel** fait référence à :

- Lignes de journal de saisie et de correction pour **Matériel**.
- Lignes de journal créées lorsqu’un journal d’utilisation du matériel est soumis.

Une fois les tarifs de prix de revient déterminés, le système exécute les étapes suivantes pour saisir le taux de revient par défaut.

1. Le système utilise la combinaison des champs **Produit** et **Unité** dans le contexte d’estimation ou de chiffres réels pour que **Matériau** corresponde aux lignes d’élément tarifaire sur les tarifs.
1. Si le système trouve une ligne d’élément tarifaire qui a un taux de revient pour la combinaison de champs **Produit** et **Unité**, le taux de revient utilisé est le taux de revient par défaut.
1. Si le système ne correspond pas aux valeurs **Produit** et **Unité**, le coût unitaire par défaut est égal à **0** (zéro).
1. Dans le contexte de l’estimation ou des chiffres réels, si le système est en mesure de trouver une ligne d’élément tarifaire correspondante, mais que la méthode de tarification n’est pas **Montant de la devise**, le taux de revient par défaut est **0** (zéro). Ce problème se produit, car Project Operations ne prend en charge que la méthode de tarification **Montant en devise** pour les matériaux utilisés sur un projet.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
