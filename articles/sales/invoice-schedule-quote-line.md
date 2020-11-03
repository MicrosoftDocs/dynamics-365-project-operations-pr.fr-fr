---
title: Planifications de facture sur une ligne de devis selon les projets
description: Cette rubrique fournit des informations sur la création de planifications de factures et de jalons pour les lignes de devis.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3ead79371c5ebf5801123e47dc0d24e35ae51e58
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075673"
---
# <a name="invoice-schedules-on-project-based-quote-lines"></a><span data-ttu-id="f2ffb-103">Planifications de facture sur une ligne de devis selon les projets</span><span class="sxs-lookup"><span data-stu-id="f2ffb-103">Invoice schedules on project-based quote lines</span></span>

<span data-ttu-id="f2ffb-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="f2ffb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f2ffb-105">Une ligne de devis selon les projets donne la possibilité d’exprimer une planification de facture.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-105">A project-based quote line gives the ability to express an invoice schedule.</span></span> <span data-ttu-id="f2ffb-106">Ceci est facultatif lors de la phase de devis, car l’application ne prend pas en charge la facturation d’un projet lorsqu’il est lié à une ligne de devis.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-106">This is optional during the quote phase because the application does not support invoicing a project when it is tied to a Quote line.</span></span> <span data-ttu-id="f2ffb-107">La facturation n’est autorisée qu’une fois le devis obtenu.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-107">Invoicing is only allowed after the quote is won.</span></span> <span data-ttu-id="f2ffb-108">Le seul impact en aval de la création d’une planification de facture pendant la phase de devis est que cette planification de facture est copiée dans la ligne de contrat basée sur le projet.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-108">The only downstream impact of creating an invoice schedule during the quote phase, is that this invoice schedule is copied over to the project-based contract line.</span></span> <span data-ttu-id="f2ffb-109">Si vous ne créez pas de planification de facture pendant la phase de devis, vous pourrez le faire sur la ligne du contrat selon le projet.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-109">If you do not create an invoice schedule during the quote phase, you will be able to do so on the project-based contract line.</span></span>

<span data-ttu-id="f2ffb-110">Dans l’ensemble, le but des planifications de facture est de permettre la création automatique de projets de factures pour une ligne de contrat selon un projet.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-110">Overall, the purpose of invoice schedules is to allow for the automatic creation of draft invoices for a project-based contract line.</span></span> 

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-quote-line"></a><span data-ttu-id="f2ffb-111">Créer une planification de facture de temps et de matériel pour une ligne de devis selon un projet</span><span class="sxs-lookup"><span data-stu-id="f2ffb-111">Create a Time and material invoice schedule for a project-based quote line</span></span>

<span data-ttu-id="f2ffb-112">Lorsque la méthode de facturation pour une ligne de devis selon un projet est Heure et matériel, le système génère une planification de facture basée sur la date.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-112">When the billing method for a project-based quote line is Time and material, the system generates a date-based invoice schedule.</span></span> <span data-ttu-id="f2ffb-113">Pour générer automatiquement une planification de facture basée sur la date, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-113">To automatically generate a date-based invoice schedule, complete the following steps.</span></span>

1. <span data-ttu-id="f2ffb-114">Accédez à **Paramètres** > **Fréquences de facturation** et configurez une fréquence de facturation.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-114">Go to **Settings** > **invoice frequencies** and set up an invoice frequency.</span></span>
2. <span data-ttu-id="f2ffb-115">Sur la page **Citations** , ouvrez le devis du projet et sur l’onglet **Résumé** , définissez une date de livraison demandée.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-115">On the **Quotes** page, open the Project quote and on the **Summary** tab, set a requested delivery date.</span></span>
3. <span data-ttu-id="f2ffb-116">Ouvrez la ligne de devis Heure et matériel pour laquelle vous devez créer une planification de facture basée sur la date.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-116">Open the time and material quote line that you need to create a date-based invoice schedule for.</span></span> 
4. <span data-ttu-id="f2ffb-117">Sur l’onglet **Planification de facture** , sélectionnez des valeurs dans les champs **Début de la facturation** et **Fréquence de facturation**.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-117">On the **Invoice Schedule** tab, select values in the **Billing start** and **Invoice Frequency** fields.</span></span> 
5. <span data-ttu-id="f2ffb-118">Sur la sous-grille, sélectionnez **Générer une planification de facture**.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-118">On the sub-grid, select **Generate Invoice Schedule**.</span></span>
6. <span data-ttu-id="f2ffb-119">L’application génère la planification de facture avec les champs **Date d’exécution de la facture** , **Date limite de transaction** , et **Statut d’exécution** définis de la manière suivante :</span><span class="sxs-lookup"><span data-stu-id="f2ffb-119">The application generates the invoice schedule with the **Invoice Run Date** , **Transaction Cutoff Date** , and **Run Status** fields set in the following way:</span></span>

    - <span data-ttu-id="f2ffb-120">**Date d’exécution de la facture** est défini sur la date qui est dictée en fonction de la fréquence de facturation.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-120">**Invoice Run Date** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="f2ffb-121">**Date limite de transaction** est défini sur la veille de la **Date d’exécution de la facture**.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-121">**Transaction cut-off date** is set to the day before the **Invoice Run Date**.</span></span>
    - <span data-ttu-id="f2ffb-122">**Statut d’exécution** est automatiquement défini sur **Ne pas exécuter**.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-122">**Run Status** is automatically set to **Not Run**.</span></span> <span data-ttu-id="f2ffb-123">Lorsque la tâche de création automatique de facture s’exécute pour une certaine date d’exécution de facture, elle met à jour ce champ sur **Exécution réussie** ou **Échec de l’exécution**.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-123">When the automatic invoice creation job runs for a certain invoice run date, it will update this field to either **Run Successful** or **Run Failed**.</span></span>

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-quote-line"></a><span data-ttu-id="f2ffb-124">Créer une planification de facture à prix fixe pour une ligne de devis selon un projet</span><span class="sxs-lookup"><span data-stu-id="f2ffb-124">Create a Fixed price invoice schedule for a project-based quote line</span></span>

<span data-ttu-id="f2ffb-125">Lorsque la ligne de devis selon un projet a une méthode de facturation **Fixe** , le système crée une planification de facture basée sur des jalons.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-125">When the project-based quote line has a **Fixed** billing method, the system creates a milestone-based invoice schedule.</span></span> <span data-ttu-id="f2ffb-126">Effectuez les étapes suivantes pour générer automatiquement cette planification pour un ensemble fixe de jalons qui sont également répartis pour la période calendaire.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-126">Complete the following steps to automatically generate this schedule for a fixed set of milestones that are equally distributed for the calendar period.</span></span>

1. <span data-ttu-id="f2ffb-127">Accédez à **Paramètres** > **Fréquences de facturation** et configurez une fréquence de facturation.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-127">Go to **Settings** > **invoice frequencies** and set up an invoice frequency.</span></span>
2. <span data-ttu-id="f2ffb-128">Sur la page **Citations** , ouvrez le devis du projet et sur l’onglet **Résumé** , définissez une date de livraison demandée.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-128">On the **Quotes** page, open the Project quote and on the **Summary** tab, set a requested delivery date.</span></span>
3. <span data-ttu-id="f2ffb-129">Ouvrez la ligne de devis à prix fixe pour laquelle vous devez créer une planification de jalon.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-129">Open the fixed price quote line that you need to create a milestone schedule for.</span></span> 
4. <span data-ttu-id="f2ffb-130">Sur l’onglet **Planification de facture** , sélectionnez des valeurs dans les champs **Début de la facturation** et **Fréquence de facturation**.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-130">On the **Invoice Schedule** tab, select values in the **Billing start** and **Invoice Frequency** fields.</span></span> 
5. <span data-ttu-id="f2ffb-131">Sur la sous-grille, sélectionnez **Générer des jalons périodiques**.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-131">On the sub-grid, select **Generate Periodic Milestones**.</span></span>
6. <span data-ttu-id="f2ffb-132">L’application génère la planification de facture avec un nom de jalon, une date et un montant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-132">The application generates the invoice schedule with a milestone name, date, and amount.</span></span>

    - <span data-ttu-id="f2ffb-133">Le nom du jalon est défini sur la date qui est dictée en fonction de la fréquence de facturation.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-133">The milestone name is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="f2ffb-134">La date du jalon est défini sur la date qui est dictée en fonction de la fréquence de facturation.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-134">The milestone date is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="f2ffb-135">Le montant du jalon est calculé en divisant le montant du devis sur la ligne de devis selon le projet par le nombre de jalons dicté par la fréquence et le début de la facturation et les dates de livraison demandées.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-135">The milestone amount is computed by dividing the quote amount on the project-based quote line by the number of milestones as dictated by the frequency and billing start and requested delivery dates.</span></span>
    - <span data-ttu-id="f2ffb-136">Si la ligne de devis a également un montant de taxe estimé, cette valeur est répartie de manière égale entre chaque jalon lors de la génération de jalons périodiques.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-136">If the Quote line also has as estimated tax amount, this value is split between each milestone equally when generating periodic milestones.</span></span>

### <a name="manually-create-milestones"></a><span data-ttu-id="f2ffb-137">Créer manuellement des jalons</span><span class="sxs-lookup"><span data-stu-id="f2ffb-137">Manually create milestones</span></span>

<span data-ttu-id="f2ffb-138">Les jalons à prix fixe peuvent également être générés manuellement lorsqu’ils ne sont pas périodiquement fractionnés.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-138">Fixed price milestones can also be generated manually when they are not periodically split.</span></span> <span data-ttu-id="f2ffb-139">Pour créer manuellement un jalon :</span><span class="sxs-lookup"><span data-stu-id="f2ffb-139">To create a milestone manually:</span></span>

<span data-ttu-id="f2ffb-140">Ouvrez la ligne de devis à prix fixe où vous devez créer un jalon.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-140">Open the Fixed price quote line where you need to create a milestone.</span></span> <span data-ttu-id="f2ffb-141">Sur l’onglet **Planification de facture** , dans la sous-grille, sélectionnez **+ Créer un jalon de ligne de devis** et entrez les informations requises en vous basant sur le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-141">On the **Invoice Schedule** tab, on the sub-grid, select **+ Create new quote line milestone** and enter the required information based on the following table.</span></span>

| <span data-ttu-id="f2ffb-142">**Champ**</span><span class="sxs-lookup"><span data-stu-id="f2ffb-142">**Field**</span></span> | <span data-ttu-id="f2ffb-143">**Emplacement**</span><span class="sxs-lookup"><span data-stu-id="f2ffb-143">**Location**</span></span> | <span data-ttu-id="f2ffb-144">**Pertinence, objectif et conseils**</span><span class="sxs-lookup"><span data-stu-id="f2ffb-144">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="f2ffb-145">**Impact en aval**</span><span class="sxs-lookup"><span data-stu-id="f2ffb-145">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="f2ffb-146">Nom du jalon</span><span class="sxs-lookup"><span data-stu-id="f2ffb-146">Milestone name</span></span> | <span data-ttu-id="f2ffb-147">Création rapide</span><span class="sxs-lookup"><span data-stu-id="f2ffb-147">Quick create</span></span> | <span data-ttu-id="f2ffb-148">Nom du jalon.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-148">The name of the milestone.</span></span> | <span data-ttu-id="f2ffb-149">Ceci est propagé au jalon de la ligne de contrat de projet et à la facture</span><span class="sxs-lookup"><span data-stu-id="f2ffb-149">This is propagated to the project contract line milestone and to the invoice</span></span> |
| <span data-ttu-id="f2ffb-150">Tâche du projet</span><span class="sxs-lookup"><span data-stu-id="f2ffb-150">Project Task</span></span> | <span data-ttu-id="f2ffb-151">Création rapide</span><span class="sxs-lookup"><span data-stu-id="f2ffb-151">Quick create</span></span> | <span data-ttu-id="f2ffb-152">Si le jalon est lié à la tâche de projet, vous pouvez utiliser cette référence pour ajouter une logique personnalisée et définir le statut du jalon en fonction du statut de la tâche.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-152">If the milestone is tied to project task, you can use this reference to add custom logic set the milestone status based on the task status.</span></span> | <span data-ttu-id="f2ffb-153">L’application n’a pas d’impact en aval de cette référence à une tâche.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-153">The application, does not have any downstream impact of this reference to a task.</span></span> |
| <span data-ttu-id="f2ffb-154">Date du jalon</span><span class="sxs-lookup"><span data-stu-id="f2ffb-154">Milestone date</span></span> | <span data-ttu-id="f2ffb-155">Création rapide</span><span class="sxs-lookup"><span data-stu-id="f2ffb-155">Quick create</span></span> | <span data-ttu-id="f2ffb-156">Définissez la date à laquelle le processus de création automatique de facture doit rechercher le statut de ce jalon pour le prendre en compte pour la facturation.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-156">Set the date on which the automatic invoice creation process should look for the status of this milestone to consider it for invoicing.</span></span> | <span data-ttu-id="f2ffb-157">Ceci est propagé au jalon de la ligne de contrat de projet et à la facture.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-157">This is propagated to the project contract line milestone and to the invoice.</span></span> |
| <span data-ttu-id="f2ffb-158">Statut de la facture</span><span class="sxs-lookup"><span data-stu-id="f2ffb-158">Invoice status</span></span> | <span data-ttu-id="f2ffb-159">Création rapide</span><span class="sxs-lookup"><span data-stu-id="f2ffb-159">Quick create</span></span> | <span data-ttu-id="f2ffb-160">Lorsqu’un jalon est créé, ce statut est toujours défini sur **Non prêt pour la facturation**.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-160">When a milestone is created, this status is always set to **Not ready for invoicing**.</span></span> | <span data-ttu-id="f2ffb-161">Ceci est propagé au jalon de la ligne de contrat de projet et à la facture.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-161">This is propagated to the project contract line milestone and to the invoice.</span></span> |
| <span data-ttu-id="f2ffb-162">Montant de la ligne</span><span class="sxs-lookup"><span data-stu-id="f2ffb-162">Line Amount</span></span> | <span data-ttu-id="f2ffb-163">Création rapide</span><span class="sxs-lookup"><span data-stu-id="f2ffb-163">Quick create</span></span> | <span data-ttu-id="f2ffb-164">Montant ou valeur du jalon qui sera facturé au client.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-164">Amount or value of the milestone that will be invoiced to the customer.</span></span> | <span data-ttu-id="f2ffb-165">Ceci est propagé au jalon de la ligne de contrat de projet et à la facture.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-165">This is propagated to the project contract line milestone and to the invoice.</span></span> |
| <span data-ttu-id="f2ffb-166">Taxes</span><span class="sxs-lookup"><span data-stu-id="f2ffb-166">Tax</span></span> | <span data-ttu-id="f2ffb-167">Création rapide</span><span class="sxs-lookup"><span data-stu-id="f2ffb-167">Quick create</span></span> | <span data-ttu-id="f2ffb-168">Montant de taxe qui sera appliqué au jalon.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-168">Tax amount that will be applied to the milestone.</span></span> | <span data-ttu-id="f2ffb-169">Ceci est propagé au jalon de la ligne de contrat de projet et à la facture.</span><span class="sxs-lookup"><span data-stu-id="f2ffb-169">This is propagated to the project contract line milestone and to the invoice.</span></span> |