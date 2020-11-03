---
title: Dépenses intersociétés
description: Un travailleur qui est employé par une entité juridique dans une organisation peut effectuer un travail pour une autre entité juridique de la même organisation. Dans ce cas, vous pouvez utiliser la fonction de dépense intersociétés pour affecter les dépenses du travailleur à l'entité juridique pour laquelle le travail a été effectué.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075891"
---
# <a name="intercompany-expenses"></a>Dépenses intersociétés

[!include [banner](../includes/banner.md)]

Un travailleur qui est employé par une entité juridique dans une organisation peut effectuer un travail pour une autre entité juridique de la même organisation. Dans ce cas, vous pouvez utiliser la fonction de dépense intersociétés pour affecter les dépenses du travailleur à l'entité juridique pour laquelle le travail a été effectué. L'entité juridique qui emploie le travailleur s'appelle l'entité juridique prêteuse. L'entité juridique pour laquelle le travailleur engage des dépenses est appelée l'entité juridique emprunteuse. 

Avant qu'un travailleur puisse créer et soumettre des dépenses pour un travail effectué pour une autre entité juridique, dans l'entité juridique prêteuse, sur la page **Paramètres de gestion des dépenses** , sélectionnez l'option **Autoriser les lignes de dépenses intersociétés**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Écriture fiscale pour les dépenses intersociétés

[!include [banner](../includes/banner.md)]

Si vous souhaitez utiliser des groupes de taxes associés à l'entité juridique de prêt (source) au lieu de l'entité juridique emprunteuse (de destination) dans votre note de frais, vous devrez les configurer dans la configuration de la taxe de vente de la comptabilité. Lorsque le paramètre de comptabilité est sélectionné, **Entité juridique pour la comptabilisation fiscale intersociétés** est défini sur **Source** et **Appliquer les règles d'imposition de la taxe de vente** est défini sur **Non** , la combinaison fiscale de la personne morale prêteuse sera utilisée. Lorsque le même paramètre est défini sur **Destination** , la combinaison fiscale pour la personne morale emprunteuse sera utilisée. Pour les personnes morales aux États-Unis, lorsque le paramètre est défini sur **Source** , le champ **Taxe déductible** doit également être configuré sur la page **Groupes de validations dans la comptabilité**. Le moteur de comptabilité utilisera les informations de ce champ pour la saisie comptable liée aux taxes.   
Le comportement est cohérent pour les lignes de dépenses validées avec ou sans projet.  
