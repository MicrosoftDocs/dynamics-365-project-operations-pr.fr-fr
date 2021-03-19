---
title: Dépenses intersociétés
description: Cette rubrique fournit des informations sur l'utilisation des dépenses intersociétés pour affecter les dépenses du collaborateur à l’entité juridique pour laquelle le travail a été effectué.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271530"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="73971-103">Dépenses intersociétés</span><span class="sxs-lookup"><span data-stu-id="73971-103">Intercompany expenses</span></span>

<span data-ttu-id="73971-104">Un collaborateur employé par une entité juridique d’une organisation peut effectuer du travail pour une autre entité juridique de la même organisation.</span><span class="sxs-lookup"><span data-stu-id="73971-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="73971-105">Vous pouvez utiliser les dépenses intersociétés pour affecter les dépenses du collaborateur à l’entité juridique pour laquelle le travail a été effectué.</span><span class="sxs-lookup"><span data-stu-id="73971-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="73971-106">L'entité juridique qui emploie le travailleur s'appelle l'entité juridique prêteuse.</span><span class="sxs-lookup"><span data-stu-id="73971-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="73971-107">L'entité juridique pour laquelle le travailleur engage des dépenses est appelée l'entité juridique emprunteuse.</span><span class="sxs-lookup"><span data-stu-id="73971-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="73971-108">Avant qu'un collaborateur puisse créer et soumettre des dépenses intersociétés, vous devez activer les lignes de dépenses intersociétés.</span><span class="sxs-lookup"><span data-stu-id="73971-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="73971-109">Dans l'entité juridique prêteuse, sur la page **Paramètres de gestion des dépenses**, sélectionnez **Autoriser les lignes de dépenses intersociétés**.</span><span class="sxs-lookup"><span data-stu-id="73971-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="73971-110">Écriture fiscale pour les dépenses intersociétés</span><span class="sxs-lookup"><span data-stu-id="73971-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="73971-111">Avant de pouvoir utiliser des groupes taxe associés à l’entité juridique (source) prêteuse au lieu de l’entité juridique (destination) emprunteuse dans votre note de frais, vous devez activer la fonctionnalité dans le Paramètres de taxe comptabilité.</span><span class="sxs-lookup"><span data-stu-id="73971-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="73971-112">Lorsque le paramètre **Entité juridique pour la validation des taxes intersociétés** est défini sur **Source** et que le champ **Appliquer les règles de taxe** est défini sur **Non**, la combinaison fiscale de l’entité juridique prêteuse est utilisée.</span><span class="sxs-lookup"><span data-stu-id="73971-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="73971-113">Lorsque le même paramètre est défini sur **Destination**, la combinaison fiscale pour la personne morale emprunteuse sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="73971-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="73971-114">Pour les personnes morales aux États-Unis, lorsque le paramètre est défini sur **Source**, le champ **Taxe déductible** doit également être configuré sur la page **Groupes de validations dans la comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="73971-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="73971-115">Le moteur de comptabilité utilisera les informations de ce champ pour la saisie comptable liée aux taxes.</span><span class="sxs-lookup"><span data-stu-id="73971-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="73971-116">Le comportement est cohérent pour les lignes de dépenses validées avec ou sans projet.</span><span class="sxs-lookup"><span data-stu-id="73971-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]