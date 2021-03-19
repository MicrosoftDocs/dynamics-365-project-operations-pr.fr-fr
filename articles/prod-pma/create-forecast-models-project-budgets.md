---
title: Créer des modèles de prévision pour les budgets de projet
description: Cette rubrique décrit comment créer un modèle de prévision pour les budgets restants.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
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
ms.openlocfilehash: 5a3b9d3c154a85b50536a67ae0eb45d9b4f25f15
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271035"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="b5671-103">Créer des modèles de prévision pour les budgets de projet</span><span class="sxs-lookup"><span data-stu-id="b5671-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5671-104">Cette rubrique décrit comment créer un modèle de prévision pour les budgets restants.</span><span class="sxs-lookup"><span data-stu-id="b5671-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="b5671-105">Un projet soumis au contrôle budgétaire utilise deux types de budget : d'origine et restant.</span><span class="sxs-lookup"><span data-stu-id="b5671-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="b5671-106">Lorsque vous créez un budget de projet, vous devez spécifier les modèles de prévisions budgétaires d'origine et restants qui ont été créés dans la page **Modèles de prévision**.</span><span class="sxs-lookup"><span data-stu-id="b5671-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="b5671-107">Les budgets de projet basés sur les modèles spécifiés sont créés lorsque vous engagez le budget de projet.</span><span class="sxs-lookup"><span data-stu-id="b5671-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="b5671-108">Un modèle de prévision utilisé pour le contrôle budgétaire ne peut pas avoir de sous-modèle ou être utilisé comme sous-modèle.</span><span class="sxs-lookup"><span data-stu-id="b5671-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="b5671-109">Sélectionnez **Gestion et comptabilité des projets** > **Configurer** > **Prévisions**  > **Modèles de prévision**.</span><span class="sxs-lookup"><span data-stu-id="b5671-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="b5671-110">Sélectionnez **Nouveau** pour créer un nouveau modèle de prévision, puis entrez un numéro d'identification de modèle et un nom pour le nouveau modèle.</span><span class="sxs-lookup"><span data-stu-id="b5671-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="b5671-111">Définissez l'option **Arrêté** sur **Oui** pour empêcher toute modification des lignes de prévision du modèle de prévision.</span><span class="sxs-lookup"><span data-stu-id="b5671-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="b5671-112">Si les lignes de prévision auxquelles le modèle est associé doivent générer des prévisions de flux de trésorerie dans la comptabilité, définissez **Inclure dans les prévisions de flux de trésorerie** sur **Oui.**</span><span class="sxs-lookup"><span data-stu-id="b5671-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="b5671-113">Pour utiliser la date du projet comme date de facturation, définissez **Date de facturation prévue** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="b5671-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="b5671-114">Dans le champ **Type de budget**, sélectionnez les types de modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="b5671-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="b5671-115">**Budget d'origine** : Utilisez les montants budgétaires d'origine engagés lors de la création et de l'approbation du budget initial.</span><span class="sxs-lookup"><span data-stu-id="b5671-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="b5671-116">**Budget qui reste** : Utilisez les montants budgétaires restants pendant la durée de vie du projet.</span><span class="sxs-lookup"><span data-stu-id="b5671-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="b5671-117">Les soldes de ce modèle de prévision sont réduits par les transactions réelles et augmentés ou diminués par les révisions budgétaires.</span><span class="sxs-lookup"><span data-stu-id="b5671-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="b5671-118">**Report** : Utilisez les montants du budget reporté pour le projet.</span><span class="sxs-lookup"><span data-stu-id="b5671-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="b5671-119">Le report est un processus facultatif qui peut être exécuté pour transférer des montants budgétaires inutilisés d'un exercice à un autre.</span><span class="sxs-lookup"><span data-stu-id="b5671-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="b5671-120">Définissez les options suivantes comme requis :</span><span class="sxs-lookup"><span data-stu-id="b5671-120">Set the following options as required:</span></span>

   - <span data-ttu-id="b5671-121">Activez **Date de facturation prévue** pour utiliser la date du projet comme date de facturation.</span><span class="sxs-lookup"><span data-stu-id="b5671-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="b5671-122">Activez **Prévisions avec WIP** pour prévoir en fonction des travaux en cours (WIP), puis sélectionnez le type de WIP.</span><span class="sxs-lookup"><span data-stu-id="b5671-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="b5671-123">Vous pouvez conserver la valeur par défaut **Type de budget** comme **Aucun** ou entrez un nouveau type.</span><span class="sxs-lookup"><span data-stu-id="b5671-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="b5671-124">Le type de budget ne peut pas être modifié une fois que vous avez modifié un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="b5671-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="b5671-125">Si vous modifiez le type de budget par défaut, toutes les autres options ne seront plus disponibles pour les mises à jour et vous ne pourrez pas réutiliser ce modèle de prévision.</span><span class="sxs-lookup"><span data-stu-id="b5671-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]