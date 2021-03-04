---
title: Nouveautés ou modifications de la mise à jour (version 22) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 22) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150980"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="a0c91-103">Mise à jour (version 22) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="a0c91-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a0c91-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a0c91-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a0c91-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a0c91-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a0c91-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a0c91-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a0c91-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a0c91-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a0c91-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a0c91-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a0c91-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 22) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="a0c91-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="a0c91-110">Cette version a le numéro de build V 3.10.33.48 et est généralement disponible via une mise à jour automatique en juin 2020.</span><span class="sxs-lookup"><span data-stu-id="a0c91-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="a0c91-111">Mise à jour (version 22)</span><span class="sxs-lookup"><span data-stu-id="a0c91-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a0c91-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="a0c91-112">Bug fixes</span></span>



<span data-ttu-id="a0c91-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="a0c91-113">**Time and Expense**</span></span>

<span data-ttu-id="a0c91-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="a0c91-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a0c91-115">Les **Entrées de temps** ne sont pas automatiquement ajoutées dans le calendrier des entrées de temps après l’importation.</span><span class="sxs-lookup"><span data-stu-id="a0c91-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="a0c91-116">Le sélecteur de date de la grille **Entrée de temps** ne reconnaît pas les paramètres régionaux d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a0c91-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="a0c91-117">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="a0c91-117">**Resource Management**</span></span>

<span data-ttu-id="a0c91-118">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="a0c91-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="a0c91-119">En mode manuel, les modifications des contours **Attribution de ressource** ne sont pas reconnues lors de la génération des **Ressources requises**.</span><span class="sxs-lookup"><span data-stu-id="a0c91-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="a0c91-120">Les **Demandes de ressources** ne prennent pas en charge les statuts de demande personnalisés.</span><span class="sxs-lookup"><span data-stu-id="a0c91-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="a0c91-121">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="a0c91-121">**Project Management**</span></span>

<span data-ttu-id="a0c91-122">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="a0c91-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="a0c91-123">L’utilisation du double-clic sur EstimateGridControl n’analyse pas correctement les nombres au format néerlandais.</span><span class="sxs-lookup"><span data-stu-id="a0c91-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="a0c91-124">Les heures affectées ne sont pas mises à jour correctement lorsque les affectations sont modifiées à l’aide du complément Microsoft Project pour ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="a0c91-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="a0c91-125">Les grilles Suivi du projet et Estimations affichent un code devise de vente incorrect lorsque la devise du contrat est différente de la devise du client et l’organisation est configurée pour afficher des codes devise au lieu de symboles de devise.</span><span class="sxs-lookup"><span data-stu-id="a0c91-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="a0c91-126">La date de fin d’un membre de l’équipe ajoute un jour si le calendrier des heures de travail est de 24 heures par jour.</span><span class="sxs-lookup"><span data-stu-id="a0c91-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="a0c91-127">Dans le calendrier du projet, l’ajout d’une catégorie de transaction à une tâche ne déclenche pas l’enregistrement automatique.</span><span class="sxs-lookup"><span data-stu-id="a0c91-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="a0c91-128">L’erreur suivante s’affiche lors de l’ajout d’un membre de l’équipe au modèle de projet : « Les ressources requises ne peuvent pas être associées aux modèles de projet ».</span><span class="sxs-lookup"><span data-stu-id="a0c91-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="a0c91-129">Le script de règle de ruban « msdyn.Approval.CanApproveOrReject » affiche une erreur d’expiration du délai.</span><span class="sxs-lookup"><span data-stu-id="a0c91-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="a0c91-130">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="a0c91-130">**Sales**</span></span>

<span data-ttu-id="a0c91-131">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="a0c91-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="a0c91-132">Un message d’erreur de validation ne s’affiche pas lorsqu’une liste de prix de revient est sélectionnée lors de la recherche de tarifs sur le formulaire/l’entité Nouveaux tarifs du projet de devis.</span><span class="sxs-lookup"><span data-stu-id="a0c91-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="a0c91-133">La clôture du devis comme conclue ne permet pas d’accéder au contrat créé si un BPF joint au devis est en phase finale.</span><span class="sxs-lookup"><span data-stu-id="a0c91-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="a0c91-134">La contrepassation des **Ventes non facturées** est liée au coût d’origine lorsqu’une entrée de temps est rappelée.</span><span class="sxs-lookup"><span data-stu-id="a0c91-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="a0c91-135">Après avoir sélectionné le bouton **Confirmer**, le statut de la facture ne passe pas à **Confirmé** sauf si la facture est actualisée.</span><span class="sxs-lookup"><span data-stu-id="a0c91-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>
