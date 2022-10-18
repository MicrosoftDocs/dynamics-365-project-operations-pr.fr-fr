---
title: Processus de conversion de planification de projet Project Service Automation vers Project Operations
description: Cet article offre une vue d’ensemble des changements de fonctionnalités de Microsoft Dynamics 365 Project Service Automation vers Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642565"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Processus de conversion de planification de projet Project Service Automation vers Project Operations

Une fois qu’un projet a été mis à niveau avec succès de Microsoft Dynamics 365 Project Service Automation 3.X vers Dynamics 365 Project Operations Lite, il n’est pas possible de modifier les tâches de projet dans la structure de répartition du travail (WBS) de la grille des tâches. Les clients pourront consulter les WBS dans la grille de suivi où de nouveaux champs ont été ajoutés pour fournir tous les détails liés à la tâche. Pour les projets où des modifications de WBS sont nécessaires, vous pouvez convertir de manière sélective les projets éligibles vers la nouvelle expérience de planification de Project for the Web.

## <a name="project-conversion-process"></a>Processus de conversion de projet

Pour convertir un projet, procédez comme suit.

1. Ouvrez la page principale du projet et sélectionnez **Convertir** dans le volet Actions.
1. Dans la boîte de message de confirmation, sélectionnez **OK** pour commencer la conversion du projet. Les actions suivantes se produisent :

    1. Une barre de message qui apparaît sur la page principale du projet indique : « La planification du projet est en cours de conversion. Vous ne pouvez pas apporter de modifications au projet tant que la conversion n’est pas terminée. »
    1. Vous êtes redirigé vers la liste de projets.

    Une fois la conversion du projet terminée, les actions suivantes se produisent :

    1. Le chef de projet affecté reçoit une notification sur le côté droit de l’application.
    1. La barre de message indiquant que la conversion est en cours est supprimée.
    1. L’onglet **Planifier** affiche la nouvelle expérience de planification avec Project for the Web. Tout utilisateur disposant des licences et des rôles de sécurité appropriés peut modifier WBS.
    1. Le champ **Moteur de planification** est mis à jour sur **Project for the Web**.
    1. Le bouton **Convertir** est supprimé du volet Actions.

> [!IMPORTANT]
> La conversion en bloc de projets n’est pas autorisée. Toute tentative de mise à jour d’un grand nombre de projets en même temps sera limitée. Cette limitation aide à garantir des performances élevées pour tous les clients.

## <a name="manual-tasks-vs-automatic-tasks"></a>Tâches manuelles et tâches automatiques

Lorsqu’un environnement est mis à niveau de Project Service Automation vers Project Operations, toutes les tâches de WBS sont considérées comme automatiquement planifiées. Le concept de tâches planifiées manuellement n’est pas disponible dans Project for the Web. Cependant, vous pouvez définir le comportement de planification préféré pour vos projets en utilisant le paramètre [Mode de planification](/project-management/scheduling-modes.md) lorsque vous créez de nouveaux projets.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Opérations restreintes pour les projets de préconversion

Cette section décrit les différences fonctionnelles auxquelles vous pouvez vous attendre lorsque les projets n’ont pas été convertis.

### <a name="copy-project"></a>Copier le projet

L’opération **Copier** n’est prise en charge que sur les projets convertis. Les projets mis à niveau ne peuvent pas être copiés avant la conversion.

### <a name="move-project"></a>Déplacer le projet

Une modification de la date de début d’un projet ne déplacera pas proportionnellement le début des tâches à moins que le projet ait été converti.

## <a name="frequently-asked-questions"></a>Questions fréquentes

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Quelles sont les différences entre les projets convertis et les nouveaux projets créés une fois la mise à niveau terminée ?

Pour les projets convertis après la mise à niveau de l’environnement, une balise sera définie pour indiquer à la planification de ne respecter que le calendrier du projet. Ce comportement correspond au comportement dans Project Service Automation. Cependant, la balise ne sera pas définie pour les nouveaux projets créés après la mise à niveau. Par conséquent, la planification respectera les heures de travail des ressources lorsqu’elles sont affectées à une tâche.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Que dois-je faire si mon projet n’a pas pu être converti ?

Si votre projet n’a pas pu être converti, la première étape consiste à consulter les journaux d’erreurs pour identifier les problèmes courants liés à votre WBS. Si les journaux n’indiquent pas d’erreur spécifique sur laquelle vous pouvez agir, contactez le service clientèle afin que votre cas puisse être examiné plus en détail.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Comment les heures de fermeture des bureaux sont-elles gérées dans Project for the Web ?

Project for the Web ne respecte pas les heures de fermeture des bureaux définies par l’entreprise au niveau de l’organisation. Cependant, il respectera les autres types de congés définis dans un modèle d’heure de travail donné.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Quelles sont les limitations de Project for the Web ?

Voir [Créer une structure de répartition du travail : limitations du projet](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Puis-je m’attendre à des changements dans mes estimations de coût et de vente ?

Dans les rares cas où les contours d’affectation de ressources sont recalculés ou lorsqu’ils tombent dans une limite de date différente de celle du projet source, vous pouvez constater des différences dans les estimations de vente et de coût. Dans le cadre du processus de mise à niveau, les clients doivent tester un échantillon représentatif de projets, afin qu’ils puissent comprendre les changements de planification potentiels.
