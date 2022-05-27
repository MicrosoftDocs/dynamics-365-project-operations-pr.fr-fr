---
title: Nouveautés ou modifications de la mise à jour (version 21) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 21) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 34d1540639352f635068b849500a104de2509a7f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577832"
---
# <a name="project-service-automation-update-release-21-v3"></a>Mise à jour (version 21) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 21) de Project Service Automation V3. Cette version a le numéro de build V 3.10.32.50 et est généralement disponible via une mise à jour automatique en juin 2020.

## <a name="update-release-21"></a>Mise à jour (version 21)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus :

- Lors de l’hébergement du contrôle **Grille d’entrée de temps** dans les tableaux de bord, la grille n’utilise pas toute la largeur du conteneur de grille de tableau de bord.
- Pour des fuseaux horaires spécifiques, le contrôle de grille **Entrée de temps** n’affiche pas d’enregistrements.
- Les entrées de temps effectuées après 21h s’affichent le mauvais jour.
- Les utilisateurs ne peuvent pas soumettre de dépenses si la catégorie de dépense **Reçu de dépenses requis** n’a aucune valeur.

**Gestion des ressources**

Les problèmes suivants ont été résolus :

- Les réservations inactives sont affichées dans la vue **Rapprochement**.
- L’exécution des ressources génériques n’a pas été validée pour s’assurer qu’il existe un statut de réservation valide.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- Les grilles du formulaire **Projet** (**Attribution de ressource**, **Tâche**, vue **Rapprochement**, **Estimations des dépenses**) restent modifiables même lorsqu’un projet n’est pas actif.
- Les clients en double ne peuvent pas être fusionnés avec les clients liés à des contrats de projet confirmés.
- Lorsqu’une ressource sans calendrier valide est ajoutée, le système ne renvoie pas de message d’erreur convivial.
- Le bouton **Ajouter une tâche** de la grille de tâches est activé lorsque le projet est lié au **Complément Microsoft Project**.
- L’effort augmente de manière incontrôlable lorsqu’une tâche avec une catégorie est affectée à une ressource doté d’un rôle pour lequel un prix de revient est défini.

**Ventes**

Les améliorations suivantes ont été apportées :

- **Fréquence de facturation** et **Début de la facturation** ont été déplacés vers l’onglet **Calendrier de facturation**.

Les problèmes suivants ont été résolus :

- La valeur **Prix de vente total** est égale à zéro (0) pour **Catégorie** même si le champ **Rôle** a un prix de vente total différent de zéro.
- Les clients ne peuvent pas modifier la valeur du champ **Statut de la facture** en **Prêt pour la facturation** lorsqu’un autre processus personnalisé met à jour un champ supplémentaire.
- Le bouton **Actualiser les lignes de facture** peut créer plusieurs lignes dupliquées s’il est sélectionné à plusieurs reprises.
- Le bouton **Mettre à jour les prix** ne fonctionne pas dans la sous-grille **Prix du rôle** dans le formulaire **Aperçu**.
- La logique **Résolution des tarifs de vente** gère de manière incorrecte les fuseaux horaires, ce qui entraîne la sélection incorrecte des tarifs.
- Le **Coût réel total** d’un projet peut diminuer d’un montant fractionnaire après l’approbation d’une entrée de temps unique.
- La logique **Résolution du prix** ne fournit pas de message d’erreur convivial si **Prix du rôle récupéré** n’a pas de valeurs dans les champs **Unité principale** et **Prix dans l’unité principale**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
