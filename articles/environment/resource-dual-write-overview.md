---
title: Intégration à double écriture Project Operations
description: Cette rubrique offre une vue d’ensemble de l’intégration à double écriture Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955655"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="fed0f-103">Vue d’ensemble Intégration à double écriture Project Operations</span><span class="sxs-lookup"><span data-stu-id="fed0f-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="fed0f-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="fed0f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fed0f-105">Project Operations utilise des [fonctionnalités de double écriture](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) pour synchroniser les données sur Microsoft Dataverse et Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="fed0f-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="fed0f-106">L’illustration suivante montre comment les données sont synchronisées dans le cadre de cette intégration entre Dataverse et Finance.</span><span class="sxs-lookup"><span data-stu-id="fed0f-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Vue d’ensemble des flux de données Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="fed0f-108">Project Operations sur Dataverse fournit une interface utilisateur moderne et une extensibilité sans code/low-code facile à l’aide de fonctionnalités Power Platform.</span><span class="sxs-lookup"><span data-stu-id="fed0f-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="fed0f-109">Les chefs de projet, les gestionnaires de ressources, les membres de l’équipe de projet et d’autres collaborateurs en front-office effectuent leurs activités dans Project Operations sur Dataverse.</span><span class="sxs-lookup"><span data-stu-id="fed0f-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="fed0f-110">Project Operations dans Finance fournit un support à la comptabilité de projet et à la constatation du produit.</span><span class="sxs-lookup"><span data-stu-id="fed0f-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="fed0f-111">Project Operations se connecte au cadre financier de Finance pour le calcul de la taxe de vente, les taux de change des devises, les rapports sur les dimensions financières, etc.</span><span class="sxs-lookup"><span data-stu-id="fed0f-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="fed0f-112">Les expériences des comptables de projet sont principalement basées dans Finance.</span><span class="sxs-lookup"><span data-stu-id="fed0f-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="fed0f-113">L’intégration Project Operations comprend l’intégration des composants suivants :</span><span class="sxs-lookup"><span data-stu-id="fed0f-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="fed0f-114">Intégration des données de configuration et d’installation Project Operations</span><span class="sxs-lookup"><span data-stu-id="fed0f-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="fed0f-115">Estimations et chiffres réels de projet</span><span class="sxs-lookup"><span data-stu-id="fed0f-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="fed0f-116">Factures de projet</span><span class="sxs-lookup"><span data-stu-id="fed0f-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="fed0f-117">Gestion des dépenses</span><span class="sxs-lookup"><span data-stu-id="fed0f-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="fed0f-118">Facture fournisseur</span><span class="sxs-lookup"><span data-stu-id="fed0f-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)