---
title: Synchronisation des contrats de projet et des projets directement depuis Project Service Automation vers Finance
description: Cet article décrit le modèle et les tâches sous-jacentes utilisés pour synchroniser les contrats de projet et les projets directement depuis Microsoft Dynamics 365 Project Service Automation vers Dynamics 365 Finance.
author: Yowelle
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 62a24f3af823d474cbb4d63f8d079c708256a75e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933857"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Synchronisation des contrats de projet et des projets directement depuis Project Service Automation vers Finance 

[!include[banner](../includes/banner.md)]



Cet article décrit le modèle et les tâches sous-jacentes utilisés pour synchroniser les contrats de projet et les projets directement depuis Dynamics 365 Project Service Automation vers Dynamics 365 Finance.

> [!NOTE] 
> Si vous utilisez Enterprise Edition 7.3.0, vous devez installer KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Flux de données pour Project Service Automation vers Finance

> [!NOTE]
> Avant de pouvoir utiliser la solution d’intégration Project Service Automation vers Finance, vous devez bien connaître la fonctionnalité d’intégration de données Dynamics 365.

La solution d’intégration Project Service Automation vers Finance utilise la fonction d’intégration de données pour synchroniser les données entre les instances de Project Service Automation et Finance. Le modèle d’intégration disponible avec la fonctionnalité d’intégration de données permet le flux de données sur les contrats de projet, les projets et les lignes de contrat de projet, sans oublier les jalons de ligne de contrat de projet depuis Project Service Automation vers Finance.

L’illustration suivante montre comment les données sont synchronisées entre Project Service Automation et Finance.

[![Flux de données pour l’intégration de Project Service Automation avec Finance.](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Modèles et tâches

Pour accéder aux modèles disponibles, dans le centre d’administration Microsoft Power Apps, sélectionnez **Projets**, puis, dans le coin supérieur droit, sélectionnez **Nouveau projet** pour sélectionner des modèles publics.

Les modèles et les tâches sous-jacentes suivants sont utilisés pour synchroniser les projets de contrat et les projets de Project Service Automation vers Finance :

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Intégration avec Dynamics 365 Project Service Automation v2.x
- **Nom du modèle dans l’intégration de données :** Projets et contrats (Project Service Automation vers Finance)
- **Nom des tâches dans le projet :**

    - Contrats de projet Project Service Automation vers Finance
    - Projets Project Service Automation vers Finance
    - Lignes de contrats de projet Project Service Automation vers Finance
    - Jalons de lignes de contrats de projet Project Service Automation vers Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Intégration avec Dynamics 365 Project Service Automation v3.x
Il y a un changement de schéma dans Project Service Automation qui a un impact sur le modèle de jalon de ligne de contrat de projet et l’utilisation de la version v2 du modèle est requise pour intégrer Project Service Automation v3.x à Dynamics 365.

- **Nom du modèle dans l’intégration de données :** Projets et contrats (Project Service Automation 3.x vers Finance) – v2
- **Nom des tâches dans le projet :**

    - Contrats de projet Project Service Automation vers Finance
    - Projets Project Service Automation vers Finance
    - Lignes de contrats de projet Project Service Automation vers Finance
    - Jalons de lignes de contrats de projet Project Service Automation vers Finance

Avant que la synchronisation des contrats de projet et des projets puisse avoir lieu, vous devez synchroniser les comptes.

## <a name="entity-set"></a>Ensemble d’entités

| Project Service Automation       | Finances                                                |
|----------------------------------|--------------------------------------------------------|
| Commandes                           | Entité d’intégration pour le contrat de projet                |
| Projets                         | Entité d’intégration pour le projet                         |
| Lignes de commande                      | Entité d’intégration pour la ligne de contrat de projet           |
| Jalons de la ligne de contrat du projet | Entité d’intégration pour le jalon de ligne de contrat de projet |

## <a name="entity-flow"></a>Flux d’entité

Les contrats de projet sont gérés dans Project Service Automation et synchronisés vers Finance en tant que contrats de projet. Dans le cadre du modèle d’intégration, vous pouvez définir la source d’intégration dans Finance pour le contrat de projet.

Le temps, le matériel et les projets à prix fixe sont gérés dans Project Service Automation et synchronisés avec Finance en tant que projets. Dans le cadre de l’intégration du modèle, vous pouvez définir la source d’intégration du projet dans Finance. Actuellement, seuls les projets de durée et de matériel et à prix fixe sont pris en charge.


Les lignes de contrat de projet sont gérées dans Project Service Automation et synchronisées vers Finance en tant que règles de facturation de contrat. Si la méthode de facturation diffère du type de projet par défaut, la synchronisation met à jour le type de projet pour le projet de ligne de contrat et le groupe de projets.

Les jalons de ligne de contrat de projet sont gérées dans Project Service Automation et synchronisées vers Finance en tant que jalons de règles de facturation de contrat.

## <a name="project-service-automation-to-finance-integration-solution"></a>Solution d’intégration de Project Service Automation vers Finance

Le champ **ID du contrat de projet** est disponible sur la page **Contrats de projet**. Ce champ est devenu une clé naturelle et unique pour soutenir l’intégration.

Lorsqu’un nouveau contrat de projet est créé, si une valeur **ID du contrat de projet** n’existe pas déjà, elle est automatiquement générée à l’aide d’une séquence de nombres. La valeur se compose de **ORD** suivi d’une séquence numérique incrémentielle, puis d’un suffixe de six caractères. Prenons un exemple : **ORD-01022-Z4M9Q0**.

Le champ **Numéro de projet** est disponible sur la page **Projets**. Ce champ est devenu une clé naturelle et unique pour soutenir l’intégration.

Lorsqu’un nouveau projet est créé, si une valeur **Numéro de projet** n’existe pas déjà, elle est automatiquement générée à l’aide d’une séquence de nombres. La valeur se compose de **PRJ** suivi d’une séquence numérique incrémentielle, puis d’un suffixe de six caractères. Prenons un exemple : **PRJ-01049-CCNID0**.

Lorsque la solution d’intégration Project Service Automation vers Finance est appliquée, un script de mise à niveau définit le champ **ID du contrat de projet** pour les contrats de projet existants et le champ **Numéro de projet** pour les projets existants dans Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Prérequis et configuration de mappage

- Avant que la synchronisation des contrats de projet et des projets puisse avoir lieu, vous devez synchroniser les comptes.
- Dans votre jeu de connexions, ajoutez un mappage de champ de clé d’intégration pour **msdyn\_organizationalunits** à **msdyn\_name \[Name\]**. Vous devrez peut-être d’abord ajouter un projet à l’ensemble de connexions. Pour plus d’informations, consultez [Intégrer les données dans Common Data Service pour les applications](/powerapps/administrator/data-integrator).
- Dans votre jeu de connexions, ajoutez un mappage de champ de clé d’intégration pour **msdyn\_projects** à **msdynce\_projectnumber \[Project Number\]**. Vous devrez peut-être d’abord ajouter un projet à l’ensemble de connexions. Pour plus d’informations, consultez [Intégrer les données dans Common Data Service pour les applications](/powerapps/administrator/data-integrator).
- **SourceDataID** pour les contrats de projet et les projets peuvent être mis à jour à une valeur différente ou supprimés du mappage. La valeur par défaut du modèle est **Project Service Automation**.
- Le mappage **PaymentTerms** doit être mis à jour afin de refléter les conditions de paiement valides dans Finance. Vous pouvez également supprimer le mappage de la tâche de projet. La carte de valeur par défaut a des valeurs par défaut pour les données de démonstration. Le tableau suivant montre les valeurs dans Project Service Automation.

    | active | Description   |
    |-------|---------------|
    | 1     | Net 30 jours        |
    | 2     | 2%% 10j, net 30j |
    | 3     | Net 45 jours        |
    | 4     | Net 60 jours        |

## <a name="power-query"></a>Power Query

Utilisez Microsoft Power Query pour Excel pour filtrer les données si les conditions suivantes sont réunies :

- Vous avez des commandes client dans Dynamics 365 Sales.
- Vous disposez de plusieurs unités organisationnelles dans Project Service Automation, et ces unités organisationnelles seront mappées à plusieurs entités juridiques dans Finance.

Si vous devez utiliser Power Query, suivez les instructions ci-après :

- Le modèle Projets et contrats (PSA vers Fin and Ops) a un filtre par défaut qui inclut uniquement les commandes client de type **Élément de travail (msdyn\_ordertype = 192350001)**. Ce filtre permet de garantir que les contrats de projet ne sont pas créés pour les commandes client dans Finance. Si vous créez votre propre modèle, vous devez ajouter ce filtre.
- Créez un filtre Power Query qui n’inclut que les organisations contractuelles qui doivent être synchronisées avec l’entité juridique de l’ensemble de connexions d’intégration. Par exemple, les contrats de projet que vous avez avec l’unité d’organisation de contrat de Contoso US doivent être synchronisés avec l’entité juridique USSI, mais les contrats de projet que vous avez avec l’unité d’organisation de contrat de Contoso Global doivent être synchronisés avec l’entité juridique USMF. Si vous n’ajoutez pas ce filtre à votre mappage de tâches, tous les contrats de projet seront synchronisés avec l’entité juridique définie pour l’ensemble de connexions, quelle que soit l’unité d’organisation du contrat.

## <a name="template-mapping-in-data-integration"></a>Mappage de modèles dans l’intégration de données

> [!NOTE] 
> Les champs **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** et **AddressZipCode** ne sont pas inclus dans le mappage par défaut des contrats de projet. Vous pouvez ajouter les mappages si vous souhaitez que ces données soient synchronisées pour les contrats de projet.
>
> Les champs **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** et **ProjectType** ne sont pas inclus dans le mappage par défaut pour les projets. Vous pouvez ajouter les mappages si vous souhaitez que ces données soient synchronisées pour les projets.

Les illustrations suivantes montrent des exemples de mappage de tâches de modèle dans l’intégration de données. Le mappage affiche les informations de champ qui seront synchronisées de Project Service Automation vers Finance.

[![Mappage du modèle de contrat de projet.](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mappage du modèle de projet.](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mappage du modèle des lignes de contrat de projet.](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mappage du modèle des jalons des lignes de contrat de projet.](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Cartographie des jalons de la ligne de contrat de projet dans les projets et contrats (PSA 3.x vers Dynamics) - modèle v2 :

[![Mappage des jalons des lignes de contrat de projet avec la version 2 du modèle.](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]