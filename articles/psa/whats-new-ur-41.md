---
title: Nouveautés ou modifications de la mise à jour (version 41) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Microsoft Dynamics 365 Project Service Automation version 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930545"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Nouveautés ou modifications de la mise à jour (version 41) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour de Project Service Automation version 41, V3. Cette version a le numéro de build V3.10.62.162 et sera disponible partout par mise à jour automatique en mars 2022.

## <a name="update-release-41"></a>Mise à jour (version 41)

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.

**Gestion du projet**
- Lorsque vous tentez de créer un projet à partir d’un modèle basé sur un projet créé à partir du complément de bureau, l’erreur suivante s’affiche : « Validation du champ Travail planifié de l’affectation des ressources : la date de fin de chaque tranche de temps d’affectation des ressources ne doit pas être antérieure à sa date de début Date ».

**Temps et dépenses**
- Lorsque vous essayez de supprimer une entrée de temps, le message d’erreur suivant s’affiche : « Une erreur inattendue s’est produite à partir du code ISV ».

**Vente**
- Lorsque vous créez une facture pour un jalon à prix fixe, les champs **Description** et **Description externe** ne sont pas remplis. 
