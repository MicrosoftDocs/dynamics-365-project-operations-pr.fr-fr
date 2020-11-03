---
title: Transférer les budgets de projet à la fin de l’exercice comptable
description: Cet article fournit des informations sur la façon de transférer les montants budgétaires restants vers les années futures et de créer les détails du registre budgétaire.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26e013ab99e9a0aeafe25916715ce0ee024df3f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075873"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a>Transférer les budgets de projet à la fin de l’exercice comptable

[!include [banner](../includes/banner.md)]

Lorsque vous travaillez sur un projet pluriannuel, vous pouvez avoir un budget restant à la fin de l'exercice. Vous pouvez transférer les montants budgétaires restants vers une année future et créer des détails de registre budgétaire pour les montants dans les comptes généraux associés. Avant de reporter les montants restants, examinez et analysez les montants budgétaires restants.

## <a name="review-and-analyze-remaining-budget-amounts"></a>Examiner et analyser les montants budgétaires restants

Effectuez les étapes suivantes pour examiner les montants budgétaires de fin d'exercice des projets, mais ne reportez pas les montants.

1. Accédez à **Gestion de projet et comptabilité** > **Périodique** > **Budgets** > **Reporter des budgets**. 
2. Sur la page **Processus de report du budget du projet** , dans l'onglet **Options de fin d'exercice** , vérifiez que **Reporter les montants budgétaires restants du projet** n'est pas activé.
3. Dans l'onglet **Paramètres** , dans le champ **Année budgétaire du projet** , sélectionnez l'exercice pour lequel vous souhaitez afficher le montant budgétaire restant. 
4. Dans le champ **Ouverture de l'exercice** , sélectionnez l'exercice pour lequel vous souhaitez afficher le montant budgétaire restant. 
5. Dans le champ **À partir du modèle de prévision** , sélectionnez **Budget restant**. 
6. Pour inclure les projets qui répondent aux critères sélectionnés et qui n'ont pas de budget restant, sélectionnez **Afficher zéro en tant que montant restant**.  
7. Dans l'onglet **Sélectionner les budgets** , sélectionnez **Récupérer tous les budgets** pour charger tous les budgets correspondant aux critères sélectionnés, puis sélectionnez **Traiter**. 
8. Pour concevoir une requête de base de données qui charge un ensemble spécifique de budgets dans le volet, sélectionnez **Récupérer les budgets sélectionnés**.

Pour plus d'informations sur une ligne spécifique du volet, sélectionnez la ligne, puis sélectionnez **Afficher les détails budgétaires** ou **Afficher les comptes**.

## <a name="carry-forward-remaining-budget-amounts"></a>Reporter les montants budgétaires restants 

Lorsque vous traitez les montants budgétaires restants, vous pouvez créer des transactions dans la comptabilité pour les montants que vous reportez. Pour créer des écritures comptables, suivez les étapes de la section [Reporter les montants budgétaires et créer des écritures comptables](#carry-forward). 

> [!NOTE]
> Les montants budgétaires reportés sont transférés vers le modèle de prévision sélectionné dans la page **Modèles de prévision** comme modèle de prévision de report.  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a>Reporter les montants budgétaires et créer des écritures comptables

1.  Sélectionnez **Gestion de projet et comptabilité** > **Périodique** > **Budgets** > **Reporter des budgets**. 
2. Sur la page **Processus de report du budget du projet** , sélectionnez **Fin d'exercice** , puis activez **Reporter les montants budgétaires restants du projet** et **Créer des écritures de registre budgétaire dans la comptabilité**. 
3. Dans l'onglet **Paramètres** , dans le groupe de champs **Paramètres du projet** , sélectionnez les éléments suivants :

   - **Année budgétaire du projet**  : sélectionnez le début de l'exercice pour lequel vous souhaitez afficher les montants budgétaires restants. 
   - **Compte de résultat**  : Créez des transactions de compte de résultat dans la comptabilité. 
   -  **TEC**  : Créez des transactions Travail en cours (TEC) dans la comptabilité.
   -  **Paie**  : Créez des transactions de répartition de la paie dans la comptabilité. 

5. Dans le groupe de champs **Comptabilité** , renseignez les informations suivantes : 

   - Dans le champ **Ouverture de l'exercice** , sélectionnez l'exercice vers lequel vous souhaitez transférer les montants budgétaires restants pour les projets. La valeur par défaut est un an après la valeur du champ **Année budgétaire du projet**.
   -  Dans le champ **Période de report** , sélectionnez la période pour laquelle vous souhaitez créer les détails du registre budgétaire dans la comptabilité. Il s'agit généralement de la première période de l'ouverture de l'exercice.

6. Dans le groupe de champs **Copier de/vers** , renseignez les informations suivantes :

   - Dans le champ **À partir du modèle de prévision** , sélectionnez le modèle de prévision budgétaire du projet associé aux montants budgétaires restants que vous souhaitez transférer pour les projets. 
   - Dans le champ **Vers le modèle de budget comptable** , sélectionnez le modèle de budget comptable associé aux montants budgétaires que vous souhaitez transférer vers la comptabilité. 
   -  Sélectionnez **Transférer la devise de vente** pour utiliser la devise de vente du projet pour les écritures comptables créées lorsque vous transférez les montants budgétaires des projets. Lorsque l'option n'est pas sélectionnée, les écritures utilisent la devise comptable. 
   -  Sélectionner **Afficher zéro en tant que montant restant** pour inclure les projets qui n'ont aucun montant budgétaire restant, mais qui répondent aux autres critères que vous sélectionnez dans les projets affichés dans le volet inférieur.

7. Dans l'onglet **Sélectionner les budgets** , sélectionnez **Récupérer tous les budgets** pour charger tous les budgets correspondant aux critères sélectionnés. Si vous préférez concevoir une requête de base de données qui charge un ensemble spécifique de budgets de projet dans le volet, sélectionnez **Récupérer les budgets sélectionnés**.
8. Pour chaque projet que vous souhaitez traiter, sélectionnez l'option au début de la ligne du projet.

    > [!TIP]
    > Pour sélectionner tous ou la plupart des projets, cochez la case dans le coin supérieur gauche. Pour exclure le traitement d'un projet, décochez la case correspondant à ce projet.

9. Pour transférer les montants budgétaires restants pour les projets sélectionnés vers le exercice sélectionné et créer les détails du registre budgétaire dans la comptabilité, sélectionnez **Traiter**.

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a>Reporter les montants budgétaires sans créer d'écritures comptables

1. Accédez à **Gestion de projet et comptabilité** > **Périodique** > **Budgets** > **Reporter des budgets**.
2. Sur la page **Processus de report du budget du projet** , dans le champ **Options de fin d'exercice** , sélectionnez **Reporter les montants budgétaires restants du projet**.
3. Dans le groupe **Paramètres** , dans le champ **Année budgétaire du projet** , sélectionnez l'exercice pour lequel vous souhaitez afficher les montants budgétaires restants.
4. Dans le groupe **Copier de/vers** , renseignez les informations suivantes :

   - Dans le champ **À partir du modèle de prévision** , sélectionnez le modèle de prévision budgétaire du projet associé aux montants budgétaires restants que vous souhaitez transférer pour les projets. 
   - Sélectionnez **Afficher zéro en tant que montant restant** pour inclure les projets qui n'ont pas de montant budgétaire restant, mais qui répondent aux critères sélectionnés.
   - Dans le groupe **Sélectionner les budgets** , sélectionnez **Récupérer tous les budgets** pour charger tous les budgets correspondant aux critères sélectionnés. Pour concevoir une requête de base de données qui charge un ensemble spécifique de budgets de projet dans le volet, sélectionnez **Récupérer les budgets sélectionnés**.

5. Pour chaque projet que vous souhaitez traiter, sélectionnez l'option au début de la ligne du projet. 
6. Sélectionnez **Traiter** pour transférer les montants budgétaires restants pour les projets sélectionnés vers le exercice sélectionné.

