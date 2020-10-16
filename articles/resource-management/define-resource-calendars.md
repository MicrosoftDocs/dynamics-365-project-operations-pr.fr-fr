---
title: Définir les calendriers de ressources
description: Cette rubrique fournit des informations sur la définition des calendriers d’heures de travail pour les ressources dans Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ab39d7e5dc2d8c01ed49ca0f1a4d1691aaf15637
ms.sourcegitcommit: 396e0fea2f1598a5313cb0128eca4fe0bb5aade9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961856"
---
# <a name="define-resource-calendars"></a>Définir les calendriers de ressources

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Chaque ressource réservable travaillant sur un projet doit disposer d’un calendrier d’heures de travail pour définir sa disponibilité. Les heures de travail d’une ressource peuvent être définies de deux manières : 

   - Définir des règles de calendrier individuelles pour une ressource
   - Appliquer un modèle de calendrier existant pour la ressource

## <a name="define-a-resources-working-hours"></a>Définir les heures de travail d’une ressource

1. Sur le menu **Ressources**, sélectionnez **Ressources**.
2. Dans la vue de la grille, sélectionnez la **Ressource réservable** applicable.
3. Sur la page **Détails de la ressource**, sélectionnez l’onglet **Heures d’ouverture**. Par défaut, le calendrier des ressources réservables utilise par défaut les heures de travail du modèle d’heures de travail par défaut défini pour l’organisation.
4. Pour mettre à jour les heures de travail, cliquez avec le bouton droit sur la date de début de la règle de calendrier proposée à définir. Utilisez le menu des règles de calendrier pour définir une règle de calendrier pour un jour spécifique, le reste de la série ou le calendrier entier.
5. Une fois l’option sélectionnée, vous pouvez définir :

    - Le jour de la semaine où les heures de travail s’appliqueront.
    - Les temps de travail dans chaque jour.
    - Fuseau horaire local de la règle de calendrier.
    - Le cas échéant, le temps non travaillé peut également être spécifié pour la règle.

## <a name="applying-a-calendar-template-to-a-resource"></a>Application d’un modèle de calendrier à une ressource

1. Sur le menu **Ressources**, sélectionnez **Ressources**.
2. Dans la vue en grille, sélectionnez jusqu’à 25 **Ressources réservables** à mettre à jour.
3. Sélectionnez **Définir le calendrier** et une boîte de dialogue vous proposera une liste des modèles d’heures de travail disponibles.
4. Sélectionnez le modèle à utiliser, puis sélectionnez **Appliquer**.
