---
title: Nouveautés ou modifications de la mise à jour (version 23) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Project Service Automation version 23, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 968626c7b2097a9b85178cb000b3633a766f54c9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913026"
---
# <a name="project-service-automation-update-release-23-v3"></a>Mise à jour (version 23) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour version 23 de Project Service Automation V3. Cette version a le numéro de build V3.10.34.30 et est généralement disponible par mise à jour automatique en août 2020.

## <a name="update-release-23"></a>Mise à jour (version 23)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus :
- Gérer le cas limite dans **Supprimer membre de l’équipe de projet** pour fournir une exception significative.
- L’importation des affectations entraîne un écran de suppression vide.

**Gestion des ressources**

Les problèmes suivants ont été résolus :

- La **carte des ressources de grille d’utilisation des ressources** présente des données incorrectes lorsque l’échelle de temps est supérieure à cinq jours.
- Lorsque les clients créent une ressource réservable, le plug-in échoue par intermittence à ajouter automatiquement la ressource à un groupe Microsoft Office 365.
- La vue **Rapprochement** n’affiche pas correctement les contours manuels dans la vue **Semaine** ou **Mois**.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- Un nombre excessif d’entités **Récupération multiple pour les paramètres de l’utilisateur** entraîne une dégradation des performances des approbations de projet et d’autres opérations.
- La recherche de ressources de grille **Planification des tâches** est limitée pour n’afficher qu’un maximum de cinq membres de l’équipe de projet. 
- La recherche de ressources de grille **Planification des tâches** ne filtre pas les ressources inactives.
- Le mode manuel ne fonctionne pas comme prévu dans la structure de répartition du travail de planification de projet.
- La grille **Planification des tâches** affiche **Catégories de transactions inactives**.
- La grille **Affectation des ressources** ne s’arrondit pas correctement lorsqu’une tâche a plusieurs affectations.
- Les valeurs d’arrondi sont différentes entre le coût planifié et le coût réel pour une seule tâche.

**Ventes**

Les problèmes suivants ont été résolus :

- Le fait de double-cliquer sur **Récupérer toutes les catégories de transactions** crée plusieurs lignes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
