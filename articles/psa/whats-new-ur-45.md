---
title: Nouveautés ou modifications de la mise à jour (version 45) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Microsoft Dynamics 365 Project Service Automation version 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169154"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Nouveautés ou modifications de la mise à jour (version 45) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour de Project Service Automation version 45, V3. Cette version a le numéro de build V3.10.76.168 et est généralement disponible par le biais d’une mise à jour automatique en juillet 2022.

## <a name="update-release-45"></a>Mise à jour (version 45)

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.

**Vente**

- Les utilisateurs ne peuvent pas créer de factures après avoir essayé de créer une facture sans aucune vente non facturée, s'ils consultent également la même instance de la page et ne l'actualisent pas.

**Temps et dépenses**

- Lorsque Modern Approvals est activé et qu'une approbation de projet rappelée est approuvée, l'étape d'enregistrement est incorrectement mise à jour pour **Rappeler la demande approuvée**.
- Lorsque Modern Approvals est activé et que Cloud Flows est inactif, le processus d'approbation échoue et les utilisateurs qui soumettent ou approuvent ne sont pas avertis.
