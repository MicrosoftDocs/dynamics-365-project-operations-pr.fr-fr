---
title: Considérations de mise à niveau pour les approbations modernes
description: L’article couvre les points que les administrateurs doivent prendre en compte lorsqu’ils activent la fonctionnalité d’approbations modernes.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931741"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>Considérations de mise à niveau pour les approbations modernes 

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Dans le cadre de la version de la 1ère vague d’avril 2022, la fonctionnalité d’approbations modernes sera activée par défaut. Cette fonctionnalité améliore la fiabilité de la logique d’approbation et garantit que vous pouvez déterminer la raison de l’échec de la logique d’approbation.

Dans le cadre de ce changement, les changements de statut des approbations de projet sont mis à jour. Le statut va maintenant directement de **Soumis** vers **Approuvé**. **En attente** n’est plus un statut pour les approbations. Pour déterminer si une approbation est en attente, vérifiez que l’approbation fait partie d’un ensemble d’approbations et examinez l’état de l’ensemble d’approbations joint.

## <a name="before-you-upgrade"></a>Avant de procéder à la mise à niveau

Avant de passer aux approbations modernes, assurez-vous que vous n’avez aucune approbation en attente. Les approbations modernes n’utilisent pas le statut **En attente**. Par conséquent, toutes les approbations encore marquées comme **En attente** après la mise à niveau ne sera pas traitée.

## <a name="after-you-upgrade"></a>Après la mise à niveau

Après la mise à niveau vers les approbations modernes, un Administrateur doit valider que le flux de cloud qui traite les approbations a été activé.

1. Se connecter à [flow.microsoft.com](https://flow.microsoft.com)
2. Dans le coin supérieur droit de la page, basculez votre environnement vers l’environnement que vous avez mis à niveau.
3. Sélectionnez **Solutions** pour répertorier les solutions installées dans l‘environnement.
4. Dans la liste des solutions, sélectionnez **Project Operations** ou **Project Service**.
5. Remplacez le filtre **Tout** par **Flux de cloud**.
6. Vérifiez que l’option **Project Service – Planifier de manière récurrente les ensembles d’approbations du projet** est définie sur **Activé**. Si ce n’est pas le cas, sélectionnez le flux, puis **Activer**.
7. Vérifiez que le traitement a lieu toutes les cinq minutes en examinant la liste **Tâches système** dans la zone **Réglages**.

## <a name="short-term-rollback"></a>Restauration à court terme

Si vous ne parvenez pas à appliquer les modifications ou si vous rencontrez un grave problème avec cette fonctionnalité, vous pouvez temporairement revenir au processus d’approbation d’origine en procédant comme suit :
1. Connectez-vous à votre environnement et vérifiez qu’aucune approbation n’est en attente.
2. Accédez à **Réglages** > **Paramètres de projet**.
3. Sélectionnez **Contrôle des fonctionnalités**, puis sélectionnez **Approbations modernes** pour désactiver la fonction.

## <a name="removing-the-feature-flag"></a>Suppression de l’indicateur de fonctionnalité

Dans la mise à jour de la 2e vague d’octobre 2022, la possibilité de désactiver cette fonctionnalité sera supprimée.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
