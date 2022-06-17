---
title: Nouveautés ou modifications de la mise à jour (version 39) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Microsoft Dynamics 365 Project Service Automation version 39, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/20/2022
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
ms.openlocfilehash: d5b5938762d98acaead9e26c47bce07e0059faf6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922449"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-39-v3"></a>Nouveautés ou modifications de la mise à jour (version 39) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour de Project Service Automation version 39, V3. Cette version a le numéro de build V3.10.60.170 et est généralement disponible par mise à jour automatique en janvier 2022.

## <a name="update-release-39"></a>Mise à jour (version 39)

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.

**GÉNÉRAL**

- Plusieurs améliorations ont été apportées au plan du site pour la traduction arabe.

**Gestion du projet**

- Une erreur se produit lorsque vous remplacez le chef de projet d’un projet par un utilisateur qui fait déjà partie de l’équipe du projet.

**Vente**

- Le propriétaire de la **Liste de prix du contrat de projet** est incorrect lorsque la liste de prix est créée automatiquement. 
- La date d’effet d’une liste de prix n’est pas respectée lorsque la liste de prix est appliquée au paramètre de projet.
- L’unité contractante peut ne pas avoir la bonne valeur par défaut lors de la modification de deux devis distincts.
