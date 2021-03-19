---
title: Ajouter de nouveaux formulaires d'entité personnalisée (Project Service Automation 2.x)
description: Cette rubrique fournit des informations pour ajouter des formulaires d'entité personnalisée pour des opportunités, des devis, des commandes ou des factures dans Dynamics 365 Project Service Automation 2.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c9e31dc6d4d5a8ad5cc568f2d7d673c8703936d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284850"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="a9fa8-103">Ajouter de nouveaux formulaires d'entité personnalisée (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="a9fa8-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a><span data-ttu-id="a9fa8-104">Champ Type</span><span class="sxs-lookup"><span data-stu-id="a9fa8-104">Type field</span></span> 

<span data-ttu-id="a9fa8-105">Dynamics 365 Project Service Automation s'appuie sur le champ **Type** (**msdyn\_ordertype**) des entités Opportunité, Devis, Commande et Facture pour distinguer les versions **basées sur le travail** de ces entités des versions des **basées sur les articles** et **basées sur le service**.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-105">Dynamics 365 Project Service Automation relies on the **Type** (**msdyn\_ordertype**) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="a9fa8-106">Les versions basées sur le travail de ces entités sont gérées par PSA.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="a9fa8-107">Un grande partie de la logique métier côté client et côté serveur de la solution dépend du champ **Type**.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="a9fa8-108">Par conséquent, il est important que le champ soit initialisé avec une valeur appropriée lorsque les entités sont créées.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="a9fa8-109">Une valeur incorrecte peut entraîner des comportement incorrects, et une partie de la logique métier peut ne pas fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="a9fa8-110">Changement automatique de formulaire</span><span class="sxs-lookup"><span data-stu-id="a9fa8-110">Automatic form switching</span></span>

<span data-ttu-id="a9fa8-111">Pour éviter une corruption potentielles des données et des comportement inattendus engendrés par une initialisation et une édition incorrectes des enregistrements d'entité des ventes, PSA inclut désormais une logique de basculement automatique entre les formulaires prêts à l'emploi.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="a9fa8-112">Cette logique fait basculer les utilisateurs vers le formulaire approprié pour utiliser la version basée sur le travail ou tout autre type d'entité Opportunité, Devis, Commande ou Facture.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="a9fa8-113">Lorsqu'un utilisateur ouvre la version basée sur le travail d'une entité Opportunité, Devis, Commande ou Facture, le passage du formulaire bascule vers **Informations sur le projet**.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="a9fa8-114">La logique de basculement automatique entre les formulaires s'appuie sur le mappage entre la valeur **formId** et le champ **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="a9fa8-115">Tous les formulaires prêts à l'emploi ont été ajoutés à ce mappage.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="a9fa8-116">Toutefois, les formulaires personnalisés doivent être ajoutés manuellement pour indiquer la version de l'entité qu'ils prévoient de gérer.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="a9fa8-117">Ceci est basé sur le champ **msdyn\_ordertype**.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="a9fa8-118">Si le basculement entre formulaires est manquant du mappage, la logique bascule vers le formulaire prêt à l'emploi, selon la valeur enregistrée dans le champ **msdyn\_ordertype** de l'entité.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="a9fa8-119">Ajouter des formulaires personnalisés et activer la logique de basculement entre les formulaires</span><span class="sxs-lookup"><span data-stu-id="a9fa8-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="a9fa8-120">Cet exemple explique comment ajouter un formulaire personnalisé, **Mes informations de projet**, de manière à l'adapter aux opportunités basées sur le travail.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-120">The following example shows how to add a custom form, **My Project Information**, so that it works with work-based opportunities.</span></span> <span data-ttu-id="a9fa8-121">Le même processus est utilisé pour ajouter des formulaires personnalisés afin qu'ils s'exécutent avec des devis, des commandes et des factures.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="a9fa8-122">Suivez les étapes ci-dessous pour créer une version personnalisée du formulaire **Informations sur le projet**.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="a9fa8-123">Dans l'entité Opportunité, ouvrez le formulaire **Informations sur le projet**, puis enregistrez une copie nommée **Mes informations de projet**.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="a9fa8-124">Ouvrez le nouveau formulaire, puis, dans les propriétés, vérifiez que les scripts d'initialisation de formulaire du formulaire **Informations sur le projet** sont présents.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="a9fa8-125">Ne supprimez pas les scripts.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-125">Don't remove the scripts.</span></span> <span data-ttu-id="a9fa8-126">Sinon, certaines données peuvent être initialisées incorrectement.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="a9fa8-127">Vérifiez que le champ **Type** (**msdyn\_ordertype**) existe dans le formulaire.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-127">Verify that the **Type** (**msdyn\_ordertype**) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="a9fa8-128">Ne supprimez pas ce champ.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-128">Don't remove this field.</span></span> <span data-ttu-id="a9fa8-129">Sinon, les scripts d'initialisation échoueront.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="a9fa8-130">Recherchez la valeur **formId** du nouveau formulaire.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="a9fa8-131">Vous avez effectuer cette étape de deux manières :</span><span class="sxs-lookup"><span data-stu-id="a9fa8-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="a9fa8-132">Exportez le formulaire **Mes informations de projet** dans le cadre d'une solution non gérée, puis recherchez la valeur **formId** dans le fichier customization.xml de la solution exportée.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="a9fa8-133">Ouvrez le formulaire **Mes informations de projet** dans l'éditeur de formulaires, puis recherchez l'identificateur global unique (GUID) à côté du paramètre **fromId** dans l'URL, comme présenté dans l'illustration qui suit.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![Valeur formId du nouveau formulaire dans l'URL](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="a9fa8-135">Créez un mappage **msdyn\_ordertype** pour la valeur **formId** en modifiant la ressource web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="a9fa8-136">Supprimez le code de la ressource, et remplacez-le par le code suivant.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-136">Remove the code from the resource, and replace it with the following code.</span></span>

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. <span data-ttu-id="a9fa8-137">Enregistrez, puis publiez les personnalisations.</span><span class="sxs-lookup"><span data-stu-id="a9fa8-137">Save and then publish the customizations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]