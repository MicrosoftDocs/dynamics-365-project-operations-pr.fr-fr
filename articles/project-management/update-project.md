---
title: Mettre à jour un projet
description: Cette rubrique offre des informations sur la mise à jour des projets dans Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c07542444b970430d8143a60aad6970305769b22
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993368"
---
# <a name="update-a-project"></a><span data-ttu-id="256eb-103">Mettre à jour un projet</span><span class="sxs-lookup"><span data-stu-id="256eb-103">Update a project</span></span>

<span data-ttu-id="256eb-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="256eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="256eb-105">Vous trouverez ci-dessous un résumé des champs qui peuvent être mis à jour sur un projet après sa création et toutes les implications applicables des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="256eb-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="256eb-106">Champs de détail du projet</span><span class="sxs-lookup"><span data-stu-id="256eb-106">Project detail fields</span></span>

- <span data-ttu-id="256eb-107">**Nom** : Titre du projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="256eb-108">**Description** : Vue d’ensemble du projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="256eb-109">**Client** : L’entreprise à laquelle le projet sera fourni.</span><span class="sxs-lookup"><span data-stu-id="256eb-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="256eb-110">**Modèle de calendrier** : Heures de travail du projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="256eb-111">Lorsque le champ est modifié, la planification entière est recalculée.</span><span class="sxs-lookup"><span data-stu-id="256eb-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="256eb-112">**Devise** : Devise du projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="256eb-113">Ce champ est par défaut basé sur la devise définie dans l’unité contractuelle.</span><span class="sxs-lookup"><span data-stu-id="256eb-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="256eb-114">Lorsque l’unité contractuelle est mise à jour, le champ est également mis à jour.</span><span class="sxs-lookup"><span data-stu-id="256eb-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="256eb-115">**Unité contractuelle** : Unité d’organisation qui représente le groupe de sociétés ou la division principalement responsables de remporter la vente et de gérer la prestation du travail et des services au client.</span><span class="sxs-lookup"><span data-stu-id="256eb-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="256eb-116">**Gestionnaire de projet** : Membre de l’équipe de projet qui a le pouvoir d’examiner et d’approuver les entrées de temps et les dépenses.</span><span class="sxs-lookup"><span data-stu-id="256eb-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="256eb-117">Champs d’estimation</span><span class="sxs-lookup"><span data-stu-id="256eb-117">Estimate fields</span></span>

- <span data-ttu-id="256eb-118">**Date de début estimée** : Date à laquelle le projet commencera.</span><span class="sxs-lookup"><span data-stu-id="256eb-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="256eb-119">Lorsque ce champ est mis à jour, toutes les tâches du projet seront déplacées proportionnellement à la nouvelle date de début.</span><span class="sxs-lookup"><span data-stu-id="256eb-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="256eb-120">**Date de fin** : Date à laquelle le projet doit se terminer.</span><span class="sxs-lookup"><span data-stu-id="256eb-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="256eb-121">**Effort** : Effort estimé du projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="256eb-122">Lorsque des tâches sont ajoutées au projet, ce champ n’est plus modifiable.</span><span class="sxs-lookup"><span data-stu-id="256eb-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="256eb-123">**Coût estimé de la main-d’œuvre** : Coût estimé de la main-d’œuvre du projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="256eb-124">Lorsque des coûts de main-d’œuvre sont ajoutés au projet, ce champ n’est plus modifiable.</span><span class="sxs-lookup"><span data-stu-id="256eb-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="256eb-125">**Dépenses estimées** : Dépenses estimées du projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="256eb-126">Lorsque des dépenses sont ajoutées au projet, ce champ n’est plus modifiable.</span><span class="sxs-lookup"><span data-stu-id="256eb-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="256eb-127">Champs des chiffres réels du projet</span><span class="sxs-lookup"><span data-stu-id="256eb-127">Project actual fields</span></span>
- <span data-ttu-id="256eb-128">**Début réel** : Date à laquelle le projet a commencé.</span><span class="sxs-lookup"><span data-stu-id="256eb-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="256eb-129">**Fin réelle** : À mettre à jour lorsqu’un projet est terminé.</span><span class="sxs-lookup"><span data-stu-id="256eb-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="256eb-130">Champs de statut du projet</span><span class="sxs-lookup"><span data-stu-id="256eb-130">Project status fields</span></span>

- <span data-ttu-id="256eb-131">**Statut général du projet** : Intégrité globale du projet fournie par le chef de projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="256eb-132">**Commentaires** : Récit concernant l’intégrité actuelle du projet fourni par le chef de projet.</span><span class="sxs-lookup"><span data-stu-id="256eb-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]