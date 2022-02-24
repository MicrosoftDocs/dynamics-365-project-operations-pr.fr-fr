---
title: Configurer la gestion des dépenses
description: Cet article décrit les considérations et les décisions que vous devez prendre pendant le processus de planification avant de configurer la gestion des dépenses dans Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271350"
---
# <a name="configure-expense-management"></a>Configurer la gestion des dépenses

Cette rubrique décrit les considérations et les décisions que vous devez prendre pendant le processus de planification avant de configurer la gestion des dépenses. Dans la gestion des dépenses, vous pouvez stocker des informations sur les modes de paiement, les demandes de déplacement, les notes de frais, les politiques, etc.

Étant donné qu'un grand nombre des décisions que vous prenez lorsque vous planifiez votre configuration pour la gestion des dépenses sont basées sur la hiérarchie et la structure financière de votre organisation, vous devez vous référer aux documents de planification de ces domaines.

## <a name="intercompany-expenses"></a>Dépenses intersociétés

Lorsque vous activez les dépenses intersociétés, vous autorisez les entités juridiques et les employés à engager des dépenses pour le compte d'une autre entité juridique et vous percevez le paiement de l'entité juridique employée au sein de votre organisation. Par exemple, un employé de l'entité juridique A termine un projet pour l'entité juridique B et le projet entraîne des frais de déplacement. Si les dépenses intersociétés sont activées, l'employé peut alors déposer une note de frais qui publiera la dépense à l'entité juridique B, et la dépense doit alors être payée par l'entité juridique A. Si votre organisation n'est pas constituée de plusieurs entités juridiques, vous n'avez pas besoin d'activer les dépenses intersociétés.

**Décision :** Voulez-vous activer les dépenses intersociétés ?

## <a name="financial-management"></a>Gestion financière

La gestion des dépenses est étroitement intégrée à la gestion financière de votre organisation. Une grande partie de votre configuration de la gestion des dépenses sera basée sur les décisions que vous avez prises concernant les finances de votre organisation. Les sections suivantes décrivent les différents domaines qui nécessitent une planification et des décisions, en fonction des décisions financières de votre organisation et des recommandations de votre équipe de direction.

### <a name="per-diems"></a>Indemnités quotidiennes

Vous devez définir les indemnités journalières des employés fournies par votre organisation. Étant donné que les indemnités journalières permettent généralement de couvrir les dépenses telles que les repas, les hébergements et d’autres dépenses annexes, vous pouvez créer des règles pour les indemnités journalières que votre organisation verse. Le taux d’indemnité journalière peut être basé sur la période de l’année et/ou le lieu du déplacement. Lorsque vous définissez une règle d’indemnités journalières, vous pouvez indiquer qu’un pourcentage du taux d’indemnité journalière est retenu si un collaborateur bénéficie de repas ou services gratuits. Vous pouvez également définir des niveaux de montants journaliers pour définir le nombre d'heures minimal et maximal pouvant être appliqué aux déplacements d'un collaborateur.

**Décisions :**

- Règles d'indemnités journalières par défaut pour le premier et le dernier jour :

    - Quel est le nombre minimum d'heures qu'un employé peut indiquer pour une journée afin de percevoir une indemnité journalière ?
    - Y a-t-il une réduction du montant offert pour les repas du premier et du dernier jour ? En cas de réduction, quel est le pourcentage de cette réduction ?
    - Y a-t-il une réduction du montant offert pour l'hébergement à l'hôtel le premier et le dernier jour ? En cas de réduction, quel est le pourcentage de cette réduction ?
    - Y a-t-il une réduction du montant offert pour les autres dépenses engagées le premier et le dernier jour ? En cas de réduction, quel est le pourcentage de cette réduction ?

- Règles d’indemnités journalières par défaut :

    - Existe-t-il un pourcentage de réduction de l’allocation journalière pour chaque repas si, par exemple, le repas est gratuit ? En cas de réduction, quel est le pourcentage de réduction pour chaque repas ?
    - La réduction de repas est-elle calculée par jour, par déplacment ou par le nombre de repas par jour ?
    - Les montants des indemnités journalières devraient-ils être arrondis de manière habituelle ou arrondis à l'unité supérieure ?
    - Les indemnités journalières sont-elles calculées sur une période de 24 heures ou sur un jour calendaire ?

- Règles d'indemnités journalières basées sur l'emplacement :

    - Les montants journaliers varient-ils selon l'emplacement ? Quels emplacements sont concernés ?
    - Si les montants journaliers varient selon l'emplacement, pour chaque emplacement, quel pourcentage est prévu pour les types de dépenses suivants :

        - Repas
        - Hôtel
        - Autres dépenses

### <a name="expense-management-journals-and-accounts"></a>Journaux et comptes de gestion des dépenses

La gestion des dépenses nécessite que vous utilisiez plusieurs journaux et comptes. Vous devez décider, par exemple, si le même compte est utilisé pour les avances de fonds et les litiges de paiement de carte de crédit.

**Décisions :**

- Dans quel journal de comptabilité les notes de frais approuvées sont-elles comptabilisées ?
- Quel compte est utilisé pour les avances de fonds ?
- Les avances de fonds doivent-elles être comptabilisées immédiatement ?

### <a name="payment-methods"></a>Modes de paiement

Lorsque vous autorisez les employés à engager des dépenses au nom de votre entreprise, vous devez définir les modes de paiement que les employés sont autorisés à utiliser. Par exemple, vous pouvez autoriser des collaborateurs à utiliser des espèces ou une carte de crédit d’entreprise. Vous pouvez également autoriser des collaborateurs à utiliser des cartes de crédit personnelles pour les rembourser ensuite. Vous devez prendre les décisions suivantes pour chaque mode de paiement que vous autorisez.

**Décisions :**

- Quels modes de paiement sont autorisés ?
- À qui appartiennent les dépenses sur le mode de paiement ?
- Existe-t-il un type de compte de contrepartie ? S'il existe un type de compte de contrepartie, de quoi s'agit-il ?
- S'il existe un compte de contrepartie, quel est ce compte ?
- Si le mode de paiement est une carte de crédit, le mode de paiement doit-il être utilisé uniquement avec les transactions importées ?

### <a name="expense-categories-and-shared-categories"></a>Catégories de dépenses et catégories partagées

Lorsque les employés créent une note de frais, chaque dépense qu'ils enregistrent doit être associée à une catégorie de dépenses. Les catégories de dépenses sont dérivées de catégories partagées qui peuvent être partagées entre les entités juridiques de votre organisation. Ces catégories peuvent également être partagées dans Gestion de projet et comptabilité, selon la façon dont votre organisation est définie. En fonction de la définition de votre organisation et des conseils de l'équipe de mise en œuvre, déterminez si les catégories utilisées dans la gestion des dépenses seront utilisées uniquement dans la gestion des dépenses ou si elles devraient être partagées entre Gestion de projet et comptabilité et Gestion des dépenses. Notez que ces catégories peuvent être partagées entre Projet et Dépense ou entre Projet et Prodiuction, mais pas entre Dépense et Production. Vous devez prendre les décisions suivantes pour chaque catégorie de dépenses.

**Décisions :**

- Qu’est-ce que la catégorie de dépense ? Les exemples incluent des catégories pour les vols, l’hôtel ou le kilométrage.
- La catégorie de dépenses peut-elle également être utilisée dans Gestion de projet et comptabilité ?
- Qu’est-ce que le type de dépense ?
- Quel est le mode de paiement par défaut pour la catégorie de dépenses ?
- Les dépenses de la catégorie de dépenses doivent-elles être détaillées ?
- Quel est le compte par défaut principal pour la catégorie de dépenses ?
- Quel est le groupe de taxe d’article par défaut pour la catégorie de dépenses ?
- Des modes de paiement supplémentaires sont-ils autorisés pour la catégorie de dépenses ? Si des modes de paiement supplémentaires sont autorisés, quels sont-ils ?
- Y a-t-il des sous-catégories dans cette catégorie de dépenses ? S’il existe des sous-catégories, vous devez également prendre les décisions suivantes :

    - Certaines des sous-catégories sont-elles exclues du recouvrement fiscal ?
    - Quel est le groupe de taxe d’article des sous-catégories ?

Si la catégorie de dépense est également utilisée dans Gestion de projet et comptabilité, répondez aux questions restantes. Sinon, passez à la section suivante.

- Quels comptes de coûts seront utilisés pour les dépenses suivantes ?

    - Coût
    - Répartition de la paie
    - TEC-Valeur de coût
    - Coût-article
    - TEC-valeur de coût-article
    - Perte accumulée
    - TEC-perte accumulée

- Quels comptes de revenus seront utilisés pour les éléments suivants ?

    - Revenu facturé
    - Revenus accumulés-valeur des ventes
    - Travaux en cours – prix de vente
    - Produit à recevoir – production
    - Travaux en cours – production
    - Produit à recevoir – profit
    - TEC-marge
    - Revenus accumulés-abonnement
    - TEC-abonnement

### <a name="taxes"></a>Taxes

Pour les taxes liées aux dépenses, vous devez déterminer ce qui est inclus ou activé sur les notes de frais.

**Décisions :**

- La taxe de vente est-elle incluse dans les montants des dépenses ?
- Le recouvrement fiscal doit-il être activé sur les dépenses ?

    > [!NOTE]
    > Lorsque vous planifiez la comptabilité, si vous décidez d'appliquer la taxe de vente américaine et d'utiliser des règles fiscales, vous ne pouvez pas activer le recouvrement fiscal sur les dépenses. (Pour appliquer la taxe de vente américaine et utiliser de règles fiscales, définissez l'option **Appliquer les règles de taxe** sur **Oui** .)

## <a name="policies"></a>Stratégies

En créant des politiques de notes de frais, vous pouvez aider votre organisation à économiser du temps et de l'argent lorsque les employés engagent des dépenses en son nom. Les politiques aident à garantir que les employés respectent leur budget, fournissent toutes les informations requises et dépensent de l'argent uniquement lorsqu'ils en ont besoin. Vous devez prendre les décisions suivantes pour chaque politique de note de frais et chaque politique d'approbation de note de frais que vous créez.

**Décisions :**

- Quel est le nom de la politique ?
- À quoi sert la politique de dépenses ?
- Si vous avez précédemment décidé d'activer les dépenses intersociétés, à quelles entreprises de votre organisation cette politique s'appliquera-t-elle ?
- Quand la politique entre-t-elle en vigueur ?
- Quand la politique expire-t-elle ?
- Quelle est la règle de la politique ?
- Quel est le résultat de la règle de la politique ?


[!INCLUDE[footer-include](../includes/footer-banner.md)]