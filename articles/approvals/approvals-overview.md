---
title: Vue d’ensemble des approbations
description: Cette rubrique offre des informations sur l’utilisation des approbations dans Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 9148c9f55e8664850c38aebbc9c4bbaa243475ad
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368653"
---
# <a name="approvals-overview"></a><span data-ttu-id="f7d4b-103">Vue d’ensemble des approbations</span><span class="sxs-lookup"><span data-stu-id="f7d4b-103">Approvals overview</span></span>

<span data-ttu-id="f7d4b-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="f7d4b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f7d4b-105">Les soumissions de temps, de dépenses et d’utilisation du matériel passent par un workflow d’approbation.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-105">Time, expense, and material usage submissions move through an approval workflow.</span></span> <span data-ttu-id="f7d4b-106">Une fois les écritures approuvées, les transactions sont enregistrées en chiffres réels ou le temps est réservé dans le calendrier.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="f7d4b-107">Workflow des approbations</span><span class="sxs-lookup"><span data-stu-id="f7d4b-107">Approvals workflow</span></span>
<span data-ttu-id="f7d4b-108">Lorsque vous créez et soumettez une entrée de temps, de dépense ou d’utilisation du matériel, un enregistrement d’approbation est créé.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-108">When you create and submit a time, expense, or material usage entry, an approval record is created.</span></span> <span data-ttu-id="f7d4b-109">L’approbateur ou le responsable du projet examine et approuve l’entrée.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-109">The project approver or manager reviews and approves the entry.</span></span> <span data-ttu-id="f7d4b-110">Si l’entrée est liée à un projet, les chiffres réels seront créés lors de son approbation.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-110">If the entry is related to a project, the actuals will be created when it's approved.</span></span> <span data-ttu-id="f7d4b-111">Cela permet de suivre le coût et la facturation.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-111">This allows the cost and billing to be tracked.</span></span>

## <a name="approve-an-entry"></a><span data-ttu-id="f7d4b-112">Approuver une entrée</span><span class="sxs-lookup"><span data-stu-id="f7d4b-112">Approve an entry</span></span>
<span data-ttu-id="f7d4b-113">La page **Approbations** vous permet de basculer entre différentes vues afin de pouvoir afficher les différents types d’approbations.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-113">The **Approvals** page allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="f7d4b-114">Accédez à la page **Approbations** et sélectionnez **Dépenses**, **Temps**, **Utilisation du matériel** ou **Rappels**.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-114">Go to the **Approvals** page and select **Expenses**, **Time**, **Material Usage**, or **Recalls**.</span></span>
2. <span data-ttu-id="f7d4b-115">Passez en revue chaque approbation et sélectionnez celles que vous souhaitez approuver.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="f7d4b-116">Sélectionnez **Approuver** pour approuver les entrées sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="f7d4b-117">Le système traite ces entrées et crée des chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-117">The system processes these entries and create actuals.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="f7d4b-118">Refuser une entrée</span><span class="sxs-lookup"><span data-stu-id="f7d4b-118">Reject an entry</span></span>
<span data-ttu-id="f7d4b-119">En tant qu’approbateur de projet, vous devrez peut-être renvoyer une entrée à un utilisateur pour correction.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="f7d4b-120">Accédez à la page **Approbations** et sélectionnez l’entrée à rejeter.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-120">Go to the **Approvals** page and select the entry to reject.</span></span> 
2. <span data-ttu-id="f7d4b-121">Sélectionnez **Rejeter**.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-121">Select **Reject**.</span></span>
3. <span data-ttu-id="f7d4b-122">Vous pouvez ajouter un commentaire dans la boîte de dialogue **Commentaires sur le rejet** pour informer l’utilisateur de la raison pour laquelle l’entrée est rejetée.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-122">Optional, add a comment in the **Rejection Comments** dialog box to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="f7d4b-123">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-123">Select **OK**.</span></span> <span data-ttu-id="f7d4b-124">L’entrée sera retournée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-124">The entry will be returned to the user.</span></span>
  
## <a name="cancel-approval"></a><span data-ttu-id="f7d4b-125">Annuler l’approbation</span><span class="sxs-lookup"><span data-stu-id="f7d4b-125">Cancel approval</span></span>
<span data-ttu-id="f7d4b-126">Dans certains cas, vous devrez peut-être annuler une entrée précédemment approuvée.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-126">In some cases, you might need to cancel a previously approved entry.</span></span> <span data-ttu-id="f7d4b-127">L’annulation d’une entrée précédemment approuvée aura un impact financier.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-127">Canceling a previously approved entry will have a financial impact.</span></span> 

## <a name="approving-recall-requests"></a><span data-ttu-id="f7d4b-128">Demandes de rappel d’approbation</span><span class="sxs-lookup"><span data-stu-id="f7d4b-128">Approving recall requests</span></span>
<span data-ttu-id="f7d4b-129">Dans certains cas, un consultant peut avoir besoin de rappeler une entrée précédemment approuvée.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-129">In some cases, a consultant may need to recall a previously approved entry.</span></span> <span data-ttu-id="f7d4b-130">L’annulation d’une entrée précédemment approuvée aura un impact financier.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-130">Canceling a previously approved entry will have a financial impact.</span></span> <span data-ttu-id="f7d4b-131">L’approbateur de projet doit approuver le rappel pour annuler la transaction dans les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-131">The project approver is required to approve the recall to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="f7d4b-132">Spécifier des approbateurs de projet</span><span class="sxs-lookup"><span data-stu-id="f7d4b-132">Specify Project approvers</span></span>
<span data-ttu-id="f7d4b-133">Chaque projet dispose d’un certain nombre de membres de l’équipe de projet.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-133">Each project has a number of project team members.</span></span> <span data-ttu-id="f7d4b-134">Vous pouvez spécifier les membres de l’équipe qui sont également des approbateurs de projet.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-134">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="f7d4b-135">Accédez à la page **Projets** et ouvrez le projet dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-135">Go to the **Projects** page and open the project from the list.</span></span>
2. <span data-ttu-id="f7d4b-136">Sur l’onglet **Équipe**, sélectionnez le membre de l’équipe qui sera un approbateur de projet, puis sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-136">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="f7d4b-137">Définissez le champ **Approbateur du projet** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-137">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="f7d4b-138">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-138">Select **Save**.</span></span>
5. <span data-ttu-id="f7d4b-139">Répétez les étapes 2 à 4 pour ajouter des approbateurs de projet supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-139">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="f7d4b-140">Configurer le gestionnaire de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="f7d4b-140">Configure the user's manager</span></span>

1. <span data-ttu-id="f7d4b-141">Accédez à **Paramètres** > **Sécurité** > **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-141">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="f7d4b-142">Sélectionnez l’utilisateur auquel vous affectez un responsable et dans la zone **Informations sur l’organisation**, sélectionnez le responsable dans la liste.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-142">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="f7d4b-143">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="f7d4b-143">Select **Save**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
