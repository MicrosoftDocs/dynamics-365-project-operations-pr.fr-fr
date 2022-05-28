---
title: Nouveautés ou modifications de la mise à jour (version 40) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de la version 40, V3 de Microsoft Dynamics 365 Project Service Automation.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: 25f375ce648eb7d233f6433739832caee351830d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588641"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Nouveautés ou modifications de la mise à jour (version 40) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 40), V3 de Project Service Automation. Cette version a un numéro de build V3.10.61.61 et est généralement disponible via une mise à jour automatique en février 2022.

## <a name="update-release-40"></a>Mise à jour (version 40)

### <a name="features"></a>Fonctionnalités
La phase 1 de la mise à niveau de Project Service Automation vers Project Operations - simplifié sera publiée en février 2022 pour tous les clients. Pour vérifier l’éligibilité, voir [Effectuer une mise à niveau de Project Service Automation vers Project Operations](upgrade-project-operations-non-stocked.md). Si l’application n’apparaît pas dans votre instance dans le centre d’administration Power Platform, contactez le support et demandez que le vol soit activé pour vos environnements. Votre demande doit inclure une liste d’ID d’environnement dans lesquels le vol doit être activé.

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.

**Temps et dépenses**
- Une entrée de note est manquante lorsqu’une entrée de temps est rejetée ou annulée. 

**Vente**

- Lorsque vous mettez à jour des estimations de coûts ou de ventes à l’aide de plug-ins prêts à l’emploi, vous êtes autorisé à tort à envoyer des charges utiles JSON qui ne sont pas valides en dehors de l’interface utilisateur.
- Lorsque vous mettez à jour les lignes de devis à l’aide de la vue rapide, vous êtes autorisé à activer les devis.
