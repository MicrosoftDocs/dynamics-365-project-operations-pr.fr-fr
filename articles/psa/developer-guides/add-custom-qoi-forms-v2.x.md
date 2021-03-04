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
ms.openlocfilehash: 31986efed81892cc5722cb8f5e292cde14d8843d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144590"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>Ajouter de nouveaux formulaires d'entité personnalisée (Project Service Automation 2.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

## <a name="type-field"></a>Champ Type 

Dynamics 365 Project Service Automation s'appuie sur le champ **Type** (**msdyn\_ordertype**) des entités Opportunité, Devis, Commande et Facture pour distinguer les versions **basées sur le travail** de ces entités des versions des **basées sur les articles** et **basées sur le service**. Les versions basées sur le travail de ces entités sont gérées par PSA. Un grande partie de la logique métier côté client et côté serveur de la solution dépend du champ **Type**. Par conséquent, il est important que le champ soit initialisé avec une valeur appropriée lorsque les entités sont créées. Une valeur incorrecte peut entraîner des comportement incorrects, et une partie de la logique métier peut ne pas fonctionner correctement.

## <a name="automatic-form-switching"></a>Changement automatique de formulaire

Pour éviter une corruption potentielles des données et des comportement inattendus engendrés par une initialisation et une édition incorrectes des enregistrements d'entité des ventes, PSA inclut désormais une logique de basculement automatique entre les formulaires prêts à l'emploi. Cette logique fait basculer les utilisateurs vers le formulaire approprié pour utiliser la version basée sur le travail ou tout autre type d'entité Opportunité, Devis, Commande ou Facture. Lorsqu'un utilisateur ouvre la version basée sur le travail d'une entité Opportunité, Devis, Commande ou Facture, le passage du formulaire bascule vers **Informations sur le projet**.

La logique de basculement automatique entre les formulaires s'appuie sur le mappage entre la valeur **formId** et le champ **msdyn\_ordertype**. Tous les formulaires prêts à l'emploi ont été ajoutés à ce mappage. Toutefois, les formulaires personnalisés doivent être ajoutés manuellement pour indiquer la version de l'entité qu'ils prévoient de gérer. Ceci est basé sur le champ **msdyn\_ordertype**. Si le basculement entre formulaires est manquant du mappage, la logique bascule vers le formulaire prêt à l'emploi, selon la valeur enregistrée dans le champ **msdyn\_ordertype** de l'entité.

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>Ajouter des formulaires personnalisés et activer la logique de basculement entre les formulaires

Cet exemple explique comment ajouter un formulaire personnalisé, **Mes informations de projet**, de manière à l'adapter aux opportunités basées sur le travail. Le même processus est utilisé pour ajouter des formulaires personnalisés afin qu'ils s'exécutent avec des devis, des commandes et des factures.

Suivez les étapes ci-dessous pour créer une version personnalisée du formulaire **Informations sur le projet**.

1. Dans l'entité Opportunité, ouvrez le formulaire **Informations sur le projet**, puis enregistrez une copie nommée **Mes informations de projet**.
2. Ouvrez le nouveau formulaire, puis, dans les propriétés, vérifiez que les scripts d'initialisation de formulaire du formulaire **Informations sur le projet** sont présents. 

    > [!IMPORTANT]
    > Ne supprimez pas les scripts. Sinon, certaines données peuvent être initialisées incorrectement.

3. Vérifiez que le champ **Type** (**msdyn\_ordertype**) existe dans le formulaire. 

    > [!IMPORTANT]
    > Ne supprimez pas ce champ. Sinon, les scripts d'initialisation échoueront.

4. Recherchez la valeur **formId** du nouveau formulaire. Vous avez effectuer cette étape de deux manières :

    - Exportez le formulaire **Mes informations de projet** dans le cadre d'une solution non gérée, puis recherchez la valeur **formId** dans le fichier customization.xml de la solution exportée.
    - Ouvrez le formulaire **Mes informations de projet** dans l'éditeur de formulaires, puis recherchez l'identificateur global unique (GUID) à côté du paramètre **fromId** dans l'URL, comme présenté dans l'illustration qui suit.

    ![Valeur formId du nouveau formulaire dans l'URL](media/how-to-add-custom-forms-in-v2.0.png)

5. Créez un mappage **msdyn\_ordertype** pour la valeur **formId** en modifiant la ressource web msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js. Supprimez le code de la ressource, et remplacez-le par le code suivant.

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

6. Enregistrez, puis publiez les personnalisations.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]