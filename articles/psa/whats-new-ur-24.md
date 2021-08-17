---
title: Nouveautés ou modifications de la mise à jour (version 24) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 24) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 51d08dd147b7804cb5c9255159aeab2ecd94f4597d6e99c5fa92efe1246c44d0
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998053"
---
# <a name="project-service-automation-update-release-24-v3"></a>Mise à jour (version 24) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 24) de Project Service Automation V3. Cette version a le numéro de build V3.10.42.43 et est généralement disponible par mise à jour automatique en octobre 2020.

## <a name="update-release-24"></a>Mise à jour (version 24)

### <a name="bug-fixes"></a>Corrections de bogues

**Ventes**

Les problèmes suivants ont été résolus :

- Problème lors de la définition des tarifs par défaut des produits.
- Les performances en matière de devis remportés sont lentes en raison de la copie intégrée des tarifs et des enregistrements Prix du rôle.
- **Contrat de projet/Centre des ventes** > **Ligne de produit/Quantité ligne de commande** est automatiquement arrondi à l’entier le plus proche.
- Élevez les privilèges système lors de la lecture des tarifs.
- Copiez les champs d’adresse client **address1_freighttermscode** et **address1_shippingmethodcode** vers Devis/Commande. 


**Temps et dépenses**

Les problèmes suivants ont été résolus :

- La **Grille d’entrée de temps** ne prend pas en charge le comportement **Date uniquement**.
- Le champ **Entrée de temps** ne s’actualise pas automatiquement. Une actualisation manuelle est requise.
- Impossible d’importer les entrées de temps d’une affectation en cas de pause (0 heure) dans les affectations d’une ressource.
- Lors de la création d’une entrée de temps, définissez le début sur **msdyn_date**.
- Réactivez la modification en bloc pour l’entrée de temps.

**Gestion des ressources**

Les problèmes suivants ont été résolus :

- Essayer de mettre à jour le statut d’une réservation interjournalière sans besoin lève une exception de référence nulle.
- Erreur lors du chargement de la **Vue de rapprochement**.


**Gestion du projet**

Les problèmes suivants ont été résolus :

- Dans le **Calendrier du projet**, lors du passage du mode **Manuel** au mode **Automatique**, l’enregistrement automatique ne se fait pas.
- Les frais ne doivent pas être calculés en fonction de la variance **Grille de suivi de projet**.
- Comportement incohérent pour les colonnes **Balise des estimations** lors du chargement et de la modification du type **Phase de temps**.
- Le coût réel d’un projet peut ne pas refléter les totaux de **Chiffres réels**.
- **Date de fin estimée** sur l’onglet **Résumé** ne correspond pas au **Calendrier WBS**.
- **Mettre à jour les heures réelles** sur retrait négatif ne fonctionne pas correctement.
- Un chef de projet en dehors de la racine **UO** ne peut pas créer un projet.
- Les modifications apportées à la tâche ou à la catégorie sur **Estimations des frais** ne sont pas conservées.
- **Copie du contrat** copie les calendriers de facturation et le statut d’exécution.
- Le bouton **Actualiser les statistiques** ne calcule pas correctement les tâches récapitulatives.
- Complément Microsoft Project : correction d’une erreur de référence nulle si un membre de l’équipe a une unité de ressources vide.



[!INCLUDE[footer-include](../includes/footer-banner.md)]