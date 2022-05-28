---
title: Nouveautés ou modifications de la mise à jour (version 34) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 34) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: c7a4feaeebf8fa2ef3447dc6dfc3d0903266f3b2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588687"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Nouveautés ou modifications de la mise à jour (version 34) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 34) de Project Service Automation V3. Cette version a le numéro de build V3.10.55.38 et est généralement disponible par le biais d’une mise à jour automatique en juillet 2021.

## <a name="update-release-34"></a>Mise à jour (version 34)

### <a name="bug-fixes"></a>Corrections de bogues
Les problèmes suivants ont été résolus.

**GÉNÉRAL**

- Les mises à jour pilotées par les éditeurs n′activent pas le nouveau workflow d′approbation moderne.
- Les attributs **Statut de destination** et **Type d′action** sont manquants dans la page principale **Ensemble d′approbation**.

**Temps et dépenses**

- Impossible d′approuver une requête de rappel en utilisant le flux d′approbation moderne.
- La copie d′une semaine d′entrées de temps ne fonctionne pas si vous copiez des entrées non liées à l′utilisateur connecté.

**Planification de projet**

- Les contours d′affectation des ressources sont corrompus lors de l′importation à partir du complément de bureau Microsoft Project.

**Gestion des ressources**

- Si vous publiez un projet à partir du complément client de bureau Microsoft Project, la date de fin des exigences existantes est modifiée.
- La précision décimale dépasse les deux décimales dans la boîte de dialogue de confirmation des réservations étendues.

**Vente**

- Si vous ajoutez une ligne basée sur un produit avec un produit existant à un contrat de projet, une exception **clé introuvable dans le dictionnaire** s′affiche.
- Les pistes ne peuvent pas être qualifiées si un type de commande est mappé d′un prospect à une opportunité.
