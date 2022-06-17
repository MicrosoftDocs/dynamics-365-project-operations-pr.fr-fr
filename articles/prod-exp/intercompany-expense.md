---
title: Dépenses intersociétés
description: Cet article fournit des informations sur l’utilisation des dépenses intersociétés pour affecter les dépenses du collaborateur à l’entité juridique pour laquelle le travail a été effectué.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932385"
---
# <a name="intercompany-expenses"></a>Dépenses intersociétés

Un collaborateur employé par une entité juridique d’une organisation peut effectuer du travail pour une autre entité juridique de la même organisation. Vous pouvez utiliser les dépenses intersociétés pour affecter les dépenses du collaborateur à l’entité juridique pour laquelle le travail a été effectué. L’entité juridique qui emploie le travailleur s’appelle l’entité juridique prêteuse. L’entité juridique pour laquelle le travailleur engage des dépenses est appelée l’entité juridique emprunteuse. 

Avant qu’un collaborateur puisse créer et soumettre des dépenses intersociétés, vous devez activer les lignes de dépenses intersociétés. Dans l’entité juridique prêteuse, sur la page **Paramètres de gestion des dépenses**, sélectionnez **Autoriser les lignes de dépenses intersociétés**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Écriture fiscale pour les dépenses intersociétés

[!include [banner](../includes/banner.md)]

Avant de pouvoir utiliser des groupes taxe associés à l’entité juridique (source) prêteuse au lieu de l’entité juridique (destination) emprunteuse dans votre note de frais, vous devez activer la fonctionnalité dans le Paramètres de taxe comptabilité. Lorsque le paramètre **Entité juridique pour la validation des taxes intersociétés** est défini sur **Source** et que le champ **Appliquer les règles de taxe** est défini sur **Non**, la combinaison fiscale de l’entité juridique prêteuse est utilisée. Lorsque le même paramètre est défini sur **Destination**, la combinaison fiscale pour la personne morale emprunteuse sera utilisée. Pour les personnes morales aux États-Unis, lorsque le paramètre est défini sur **Source**, le champ **Taxe déductible** doit également être configuré sur la page **Groupes de validations dans la comptabilité**. Le moteur de comptabilité utilisera les informations de ce champ pour la saisie comptable liée aux taxes.   
Le comportement est cohérent pour les lignes de dépenses validées avec ou sans projet.  

## <a name="new-expense-expression-builder"></a>Nouveau générateur d′expressions des dépenses

Le nouveau générateur d′expressions des dépenses résout les problèmes liés aux scénarios de dépenses intersociétés qui utilisent des projets. Cette fonctionnalité garantit que, lorsque vous créez une dépense intersociétés, la stratégie de dépenses est correctement validée par rapport au projet sélectionné sur la ligne de dépenses, et la note de frais peut être soumise avec succès.

Pour que la fonctionnalité de générateur d′expressions des dépenses fonctionne, elle doit être activée. De plus, la stratégie de dépenses qui a un ID de projet doit être configurée.

Si vous avez déjà configuré des stratégies qui valident l′ID de projet sur la ligne de dépense, elles doivent être supprimées. Vous pouvez ensuite activer la fonctionnalité et reconfigurer les stratégies.

Pour activer cette fonctionnalité, suivez les étapes ci-après.

1. Accédez à **Espaces de travail** \> **Gestion des fonctionnalités**.
2. Dans la liste, sélectionnez le **nouveau générateur d′expressions des dépenses qui résout les problèmes liés aux scénarios de dépenses intersociétés qui utilisent des projets**. Sélectionnez ensuite **Activer maintenant**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
