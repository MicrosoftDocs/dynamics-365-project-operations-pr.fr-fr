---
title: Nouveautés ou modifications de la mise à jour (version 21) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 21) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: b1194c1cf1997b68030fe88360c6ebb756c715fd
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147020"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="8ce7d-103">Mise à jour (version 21) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="8ce7d-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8ce7d-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8ce7d-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8ce7d-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8ce7d-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8ce7d-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8ce7d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8ce7d-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 21) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="8ce7d-110">Cette version a le numéro de build V 3.10.32.50 et est généralement disponible via une mise à jour automatique en juin 2020.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="8ce7d-111">Mise à jour (version 21)</span><span class="sxs-lookup"><span data-stu-id="8ce7d-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8ce7d-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="8ce7d-112">Bug fixes</span></span>

<span data-ttu-id="8ce7d-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="8ce7d-113">**Time and Expense**</span></span>

<span data-ttu-id="8ce7d-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="8ce7d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ce7d-115">Lors de l’hébergement du contrôle **Grille d’entrée de temps** dans les tableaux de bord, la grille n’utilise pas toute la largeur du conteneur de grille de tableau de bord.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="8ce7d-116">Pour des fuseaux horaires spécifiques, le contrôle de grille **Entrée de temps** n’affiche pas d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="8ce7d-117">Les entrées de temps effectuées après 21h s’affichent le mauvais jour.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="8ce7d-118">Les utilisateurs ne peuvent pas soumettre de dépenses si la catégorie de dépense **Reçu de dépenses requis** n’a aucune valeur.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="8ce7d-119">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="8ce7d-119">**Resource Management**</span></span>

<span data-ttu-id="8ce7d-120">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="8ce7d-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ce7d-121">Les réservations inactives sont affichées dans la vue **Rapprochement**.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="8ce7d-122">L’exécution des ressources génériques n’a pas été validée pour s’assurer qu’il existe un statut de réservation valide.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="8ce7d-123">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="8ce7d-123">**Project Management**</span></span>

<span data-ttu-id="8ce7d-124">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="8ce7d-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ce7d-125">Les grilles du formulaire **Projet** (**Attribution de ressource**, **Tâche**, vue **Rapprochement**, **Estimations des dépenses**) restent modifiables même lorsqu’un projet n’est pas actif.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="8ce7d-126">Les clients en double ne peuvent pas être fusionnés avec les clients liés à des contrats de projet confirmés.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="8ce7d-127">Lorsqu’une ressource sans calendrier valide est ajoutée, le système ne renvoie pas de message d’erreur convivial.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="8ce7d-128">Le bouton **Ajouter une tâche** de la grille de tâches est activé lorsque le projet est lié au **Complément Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="8ce7d-129">L’effort augmente de manière incontrôlable lorsqu’une tâche avec une catégorie est affectée à une ressource doté d’un rôle pour lequel un prix de revient est défini.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="8ce7d-130">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="8ce7d-130">**Sales**</span></span>

<span data-ttu-id="8ce7d-131">Les améliorations suivantes ont été apportées :</span><span class="sxs-lookup"><span data-stu-id="8ce7d-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="8ce7d-132">**Fréquence de facturation** et **Début de la facturation** ont été déplacés vers l’onglet **Calendrier de facturation**.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="8ce7d-133">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="8ce7d-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="8ce7d-134">La valeur **Prix de vente total** est égale à zéro (0) pour **Catégorie** même si le champ **Rôle** a un prix de vente total différent de zéro.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="8ce7d-135">Les clients ne peuvent pas modifier la valeur du champ **Statut de la facture** en **Prêt pour la facturation** lorsqu’un autre processus personnalisé met à jour un champ supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="8ce7d-136">Le bouton **Actualiser les lignes de facture** peut créer plusieurs lignes dupliquées s’il est sélectionné à plusieurs reprises.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="8ce7d-137">Le bouton **Mettre à jour les prix** ne fonctionne pas dans la sous-grille **Prix du rôle** dans le formulaire **Aperçu**.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="8ce7d-138">La logique **Résolution des tarifs de vente** gère de manière incorrecte les fuseaux horaires, ce qui entraîne la sélection incorrecte des tarifs.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="8ce7d-139">Le **Coût réel total** d’un projet peut diminuer d’un montant fractionnaire après l’approbation d’une entrée de temps unique.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="8ce7d-140">La logique **Résolution du prix** ne fournit pas de message d’erreur convivial si **Prix du rôle récupéré** n’a pas de valeurs dans les champs **Unité principale** et **Prix dans l’unité principale**.</span><span class="sxs-lookup"><span data-stu-id="8ce7d-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
