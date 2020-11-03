---
title: Dépenses intersociétés
description: Un travailleur qui est employé par une entité juridique dans une organisation peut effectuer un travail pour une autre entité juridique de la même organisation. Dans ce cas, vous pouvez utiliser la fonction de dépense intersociétés pour affecter les dépenses du travailleur à l'entité juridique pour laquelle le travail a été effectué.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075891"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="0878e-104">Dépenses intersociétés</span><span class="sxs-lookup"><span data-stu-id="0878e-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0878e-105">Un travailleur qui est employé par une entité juridique dans une organisation peut effectuer un travail pour une autre entité juridique de la même organisation.</span><span class="sxs-lookup"><span data-stu-id="0878e-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="0878e-106">Dans ce cas, vous pouvez utiliser la fonction de dépense intersociétés pour affecter les dépenses du travailleur à l'entité juridique pour laquelle le travail a été effectué.</span><span class="sxs-lookup"><span data-stu-id="0878e-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="0878e-107">L'entité juridique qui emploie le travailleur s'appelle l'entité juridique prêteuse.</span><span class="sxs-lookup"><span data-stu-id="0878e-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="0878e-108">L'entité juridique pour laquelle le travailleur engage des dépenses est appelée l'entité juridique emprunteuse.</span><span class="sxs-lookup"><span data-stu-id="0878e-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="0878e-109">Avant qu'un travailleur puisse créer et soumettre des dépenses pour un travail effectué pour une autre entité juridique, dans l'entité juridique prêteuse, sur la page **Paramètres de gestion des dépenses** , sélectionnez l'option **Autoriser les lignes de dépenses intersociétés**.</span><span class="sxs-lookup"><span data-stu-id="0878e-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="0878e-110">Écriture fiscale pour les dépenses intersociétés</span><span class="sxs-lookup"><span data-stu-id="0878e-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0878e-111">Si vous souhaitez utiliser des groupes de taxes associés à l'entité juridique de prêt (source) au lieu de l'entité juridique emprunteuse (de destination) dans votre note de frais, vous devrez les configurer dans la configuration de la taxe de vente de la comptabilité.</span><span class="sxs-lookup"><span data-stu-id="0878e-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="0878e-112">Lorsque le paramètre de comptabilité est sélectionné, **Entité juridique pour la comptabilisation fiscale intersociétés** est défini sur **Source** et **Appliquer les règles d'imposition de la taxe de vente** est défini sur **Non** , la combinaison fiscale de la personne morale prêteuse sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="0878e-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="0878e-113">Lorsque le même paramètre est défini sur **Destination** , la combinaison fiscale pour la personne morale emprunteuse sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="0878e-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="0878e-114">Pour les personnes morales aux États-Unis, lorsque le paramètre est défini sur **Source** , le champ **Taxe déductible** doit également être configuré sur la page **Groupes de validations dans la comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="0878e-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="0878e-115">Le moteur de comptabilité utilisera les informations de ce champ pour la saisie comptable liée aux taxes.</span><span class="sxs-lookup"><span data-stu-id="0878e-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="0878e-116">Le comportement est cohérent pour les lignes de dépenses validées avec ou sans projet.</span><span class="sxs-lookup"><span data-stu-id="0878e-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
