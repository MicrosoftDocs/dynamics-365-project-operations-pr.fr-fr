---
title: Vérifier les ressources proposées
description: Cet article explique comment proposer des ressources de projet.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183971"
---
# <a name="review-proposed-resources"></a>Vérifier les ressources proposées

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Les gestionnaires de ressources peuvent proposer une ressource au chef de projet à l’aide d’une demande de ressource.

Pour vérifier les ressources proposées, procédez comme suit :

1. Dans la grille **Demande** ou la demande elle-même, sélectionnez **Rechercher des ressources**.
2. Sur la page **Assistant Planifier**, sélectionnez la ressource, puis vérifiez que toutes les heures proposées sont incluses dans la réservation proposée.
3. Dans le volet **Créer une réservation de ressource**, définissez le champ **Statut de réservation** sur **Proposé**, puis sélectionnez **Réserver**.

    > [!NOTE]
    > Le fait de définir le **Statut de réservation** sur **Proposé** ne réserve pas la ressource et ne remplace pas la ressource générique par le membre de l’équipe nommé.

    Les mises à jour de statut suivantes se produisent :

    - Sur la page **Assistant de planification**, les indicateurs de statut sont mis à jour pour indiquer que la réservation est proposée, et non pas réservée fermement.
    - Sur la demande de ressources, l'examinateur de la demande doit remplace le statut par **Révision nécessaire**.
    - Sur l’onglet **Équipe** du projet, la valeur **Statut de la demande** du membre d’équipe générique est automatiquement remplacée par **Révision nécessaire**.

Le chef du projet peut accepter ou rejeter la proposition.

Lorsque les gestionnaires de ressources traitent des demandes de ressources, ils peuvent utiliser l’une des approches suivantes :

- Proposer plusieurs ressources pour satisfaire la demande si aucune ressource n’est disponible pour accomplir les heures requises. Les heures proposées sont alors fractionnées entre plusieurs ressources qui peuvent satisfaire les heures obligatoires. Dans ce scénario, les heures ne peuvent pas se chevaucher.
- Proposer moins de ressources que requis. Dans ce scénario, la capacité des ressources proposées est inférieure aux heures requises spécifiées par le demandeur. Lorsque le demandeur accepte les ressources proposées, un besoin en ressources non satisfait est créé pour capturer la demande restante.
- Réserver plusieurs ressources pour satisfaire la demande si aucune ressource n’est disponible pour effectuer les tâches.
- Réserver moins de ressources que nécessaire. Dans ce scénario, les heures réservées sont inférieures aux heures requises. Le système vous guide pour proposer des ressources plutôt que des réservations, afin que le demandeur puisse vérifier et assurer le suivi de la demande restante.

## <a name="resource-availability"></a>La disponibilité des ressources

Les gestionnaires de ressources doivent pouvoir afficher la disponibilité des ressources et mettre à jour les réservations. Dans certains cas, il n’y a pas de demande formelle (demande de ressources). Cependant, un gestionnaire de ressources doit répondre à une demande imprévue qui provient d’autres canaux tels que les e-mails, les appels téléphoniques ou les messages instantanés. Les gestionnaires de ressources utilisent le **Tableau de planification** pour mettre à jour les ressources et les réservations.

Les heures de travail des ressources sont utilisées comme base pour calculer la disponibilité d’une ressource. Les réservations de ressource consomment la capacité des ressources.

Le **Tableau de planification** utilise des couleurs et de l’ombrage pour afficher les réservations, la disponibilité et les surréservations, ainsi que le statut des réservations. Un paramètre sur le **Tableau de planification** permet d’afficher une légende.

Si une flèche pointant vers la droite apparaît en regard d’une ressource réservable individuelle sur le **Tableau de planification**, la ressource peut être développée pour afficher les détails du travail pour lequel la ressource est réservée.

Comme Dynamics 365 Project Operations utilise le moteur Universal Resource Scheduling, si vous avez également Dynamics 365 Field Service installé, vous pouvez afficher les détails des réservations de ressource des projets, des ordres de travail, ainsi que les autres entités auxquelles vous avez étendu la planification.

Pour afficher plus de détails sur une ressource spécifique, cliquez dessus avec le bouton droit pour ouvrir la carte correspondante.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
