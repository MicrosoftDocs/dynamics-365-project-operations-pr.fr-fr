---
title: Sécurité et approbations
description: Cet article fournit des informations sur la configuration de la sécurité pour l’utilisation des approbations dans Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841920"
---
# <a name="security-and-approvals"></a>Sécurité et approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Microsoft Dynamics 365 Project Operations utilise deux rôles de sécurité pour permettre l’approbation des entrées de temps, de dépenses et de matériel :

- Approbateur du projet
- Administrateur approbateur du projet

## <a name="project-approver"></a>Approbateur du projet

Vous devez avoir le rôle de sécurité **Approbateur de projet** pour approuver les entrées de temps, de dépenses et de matériel du projet. Vous devez également avoir accès aux entités associées pertinentes, telles que **Projet**. Cet accès peut être attribué par un utilisateur avec le rôle **Chef de projet**. De plus, vous devez être un membre de l’équipe du projet et marqué comme approbateur.

Pour approuver les entrées non liées à un projet, vous devez être le responsable de l’expéditeur.

## <a name="project-approver-admin"></a>Administrateur approbateur du projet

> [!NOTE]
> La fonctionnalité [Ensembles d’approbation](approval-sets.md) doit être activée avant de pouvoir utiliser la fonctionnalité Administrateur approbateur de projet.

Le rôle de sécurité **Administrateur approbateur de projet** permet aux utilisateurs de contourner les politiques et autorise l’approbation des entrées dans tous les projets. L’attribution de ce rôle contourne la logique de validation qui nécessite l’appartenance à une équipe et le fait d’être marqué comme approbateur. Vous devez avoir accès aux tables associées pertinentes, telles que **Projet**, via les rôles de sécurité qui vous sont attribués.

Le contexte utilisateur SYSTEM contourne les validations de la même manière que le rôle de sécurité Administrateur approbateur de projet.
