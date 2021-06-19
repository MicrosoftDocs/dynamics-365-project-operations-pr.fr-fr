---
title: Projeter les commandes client pour les projets temps et matériels
description: Cette rubrique explique comment créer des commandes client basées sur des projets pour des projets de temps et matériels.
author: Yowelle
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: dec9bc700d18f71ec7c9e976b38cb8cbb41f21b5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009658"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="161fe-103">Projeter les commandes client pour les projets temps et matériels</span><span class="sxs-lookup"><span data-stu-id="161fe-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="161fe-104">Cette rubrique décrit comment créer une commande client pour un projet.</span><span class="sxs-lookup"><span data-stu-id="161fe-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="161fe-105">Les commandes client ne peuvent être créées que pour des projets de type **temps et matériel**.</span><span class="sxs-lookup"><span data-stu-id="161fe-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="161fe-106">Si un projet temporel et matériel a plusieurs sources de financement sur le contrat de projet, vous devez activer le paramètre **Autoriser les commandes client pour des projets avec plusieurs sources de financement** sur la page **Gestion de projet et comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="161fe-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="161fe-107">La prise en charge des commandes client de projet avec plusieurs sources de financement est disponible à partir de la version 10.0.2 de l’application.</span><span class="sxs-lookup"><span data-stu-id="161fe-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="161fe-108">Le paramètre permettant d’activer la prise en charge des commandes client de projet avec plusieurs sources de financement sera supprimé dans la vague de publication d’avril 2020, après quoi la fonctionnalité sera toujours activée.</span><span class="sxs-lookup"><span data-stu-id="161fe-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="161fe-109">Vous pouvez créer des commandes client basées sur un projet de deux manières :</span><span class="sxs-lookup"><span data-stu-id="161fe-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="161fe-110">Accédez au projet lui-même.</span><span class="sxs-lookup"><span data-stu-id="161fe-110">Go to the project itself.</span></span> <span data-ttu-id="161fe-111">Dans le volet Actions, sélectionnez **Gérer > Tâches d’article > Commande client**.</span><span class="sxs-lookup"><span data-stu-id="161fe-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="161fe-112">Les informations sur le projet seront par défaut la commande client du projet.</span><span class="sxs-lookup"><span data-stu-id="161fe-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="161fe-113">Si le contrat de projet a plus d’une source de financement, vous devrez sélectionner la source de financement pour définir le client pour la commande client.</span><span class="sxs-lookup"><span data-stu-id="161fe-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="161fe-114">S’il n’y a qu’une seule source de financement pour le projet, le client sera automatiquement défini.</span><span class="sxs-lookup"><span data-stu-id="161fe-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="161fe-115">Accédez à la page de la liste **Toute commande client** et créez une nouvelle commande client.</span><span class="sxs-lookup"><span data-stu-id="161fe-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="161fe-116">Vous devrez sélectionner le projet pour la commande client.</span><span class="sxs-lookup"><span data-stu-id="161fe-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="161fe-117">Une fois le projet sélectionné, le client sera défini à partir de la source de financement ou vous devrez sélectionner la source de financement si le contrat de projet comporte plusieurs sources de financement.</span><span class="sxs-lookup"><span data-stu-id="161fe-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]