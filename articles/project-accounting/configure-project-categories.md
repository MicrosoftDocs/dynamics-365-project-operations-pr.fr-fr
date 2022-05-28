---
title: Configurer les catégories de projets
description: Cette rubrique fournit des informations sur le paramétrage des catégories de projet.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 94b66feef4164f3cd52d5fe917071647f731b047
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591539"
---
# <a name="configure-project-categories"></a>Configurer les catégories de projets

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Project Operations offre de solides capacités de catégorisation des revenus et des dépenses sur les projets. Les catégories permettent de rendre compte des transactions de projet, de les analyser et de piloter la validation en comptabilité.

Le diagramme suivant illustre la corrélation entre les catégories de transaction, les catégories partagées et les catégories de projet. 

Les catégories de transaction constituent le regroupement de base des transactions de projet. Au sein de ce regroupement se trouve un ensemble de catégories qui peuvent être partagées sur l’ensemble des applications et des modules. Pour aller encore plus loin dans les détails, les catégories de projets sont le niveau de catégories le plus granulaire. Les catégories de projet sont spécifiques à l’entité juridique, au module et à l’application.

![Corrélation entre les catégories de transaction, les catégories partagées et les catégories de projet.](media/project-categories.png)

## <a name="transaction-categories"></a>Catégories de transactions

Les catégories de transaction représentent le regroupement de base des transactions de projet et ne sont pas spécifiques à la société ou au type de transaction. Par exemple, Contoso Robotics utilise les catégories Conception, Déplacement, Installation et Transaction de service pour regrouper les transactions de projet.

Les catégories de transaction sont définies dans le module Project Operations. 
1. Accédez à **Paramètres** \> **Catégories de transaction** pour ouvrir le formulaire. 
2. Créez une catégorie de transaction en sélectionnant **Nouveau** ou en sélectionnant **Importer depuis Excel**.

## <a name="shared-categories"></a>Catégories partagées

Dynamics 365 utilise le concept des catégories partagées pour catégoriser les dépenses dans différentes applications telles que Dynamics 365 Finance, Dynamics 365 Supply Chain et Dynamics 365 Project Operations. Pour chaque catégorie de transaction créée, Project Operations crée automatiquement quatre catégories partagées associées : Heures, Dépenses, Frais et Article. Vous pouvez consulter et ajuster les catégories partagées en accédant à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Catégories partagées**.

## <a name="project-categories"></a>Catégories de projets

Les catégories de projet représentent le niveau le plus granulaire de configuration de catégorie et doivent être configurées séparément, et pour chaque entreprise, par un comptable de projet.

1. Accédez à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Catégories de projets**.
2. Cliquez sur **Nouveau**.
3. Sélectionnez l’**Identificateur de catégorie** de la catégorie partagée créée dans la section précédente. Project Operations permet d’utiliser uniquement les catégories partagées associées aux catégories de transactions.
4. Sélectionnez un groupe de catégories.

## <a name="category-groups"></a>Groupes de catégories

Les groupes de catégories permettent de partager des propriétés, principalement des profils de validation, entre des catégories de projets associées. Au moins un groupe de catégories doit être affecté à chaque type de transaction et chaque catégorie de projet se voit affecter un groupe.

Les spécifications de validation dans Project Operations sont définies par les règles de profil de coût et de produit du projet, les catégories de projet et les groupes de catégories. Vous pouvez configurer des groupes de catégories en accédant à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Groupes de catégories**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]