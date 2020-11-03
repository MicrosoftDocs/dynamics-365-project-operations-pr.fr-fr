---
title: Entrée de dépense (simplifiée)
description: Cette rubrique fournit des informations sur la façon d’utiliser la saisie de dépenses dans un déploiement simplifié.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075624"
---
# <a name="expense-entry-lite"></a>Entrée de dépense (simplifiée)

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

La gestion de base ou simplifiée des dépenses est la capacité d’enregistrer des dépenses simples. Vous pouvez enregistrer les dépenses par rapport à un projet, puis l’approbateur de projet les examinera et les approuvera.

Pour plus d’informations sur les fonctionnalités de dépense dans Project Operations Dynamics 365, voir [Vue d’ensemble des dépenses](expense-overview.md).

## <a name="capture-a-basic-expense"></a>Capturer une dépense de base

Vous pouvez capturer vos dépenses afin de pouvoir les envoyer à l’approbateur.

1. Accédez à **Dépenses** et sélectionnez **Nouveau**.
2. Sur la page **Nouvelle dépense** , entrez les informations sur la dépense requise, puis cliquez sur **Enregistrer**.

## <a name="submit-a-basic-expense"></a>Envoyer une dépense de base

Une fois que vous avez fini de saisir toutes vos dépenses et que vous êtes prêt à les faire approuver, vous devez les envoyer.

1. Accédez à **Dépenses** et sélectionnez une dépense. Sinon, sélectionnez toutes les dépenses en utilisant la case à cocher sur l’en-tête.
2. Sélectionnez **Soumettre**. Le système traite les entrées sélectionnées, puis crée des demandes d’approbation des dépenses.

## <a name="recall-a-basic-expense"></a>Rappeler une dépense de base

Lorsque vous envoyez une dépense par erreur, vous pouvez la rappeler. Le temps nécessaire pour rappeler une entrée de dépense dépend de son stade d’approbation.  Si l’approbateur n’a pas encore approuvé l’entrée, le rappel peut avoir lieu immédiatement. Cependant, si l’entrée a déjà été approuvée, l’approbateur est invité à approuver le rappel et à annuler les transactions.

1. Accédez à **Dépenses** , puis, dans la liste des dépenses, sélectionnez la dépense à rappeler.
2. Sélectionnez **Rappeler**. Si l’entrée de dépenses n’a pas encore été approuvée, le système la rappelle immédiatement. Si l’écriture de dépenses a déjà été approuvée, une demande de rappel est créée pour informer l’approbateur que vous souhaitez annuler la dépense. L’approbateur confirmera alors que l’annulation peut être effectuée et l’entrée sera renvoyée.

## <a name="delete-a-basic-expense"></a>Supprimer une dépense de base

Les dépenses qui n’ont pas encore été envoyées peuvent être supprimées. Pour supprimer une dépense déjà envoyée, vous devez d’abord la rappeler.

## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble des approbations](../approvals/approvals-overview.md)
