---
title: Nouveautés ou modifications de la mise à jour (version 24) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 24) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146705"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="9c060-103">Mise à jour (version 24) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="9c060-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9c060-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9c060-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9c060-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="9c060-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9c060-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9c060-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9c060-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="9c060-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9c060-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9c060-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9c060-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 24) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="9c060-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="9c060-110">Cette version a le numéro de build V3.10.42.43 et est généralement disponible par mise à jour automatique en octobre 2020.</span><span class="sxs-lookup"><span data-stu-id="9c060-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="9c060-111">Mise à jour (version 24)</span><span class="sxs-lookup"><span data-stu-id="9c060-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9c060-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="9c060-112">Bug fixes</span></span>

<span data-ttu-id="9c060-113">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="9c060-113">**Sales**</span></span>

<span data-ttu-id="9c060-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="9c060-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c060-115">Problème lors de la définition des tarifs par défaut des produits.</span><span class="sxs-lookup"><span data-stu-id="9c060-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="9c060-116">Les performances en matière de devis remportés sont lentes en raison de la copie intégrée des tarifs et des enregistrements Prix du rôle.</span><span class="sxs-lookup"><span data-stu-id="9c060-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="9c060-117">**Contrat de projet/Centre des ventes** > **Ligne de produit/Quantité ligne de commande** est automatiquement arrondi à l’entier le plus proche.</span><span class="sxs-lookup"><span data-stu-id="9c060-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="9c060-118">Élevez les privilèges système lors de la lecture des tarifs.</span><span class="sxs-lookup"><span data-stu-id="9c060-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="9c060-119">Copiez les champs d’adresse client **address1_freighttermscode** et **address1_shippingmethodcode** vers Devis/Commande.</span><span class="sxs-lookup"><span data-stu-id="9c060-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="9c060-120">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="9c060-120">**Time and Expense**</span></span>

<span data-ttu-id="9c060-121">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="9c060-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c060-122">La **Grille d’entrée de temps** ne prend pas en charge le comportement **Date uniquement**.</span><span class="sxs-lookup"><span data-stu-id="9c060-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="9c060-123">Le champ **Entrée de temps** ne s’actualise pas automatiquement.</span><span class="sxs-lookup"><span data-stu-id="9c060-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="9c060-124">Une actualisation manuelle est requise.</span><span class="sxs-lookup"><span data-stu-id="9c060-124">A manual refresh is required.</span></span>
- <span data-ttu-id="9c060-125">Impossible d’importer les entrées de temps d’une affectation en cas de pause (0 heure) dans les affectations d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="9c060-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="9c060-126">Lors de la création d’une entrée de temps, définissez le début sur **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="9c060-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="9c060-127">Réactivez la modification en bloc pour l’entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="9c060-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="9c060-128">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="9c060-128">**Resource Management**</span></span>

<span data-ttu-id="9c060-129">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="9c060-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c060-130">Essayer de mettre à jour le statut d’une réservation interjournalière sans besoin lève une exception de référence nulle.</span><span class="sxs-lookup"><span data-stu-id="9c060-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="9c060-131">Erreur lors du chargement de la **Vue de rapprochement**.</span><span class="sxs-lookup"><span data-stu-id="9c060-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="9c060-132">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="9c060-132">**Project Management**</span></span>

<span data-ttu-id="9c060-133">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="9c060-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="9c060-134">Dans le **Calendrier du projet**, lors du passage du mode **Manuel** au mode **Automatique**, l’enregistrement automatique ne se fait pas.</span><span class="sxs-lookup"><span data-stu-id="9c060-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="9c060-135">Les frais ne doivent pas être calculés en fonction de la variance **Grille de suivi de projet**.</span><span class="sxs-lookup"><span data-stu-id="9c060-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="9c060-136">Comportement incohérent pour les colonnes **Balise des estimations** lors du chargement et de la modification du type **Phase de temps**.</span><span class="sxs-lookup"><span data-stu-id="9c060-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="9c060-137">Le coût réel d’un projet peut ne pas refléter les totaux de **Chiffres réels**.</span><span class="sxs-lookup"><span data-stu-id="9c060-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="9c060-138">**Date de fin estimée** sur l’onglet **Résumé** ne correspond pas au **Calendrier WBS**.</span><span class="sxs-lookup"><span data-stu-id="9c060-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="9c060-139">**Mettre à jour les heures réelles** sur retrait négatif ne fonctionne pas correctement.</span><span class="sxs-lookup"><span data-stu-id="9c060-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="9c060-140">Un chef de projet en dehors de la racine **UO** ne peut pas créer un projet.</span><span class="sxs-lookup"><span data-stu-id="9c060-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="9c060-141">Les modifications apportées à la tâche ou à la catégorie sur **Estimations des frais** ne sont pas conservées.</span><span class="sxs-lookup"><span data-stu-id="9c060-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="9c060-142">**Copie du contrat** copie les calendriers de facturation et le statut d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9c060-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="9c060-143">Le bouton **Actualiser les statistiques** ne calcule pas correctement les tâches récapitulatives.</span><span class="sxs-lookup"><span data-stu-id="9c060-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="9c060-144">Complément Microsoft Project : correction d’une erreur de référence nulle si un membre de l’équipe a une unité de ressources vide.</span><span class="sxs-lookup"><span data-stu-id="9c060-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

