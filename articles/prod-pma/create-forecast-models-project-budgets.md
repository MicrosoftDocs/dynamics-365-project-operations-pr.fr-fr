---
title: Créer des modèles de prévision pour les budgets de projet
description: Cet article décrit comment créer un modèle de prévision pour les budgets restants.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e6b1419c41124d2062595f7346efb7538e50ee33
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916699"
---
# <a name="create-forecast-models-for-project-budgets"></a>Créer des modèles de prévision pour les budgets de projet 

[!include [banner](../includes/banner.md)]

Cet article décrit comment créer un modèle de prévision pour les budgets restants. Un projet soumis au contrôle budgétaire utilise deux types de budget : d’origine et restant. Lorsque vous créez un budget de projet, vous devez spécifier les modèles de prévisions budgétaires d’origine et restants qui ont été créés dans la page **Modèles de prévision**. Les budgets de projet basés sur les modèles spécifiés sont créés lorsque vous engagez le budget de projet.

> [!NOTE]
> Un modèle de prévision utilisé pour le contrôle budgétaire ne peut pas avoir de sous-modèle ou être utilisé comme sous-modèle.

1. Sélectionnez **Gestion et comptabilité des projets** > **Configurer** > **Prévisions**  > **Modèles de prévision**.
2. Sélectionnez **Nouveau** pour créer un nouveau modèle de prévision, puis entrez un numéro d’identification de modèle et un nom pour le nouveau modèle. 
3. Définissez l’option **Arrêté** sur **Oui** pour empêcher toute modification des lignes de prévision du modèle de prévision. 
4. Si les lignes de prévision auxquelles le modèle est associé doivent générer des prévisions de flux de trésorerie dans la comptabilité, définissez **Inclure dans les prévisions de flux de trésorerie** sur **Oui.** 
5. Pour utiliser la date du projet comme date de facturation, définissez **Date de facturation prévue** sur **Oui**. 
6. Dans le champ **Type de budget**, sélectionnez les types de modèles suivants :

   - **Budget d’origine** : Utilisez les montants budgétaires d’origine engagés lors de la création et de l’approbation du budget initial.
   - **Budget qui reste** : Utilisez les montants budgétaires restants pendant la durée de vie du projet. Les soldes de ce modèle de prévision sont réduits par les transactions réelles et augmentés ou diminués par les révisions budgétaires.
   - **Report** : Utilisez les montants du budget reporté pour le projet. Le report est un processus facultatif qui peut être exécuté pour transférer des montants budgétaires inutilisés d’un exercice à un autre.

7. Définissez les options suivantes comme requis :

   - Activez **Date de facturation prévue** pour utiliser la date du projet comme date de facturation.
   - Activez **Prévisions avec WIP** pour prévoir en fonction des travaux en cours (WIP), puis sélectionnez le type de WIP. 
   - Vous pouvez conserver la valeur par défaut **Type de budget** comme **Aucun** ou entrez un nouveau type. Le type de budget ne peut pas être modifié une fois que vous avez modifié un enregistrement.     
    > [!NOTE]
    > Si vous modifiez le type de budget par défaut, toutes les autres options ne seront plus disponibles pour les mises à jour et vous ne pourrez pas réutiliser ce modèle de prévision. 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]