---
title: Page d’accueil de création de rapports
description: Cette rubrique fournit des informations sur la génération de rapports dans Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom:
- dyn365-projectservice
- intro-internal
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
ms.openlocfilehash: 4e60fc8c3788f4a2997d894e79d0d510d63209dd1570d79f1c43c2814d8ab819
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998278"
---
# <a name="reporting-home-page"></a>Page d’accueil de la création de rapports

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 Project Service Automation permet aux organisations basées des projets de gérer efficacement les opérations de leur entreprise. Dans n’importe quel projet, les membres de l’équipe doivent gérer l’opportunité, le devis et planifier le travail, attribuer des ressources aux projets, gérer le travail en fonction du plan, facturer le travail, puis effectuer le travail pour réaliser le projet. La possibilité de générer des rapports sur les opérations est essentiel pour déterminer l’intégrité de l’organisation et prendre des mesures correctives nécessaires. PSA utilise les méthodes et technologies de génération de rapports de Microsoft Dynamics 365 pour toute sa génération de rapports. Pour plus d’informations sur les options de création de rapports, consultez le [Guide de création de rapports pour Dynamics 365 Customer Engagement (on-premises), version 9](/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).

## <a name="report-wizard"></a>Assistant Rapport

L’Assistant Rapport permet aux non développeurs de créer des rapports simples. Étant donné que l’application est générée sur une plateforme existante, l’expérience est identique à celle documentée dans [Créer ou modifier un rapport à l’aide de l’Assistant Rapport](/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard). Toutefois, vous utiliserez les entités spécifiques à Project Service Automation.

## <a name="custom-sql-server-reporting-services-reports"></a>Rapports SQL Server Reporting Services personnalisés

Si votre entreprise nécessite un rapport spécifique qui ne peut pas être créé à l’aide de l’Assistant Rapport, vous pouvez créer un rapport personnalisé. Vous devez avoir installé Microsoft Visual Studio, ainsi que Microsoft SQL Server Data Tools et Extensions de création de rapports. Pour plus d’informations sur les outils et les versions, voir [Environnement de rédaction de rapports à l’aide de SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools). Pour plus d’informations sur la création d’un rapport personnalisé, voir [Créer un rapport à l’aide de SQL Server Data Tools](/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).

## <a name="power-bi-insights-apps"></a>Applications Power BI Insights

Ensemble, Microsoft Power BI et Dynamics 365 vous offrent la possibilité d’utiliser les données, sous la forme d’applications d’informations. Pour plus d’informations sur la disponibilité des applications d’informations, voir [Page Applications Power BI Insights](https://powerbi.microsoft.com/power-bi-insights-apps/).


## <a name="additional-resources"></a>Ressources complémentaires
Pour plus d’informations sur la génération de rapports dans PSA, consultez les rubriques suivantes :

- [Utilisation des modèles de données Project Service](reports-working-project-service-data-model.md)
- [Tableaux de bord](reports-dashboards.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]