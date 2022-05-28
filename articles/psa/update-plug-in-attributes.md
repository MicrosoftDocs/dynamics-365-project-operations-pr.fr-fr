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
ms.reviewer: johnmichalak
ms.openlocfilehash: 0c9ac219dd19cf5dd14d54b199329de0c15fe2ae
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580868"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a>Mettre à jour les attributs de plug-in pour inclure de nouvelles dimensions de tarification

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> Si vous n’utilisez pas les fonctionnalités Devis et Contrat de Project Service Automation (PSA), vous pouvez ignorer cette rubrique.

Cette rubrique suppose que vous avez effectué les procédures décrites dans les rubriques, [Créer des champs et des entités personnalisés](create-custom-fields-entities.md), [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles](field-references.md) et [Configurer des champs personnalisés comme dimensions de tarification](set-up-pricing-dimensions.md). Si vous n’avez pas effectué ces procédures, revenez en arrière et effectuez-les, puis revenez à cette rubrique.

Lorsqu’un détail de ligne de devis est créé sur la page **Ligne de devis** pour une ligne de devis du projet, le système crée deux lignes d’estimation en arrière-plan : une ligne pour la partie Coût de l’estimation et une pour la partie Vente. La même procédure s’applique aux lignes de contrat du projet.

Lorsque vous modifiez la quantité ou un champ dans la partie Coût, cette modification est propagée à la partie Vente. Cela est possible en raison des plug-ins suivants qui doivent enregistrés à nouveau après une modification des dimensions de tarification.

- PreOperationContractLineDetailUpdate - Met à jour **msdyn_orderlinetransaction**.
- PreOperationQuoteLineDetailUpdate - Met à jour **msdyn_quotelinetransaction**.

Les étapes suivantes vous guident tout au long du processus d’enregistrement des plug-ins.

1. Ouvrez **PluginRegistrationTool** et connectez-vous à votre instance en ligne.
2. Cliquez sur **Rechercher** et recherchez le plug-in à mettre à jour.

 ![Capture d’écran de l’arborescence de recherche.](media/PRT-1.png)

3. Une fois le plug-in trouvé, sélectionnez-le, puis cliquez sur **Sélectionner sur le formulaire principal**.

4. Sélectionnez l’étape du plug-in à mettre à jour, cliquez avec le bouton droit, puis sélectionnez **Mettre à jour**.

 ![Capture d’écran du plug-in à mettre à jour.](media/PRT-2.png)
 
5. Dans la fenêtre de mise à jour, cliquez sur le bouton de sélection (**...**) dans les attributs de filtrage.

 ![Capture d’écran de la mise à jour des informations de configuration de l’étape existante.](media/PRT-3.png)
 
6. Activez les cases à cocher des attributs de tarification.

 ![Capture d’écran illustrant les cases à cocher activées pour les attributs de tarification.](media/PRT-4.png)

7. Cliquez sur **OK** pour fermer la page, puis sélectionnez **Mettre à jour l’étape**.

 ![Capture d’écran illustrant le bouton Mettre à jour l’étape.](media/PRT-5.png)
 
8. Répétez cette procédure pour le deuxième plug-in, **PreOperationQuoteLineDetail - Mise à jour de msdyn_quotelinetransaction**.

9. Fermez Plug-in Registration Tool.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
