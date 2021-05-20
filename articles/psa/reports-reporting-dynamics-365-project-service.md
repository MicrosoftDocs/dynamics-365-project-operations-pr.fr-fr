---
title: Page d’accueil de création de rapports
description: Cette rubrique fournit des informations sur la génération de rapports dans Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 32b504a862f98dac4b1d9b54289476026d988c13
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951476"
---
# <a name="reporting-home-page"></a><span data-ttu-id="41263-103">Page d’accueil de la création de rapports</span><span class="sxs-lookup"><span data-stu-id="41263-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="41263-104">Microsoft Dynamics 365 Project Service Automation permet aux organisations basées des projets de gérer efficacement les opérations de leur entreprise.</span><span class="sxs-lookup"><span data-stu-id="41263-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="41263-105">Dans n’importe quel projet, les membres de l’équipe doivent gérer l’opportunité, le devis et planifier le travail, attribuer des ressources aux projets, gérer le travail en fonction du plan, facturer le travail, puis effectuer le travail pour réaliser le projet.</span><span class="sxs-lookup"><span data-stu-id="41263-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="41263-106">La possibilité de générer des rapports sur les opérations est essentiel pour déterminer l’intégrité de l’organisation et prendre des mesures correctives nécessaires.</span><span class="sxs-lookup"><span data-stu-id="41263-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="41263-107">PSA utilise les méthodes et technologies de génération de rapports de Microsoft Dynamics 365 pour toute sa génération de rapports.</span><span class="sxs-lookup"><span data-stu-id="41263-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="41263-108">Pour plus d'informations sur les options de création de rapports, consultez le [Guide de création de rapports pour Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="41263-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="41263-109">Assistant Rapport</span><span class="sxs-lookup"><span data-stu-id="41263-109">Report Wizard</span></span>

<span data-ttu-id="41263-110">L’Assistant Rapport permet aux non développeurs de créer des rapports simples.</span><span class="sxs-lookup"><span data-stu-id="41263-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="41263-111">Étant donné que l'application est générée sur une plateforme existante, l'expérience est identique à celle documentée dans [Créer ou modifier un rapport à l'aide de l'Assistant Rapport](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="41263-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="41263-112">Toutefois, vous utiliserez les entités spécifiques à Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="41263-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="41263-113">Rapports SQL Server Reporting Services personnalisés</span><span class="sxs-lookup"><span data-stu-id="41263-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="41263-114">Si votre entreprise nécessite un rapport spécifique qui ne peut pas être créé à l’aide de l’Assistant Rapport, vous pouvez créer un rapport personnalisé.</span><span class="sxs-lookup"><span data-stu-id="41263-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="41263-115">Vous devez avoir installé Microsoft Visual Studio, ainsi que Microsoft SQL Server Data Tools et Extensions de création de rapports.</span><span class="sxs-lookup"><span data-stu-id="41263-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="41263-116">Pour plus d'informations sur les outils et les versions, voir [Environnement de rédaction de rapports à l'aide de SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="41263-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="41263-117">Pour plus d'informations sur la création d'un rapport personnalisé, voir [Créer un rapport à l'aide de SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="41263-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="41263-118">Applications Power BI Insights</span><span class="sxs-lookup"><span data-stu-id="41263-118">Power BI insights apps</span></span>

<span data-ttu-id="41263-119">Ensemble, Microsoft Power BI et Dynamics 365 vous offrent la possibilité d’utiliser les données, sous la forme d’applications d’informations.</span><span class="sxs-lookup"><span data-stu-id="41263-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="41263-120">Pour plus d’informations sur la disponibilité des applications d’informations, voir [Page Applications Power BI Insights](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="41263-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="41263-121">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="41263-121">Additional resources</span></span>
<span data-ttu-id="41263-122">Pour plus d’informations sur la génération de rapports dans PSA, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="41263-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="41263-123">Utilisation des modèles de données Project Service</span><span class="sxs-lookup"><span data-stu-id="41263-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="41263-124">Tableaux de bord</span><span class="sxs-lookup"><span data-stu-id="41263-124">Dashboards</span></span>](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]