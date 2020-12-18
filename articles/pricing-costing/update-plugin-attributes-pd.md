---
title: Mettre à jour les attributs de plug-in avec de nouvelles dimensions de tarification
description: Cette rubrique donne des informations sur la manière de mettre à jour des attributs de plug-in pour les dimensions de tarification.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643215"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="32304-103">Mettre à jour les attributs de plug-in avec de nouvelles dimensions de tarification</span><span class="sxs-lookup"><span data-stu-id="32304-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="32304-104">Cette rubrique donne des informations sur la manière de mettre à jour des attributs de plug-in pour les dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="32304-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="32304-105">Cette rubrique s'applique uniquement aux fonctionnalités de devis et de contrat dans Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="32304-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="32304-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="32304-106">Prerequisites</span></span>
<span data-ttu-id="32304-107">Avant de suivre les étapes de cette rubrique, vous devez avoir terminé les procédures décrites dans les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="32304-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="32304-108">Créer des champs et des entités personnalisés</span><span class="sxs-lookup"><span data-stu-id="32304-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="32304-109">Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles </span><span class="sxs-lookup"><span data-stu-id="32304-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="32304-110">[Configurer des champs personnalisés comme dimensions de tarification ](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="32304-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="32304-111">Si vous n’avez pas effectué ces procédures, effectuez-les, puis revenez à cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="32304-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="32304-112">Enregistrer un plug-in</span><span class="sxs-lookup"><span data-stu-id="32304-112">Register a plug-in</span></span>
<span data-ttu-id="32304-113">Lorsqu'un détail de ligne de devis est créé sur la page **Ligne de devis** pour une ligne de devis de projet, le système crée deux lignes d'estimation.</span><span class="sxs-lookup"><span data-stu-id="32304-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="32304-114">Une ligne est pour le côté coût de l'estimation et l'autre ligne est pour le côté ventes.</span><span class="sxs-lookup"><span data-stu-id="32304-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="32304-115">La même procédure s’applique aux lignes de contrat du projet.</span><span class="sxs-lookup"><span data-stu-id="32304-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="32304-116">Lorsque vous modifiez la quantité ou un champ dans la partie Coût, cette modification est aussi propagée à la partie Vente.</span><span class="sxs-lookup"><span data-stu-id="32304-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="32304-117">Cela est possible car les plug-ins PreOperation sur Quotelinedetail et les entités de détail de ligne de contrat connectent des attributs spécifiques du côté des coûts au côté des ventes de la transaction.</span><span class="sxs-lookup"><span data-stu-id="32304-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="32304-118">Si vous souhaitez que les modifications apportées aux valeurs de dimension de tarification du côté des ventes soient également apportées du côté des coûts, les plug-ins suivants doivent être réenregistrés après avoir apporté des modifications à une dimension de tarification.</span><span class="sxs-lookup"><span data-stu-id="32304-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="32304-119">Voici les plug-ins à mettre à jour et à réenregistrer :</span><span class="sxs-lookup"><span data-stu-id="32304-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="32304-120">PreOperationContractLineDetailUpdate - **Met à jour msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="32304-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="32304-121">PreOperationQuoteLineDetailUpdate - **Met à jour msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="32304-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="32304-122">Effectuez les étapes suivantes pour mettre à jour et réenregistrer les plug-ins.</span><span class="sxs-lookup"><span data-stu-id="32304-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="32304-123">Ouvrez **PluginRegistrationTool** et connectez-vous à votre environnement Dataverse Project Operations.</span><span class="sxs-lookup"><span data-stu-id="32304-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="32304-124">Sélectionnez **Rechercher** et tapez les premières lettres du plug-in à mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="32304-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="32304-125">Une fois le plug-in trouvé, sélectionnez-le, puis cliquez sur **Sélectionner sur le formulaire principal**.</span><span class="sxs-lookup"><span data-stu-id="32304-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="32304-126">Sélectionnez l’étape **Update msdyn_orderlinetransaction**, cliquez avec le bouton droit, puis sélectionnez **Mettre à jour**.</span><span class="sxs-lookup"><span data-stu-id="32304-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="32304-127">Dans la boîte de dialogue **Mettre à jour**, sélectionnez les trois points (**...**) dans les attributs de filtrage.</span><span class="sxs-lookup"><span data-stu-id="32304-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="32304-128">La fenêtre des attributs de filtrage s'ouvre et fournit une liste de tous les attributs de l'entité et des dimensions de tarification.</span><span class="sxs-lookup"><span data-stu-id="32304-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="32304-129">Cochez les cases des attributs de dimension de tarification.</span><span class="sxs-lookup"><span data-stu-id="32304-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="32304-130">Cliquez sur **OK** pour fermer la page, puis sélectionnez **Mettre à jour l’étape**.</span><span class="sxs-lookup"><span data-stu-id="32304-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="32304-131">Répétez les étapes 2 à 7 pour le deuxième plug-in, **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="32304-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="32304-132">Pour ce plug-in, vous devez mettre à jour l'étape **Update of msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="32304-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="32304-133">Fermez **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="32304-133">Close **PluginRegistrationTool**.</span></span>
