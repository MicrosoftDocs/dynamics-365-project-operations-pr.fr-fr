---
title: Nouveautés ou modifications de la mise à jour (version 18) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Project Service Automation version 18, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918861"
---
# <a name="project-service-automation-update-release-18-v3"></a>Mise à jour (version 18) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 (en ligne) et accédez à la page des solutions pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour version 18 de Project Service Automation V3. Cette version a le numéro de build V3.10.8.12 et est généralement disponible via une mise à jour automatique en avril 2020.

## <a name="update-release-18"></a>Mise à jour (version 18)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

- Résolu : les flux **Rappeler**, **Demander** et **Annuler l’approbation** génèrent des exceptions avec des messages d’erreur peu explicites.
- Résolu : lorsque le flux **Annuler l’approbation** échoue pour une dépense, une erreur d’exception pertinente n’est pas générée.
- Résolu : la grille d’entrée de temps traite de manière incorrecte les jours non ouvrables en Australie après le passage à l’heure d’été en octobre.
- Résolu : une logique par défaut incorrecte empêche la soumission des dépenses.
- Résolu : en cas d’échec de l’approbation d’une entrée de temps, l’approbation reste à l’état **En attente**.
- Résolu : erreurs SQL pour les approbations en bloc (blocage/expiration).
- Résolu : problèmes de performances importants dans l’expérience utilisateur causés par la mise à jour des membres de l’équipe lors de l’approbation des entrées de temps.

**Gestion du projet**

- Résolu : la notification de fuseau horaire a été déplacée de la vue **Rapprochement** vers le formulaire principal **Projet**.
- Résolu : le modèle de calendrier ne prend pas la valeur par défaut correcte lors de l’ouverture d’un nouveau formulaire de projet.
- Résolu : pour les navigateurs basés sur Chrome, les utilisateurs ne peuvent pas sélectionner facilement des tâches prédécesseurs à supprimer.
- Résolu : la création ou la copie d’un **Projet à partir d’un modèle vide** extrait des affectations non liées.
- Résolu : dans des cas extrêmes spécifiques, la création d’une nouvelle affectation à partir de la grille des tâches entraîne la création d’enregistrements en double.
- Résolu : en mode manuel, les utilisateurs ne peuvent pas mettre à jour les dates de début des tâches sur une valeur postérieure à la date actuelle enregistrée.

**Gestion des ressources**

- Résolu : la ligne du sous-total de la vue **Rapprochement** calcule de manière incorrecte l’écart des réservations après extension des réservations.
- Résolu : la vue **Rapprochement** affiche de manière incorrecte les affectations de ressources lorsque la ressource réservable a un calendrier qui ne correspond pas au calendrier du projet.

**Ventes**

- Résolu : lorsque les entrées de temps sont réapprouvées (**Approuver > Annuler >** approuver à nouveau), une valeur réelle non facturable en double est créée.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
