---
title: Déterminer les taux de coût pour les estimations et les réels du projet
description: Cet article fournit des informations sur la façon dont les taux de revient sur les estimations de projet et les chiffres réels sont déterminés.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410146"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Déterminer les taux de coût pour les estimations et les réels du projet

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Pour déterminer les tarifs de prix de revient et les taux de revient dans les contextes d’estimation et de chiffres réels, le système utilise les informations des champs **Date**, **Devise** et **Unité contractante** du projet concerné.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Détermination des taux de revient dans les contextes d’estimation et de chiffres réels pour Temps

Contexte de devis pour **Temps** fait référence à :

- Détails de la ligne de devis pour **Temps**.
- Détails de la ligne de contrat pour **Temps**.
- Attributions de ressources sur un projet.

Le contexte de chiffres réels pour **Temps** fait référence à :

- Lignes de journal de saisie et de correction pour **Temps**.
- Lignes de journal créées lorsqu’une entrée de temps est soumise.

Une fois les tarifs de prix de revient déterminés, le système exécute les étapes suivantes pour saisir le taux de revient par défaut.

1. Le système associe la combinaison des champs **Rôle** et **Unité d’allocation des ressources** dans le contexte d’estimation ou réel pour que **Temps** corresponde aux lignes de prix du rôle sur le tarif. Cette correspondance suppose que vous utilisez les dimensions de tarification standard pour le coût de la main-d’œuvre. Si vous avez configuré le système pour qu’il corresponde aux champs au lieu ou en plus des champs **Rôle** et **Unité d’allocation des ressources**, puis une combinaison différente sera utilisée pour récupérer une ligne de prix de rôle correspondante.
1. Si le système trouve une ligne de prix de rôle qui a un taux de coût pour la combinaison **Rôle** et **Unité d’allocation des ressources**, c’est le taux de revient par défaut.
1. Si le système ne parvient pas à faire correspondre les valeurs des champs **Rôle** et **Unité d’allocation des ressources**, il récupère les lignes de prix de rôle dont les valeurs correspondent au champ **Rôle**, sauf les valeurs nulles du champ **Unité d’allocation des ressources**. Une fois que le système a trouvé un enregistrement de prix de rôle correspondant, il utilisera par défaut le taux de revient de cet enregistrement.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
