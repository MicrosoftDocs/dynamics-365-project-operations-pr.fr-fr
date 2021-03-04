---
title: Dépenses intersociétés
description: Cette rubrique fournit des informations sur l'utilisation des dépenses intersociétés pour affecter les dépenses du collaborateur à l’entité juridique pour laquelle le travail a été effectué.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960829"
---
# <a name="intercompany-expenses"></a>Dépenses intersociétés

Un collaborateur employé par une entité juridique d’une organisation peut effectuer du travail pour une autre entité juridique de la même organisation. Vous pouvez utiliser les dépenses intersociétés pour affecter les dépenses du collaborateur à l’entité juridique pour laquelle le travail a été effectué. L'entité juridique qui emploie le travailleur s'appelle l'entité juridique prêteuse. L'entité juridique pour laquelle le travailleur engage des dépenses est appelée l'entité juridique emprunteuse. 

Avant qu'un collaborateur puisse créer et soumettre des dépenses intersociétés, vous devez activer les lignes de dépenses intersociétés. Dans l'entité juridique prêteuse, sur la page **Paramètres de gestion des dépenses**, sélectionnez **Autoriser les lignes de dépenses intersociétés**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Écriture fiscale pour les dépenses intersociétés

[!include [banner](../includes/banner.md)]

Avant de pouvoir utiliser des groupes taxe associés à l’entité juridique (source) prêteuse au lieu de l’entité juridique (destination) emprunteuse dans votre note de frais, vous devez activer la fonctionnalité dans le Paramètres de taxe comptabilité. Lorsque le paramètre **Entité juridique pour la validation des taxes intersociétés** est défini sur **Source** et que le champ **Appliquer les règles de taxe** est défini sur **Non**, la combinaison fiscale de l’entité juridique prêteuse est utilisée. Lorsque le même paramètre est défini sur **Destination**, la combinaison fiscale pour la personne morale emprunteuse sera utilisée. Pour les personnes morales aux États-Unis, lorsque le paramètre est défini sur **Source**, le champ **Taxe déductible** doit également être configuré sur la page **Groupes de validations dans la comptabilité**. Le moteur de comptabilité utilisera les informations de ce champ pour la saisie comptable liée aux taxes.   
Le comportement est cohérent pour les lignes de dépenses validées avec ou sans projet.  
