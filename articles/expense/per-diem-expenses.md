---
title: Dépenses d’indemnités journalières
description: Cet article fournit des informations sur la façon d’utiliser les dépenses d’indemnités journalières.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923185"
---
# <a name="per-diem-expenses"></a>Dépenses d’indemnités journalières

> [!IMPORTANT] 
> La fonctionnalité décrite dans cet article est accessible à des utilisateurs ciblés dans le cadre d’une préversion.

Une indemnité journalière est une compensation journalière fixe et prédéterminée qu’une entreprise verse à ses employés pour l’hébergement (hôtels), les repas et les frais accessoires que ces employés encourent lors de leurs déplacements professionnels. L’entreprise verse cette indemnité aux employés au lieu de payer les frais de déplacement réels. Les employés peuvent utiliser leurs indemnités journalières **Frais accessoires/Autre** pour couvrir les pourboires, le service de chambre, les services de blanchisserie ou de nettoyage à sec pour les réunions d’affaires importantes. Le taux d’indemnités journalières peut varier selon que l’employeur choisit de rembourser les frais combinés d’hébergement et de repas, ou seulement les frais de repas et faux frais.

Les tarifs journaliers peuvent être basés sur la période de l’année, le lieu de voyage ou les deux. Lorsque vous créez une règle d’indemnités journalières, vous pouvez indiquer qu’un pourcentage du taux d’indemnité journalière est retenu si un employé bénéficie de repas ou services gratuits. Vous pouvez également définir un nombre d’heures minimum et un nombre d’heures maximum pour lequel le taux d’indemnité journalière peut être appliqué au déplacement d’un employé.

L’indemnité journalière est calculée comme l’indemnité totale offerte par jour moins la réduction liée au repas (coût des repas gratuits) offerte à l’employé.

## <a name="configure-per-diems"></a>Configurer les indemnités journalières

Pour configurer les dépenses d’indemnités journalières, procédez comme suit.

1. Accédez à **Gestion des dépenses** \> **Configuration** \> **Général** \> **Paramètres de gestion des dépenses**.
2. Sur l’onglet **Indemnités journalières**, dans l’onglet **Calculer la réduction de repas par**, sélectionnez comment les indemnités journalières doivent être calculées :

    - **Type de repas par voyage** – Calculez l’indemnité journalière en fonction du type de repas saisi (petit-déjeuner, déjeuner ou dîner) et de la réduction liée au repas spécifiée pour chaque type de repas pour l’indemnité journalière pour la durée du voyage.
    - **Type de repas par jour** – Calculez l’indemnité journalière en fonction du type de repas saisi (petit-déjeuner, déjeuner ou dîner) et de la réduction liée au repas spécifiée pour chaque type de repas pour l’indemnité journalière par jour.
    - **Nombre de repas par jour** – Calculez l’indemnité journalière en fonction du nombre de repas saisis par jour et de la réduction liée au repas pour le nombre de repas fournis chaque jour.

3. Accédez à **Gestion des dépenses** \> **Configuration** \> **Calculs et codes** \> **Emplacements des indemnités journalières**.
4. Ajoutez des emplacements où les indemnités journalières peuvent être utilisées.
5. Pour chaque lieu que vous ajoutez, sur l’onglet **Indemnités journalières**, sélectionnez le taux des indemnités journalières et la devise qui sont valables entre des dates de début et de fin spécifiques pour l’hébergement, les repas et les autres dépenses. Pour configurer les taux d’indemnités journalières et les devises, accédez à **Gestion des dépenses** \> **Configuration** \> **Calculs et codes** \> **Indemnités journalières**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Indemnités journalières dans l’interface de dépenses réinventée

La fonctionnalité d’indemnités journalières est prise en charge dans l’espace de travail **Gestion des dépenses** réinventé dans Microsoft Dynamics 365 Finance version 10.0.25 et ultérieure.

Pour activer les indemnités journalières, procédez comme suit :

1. Dans l’espace de travail **Gestion des fonctionnalités**, recherchez et sélectionnez la fonctionnalité **Notes de frais réinventées** dans la liste, puis sélectionnez **Activer maintenant**.
2. Recherchez et sélectionnez la fonctionnalité **Indemnités journalières pour l’interface réinventée des notes de frais** dans la liste, puis sélectionnez **Activer maintenant**.

## <a name="how-the-feature-works"></a>Fonctionnement de la fonctionnalité

Cette section fournit des exemples pour trois scénarios de configuration. Pour chaque exemple, le champ **Calculer la réduction de repas par** est défini sur une autre valeur. Pour les trois exemples, le montant total à payer est le même jusqu’à ce que la réduction liée au repas soit appliquée. Après ce point, le montant total à payer diffère pour chaque exemple.

Pour créer la dépense journalière utilisée pour les trois exemples, procédez comme suit.

1. Accédez à **Espaces de travail** \> **Gestion des dépenses**.
2. Sélectionnez **Nouvelle note de frais**, ou sélectionnez une note de frais existante.
3. Ajoutez une nouvelle dépense. Dans le champ **Catégorie**, sélectionnez **Indemnités journalières**. Sélectionnez le lieu et les dates de début et de fin de votre voyage. L’indemnité journalière pour l’hébergement, les repas et les faux frais (autres dépenses) est calculée en fonction de l’indemnité journalière fixée pour l’emplacement sélectionné.

    Par exemple, vous sélectionnez **Redmond (États-Unis)** comme emplacement. L’indemnité journalière pour cet emplacement est de 150 dollars américains (150 USD) pour l’hébergement, 75 USD pour les repas et 5 USD pour les frais accessoires. La date de début est le 10 janvier et la date de fin est le 14 janvier. Par conséquent, la durée sélectionnée est de cinq jours lorsque la configuration sélectionnée est en jours calendaires avec heure, et l’heure sélectionnée commence et se termine à 12h00 aux dates de début et de fin. Voici les calculs :

    - Montant total à payer = 5 × (150 + 75 + 5) = 5 × 230 = 1 150 USD
    - Repas et partie accessoire du montant total = 5 × (75 + 5) = 400 USD

Si le petit-déjeuner, le déjeuner et le dîner ont été fournis pendant le voyage, ces repas doivent être comptabilisés comme une réduction liée au repas.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Exemple 1 : Indemnités journalières où les réductions de repas sont basées sur le type de repas par voyage

Dans cet exemple, la réduction liée au repas est de 30 % pour le petit-déjeuner, 30 % pour le déjeuner et 40 % pour le dîner. Sur la page **Paramètres de gestion des dépenses**, le champ **Calculer la réduction de repas par** est défini sur **Type de repas par trajet**. Voici les calculs si trois petits-déjeuners, deux déjeuners et aucun dîner étaient fournis à l’employé :

- Réduction liée au repas = (3 ×\[ 75 × 30 %\]) + (2 ×\[ 75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Repas et faux frais = 400 – 112,50 = 287,50 USD
- Montant total à payer = Allocation totale – Réduction liée au repas = 1 150 – 112,50 = 1 037,50 USD

![Dépenses d’indemnités journalières où la réduction liée au repas est basée sur le type de repas par voyage.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Exemple 2 : Indemnités journalières où les réductions liées au repas sont basées sur le type de repas par jour

Dans cet exemple, la réduction liée au repas est de 30 % pour le petit-déjeuner, 30 % pour le déjeuner et 40 % pour le dîner. Sur la page **Paramètres de gestion des dépenses**, le champ **Calculer la réduction de repas par** est défini sur **Type de repas par jour**. Dans ce cas, dans la grille **Repas** dans la boîte de dialogue **Modifier la dépense**, décochez les cases pour indiquer quels repas vous ont été servis pendant votre voyage.

Par exemple, voici les calculs si le petit-déjeuner était fourni les trois premiers jours du voyage :

- Réduction liée au repas quotidien pour chacun des trois premiers jours = 75 × 30 % = 22,50 USD
- Réduction totale liée au repas = 3 × 22,50 = 67,50 USD
- Repas et frais accessoires des jours 1 à 3 = 75 – 22,50 = 57,50 USD
- Total des repas et frais accessoires = Somme des repas et frais accessoires sur cinq jours = 400 – 67,50 = 332,50 USD
- Montant total à payer = Montant total – Réduction liée au repas = 1 150 – 67,50 = 1 082,50 USD

![Dépenses d’indemnités journalières où la réduction liée au repas est basée sur le type de repas par jour.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Exemple 3 : Indemnités journalières où les réductions liées au repas sont basées sur le nombre de repas par jour

Dans cet exemple, la réduction liée au repas est calculée en fonction du nombre de repas fournis par jour (c’est-à-dire le champ **Calculer la réduction de repas par** sur la page **Paramètres de gestion des dépenses** est définie sur **Nombre de repas par jour**). Dans la grille **Repas** dans la boîte de dialogue **Modifier la dépense**, décochez les cases pour indiquer quels repas ont été servis.
Dans ce cas, la réduction liée au repas est basée uniquement sur le nombre de repas fournis, et non sur le type de repas (petit-déjeuner/déjeuner/dîner) fourni.

Voici le calcul des indemnités journalières lorsque l’indemnité journalière est de 150 USD pour le logement, 75 USD pour les repas et 5 USD pour les frais accessoires :

- **Montant total à payer** = 5 × (150 + 75 + 5) = 5 × 230 = 1 150 USD
- **Un repas:** Réduction liée au repas = 20 % = 15 USD
- **Deux repas:** Réduction liée au repas = 50 % = 37,50 USD
- **Trois repas:** Réduction liée au repas = 100 % = 75 USD

Voici les calculs pour la **compensation des repas et frais accessoires**, qui inclut 5 USD pour les frais accessoires :

- Jour 1 - Deux repas fournis = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Jour 2 - Deux repas fournis = (75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- Jour 3 - Un repas fourni = (75 – 15) + 5 = 60 + 5 = 65 USD
- Jour 4 - Zéro repas fourni = (75 – 0) + 5 = 75 + 5 = 80 USD
- Jour 5 - Trois repas fournis = (75 – 75) + 5 = 0 + 5 = 5 USD

- Total des repas et frais accessoires = Repas et frais accessoires pour le jour 1 + le jour 2 + le jour 3 + le jour 4 + le jour 5 = 235 USD
- Réduction totale de repas = Réduction de repas pour le Jour 1+ Jour 2 +Jour 3+Jour 4+ Jour 5= 37,5+ 37,5+ 15 + 0+ 75 = 165 USD
- Montant total à payer = Allocation totale – Réduction totale liée au repas = 1 150 – 165 = 985 USD

![Dépenses d’indemnités journalières où la réduction liée au repas est basée sur le nombre de repas par jour.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> À partir de la version 10.0.23 de Finance, si vous utilisez l’interface de dépenses revisitée, vous ne pouvez pas créer de dépenses journalières dont les dates se chevauchent. Si vous essayez, vous recevez un message d’erreur.
