---
title: Modèle de sécurité
description: Cette rubrique fournit des informations sur le modèle de sécurité dans Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e875d1765b5038e60830d626abb5bcd61749ece1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075625"
---
# <a name="security-model"></a>Modèle de sécurité

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Microsoft Dynamics 365 Project Operations contient un modèle de sécurité unique qui permet un modèle de sécurité métier basé sur les rôles qui collabore avec Microsoft Office Groups. 


## <a name="security-roles"></a>Rôles de sécurité
Les fonctionnalités frontales de Project Operations incluent les rôles suivants :

| Rôle                          | Description                                                                                                                                                                 | Portée |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| Gestionnaire des recommandations              | Prend en charge les rapports inter-projets.                                                                                                            | Unité commerciale              |
| Approbateur du projet              | Approuve les temps et les dépenses par rapport à un projet.                                                                                                                              | Unité commerciale |
| Administrateur de facturation de projet | Crée la proposition de facture.                                                                                                                                                 | Unité commerciale |
| Chef de projet               | Crée le plan de projet et demande des ressources.                                                                                                                              | Unité commerciale |
| Ressource du projet              | Membres de l’équipe qui peuvent être réservés et signalent le temps.                                                                                                          | Unité commerciale|
| Gestionnaire des ressources              | Toutes les fonctions de gestion des ressources, telles que répondre aux demandes de ressources et aux réservations, sont séparées pour prendre en charge une configuration hybride de gestionnaire de projet + gestionnaire de ressources et un rôle de gestionnaire de ressources unique et centralisé. | Unité commerciale |


Microsoft Project pour le web comprend les rôles suivants :

| Rôle           | Description                                                                                                        | Portée  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| Utilisateur du projet   | Utilisateur collaboratif de projet capable de créer ses propres projets et de visualiser tous les projets partagés avec eux. | Utilisateur   |
| Système de projet | Rôle utilisé pour le contexte de l’application. Les clients ne doivent pas utiliser ce rôle système.                                    | Global |

## <a name="security-enforcement"></a>Application de la sécurité
Les actions exécutées au niveau du projet sont effectuées dans le contexte de l’utilisateur connecté. Cela signifie que pour créer, ouvrir ou supprimer un projet, l’utilisateur doit disposer d’un accès disponible dans CDS. L’accès à CDS peut être accordé via l’un des mécanismes possibles inclus dans la plateforme. Par exemple, un utilisateur avec une plus grande portée peut accéder au projet ou si une action de partage de projet explicite a été effectuée qui accorde l’accès à l’utilisateur.

Il est important d’en tenir compte lors de la création de projets dans Project Operations.

## <a name="modern-group-collaboration-with-project-operations"></a>Collaboration de groupe moderne avec Project Operations
Project pour le web et Project Operations prennent en charge les groupes modernes de collaboration. Les utilisateurs ajoutés au projet via un groupe peuvent modifier le plan de projet.

Project pour le web ajoute automatiquement des utilisateurs au groupe lors de l’affectation.

Les groupes permettent de travailler en collaboration sur les autorisations du projet et des artefacts de collaboration associés. Le diagramme suivant décrit les événements et les changements d’état qui se produisent pendant le processus d’attribution de groupe.

Project Operations ne crée pas de groupe via une action implicite et ne le fait que via l’action explicite d’appuyer sur des groupes.

La recherche de membre du groupe dans la boîte de dialogue **Gestion de groupe** est limitée à ceux qui sont définis comme faisant partie du groupe de sécurité de l’environnement. Pour plus d’informations, voir [Contrôle de l’accès des utilisateurs aux environnements : groupes de sécurité et licences](https://docs.microsoft.com/power-platform/admin/control-user-access).

![Mode groupe](./media/groupsmode.png)

1. Le projet est créé et appartient à l’utilisateur créateur.
2. Le propriétaire du projet est mis à jour dans l’équipe.
3. L’équipe propriétaire est mappée à Office Group spécifié ou créé.
4. Le propriétaire d’origine du projet est ajouté à Office Group.

## <a name="deployment-recommendation"></a>Recommandations en matière de déploiement
À mesure que le modèle de collaboration d’Office Group évolue, des fonctionnalités seront ajoutées pour fournir un contrôle plus détaillé au fil du temps. Les clients qui déploient Project Operations aujourd’hui sont encouragés à se concentrer sur un modèle de sécurité Microsoft Dynamics 365.

Pour en savoir plus, consultez [Sécurité dans Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Sécurité Project Operations et Microsoft Dynamics 365 Finance
Project Operations inclut notamment les rôles ci-après :

- Chef de projet
- Comptable de projet

Pour plus d’informations sur la sécurité dans Finance, voir [Sécurité basée sur les rôles](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).


