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
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274680"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Mettre à jour les attributs de plug-in avec de nouvelles dimensions de tarification

Cette rubrique donne des informations sur la manière de mettre à jour des attributs de plug-in pour les dimensions de tarification.

> [!NOTE]
> Cette rubrique s'applique uniquement aux fonctionnalités de devis et de contrat dans Dynamics 365 Project Operations.

## <a name="prerequisites"></a>Conditions préalables
Avant de suivre les étapes de cette rubrique, vous devez avoir terminé les procédures décrites dans les rubriques suivantes :

  - [Créer des champs et des entités personnalisés](create-custom-fields-entities-pricing-dimensions.md) 
  - [Ajouter des champs personnalisés au paramétrage de tarifs et aux entités transactionnelles ](add-custom-fields-price-setup-transactional-entities.md)
  - [Configurer des champs personnalisés comme dimensions de tarification ](set-up-custom-fields-pricing-dimensions.md). 
  
Si vous n’avez pas effectué ces procédures, effectuez-les, puis revenez à cette rubrique.

## <a name="register-a-plug-in"></a>Enregistrer un plug-in
Lorsqu'un détail de ligne de devis est créé sur la page **Ligne de devis** pour une ligne de devis de projet, le système crée deux lignes d'estimation. Une ligne est pour le côté coût de l'estimation et l'autre ligne est pour le côté ventes. La même procédure s’applique aux lignes de contrat du projet.

Lorsque vous modifiez la quantité ou un champ dans la partie Coût, cette modification est aussi propagée à la partie Vente. Cela est possible car les plug-ins PreOperation sur Quotelinedetail et les entités de détail de ligne de contrat connectent des attributs spécifiques du côté des coûts au côté des ventes de la transaction. Si vous souhaitez que les modifications apportées aux valeurs de dimension de tarification du côté des ventes soient également apportées du côté des coûts, les plug-ins suivants doivent être réenregistrés après avoir apporté des modifications à une dimension de tarification.

Voici les plug-ins à mettre à jour et à réenregistrer :

- PreOperationContractLineDetailUpdate - **Met à jour msdyn_orderlinetransaction**
- PreOperationQuoteLineDetailUpdate - **Met à jour msdyn_quotelinetransaction**

Effectuez les étapes suivantes pour mettre à jour et réenregistrer les plug-ins.

1. Ouvrez **PluginRegistrationTool** et connectez-vous à votre environnement Dataverse Project Operations.
2. Sélectionnez **Rechercher** et tapez les premières lettres du plug-in à mettre à jour.
3. Une fois le plug-in trouvé, sélectionnez-le, puis cliquez sur **Sélectionner sur le formulaire principal**.
4. Sélectionnez l’étape **Update msdyn_orderlinetransaction**, cliquez avec le bouton droit, puis sélectionnez **Mettre à jour**.
5. Dans la boîte de dialogue **Mettre à jour**, sélectionnez les trois points (**...**) dans les attributs de filtrage.
6. La fenêtre des attributs de filtrage s'ouvre et fournit une liste de tous les attributs de l'entité et des dimensions de tarification. Cochez les cases des attributs de dimension de tarification.
7. Cliquez sur **OK** pour fermer la page, puis sélectionnez **Mettre à jour l’étape**.
8. Répétez les étapes 2 à 7 pour le deuxième plug-in, **PreOperationQuoteLineDetail**. Pour ce plug-in, vous devez mettre à jour l'étape **Update of msdyn_quotelinetransaction**.
9. Fermez **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]