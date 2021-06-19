---
title: Configurer les catégories de dépense
description: Cette rubrique fournit des informations sur la configuration des catégories de dépenses et des catégories partagées pour les notes de frais.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: d66df1ffd2be2ff884561010c46cda255a2d2189
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001784"
---
# <a name="set-up-expense-categories"></a>Configurer les catégories de dépense

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Lorsque les employés créent des notes de frais, chaque dépense qu’ils enregistrent doit être associée à une catégorie de dépenses. Les catégories de dépenses sont dérivées de catégories partagées qui peuvent être partagées entre les entités juridiques de votre organisation. Selon la manière dont votre organisation est définie, ces catégories de dépenses peuvent également être partagées dans d’autres domaines. En fonction de la définition de votre organisation et des conseils de l’équipe de mise en œuvre, vous devez déterminer si les catégories utilisées dans la gestion des dépenses seront utilisées uniquement dans la gestion des dépenses ou devraient être partagées dans d’autres domaines.

> [!NOTE]
> Ces catégories peuvent être partagées entre la gestion de projet et la comptabilité et la gestion des dépenses, ou entre la gestion de projet et la comptabilité et la production. Cependant, ils ne peuvent pas être partagés entre Gestion des dépenses et Production.

Avant de pouvoir commencer le processus de configuration, les décisions suivantes doivent être prises pour chaque catégorie de dépenses :

- Qu’est-ce que la catégorie de dépense ? Les exemples incluent des catégories pour les vols, l’hôtel ou le kilométrage.
- La catégorie de dépenses peut-elle également être utilisée dans Gestion de projet et comptabilité ? Si c’est le cas, vous devez également prendre les décisions suivantes :

    - Quels comptes de coûts seront utilisés pour les dépenses suivantes ?

        - Coût
        - Répartition de la paie
        - TEC-Valeur de coût
        - Coût-article
        - TEC-valeur de coût-article
        - Perte accumulée
        - TEC-perte accumulée

    - Quels comptes de revenus seront utilisés pour les sources de revenus suivantes ?

        - Revenu facturé
        - Revenus accumulés-valeur des ventes
        - TEC-valeur des ventes
        - Produit à recevoir – production
        - Travaux en cours – production
        - Produit à recevoir – profit
        - TEC-marge
        - Revenus accumulés-abonnement
        - TEC-abonnement

- Qu’est-ce que le type de dépense ?
- Quel est le mode de paiement par défaut pour la catégorie de dépenses ?
- Les dépenses de la catégorie de dépenses doivent-elles être détaillées ?
- Quel est le compte par défaut principal pour la catégorie de dépenses ?
- Quel est le groupe de taxe d’article par défaut pour la catégorie de dépenses ?
- Des modes de paiement supplémentaires sont-ils autorisés pour la catégorie de dépenses ? Si oui, quelles sont-elles ?
- Y a-t-il des sous-catégories dans cette catégorie de dépenses ? S’il existe des sous-catégories, vous devez également prendre les décisions suivantes :

    - Certaines des sous-catégories sont-elles exclues du recouvrement fiscal ?
    - Quel est le groupe de taxe d’article des sous-catégories ?


[!INCLUDE[footer-include](../includes/footer-banner.md)]