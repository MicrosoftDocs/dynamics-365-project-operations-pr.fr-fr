---
title: Demande de Programme des dépenses des subventions fédérales
description: Cette rubrique fournit des informations sur la demande de programme des dépenses de subventions fédérales.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010063"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Demande de Programme des dépenses des subventions fédérales

[!include [banner](../includes/banner.md)]

Conformément à la circulaire A-133 du Bureau de la gestion et du budget (service du gouvernement américain), les organismes qui reçoivent des fonds fédéraux sont soumis à des obligations d’audit, également appelés audits uniques. Le processus de vérification sert à rendre compte des revenus et des dépenses des subventions fédérales de façon récurrente. Une partie du rapport d’audit unique comprend le Programme des dépenses des subventions fédérales (SEFA).

Le Programme des dépenses des subventions fédérales comprend le titre et le numéro du Catalogue d’assistance nationale fédérale (CFDA), le numéro de la subvention, l’année de la subvention, le nom de l’organisme fédéral fournissant les fonds et le nom de l’entité intermédiaire. La demande s’applique à une période déterminée. En règle générale, cette période est la même que la période des états financiers, c’est-à-dire un exercice.

La demande inclut les subventions dont les dates de projection se situent dans la plage de dates sélectionnée. La colonne **Organisme donateur** de la demande montre le client de la subvention ou, dans le cas d’une subvention intermédiaire, l’organisme donateur. Pour une subvention intermédiaire, la colonne **Organisme intermédiaire** affiche le client de la subvention. Si la subvention n’est pas une subvention intermédiaire, la colonne **Organisme intermédiaire** est vide.

## <a name="set-up-the-cfda-clusters"></a>Configurer les clusters CFDA

Vous devez configurer les clusters CFDA qui peuvent être associés à des numéros CFDA dans la demande de Programme des dépenses des subventions fédérales.

1. Accédez à **Gestion de projet et comptabilité \> Configurer \> Subventions \> Clusters du Catalogue d’assistance nationale fédérale**.
2. Sélectionnez **Nouveau** pour créer un cluster CFDA.
3. Entrez le nom du cluster.
4. Sélectionnez **Enregistrer** pour appliquer vos modifications.

## <a name="set-up-cfda-numbers"></a>Configurer les numéros CFDA

Vous devez configurer les numéros CFDA qui peuvent être ajoutés à des subventions et inclus dans la demande de Programme des dépenses des subventions fédérales.

1. Accédez à **Gestion de projet et comptabilité \> Configurer \> Subventions \> Numéros du Catalogue d’assistance nationale fédérale (CFDA)**.
2. Sélectionnez **Nouveau** pour créer un numéro CFDA.
3. Dans la colonne **Numéro**, entrez le numéro CFDA.
4. Appuyez sur la touche **Tabulation**.
5. Dans la colonne **Description**, tapez le titre CFDA.
6. Appuyez sur la touche **Tabulation**.
7. Facultatif : dans le champ **Cluster du programme**, ajoutez le cluster CFDA approprié.
8. Sélectionnez **Enregistrer** pour appliquer vos modifications.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Mettre en place des subventions à déclarer pour la demande de Programme des dépenses des subventions fédérales

1. Accédez à **Gestion de projet et comptabilité \> Subventions \> Subventions** et sélectionnez une subvention existante.
2. Sur le raccourci **Configurer**, dans le champ **Catalogue d’assistance nationale fédérale (CFDA)**, attribuez le numéro CFDA. Le numéro CFDA sur la subvention détermine le cluster CFDA pour le rapport.
3. Sur le raccourci **Informations de contact**, entrez les informations relatives au donateur en procédant comme suit :

    1. Dans le champ **Client subventionné**, saisissez le client responsable de la subvention. Pour une subvention existante, ces informations peuvent déjà être saisies.
    2. Indiquez si le client subventionné est le donateur. Si le client subventionné est le donateur, ne cochez pas la case **Intermédiaire**. Si un autre client est le donateur et que le client subventionné est responsable des dépenses et du suivi de l’argent, cochez la case **Intermédiaire**.

4. Si vous avez coché la case **Intermédiaire** à l’étape précédente, dans le champ **Organisme donateur**, entrez le client qui a fourni la subvention. L’organisme donateur et le client de la subvention ne peuvent pas être le même client.

Voici un exemple de subvention avec intermédiaire :

Le gouvernement fédéral a financé un projet d’infrastructure pour un État. Le gouvernement fédéral a donné l’argent à dépenser à l’État. Dans ce cas, le gouvernement fédéral est l’organisme donateur et l’État est le client subventionné.

> [!NOTE] 
> Lorsque vous activez la fonction pour la première fois, les numéros CFDA initiaux seront renseignés avec les numéros existants sur les subventions.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Exclure les subventions des rapports SEFA en fonction du type de subvention

1. Accédez à **Gestion de projet et comptabilité \> Configurer \> Subventions \> Types de subvention**.
2. Sur le raccourci **Informations par défaut**, cochez la case **Exclure du Programme des dépenses des subventions fédérales**.
3. Sélectionnez **Enregistrer** pour appliquer vos modifications.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Exécuter la demande de Programme des dépenses des subventions fédérales

1. Accédez à **Gestion de projet et comptabilité \> Demandes et rapports \> Demande de subvention \> Programme des dépenses des subventions fédérales**.
2. Dans la section **Paramètres**, suivez les étapes suivantes :

    1. Dans le champ **Intervalle de dates**, sélectionnez le code de l’intervalle de dates. Alternativement, dans les champs **Date de début** et **Date de fin**, définissez l’intervalle de dates.
    2. Facultatif : pour inclure uniquement les transactions facturées en tant que revenus dans la demande, définissez l’option **Inclure uniquement les revenus facturés** sur **Oui**.

## <a name="columns"></a>Colonnes

La demande de Programme des dépenses des subventions fédérales comprend les colonnes suivantes :

- Nom du cluster du Catalogue d’assistance nationale fédérale (CFDA)
- Organisme donateur
- Organisme intermédiaire
- Nom de la subvention
- ID de subvention
- ID de l’application de la subvention
- Catalogue d’assistance nationale fédérale (CFDA)
- Reçus
- Dépenses


[!INCLUDE[footer-include](../includes/footer-banner.md)]