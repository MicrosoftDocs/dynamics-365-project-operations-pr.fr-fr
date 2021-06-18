---
title: Nouveautés ou modifications de la mise à jour (version 31) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 31) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 160187ba7b96547e85a7a4ec4bf84c86d8fd8257
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999128"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="46a33-103">Nouveautés ou modifications de la mise à jour (version 31) de Project Service Automation (correctif logiciel), V3</span><span class="sxs-lookup"><span data-stu-id="46a33-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="46a33-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="46a33-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="46a33-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="46a33-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="46a33-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="46a33-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="46a33-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="46a33-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="46a33-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="46a33-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="46a33-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 31) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="46a33-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="46a33-110">Cette version a le numéro de build V3.10.52.77 et est généralement disponible via une mise à jour automatique en mai 2021.</span><span class="sxs-lookup"><span data-stu-id="46a33-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="46a33-111">Mise à jour (version 31)</span><span class="sxs-lookup"><span data-stu-id="46a33-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="46a33-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="46a33-112">Bug fixes</span></span>

<span data-ttu-id="46a33-113">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="46a33-113">**Time and Expense**</span></span>

<span data-ttu-id="46a33-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="46a33-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="46a33-115">Les boutons de commande du contrôle d’entrée de temps sur la page **Ressource réservable** prêtaient à confusion.</span><span class="sxs-lookup"><span data-stu-id="46a33-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="46a33-116">Une exception de référence nulle était générée dans **Project.SetTrackingFields** lors de l’approbation d’une entrée de temps.</span><span class="sxs-lookup"><span data-stu-id="46a33-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="46a33-117">**Gestion des ressources**</span><span class="sxs-lookup"><span data-stu-id="46a33-117">**Resource Management**</span></span>

<span data-ttu-id="46a33-118">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="46a33-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="46a33-119">**Créer un membre d’équipe** n’affiche pas correctement le paramètre de métadonnées de configuration de la réservation pour **Statut Réservation par défaut validée**.</span><span class="sxs-lookup"><span data-stu-id="46a33-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="46a33-120">Lors de la mise à niveau de PSA 1.X vers 3.X, le processus de mise à niveau échoue à l’étape **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="46a33-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="46a33-121">**Vente**</span><span class="sxs-lookup"><span data-stu-id="46a33-121">**Sales**</span></span>

<span data-ttu-id="46a33-122">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="46a33-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="46a33-123">Le revenu réel convertit les montants dans la devise du projet dans la grille de suivi.</span><span class="sxs-lookup"><span data-stu-id="46a33-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="46a33-124">La devise par défaut n’est pas claire lors de la création de lignes de journal, de lignes de devis et de lignes de contrats dans des scénarios où la devise de base d’une organisation diffère de la devise du projet.</span><span class="sxs-lookup"><span data-stu-id="46a33-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="46a33-125">La requête **En attente de validation du journal de correction** ne filtre pas par projet.</span><span class="sxs-lookup"><span data-stu-id="46a33-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="46a33-126">Les ventes restantes sont calculées de manière incorrecte sur un projet.</span><span class="sxs-lookup"><span data-stu-id="46a33-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="46a33-127">Les devis basés sur un contact échouent lorsqu’ils sont créés sans tarif.</span><span class="sxs-lookup"><span data-stu-id="46a33-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="46a33-128">Aucun indicateur de traitement ne s’affiche lorsque vous sélectionnez **Confirmer la facture**.</span><span class="sxs-lookup"><span data-stu-id="46a33-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="46a33-129">Aucun indicateur de traitement ne s’affiche lorsque vous sélectionnez **Créer la facture**.</span><span class="sxs-lookup"><span data-stu-id="46a33-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="46a33-130">La fermeture d’un devis avec le statut Perdu n’annule pas les réservations.</span><span class="sxs-lookup"><span data-stu-id="46a33-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







