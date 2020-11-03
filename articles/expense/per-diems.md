---
title: Indemnités quotidiennes
description: Cette rubrique fournit des informations sur les règles d’indemnités journalières utilisées dans la gestion des dépenses.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075614"
---
# <a name="per-diems"></a><span data-ttu-id="5df47-103">Indemnités quotidiennes</span><span class="sxs-lookup"><span data-stu-id="5df47-103">Per diems</span></span>

<span data-ttu-id="5df47-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="5df47-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="5df47-105">Une indemnité journalière est une allocation versée à un travailleur qui se déplace pour son travail.</span><span class="sxs-lookup"><span data-stu-id="5df47-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="5df47-106">Dans Gestion des dépenses, vous pouvez créer des règles d’indemnités journalières pour diverses situations de voyage.</span><span class="sxs-lookup"><span data-stu-id="5df47-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="5df47-107">Les tarifs journaliers peuvent être basés sur la période de l’année, le lieu de voyage ou les deux.</span><span class="sxs-lookup"><span data-stu-id="5df47-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="5df47-108">Lorsque vous créez une règle d’indemnité journalière, vous pouvez spécifier qu’un pourcentage du tarif journalier sera retenu si un travailleur reçoit des repas ou des services gratuits.</span><span class="sxs-lookup"><span data-stu-id="5df47-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="5df47-109">Vous pouvez également définir un nombre d’heures minimal et maximal que le taux journalier peut appliquer aux déplacements d’un travailleur.</span><span class="sxs-lookup"><span data-stu-id="5df47-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="5df47-110">configuration</span><span class="sxs-lookup"><span data-stu-id="5df47-110">Configuration</span></span> 

1. <span data-ttu-id="5df47-111">Pour ajouter des emplacements d’indemnités journalières, accédez à **Configurer** > **Calculs et codes** > **Emplacements des indemnités journalières**.</span><span class="sxs-lookup"><span data-stu-id="5df47-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="5df47-112">Pour chacun des emplacements ajoutés ci-dessus, sélectionnez un taux journalier et une devise valables entre une date de début et une date de fin spécifiques pour l’hôtel, les repas et d’autres dépenses.</span><span class="sxs-lookup"><span data-stu-id="5df47-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="5df47-113">Les taux journaliers et les devises sont configurés sous **Configurer** > **Calculs et codes** > **Indemnités journalières**.</span><span class="sxs-lookup"><span data-stu-id="5df47-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="5df47-114">Sur la page **Emplacements des indemnités journalières** , configurez les niveaux de taux journalier.</span><span class="sxs-lookup"><span data-stu-id="5df47-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="5df47-115">Les niveaux de taux journaliers vous permettent de définir le pourcentage de répartition d’une indemnité journalière pour les frais d’hôtel, de repas et autres.</span><span class="sxs-lookup"><span data-stu-id="5df47-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="5df47-116">Pour spécifier le pourcentage de réduction de repas pour le petit-déjeuner, le déjeuner ou le dîner, mettez à jour les champs de la page **Paramètres de gestion des dépenses** sur l’onglet **Indemnités journalières**.</span><span class="sxs-lookup"><span data-stu-id="5df47-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="5df47-117">Soumettre les dépenses en utilisant les indemnités journalières</span><span class="sxs-lookup"><span data-stu-id="5df47-117">Submit expenses using per diem</span></span>
<span data-ttu-id="5df47-118">Pour soumettre des dépenses utilisant des indemnités journalières, utilisez la catégorie de dépenses **Indemnités journalières** lorsque vous créez une note de frais.</span><span class="sxs-lookup"><span data-stu-id="5df47-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="5df47-119">Entrer **Indemnités journalières à partir de la date** , **Indemnités journalières à ce jour** et **Emplacement des indemnités journalières**.</span><span class="sxs-lookup"><span data-stu-id="5df47-119">Enter the **Per diem from date** , **Per diem to date** ,  and the **Per diem location**.</span></span> <span data-ttu-id="5df47-120">Le montant sera calculé en fonction des taux journaliers pour l’emplacement sélectionné et la réduction de repas sera calculée en fonction des niveaux de taux journaliers.</span><span class="sxs-lookup"><span data-stu-id="5df47-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
