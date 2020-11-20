---
title: Estimations de dépenses
description: Cette rubrique fournit des informations sur la définition ou l’estimation des dépenses liées au projet.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 10872366453985561bda0c07e50cff7f5f6d333e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131700"
---
# <a name="expense-estimates"></a><span data-ttu-id="65166-103">Estimations de dépenses</span><span class="sxs-lookup"><span data-stu-id="65166-103">Expense estimates</span></span>
<span data-ttu-id="65166-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="65166-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="65166-105">En plus de définir des estimations basées sur les ressources, Dynamics 365 Project Operations permet aux chefs de projet de définir les dépenses basées sur les projets pour chaque projet.</span><span class="sxs-lookup"><span data-stu-id="65166-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="65166-106">Chaque élément de dépense peut être associé à une tâche de projet ou à une catégorie de dépenses spécifique.</span><span class="sxs-lookup"><span data-stu-id="65166-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="65166-107">Les catégories de dépenses sont généralement définies au niveau de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="65166-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="65166-108">La tarification de chaque catégorie de dépenses est généralement définie dans la hiérarchie suivante :</span><span class="sxs-lookup"><span data-stu-id="65166-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="65166-109">Organisation</span><span class="sxs-lookup"><span data-stu-id="65166-109">Organization</span></span>
- <span data-ttu-id="65166-110">Client</span><span class="sxs-lookup"><span data-stu-id="65166-110">Customer</span></span>
- <span data-ttu-id="65166-111">Devis/contrat</span><span class="sxs-lookup"><span data-stu-id="65166-111">Quote/contract</span></span>

<span data-ttu-id="65166-112">Effectuez les étapes suivantes pour afficher, ajouter ou supprimer une dépense de projet.</span><span class="sxs-lookup"><span data-stu-id="65166-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="65166-113">Accédez à **Projets** et sélectionnez le projet auquel vous souhaitez travailler.</span><span class="sxs-lookup"><span data-stu-id="65166-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="65166-114">Sélectionnez l’onglet **Estimations du projet** et affichez la liste des dépenses du projet.</span><span class="sxs-lookup"><span data-stu-id="65166-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="65166-115">Sélectionnez **Nouvelle dépense** pour ajouter une dépense.</span><span class="sxs-lookup"><span data-stu-id="65166-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="65166-116">Sinon, sélectionnez une dépense à supprimer, puis sélectionnez **Supprimer la dépense**.</span><span class="sxs-lookup"><span data-stu-id="65166-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="65166-117">Les attributs suivants sont définis pour chaque poste de dépense :</span><span class="sxs-lookup"><span data-stu-id="65166-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="65166-118">**Catégorie** : Groupements communs utilisés pour décrire toutes les dépenses engagées sur un projet.</span><span class="sxs-lookup"><span data-stu-id="65166-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="65166-119">**Date de début** : Date à laquelle la dépense devrait être engagée.</span><span class="sxs-lookup"><span data-stu-id="65166-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="65166-120">**Quantité** : Nombre estimé de postes de dépenses pour une catégorie spécifique.</span><span class="sxs-lookup"><span data-stu-id="65166-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="65166-121">**Prix de revient unitaire** : Prix unitaire utilisé pour calculer le coût de la dépense.</span><span class="sxs-lookup"><span data-stu-id="65166-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="65166-122">**Prix de vente unitaire** : Prix unitaire utilisé pour calculer le prix de vente de la dépense.</span><span class="sxs-lookup"><span data-stu-id="65166-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

