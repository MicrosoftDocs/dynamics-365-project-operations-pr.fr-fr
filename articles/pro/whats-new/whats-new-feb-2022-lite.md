---
title: Nouveautés de février 2022 – Déploiement léger de Project Operations
description: Cette rubrique fournit des informations sur les mises à jour de qualité disponibles dans la version de février 2022 du déploiement simplifié de Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: af66a5f61adf4f016f3fa547bbdfc75d06b2711b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574565"
---
# <a name="whats-new-february-2022---project-operations-lite-deployment"></a>Nouveautés de février 2022 – Déploiement léger de Project Operations

_S’applique à : Déploiement simplifié – Traiter la facturation pro forma_

Ce sujet s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.28.0.120

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

À partir de cette version, vous pouvez ajouter jusqu’à 300 membres d’équipe à un seul projet. Auparavant, la limite du nombre de membres de l’équipe s’élevait à 150. Pour plus d’informations, consultez [Limites de projet](../../project-management/create-wbs.md#project-limitations).

## <a name="quality-updates"></a>Mises à jour qualité

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2497369 | La correction matérielle doit suivre la valeur de la date dans les paramètres **Correction**. |
| Facturation et tarification | 2498697 | Amélioration de la configuration de sécurité pour **Rappel d’entrée de temps**. |
| Facturation et tarification | 2517455 | L’action **Transactions de ligne de facture actualisées** ne doit pas pouvoir être déclenchée plusieurs fois simultanément pour la même facture. |
| Facturation et tarification | 2517465 | L’action **Désactiver les détails de la ligne de facture** est bloquée, car elle n’est pas prise en charge. |
| Facturation et tarification | 2556660 | Correction des vérifications d’effectivité de la date qui sont effectuées sur la liste de prix jointe à un enregistrement de paramètres de projet. |
| Gestion des opportunités | 2369202 | Correction de la logique métier qui vérifie que les listes de prix dont les dates d’effet se chevauchent peuvent être jointes au même contrat de projet. |
| Gestion des opportunités | 2385965 | Correction du comportement sur l’onglet **Clients** de la page **Contrat de projet** lorsque vous sélectionnez **Enregistrer et fermer**. |
