---
title: Vue d’ensemble des approbations
description: Cette rubrique offre des informations sur l’utilisation des approbations dans Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075600"
---
# <a name="approvals-overview"></a><span data-ttu-id="4c26c-103">Vue d’ensemble des approbations</span><span class="sxs-lookup"><span data-stu-id="4c26c-103">Approvals overview</span></span>

<span data-ttu-id="4c26c-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="4c26c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4c26c-105">Les envois de temps et de dépenses passent par un workflow d’approbation.</span><span class="sxs-lookup"><span data-stu-id="4c26c-105">Time and Expense submissions move through an approval workflow.</span></span> <span data-ttu-id="4c26c-106">Une fois les écritures approuvées, les transactions sont enregistrées en chiffres réels ou le temps est réservé dans le calendrier.</span><span class="sxs-lookup"><span data-stu-id="4c26c-106">After the entries are approved, transactions are recorded in actuals or time is booked in the schedule.</span></span>

## <a name="approvals-workflow"></a><span data-ttu-id="4c26c-107">Workflow des approbations</span><span class="sxs-lookup"><span data-stu-id="4c26c-107">Approvals workflow</span></span>
<span data-ttu-id="4c26c-108">Lorsque vous créez et envoyez une entrée de temps ou de dépense, une entrée d’approbation est créée.</span><span class="sxs-lookup"><span data-stu-id="4c26c-108">When you create and submit a time or expense entry, an approval entry is created.</span></span> <span data-ttu-id="4c26c-109">L’approbateur de projet ou votre responsable examine et approuve votre saisie.</span><span class="sxs-lookup"><span data-stu-id="4c26c-109">The Project approver or your manager reviews and approves your entry.</span></span> <span data-ttu-id="4c26c-110">Si l’entrée est liée à un projet, lorsqu’elle est approuvée, les chiffres réels seront créés.</span><span class="sxs-lookup"><span data-stu-id="4c26c-110">If the entry is related to a project, when it's approved, the actuals will be created.</span></span> <span data-ttu-id="4c26c-111">Cela permet de suivre le coût et la facturation.</span><span class="sxs-lookup"><span data-stu-id="4c26c-111">This allows the cost and billing to be tracked.</span></span> 

## <a name="approve-an-entry"></a><span data-ttu-id="4c26c-112">Approuver une entrée</span><span class="sxs-lookup"><span data-stu-id="4c26c-112">Approve an entry</span></span>
<span data-ttu-id="4c26c-113">Le formulaire **Approbations** vous permet de basculer entre différentes vues afin de pouvoir afficher les différents types d’approbations.</span><span class="sxs-lookup"><span data-stu-id="4c26c-113">The **Approvals** form allows you to switch between different views so that you can view the different types of approvals.</span></span>
  
1. <span data-ttu-id="4c26c-114">Accédez au formulaire **Approbations** et sélectionnez **Dépenses** , **Temps** , ou **Rappels**.</span><span class="sxs-lookup"><span data-stu-id="4c26c-114">Go to the **Approvals** form and select **Expenses** , **Time** , or **Recalls**.</span></span>
2. <span data-ttu-id="4c26c-115">Passez en revue chaque approbation et sélectionnez celles que vous souhaitez approuver.</span><span class="sxs-lookup"><span data-stu-id="4c26c-115">Review each approval, and select the ones you want to approve.</span></span>
3. <span data-ttu-id="4c26c-116">Sélectionnez **Approuver** pour approuver les entrées sélectionnées.</span><span class="sxs-lookup"><span data-stu-id="4c26c-116">Select **Approve** to approve the selected entries.</span></span>
<span data-ttu-id="4c26c-117">Le système traitera ces entrées et créera des chiffres réels ou une réservation.</span><span class="sxs-lookup"><span data-stu-id="4c26c-117">The system will process these entries and create actuals or a booking.</span></span>

## <a name="reject-an-entry"></a><span data-ttu-id="4c26c-118">Refuser une entrée</span><span class="sxs-lookup"><span data-stu-id="4c26c-118">Reject an entry</span></span>
<span data-ttu-id="4c26c-119">En tant qu’approbateur de projet, vous devrez peut-être renvoyer une entrée à un utilisateur pour correction.</span><span class="sxs-lookup"><span data-stu-id="4c26c-119">As the Project approver, you may have to send an entry back to a user for correction.</span></span>
  
1. <span data-ttu-id="4c26c-120">Accédez au formulaire **Approbations** et sélectionnez l’entrée à rejeter.</span><span class="sxs-lookup"><span data-stu-id="4c26c-120">Go to the **Approvals** form and select the entry to reject.</span></span> 
2. <span data-ttu-id="4c26c-121">Sélectionnez **Rejeter**.</span><span class="sxs-lookup"><span data-stu-id="4c26c-121">Select **Reject**.</span></span>
3. <span data-ttu-id="4c26c-122">Facultatif – Ajoutez un commentaire dans la boîte de dialogue **Commentaires de rejet** pour informer l’utilisateur de la raison pour laquelle l’entrée est rejetée.</span><span class="sxs-lookup"><span data-stu-id="4c26c-122">Optional - Add a comment in the **Rejection Comments** dialog to inform the user why the entry is being rejected.</span></span>
4. <span data-ttu-id="4c26c-123">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="4c26c-123">Select **OK**.</span></span> <span data-ttu-id="4c26c-124">L’entrée sera retournée à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4c26c-124">The entry will be returned to the user.</span></span>
  
## <a name="recall-entries"></a><span data-ttu-id="4c26c-125">Rappeler des entrées</span><span class="sxs-lookup"><span data-stu-id="4c26c-125">Recall entries</span></span>
<span data-ttu-id="4c26c-126">À un moment donné, vous devrez peut-être rappeler une entrée soumise.</span><span class="sxs-lookup"><span data-stu-id="4c26c-126">At some point, you might need to recall a submitted entry.</span></span> <span data-ttu-id="4c26c-127">Si l’entrée n’a pas été approuvée, elle sera retournée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4c26c-127">If the entry has not been approved, it will be returned immediately.</span></span> <span data-ttu-id="4c26c-128">Une entrée approuvée peut cependant avoir un impact matériel.</span><span class="sxs-lookup"><span data-stu-id="4c26c-128">An approved entry however, may have a material impact.</span></span> <span data-ttu-id="4c26c-129">L’approbateur de projet doit approuver le rappel afin d’annuler la transaction dans les chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="4c26c-129">The Project approver is required to approve the recall in order to reverse the transaction in Actuals.</span></span>

## <a name="specify-project-approvers"></a><span data-ttu-id="4c26c-130">Spécifier des approbateurs de projet</span><span class="sxs-lookup"><span data-stu-id="4c26c-130">Specify Project approvers</span></span>
<span data-ttu-id="4c26c-131">Chaque projet dispose d’un certain nombre de membres de l’équipe de projet.</span><span class="sxs-lookup"><span data-stu-id="4c26c-131">Each project has a number of project team members.</span></span> <span data-ttu-id="4c26c-132">Vous pouvez spécifier les membres de l’équipe qui sont également des approbateurs de projet.</span><span class="sxs-lookup"><span data-stu-id="4c26c-132">You can specify which team members are also Project approvers.</span></span>

1. <span data-ttu-id="4c26c-133">Accédez au formulaire **Projets** et ouvrez le projet dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4c26c-133">Go to the **Projects** form and open the project from the list.</span></span>
2. <span data-ttu-id="4c26c-134">Sur l’onglet **Équipe** , sélectionnez le membre de l’équipe qui sera un approbateur de projet, puis sélectionnez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="4c26c-134">On the **Team** tab, select the team member who will be a Project approver and then select **Edit**.</span></span>
3. <span data-ttu-id="4c26c-135">Définissez le champ **Approbateur du projet** sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="4c26c-135">Set the **Project Approver** field to **Yes**.</span></span>
4. <span data-ttu-id="4c26c-136">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4c26c-136">Select **Save**.</span></span>
5. <span data-ttu-id="4c26c-137">Répétez les étapes 2 à 4 pour ajouter des approbateurs de projet supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="4c26c-137">Repeat steps 2-4 to add additional Project approvers.</span></span>

## <a name="configure-the-users-manager"></a><span data-ttu-id="4c26c-138">Configurer le gestionnaire de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="4c26c-138">Configure the user's manager</span></span>

1. <span data-ttu-id="4c26c-139">Accédez à **Paramètres** > **Sécurité** > **Utilisateurs**.</span><span class="sxs-lookup"><span data-stu-id="4c26c-139">Go to **Settings** > **Security** > **Users**.</span></span>
2. <span data-ttu-id="4c26c-140">Sélectionnez l’utilisateur auquel vous affectez un responsable et dans la zone **Informations sur l’organisation** , sélectionnez le responsable dans la liste.</span><span class="sxs-lookup"><span data-stu-id="4c26c-140">Select the user to whom you are assigning a manager and in the **Organization Information** area, select the manager from the list.</span></span> 
3. <span data-ttu-id="4c26c-141">Sélectionnez **Enregistrer**.</span><span class="sxs-lookup"><span data-stu-id="4c26c-141">Select **Save**.</span></span>


