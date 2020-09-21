---
title: Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification
description: Cette rubrique donne des informations sur la mise à jour des attributs de plug-in pour les dimensions de tarification.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: e9b7e752-39c3-4610-8ced-25d9e197b705
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 746b9978f9ae63c05e1031afc31c8134f05ec195
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168089"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification

> [!NOTE]
> Si vous n'utilisez pas les fonctionnalités Devis et Contrat de Project Service Automation (PSA), vous pouvez ignorer cette rubrique.

Cette rubrique suppose que vous avez effectué les procédures décrites dans les rubriques, [Créer des champs et des entités personnalisés](create-custom-fields-entities.md), [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](field-references.md) et [Configurer des champs personnalisés comme dimensions de tarification](set-up-pricing-dimensions.md). Si vous n'avez pas effectué ces procédures, revenez en arrière et effectuez-les, puis revenez à cette rubrique.

Lorsqu'un détail de ligne de devis est créé sur la page **Ligne de devis** pour une ligne de devis du projet, le système crée deux lignes d'estimation en arrière-plan : une ligne pour la partie Coût de l'estimation et une pour la partie Vente. La même procédure s'applique aux lignes de contrat du projet.

Lorsque vous modifiez la quantité ou un champ dans la partie Coût, cette modification est propagée à la partie Vente. Cela est possible en raison des plug-ins suivants qui doivent enregistrés à nouveau après une modification des dimensions de tarification.

- PreOperationContractLineDetailUpdate - Met à jour **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Met à jour **msdyn_quotelinetransaction**.

Les étapes suivantes vous guident tout au long du processus d'enregistrement des plug-ins.

1. Ouvrez **PluginRegistrationTool** et connectez-vous à votre instance en ligne.
2. Cliquez sur **Rechercher** et recherchez le plug-in à mettre à jour.

 ![Capture d'écran de l'arborescence de recherche](media/PRT-1.png)

3. Une fois le plug-in trouvé, sélectionnez-le, puis cliquez sur **Sélectionner sur le formulaire principal**.

4. Sélectionnez l'étape du plug-in à mettre à jour, cliquez avec le bouton droit, puis sélectionnez **Mettre à jour**.

 ![Capture d'écran du plug-in à mettre à jour](media/PRT-2.png)
 
5. Dans la fenêtre de mise à jour, cliquez sur le bouton de sélection (**...**) dans les attributs de filtrage.

 ![Capture d'écran de la mise à jour les informations de configuration de l'étape existantes](media/PRT-3.png)
 
6. Activez les cases à cocher des attributs de tarification.

 ![Capture d'écran illustrant l'activation des cases à cocher des attributs de tarification](media/PRT-4.png)

7. Cliquez sur **OK** pour fermer la page, puis sélectionnez **Mettre à jour l'étape**.

 ![Capture d'écran illustrant le bouton « Mettre à jour l'étape »](media/PRT-5.png)
 
8. Répétez cette procédure pour le deuxième plug-in, **PreOperationQuoteLineDetail - Mise à jour de msdyn_quotelinetransaction**.

9. Fermez Plug-in Registration Tool.

