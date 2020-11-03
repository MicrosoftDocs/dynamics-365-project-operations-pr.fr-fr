---
title: Publier une note de frais
description: Cette rubrique explique comment publier une note de frais dans la comptabilité.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075886"
---
# <a name="post-an-expense-report"></a>Publier une note de frais

[!include [banner](../includes/banner.md)]

Une fois qu'une note de frais a été approuvée et transférée dans la feuille comptabilité, elle peut être publiée dans la comptabilité. Lorsque vous publiez une note de frais, les dépenses éligibles au recouvrement de la taxe sur la valeur ajoutée (TVA) sont identifiées. La tâche de vérification et de récupération des paiements de TVA est confiée au salarié qui est chargé de vérifier la note de frais.

Si les dépenses sur une note de frais sont imputées à une société autre que celle qui emploie l'employé, vous devez vérifier la société à laquelle ces dépenses sont dues et la société qui les doit. Par exemple, l’employé qui a soumis une note de frais travaille pour la société DAT mais a facturé une dépense à la société DIR. Dans ce cas, DAT est l’entreprise à laquelle la dépense est due et DIR est l’entreprise à laquelle la dépense est due. Après avoir vérifié ces lignes de journal, vous pouvez enregistrer les lignes de dépenses dans la comptabilité.

Pour valider une note de frais, sur la page **Notes de frais approuvées** , sélectionnez la note de frais, puis, dans le volet Actions, sélectionnez **Valider**.

Vous pouvez également valider toutes les notes de frais de la liste en même temps. Sélectionnez toutes les notes de frais, puis sélectionnez **Valider**.
