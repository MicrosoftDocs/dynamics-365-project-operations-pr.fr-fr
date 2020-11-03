---
title: Configurer les coûts standard pour la main-d’œuvre et les dépenses
description: Cette rubrique explique comment configurer les coûts standard de la main-d’œuvre et les dépenses pour un projet.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075797"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>Configurer les coûts standard pour la main-d’œuvre et les dépenses

[!include [banner](../../includes/banner.md)]

Cette rubrique explique comment configurer les coûts standard de la main-d’œuvre et les dépenses pour un projet. Cette tâche utilise le jeu de données USSI.

1. Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de revient (heure)**.
2. Cliquez sur **Nouveau**.
3. Dans le champ **Date effective** , saisissez une date.
4. Dans le champ **Prix de revient** , saisissez un numéro. Vous pouvez définir un prix de revient standard pour la catégorie de projet, ou vous pouvez définir un prix de revient par numéro d’employé, numéro de projet, catégorie, date ou toute combinaison de ces éléments. Le prix de revient appliqué correspond au prix de revient avec le plus haut niveau de détail.  
5. Sélectionnez **Enregistrer**.
6. Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de vente (heure)**.
7. Cliquez sur **Nouveau**.
8. Dans le champ **Date effective** , saisissez une date.
9. Dans le champ **Valide pour** , sélectionnez une option.
10. Dans le champ **Tarification** , saisissez un nombre. Vous pouvez configurer un prix de vente standard pour les transactions horaires ou pour une catégorie de projet. Vous pouvez également configurer les prix de vente par numéro d’employé, numéro de projet, catégorie, date de transaction ou toute combinaison de ces éléments. Le prix de vente réel, qui est appliqué lorsqu’un employé entre une transaction dans le journal des heures, correspond au prix de vente avec le niveau de détail le plus élevé. Par exemple, si un prix de vente général et un prix de vente spécifique à l’employé sont définis, le prix de vente spécifique à l’employé est utilisé.  
11. Sélectionnez **Enregistrer**.
12. Fermez la page.
13. Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de revient (dépense)**.
14. Cliquez sur **Nouveau**.
15. Dans le champ **Date effective** , saisissez une date.
16. Dans le champ **Prix de revient** , saisissez un numéro. Plusieurs champs peuvent être remplis, mais il s’agit là des champs minimum nécessaires pour enregistrer l’enregistrement.  
17. Sélectionnez **Enregistrer**.
18. Dans le volet de navigation, accédez à **Modules > Gestion de projets et comptabilité > Configuration > Prix > Prix de vente (dépense)**.
19. Cliquez sur **Nouveau**.
20. Dans le champ **Date effective** , saisissez une date.
21. Dans le champ **Valide pour** , sélectionnez une option.
22. Dans le champ **Tarification** , saisissez un nombre. Le prix de vente réel, qui est appliqué lorsqu’un employé saisit des transactions dans le journal des dépenses, correspond au prix de vente avec le niveau de détail le plus élevé. Par exemple, si un prix de vente général et un prix de vente spécifique à l’employé sont définis, le prix de vente spécifique à l’employé est utilisé.  
23. Sélectionnez **Enregistrer**.

