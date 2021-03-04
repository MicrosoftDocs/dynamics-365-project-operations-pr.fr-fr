---
title: Comment personnaliser le flux des processus d’entreprise des phases du projet ?
description: Vue d’ensemble de la personnalisation du flux des processus d’entreprise des phases du projet.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149000"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="756bd-103">Comment personnaliser le flux des processus d’entreprise des phases du projet ?</span><span class="sxs-lookup"><span data-stu-id="756bd-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="756bd-104">Il existe une limitation connue dans les précédentes versions de l’application Project Service que les noms des phases dans le flux des processus d’entreprise des phases du projet doivent correspondre exactement aux noms anglais attendus (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="756bd-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="756bd-105">Sinon, la logique métier, qui repose sur les noms de la phase en anglais, ne fonctionne pas comme prévu.</span><span class="sxs-lookup"><span data-stu-id="756bd-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="756bd-106">C’est la raison pour laquelle des actions familières comme **Changer de processus** ou **Modifier le processus** n’apparaissent pas comme disponibles dans le formulaire du projet, et que la personnalisation du flux des processus d’entreprise n’est pas encouragée.</span><span class="sxs-lookup"><span data-stu-id="756bd-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="756bd-107">Cette limite a été traitée dans la version 2.4.5.48 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="756bd-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="756bd-108">Cet article fournit des solutions suggérées pour les versions antérieures si vous devez personnaliser le flux des processus d’entreprise par défaut.</span><span class="sxs-lookup"><span data-stu-id="756bd-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="756bd-109">La logique métier nécessite un correspondance exacte avec des noms de phase en anglais</span><span class="sxs-lookup"><span data-stu-id="756bd-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="756bd-110">Le flux des processus d’entreprise des phases du projet inclut une logique métier qui pilote les comportements suivants dans l’application :</span><span class="sxs-lookup"><span data-stu-id="756bd-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="756bd-111">Lorsque le projet est associé à un devis, le code définit le flux des processus d’entreprise sur la phase **Quote**.</span><span class="sxs-lookup"><span data-stu-id="756bd-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="756bd-112">Lorsque le projet est associé à un contrat, le code définit le flux des processus d’entreprise sur la phase **Plan**.</span><span class="sxs-lookup"><span data-stu-id="756bd-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="756bd-113">Lorsque le flux des processus d’entreprise est avancé à la phase **Close**, l’enregistrement du projet est désactivé.</span><span class="sxs-lookup"><span data-stu-id="756bd-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="756bd-114">Lorsque le projet est désactivé, le formulaire et la structure de répartition du travail (WBS) du projet sont définis sur lecture seule, les réservations de ressources nommées sont libérées, et tous les tarifs associés sont désactivés.</span><span class="sxs-lookup"><span data-stu-id="756bd-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="756bd-115">Cette logique métier repose sur les noms en anglais des phases du projet.</span><span class="sxs-lookup"><span data-stu-id="756bd-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="756bd-116">Cette dépendance aux noms de phase en anglais est la principale raison pour laquelle la personnalisation du flux des processus d’entreprise des phases du projet n’est pas encouragée, de même que les actions de flux des processus d’entreprise courantes comme **Changer de processus** ou **Modifier le processus** n’apparaissent pas sur l’entité du projet.</span><span class="sxs-lookup"><span data-stu-id="756bd-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="756bd-117">Que se passe -t-il si les noms de phase ne correspondent pas aux noms en anglais ?</span><span class="sxs-lookup"><span data-stu-id="756bd-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="756bd-118">Dans la version 1.x de l’application Project Service sur la plateforme 8.2, lorsque les noms de phase du flux des processus d’entreprise ne correspondent pas exactement aux noms de phase en anglais, la logique métier qui définit la phase appropriée pour les devis ou les contrats, ou qui ferme le projet, est ignorée.</span><span class="sxs-lookup"><span data-stu-id="756bd-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="756bd-119">Aucun message d’erreur ne s’affiche.</span><span class="sxs-lookup"><span data-stu-id="756bd-119">No error messages are displayed.</span></span> <span data-ttu-id="756bd-120">Par conséquent il semble que vous puissiez personnaliser le flux des processus d’entreprise de phases du projet.</span><span class="sxs-lookup"><span data-stu-id="756bd-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="756bd-121">Toutefois, vous ne verrez aucun des processus automatiques travailler sur des devis, des contrats, et la fermeture de projet.</span><span class="sxs-lookup"><span data-stu-id="756bd-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="756bd-122">Dans la version 2.4.4.30 de l’application Project Service ou version antérieure sur la plateforme 9.0, une modification de l’architecture cruciale a été apportée aux flux des processus d’entreprise, qui nécessitait une réécriture de la logique métier de flux des processus d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="756bd-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="756bd-123">Par conséquent, si les noms de phase de processus ne correspondent pas aux noms en anglais attendus, vous recevez un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="756bd-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="756bd-124">Si vous souhaitez personnaliser le flux des processus d’entreprise de phase du projet pour l’entité de projet, vous pouvez donc uniquement ajouter de toutes nouvelles étapes au flux des processus d’entreprise par défaut pour l’entité de projet, tout en conservant les phases **Quote**, **Plan**, and **Close** actuelles.</span><span class="sxs-lookup"><span data-stu-id="756bd-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="756bd-125">Cette restriction garantit que vous ne receviez pas d’erreurs de la logique métier qui prévoit des noms de phase en anglais dans le flux des processus d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="756bd-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="756bd-126">Dans la version 2.4.5.48 ou ultérieure, la logique métier décrite dans cet article a été supprimée du flux des processus d’entreprise par défaut pour l’entité de projet.</span><span class="sxs-lookup"><span data-stu-id="756bd-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="756bd-127">La mise à niveau vers cette version ou une version ultérieure vous permettra personnaliser ou de remplacer le flux des processus d’entreprise par défaut par l’un des vôtres.</span><span class="sxs-lookup"><span data-stu-id="756bd-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="756bd-128">Solutions pour les versions antérieures</span><span class="sxs-lookup"><span data-stu-id="756bd-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="756bd-129">Si la mise à niveau n’est pas une option, vous pouvez personnaliser le flux des processus d’entreprise des phases du projet pour l’entité de projet de l’une des deux manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="756bd-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="756bd-130">Ajoutez des étapes supplémentaires à la configuration par défaut, tout en conservant les noms de phase en anglais pour **Quote**, **Plan**, and **Close**.</span><span class="sxs-lookup"><span data-stu-id="756bd-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Capture d’écran de l’ajout d’étapes à la configuration par défaut](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="756bd-132">Créez votre propre flux des processus d’entreprise et faites-en le flux des processus d’entreprise principal de l’entité de projet, ce qui vous permet d’avoir tous les noms de phase de votre choix.</span><span class="sxs-lookup"><span data-stu-id="756bd-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="756bd-133">Toutefois, si vous souhaitez utiliser les mêmes étapes de projet standard **Quote**, **Plan**, and **Close**, vous devez effectuer certaines personnalisations qui sont exclues des noms de phase personnalisés.</span><span class="sxs-lookup"><span data-stu-id="756bd-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="756bd-134">La logique la plus complexe consiste à fermer le projet, que vous pouvez toujours déclencher en désactivant simplement l’enregistrement de projet.</span><span class="sxs-lookup"><span data-stu-id="756bd-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![Personnalisation de BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="756bd-136">Considérations supplémentaires pour la version 2.4.4.30 de l’application Project Service ou version antérieure sur la plateforme 9.0</span><span class="sxs-lookup"><span data-stu-id="756bd-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="756bd-137">Dans la version 2.4.4.30 de Project Service ou version antérieure sur la plateforme 9.0, avec un flux des processus d’entreprise personnalisé, le champ **Nom de la phase** sur l’entité de projet utilisée dans les vues de listes de graphique et de projet **Projet par phase** ne sera pas mis à jour, car il est couplé au flux des processus d’entreprise des étapes du projet par défaut.</span><span class="sxs-lookup"><span data-stu-id="756bd-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="756bd-138">Vous pouvez gérer ce problème avec la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="756bd-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="756bd-139">Ajoutez un champ personnalisé pour capturer l’étape actuelle du flux des processus d’entreprise qui est mise à jour à mesure que l’utilisateur avance dans le flux des processus d’entreprise personnalisé.</span><span class="sxs-lookup"><span data-stu-id="756bd-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="756bd-140">Modifiez le graphique **Projet par phase** en fonction de votre champ personnalisé au lieu de la configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="756bd-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="756bd-141">Étapes pour créer votre propre flux des processus d’entreprise pour l’entité de projet</span><span class="sxs-lookup"><span data-stu-id="756bd-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="756bd-142">Pour créer votre propre flux des processus d’entreprise pour l’entité de projet, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="756bd-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="756bd-143">Accédez à **Paramètres** > **Centre de traitement**.</span><span class="sxs-lookup"><span data-stu-id="756bd-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="756bd-144">Ne copiez pas le flux des processus d’entreprise des phases du projet, car cela copie également la logique métier Project Service.</span><span class="sxs-lookup"><span data-stu-id="756bd-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Créer un processus](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="756bd-146">Utilisez le concepteur de processus pour créer les noms de phase de votre choix.</span><span class="sxs-lookup"><span data-stu-id="756bd-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="756bd-147">Si vous souhaitez la même fonctionnalité que les phases par défaut pour **Quote**, **Plan**, and **Close**, vous devrez créer cela en fonction des noms de phase de votre flux des processus d’entreprise personnalisé.</span><span class="sxs-lookup"><span data-stu-id="756bd-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Capture d’écran du concepteur de processus utilisé pour personnaliser le flkux des processus d’entreprise](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="756bd-149">Dans le concepteur de processus, cliquez sur **Ordre des flux des processus** pour faire du flux des processus d’entreprise personnalisé le flux des processus d’entreprise principal pour l’entité de projet en le plaçant au-dessus du flux des processus d’entreprise des phases du projet au haut de la liste.</span><span class="sxs-lookup"><span data-stu-id="756bd-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="756bd-150">Capture d’écran de l’utilisation du flux des processus de commande</span><span class="sxs-lookup"><span data-stu-id="756bd-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="756bd-151">Les étapes suivantes s’appliquent à l’application 2.4.4.30 de Project Service ou version antérieure sur la plateforme 9.0</span><span class="sxs-lookup"><span data-stu-id="756bd-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="756bd-152">Ajoutez un nouveau champ personnalisé à l’entité de projet pour capturer les phases personnalisées de votre flux des processus d’entreprise personnalisé.</span><span class="sxs-lookup"><span data-stu-id="756bd-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="756bd-153">Vous devez ajouter une logique métier (plug-in/workflow) pour mettre à jour ce champ lorsque la phase du flux des processus d’entreprise personnalisé est mise à jour.</span><span class="sxs-lookup"><span data-stu-id="756bd-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Capture d’écran de la personnalisation de l’entité de projet](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="756bd-155">Modifiez le graphique **Projet par phase** pour utiliser votre nouveau champ personnalisé pour les étapes.</span><span class="sxs-lookup"><span data-stu-id="756bd-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Capture d’écran de l’utilisation du graphique Projet par phase](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="756bd-157">Modifiez les vues de l’entité de projet pour inclure votre nouveau champ personnalisé pour les étapes.</span><span class="sxs-lookup"><span data-stu-id="756bd-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Capture d’écran de la modification des vues sur l’entité du projet](media/FAQ-Customize-BPF-8-720.png)

