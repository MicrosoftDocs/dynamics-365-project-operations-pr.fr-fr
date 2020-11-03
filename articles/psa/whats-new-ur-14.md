---
title: Nouveautés ou modifications de la mise à jour (version 14) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique donne des informations sur les nouveautés de la mise à jour (version 14) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075698"
---
# <a name="project-service-automation-update-release-14-v3"></a>Mise à jour (version 14) de Project Service Automation, V3
Nous sommes heureux d'annoncer la dernière mise à jour de l'application Dynamics 365 Project Service Automation (PSA). Cette version comprend des améliorations importantes de la qualité, des performances et de l'utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez le centre d'administration de Dynamics 365 Online et accédez à la page des solutions pour installer la mise à jour. Pour plus d'informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 14) de PSA V3. Cette version a le numéro de build V3.10.4.21 et est disponible selon le calendrier suivant :

- **Disponibilité générale (mise à jour automatique) :** janvier 2020
- **Mise à jour automatique :** février 2020

## <a name="update-release-14"></a>Mise à jour (version 14)

### <a name="enhancements"></a>Améliorations

- Ventes

     - Les valeurs de champ personnalisées dans **Détails de la ligne de devis** sont copiées dans **Détails de la ligne de contrat du projet** lorsqu'un devis est mis à jour sur **Fermé comme conclu**.
     - Les projets confirmés peuvent être **Fermés comme perdus**.

- Gestion des ressources

     - Lors de l'extension des réservations, les utilisateurs seront invités par le biais d'une boîte de dialogue de confirmation à résumer les résultats de la réservation et à fournir un lien vers la fonctionnalité Gérer les réservations.


### <a name="bug-fixes"></a>Correctifs de bogues

- Temps et dépenses

     - Correction : amélioration de l'expérience utilisateur lorsque l'utilisateur n'a sélectionné aucune entrée à corriger.

- Gestion des ressources

     - Correction : la réservation d'une ressource à plusieurs reprises remplace le nom de la ressource réservable.

- Ventes

     - Correction : le prix de vente total n'est calculé que lorsque l'utilisateur entre également un prix de revient pour les estimations de dépenses d'un projet.
     - Correction : la fermeture d'un devis comme **Conclu** échoue si le contrat de projet associé n'est pas à l'état **Brouillon**.

