---
title: Nouveautés ou modifications de la mise à jour (version 19) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 19) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143603"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="3ed9e-103">Mise à jour (version 19) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="3ed9e-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="3ed9e-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3ed9e-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3ed9e-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3ed9e-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3ed9e-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3ed9e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3ed9e-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 19) de PSA V3.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="3ed9e-110">Cette version a le numéro de build V3.10.30.41 et est généralement disponible via une mise à jour automatique en mai 2020.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="3ed9e-111">Mise à jour (version 19)</span><span class="sxs-lookup"><span data-stu-id="3ed9e-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3ed9e-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="3ed9e-112">Bug fixes</span></span>

<span data-ttu-id="3ed9e-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="3ed9e-113">**Time and Expense**</span></span>

<span data-ttu-id="3ed9e-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="3ed9e-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="3ed9e-115">Les erreurs dérivées des importations d’entrée de temps ne sont pas affichées correctement.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="3ed9e-116">La grille d’entrée de temps ne prend pas en charge le comportement du champ **Date uniquement**.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="3ed9e-117">Les ressources du projet ne peuvent pas créer une dépense avec un projet.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="3ed9e-118">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="3ed9e-118">**Project Management**</span></span>

<span data-ttu-id="3ed9e-119">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="3ed9e-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="3ed9e-120">La tâche petit-enfant crée une estimation incorrecte de l’effort lors du calcul du coût final.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="3ed9e-121">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="3ed9e-121">**Sales**</span></span>

<span data-ttu-id="3ed9e-122">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="3ed9e-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="3ed9e-123">L’action **Recalculer** ne fonctionne pas avec les détails de la ligne de contrat ou les détails de la ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="3ed9e-124">**Mettre à jour les prix** est manquant pour les estimations des dépenses.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="3ed9e-125">Les clients ne peuvent pas sélectionner des raisons de statut de contrat personnalisées dans la page **Contrat du projet**.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="3ed9e-126">Les clients constatent une dégradation des performances lors de la création de tarifs personnalisés à partir d’un devis.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="3ed9e-127">Les clients constatent une incohérence dans les valeurs par défaut pour **unité** sur les pages **Détails de la ligne de devis** et **Détails de la ligne de contrat**.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="3ed9e-128">L’ajout d’éléments de catégorie de transaction non facturables à une ligne de contrat facturable ne respecte pas le type de facturation **Non facturable** de la catégorie de transaction.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="3ed9e-129">Les clients ne peuvent pas utiliser les nouveaux rôles et la nouvelle catégorie ajoutés sur les contrats déjà créés.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="3ed9e-130">Ls clients constatent une dégradation des performances. Récupération inutile dans PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="3ed9e-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="3ed9e-131">Les rôles définis comme non facturables dans la liste **Catégories de ressource** doivent être ajoutés à l’onglet **Rôles facturables** en tant que **Non facturables** sur la ligne de contrat d’un projet.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="3ed9e-132">Les clients peuvent constater une dégradation des performances lors de la création d’un projet, car **GetBookableResourceIdFromUser** récupère toutes les colonnes de ressources réservables au lieu de l’ID principal.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="3ed9e-133">L’entité **TransactionType** ne dispose pas du plug-in de mise à jour avant validation qui empêche les utilisateurs d’entrer **Units** et **UnitGroups** qui ne sont pas valides pour les types de transaction.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="3ed9e-134">L’étape **Supprimer** ne fonctionne pas pour l’importation d’entrées de temps.</span><span class="sxs-lookup"><span data-stu-id="3ed9e-134">The **Remove** step does not work for time entry import.</span></span>
