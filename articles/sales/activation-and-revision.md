---
title: Activer et réviser un devis de projet
description: Cet article fournit des informations sur la façon d’activer et de réviser les devis dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e71102078832ac7d5f8e5edb40cc484df927eda4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410333"
---
# <a name="activate-and-revise-a-project-quote"></a>Activer et réviser un devis de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Les fonctionnalités d’activation et de révision vous aident à suivre la gestion des versions des devis basés sur des projets pendant les phases d’estimation et de négociation. Lorsqu’un brouillon de devis est activé, il passe en lecture seule.

Les fonctionnalités d’activation et de révision vous aident à effectuer les tâches suivantes :

- Gagnez ou perdez des devis uniquement après l’activation.
- Révisez un devis pour apporter des modifications au devis existant ou créer une nouvelle version.

> [!NOTE]
> Une fois la fonctionnalité d’activation et de révision des devis activée, elle ne peut pas être désactivée.

Pour activer la possibilité d’activer et de réviser les devis basés sur des projets, procédez comme suit.

1. Accédez à **Paramètres** \> **Paramètres**.
1. Ouvrir l’enregistrement **Paramètres**.
1. Dans le volet Actions, sur l’onglet **Contrôle des fonctionnalités**, sélectionnez **Activer l’activation et la révision des devis**.
1. Dans la boîte de dialogue de confirmation, sélectionnez **OK**.
1. Après quelques instants, actualisez votre navigateur. Les capacités d’activation et de révision devraient maintenant être disponibles. Vous saurez que ces fonctionnalités ont été activées si le bouton **Activer l’activation et la révision des devis** n’apparaît plus dans le volet Actions.

## <a name="activating-a-quote"></a>Activation d’un devis

Une fois la fonction d’activation et de révision des devis activée, les boutons **Fermer un devis comme conclu** et **Fermer un devis comme perdu** du volet Actions ne sont pas disponibles pour les brouillons de devis de projet. Ils ne sont disponibles qu’après l’activation d’un devis.

L’activation représente l’étape du processus de devis à laquelle vous souhaitez empêcher d’autres modifications du devis. À ce stade, le devis est envoyé pour examen interne ou au client.

Les boutons **Fermer un devis comme conclu** et **Fermer un devis comme perdu** du volet Actions sont disponibles pour les devis activés. Selon le résultat de l’examen interne ou client, vous pouvez utiliser l’un de ces boutons pour fermer un devis activé. Vous pouvez négocier et modifier les devis activés en sélectionnant **Réviser le devis**.

## <a name="revising-a-quote"></a>Réviser un devis

Si vous devez apporter des modifications à un devis activé, sélectionnez **Réviser un devis**. Le devis est clos et le code de motif **révisé** est utilisé. Un devis est alors créé avec le même ID et un numéro de révision incrémenté. Tous les détails du devis d’origine sont copiés dans la nouvelle version. Le nouveau devis est à l’état de brouillon et peut être modifié au besoin.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
