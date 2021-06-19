---
title: Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification
description: Cette rubrique donne des informations sur la mise à jour des attributs de plug-in pour les dimensions de tarification.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b0d50733340f277453f4ef5b52bdd3ee089449cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012808"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="de057-103">Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="de057-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="de057-104">Si vous n’utilisez pas les fonctionnalités Devis et Contrat de Project Service Automation (PSA), vous pouvez ignorer cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="de057-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="de057-105">Cette rubrique suppose que vous avez effectué les procédures décrites dans les rubriques, [Créer des champs et des entités personnalisés](create-custom-fields-entities.md), [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](field-references.md) et [Configurer des champs personnalisés comme dimensions de tarification](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="de057-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="de057-106">Si vous n’avez pas effectué ces procédures, revenez en arrière et effectuez-les, puis revenez à cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="de057-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="de057-107">Lorsqu’un détail de ligne de devis est créé sur la page **Ligne de devis** pour une ligne de devis du projet, le système crée deux lignes d’estimation en arrière-plan : une ligne pour la partie Coût de l’estimation et une pour la partie Vente.</span><span class="sxs-lookup"><span data-stu-id="de057-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="de057-108">La même procédure s’applique aux lignes de contrat du projet.</span><span class="sxs-lookup"><span data-stu-id="de057-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="de057-109">Lorsque vous modifiez la quantité ou un champ dans la partie Coût, cette modification est propagée à la partie Vente.</span><span class="sxs-lookup"><span data-stu-id="de057-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="de057-110">Cela est possible en raison des plug-ins suivants qui doivent enregistrés à nouveau après une modification des dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="de057-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="de057-111">PreOperationContractLineDetailUpdate - Met à jour **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="de057-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="de057-112">PreOperationQuoteLineDetailUpdate - Met à jour **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="de057-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="de057-113">Les étapes suivantes vous guident tout au long du processus d’enregistrement des plug-ins.</span><span class="sxs-lookup"><span data-stu-id="de057-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="de057-114">Ouvrez **PluginRegistrationTool** et connectez-vous à votre instance en ligne.</span><span class="sxs-lookup"><span data-stu-id="de057-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="de057-115">Cliquez sur **Rechercher** et recherchez le plug-in à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="de057-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Capture d’écran de l’arborescence de recherche](media/PRT-1.png)

3. <span data-ttu-id="de057-117">Une fois le plug-in trouvé, sélectionnez-le, puis cliquez sur **Sélectionner sur le formulaire principal**.</span><span class="sxs-lookup"><span data-stu-id="de057-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="de057-118">Sélectionnez l’étape du plug-in à mettre à jour, cliquez avec le bouton droit, puis sélectionnez **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="de057-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Capture d’écran du plug-in à mettre à jour](media/PRT-2.png)
 
5. <span data-ttu-id="de057-120">Dans la fenêtre de mise à jour, cliquez sur le bouton de sélection (**...**) dans les attributs de filtrage.</span><span class="sxs-lookup"><span data-stu-id="de057-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Capture d’écran de la mise à jour les informations de configuration de l’étape existantes](media/PRT-3.png)
 
6. <span data-ttu-id="de057-122">Activez les cases à cocher des attributs de tarification.</span><span class="sxs-lookup"><span data-stu-id="de057-122">Select the pricing attribute check boxes.</span></span>

 ![Capture d’écran illustrant l’activation des cases à cocher des attributs de tarification](media/PRT-4.png)

7. <span data-ttu-id="de057-124">Cliquez sur **OK** pour fermer la page, puis sélectionnez **Mettre à jour l’étape**.</span><span class="sxs-lookup"><span data-stu-id="de057-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Capture d’écran illustrant le bouton « Mettre à jour l’étape »](media/PRT-5.png)
 
8. <span data-ttu-id="de057-126">Répétez cette procédure pour le deuxième plug-in, **PreOperationQuoteLineDetail - Mise à jour de msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="de057-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="de057-127">Fermez Plug-in Registration Tool.</span><span class="sxs-lookup"><span data-stu-id="de057-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]