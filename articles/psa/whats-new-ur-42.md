---
title: Nouveautés ou modifications de la mise à jour (version 42) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de la version 42, V3 de Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/05/2022
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
ms.openlocfilehash: 32cb7a4c5fc29d5c0dcec37dd395ae69037435a2
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589193"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-42-v3"></a>Nouveautés ou modifications de la mise à jour (version 42) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 42), V3 de Project Service Automation. Cette version a le numéro de build V3.10.73.61 et est généralement disponible via une mise à jour automatique en avril 2022.

## <a name="update-release-42"></a>Mise à jour (version 42)

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.

**Temps et dépenses**

- Lorsqu’une feuille de temps est rejetée, l’utilisateur qui l’a rejetée est incorrectement identifié comme **Système**.
- Lorsque les entrées de temps sont importées, la valeur **Catégorie de ressource** est manquante.
- Les approbateurs de projet peuvent approuver les projets soumis lorsque leurs autorisations ne sont pas spécifiquement définies sur **Peut approuver**.

**Vente**

- Lorsque les valeurs réelles sont consignées sur des tâches de niveau non racine, les coûts réels sont agrégés de manière incorrecte.
