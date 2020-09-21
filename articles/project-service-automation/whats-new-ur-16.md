---
title: Nouveautés de la mise à jour (version 16) de Project Service Automation, V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 16) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168045"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="33cdd-103">Mise à jour (version 16) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="33cdd-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="33cdd-104">Nous sommes heureux d'annoncer la dernière mise à jour de l'application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="33cdd-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="33cdd-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="33cdd-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="33cdd-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="33cdd-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="33cdd-107">Pour effectuer une mise à jour vers cette version, visitez le centre d'administration de Dynamics 365 (en ligne) et accédez à la page des solutions pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="33cdd-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="33cdd-108">Pour plus d'informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="33cdd-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="33cdd-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 16) de PSA V3.</span><span class="sxs-lookup"><span data-stu-id="33cdd-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="33cdd-110">Cette version a le numéro de build V3.10.6.34 et est généralement disponible par mise à jour automatique en janvier 2020.</span><span class="sxs-lookup"><span data-stu-id="33cdd-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="33cdd-111">Mise à jour (version 16)</span><span class="sxs-lookup"><span data-stu-id="33cdd-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="33cdd-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="33cdd-112">Bug fixes</span></span>

-   <span data-ttu-id="33cdd-113">Temps et dépenses</span><span class="sxs-lookup"><span data-stu-id="33cdd-113">Time and Expense</span></span>

    -   <span data-ttu-id="33cdd-114">Résolu : Les utilisateurs qui tentaient de soumettre des entrées de temps et de dépenses supprimées pour les approbations reçoivent désormais des messages d'erreur pertinents.</span><span class="sxs-lookup"><span data-stu-id="33cdd-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="33cdd-115">Gestion du projet</span><span class="sxs-lookup"><span data-stu-id="33cdd-115">Project Management</span></span>

    -   <span data-ttu-id="33cdd-116">Résolu : Les unités de ressources définies pour les membres de l'équipe dans les modèles sont respectées et les modèles sont appliqués à un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="33cdd-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="33cdd-117">Résolu : Gestion améliorée de la réaffectation de la propriété d'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="33cdd-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="33cdd-118">Résolu : Les projets en cours de copie ne seront pas autorisés à être copiés tant que toutes les opérations de copie ne seront pas terminées.</span><span class="sxs-lookup"><span data-stu-id="33cdd-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="33cdd-119">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="33cdd-119">Resource Management</span></span>

    -   <span data-ttu-id="33cdd-120">Résolu : Les réservations prolongées gèrent désormais correctement les courtes durées et ne créent plus de zéro heure pour les réservations prolongées.</span><span class="sxs-lookup"><span data-stu-id="33cdd-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="33cdd-121">Résolu : La vue de réconciliation s'affiche désormais lorsque le fuseau horaire du projet est +5 :30 GMT et que l'heure de l'utilisateur est différente.</span><span class="sxs-lookup"><span data-stu-id="33cdd-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="33cdd-122">Ventes</span><span class="sxs-lookup"><span data-stu-id="33cdd-122">Sales</span></span>

    -   <span data-ttu-id="33cdd-123">Résolu : Lorsqu'un projet mappé sur une ligne de contrat est supprimé et qu'un nouveau projet est mappé, les enregistrements réels du nouveau projet ne sont pas réévalués en fonction des règles de facturation et de tarification définies sur la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="33cdd-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="33cdd-124">Cela a été corrigé dans cette version.</span><span class="sxs-lookup"><span data-stu-id="33cdd-124">This has been fixed in this release.</span></span> <span data-ttu-id="33cdd-125">Les prix et les enregistrements réels du projet nouvellement mappé seront inversés et recréés correctement en fonction des règles de tarification et de facturation de la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="33cdd-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="33cdd-126">Les enregistrements réels du projet non mappé seront également réévalués et recréés en conséquence.</span><span class="sxs-lookup"><span data-stu-id="33cdd-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="33cdd-127">Résolu : Une validation supplémentaire a été ajoutée à un champ **Montant** d'une ligne d'estimation pour garantir que les valeurs nulles ne sont pas persistantes.</span><span class="sxs-lookup"><span data-stu-id="33cdd-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="33cdd-128">Résolu : Lorsque les chiffres réels ont été mis à jour sur un projet, un bouton d'actualisation a été ajouté au formulaire principal du projet pour permettre aux utilisateurs de resynchroniser les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="33cdd-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="33cdd-129">Résolu : Lorsque les utilisateurs passent de 2.X à 3.X, les projets avec une valeur NULL pour le nom du projet seront autorisés.</span><span class="sxs-lookup"><span data-stu-id="33cdd-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

