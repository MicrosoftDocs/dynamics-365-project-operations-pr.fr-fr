---
title: Nouveautés ou modifications de la mise à jour (version 37) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de la version 37, V3 de Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593471"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Nouveautés ou modifications de la mise à jour (version 37) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 37), V3 de Project Service Automation. Cette version a le numéro de build V3.10.58.120 et est mise à la disposition générale via une mise à jour automatique en novembre 2021.

## <a name="update-release-37"></a>Mise à jour (version 37)

### <a name="bug-fixes"></a>Correctifs de bogues

Les problèmes suivants ont été résolus.

**Temps et dépenses**
- Les utilisateurs ne peuvent pas supprimer une entrée de temps en effaçant la cellule.
- La vue **Mes approbations ayant échoué** ne contient que les approbations de projet avec le statut **Envoyé**.

**Gestion des projets**
- Les utilisateurs reçoivent une erreur d’exception de référence nulle lors de l’ouverture d’un projet dans le complément de bureau Microsoft si le nom du poste du membre de l’équipe du projet est vide.
- Aucun bouton **Enregistrer** n’est disponible sur la page **Tâche du projet** ; par conséquent, les utilisateurs ne peuvent pas enregistrer les modifications apportées aux enregistrements de tâche.
- Les utilisateurs ne peuvent pas supprimer un projet dont une tâche est associée à un devis avec le statut **Conclu**.

**Vente**
- Le champ **Devise** de la page **Projet** est mise à jour pour correspondre à la devise du modèle appliqué.
- Le coût est calculé de manière incorrecte dans les tâches avec plusieurs devises.
