---
title: Configurer les catégories de projets
description: Cette rubrique fournit des informations sur le paramétrage des catégories de projet.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3698b68b5dd0460343d26af0fcea5b9a56be4083
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131925"
---
# <a name="configure-project-categories"></a>Configurer les catégories de projets

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Project Operations offre de solides capacités de catégorisation des revenus et des dépenses sur les projets. Les catégories offrent la possibilité de rendre compte et d’analyser les transactions du projet et de diriger la validation dans la comptabilité.

Le diagramme suivant illustre la corrélation entre les catégories de transaction, les catégories partagées et les catégories de projet. 

Les catégories de transaction constituent le regroupement de base des transactions de projet. Au sein de ce groupe, il existe un ensemble de catégories partagées qui peuvent être partagées entre les applications et les modules. Pour aller encore plus loin dans les détails, les catégories de projets sont le niveau de catégories le plus granulaire. Les catégories de projet sont spécifiques à l’entité juridique, au module et à l’application.

![Corrélation entre les catégories de transaction, les catégories partagées et les catégories de projet](media/project-categories.png)

## <a name="transaction-categories"></a>Catégories de transactions

Les catégories de transaction représentent le regroupement de base des transactions de projet et ne sont pas spécifiques à la société ou au type de transaction. Par exemple, Contoso Robotics utilise les catégories Conception, Déplacement, Installation et Transaction de service pour regrouper les transactions de projet.

Les catégories de transaction sont définies dans le module Project Operations. 
1. Accédez à **Paramètres** \> **Catégories de transaction** pour ouvrir le formulaire. 
2. Créez une catégorie de transaction en sélectionnant **Nouveau** ou en sélectionnant **Importer depuis Excel**.

## <a name="shared-categories"></a>Catégories partagées

Dynamics 365 utilise le concept de catégories partagées pour classer les dépenses dans différentes applications, telles que Dynamics 365 Finance, Dynamics 365 Supply Chain et Dynamics 365 Project Operations. Pour chaque catégorie de transaction créée, Project Operations crée automatiquement quatre catégories partagées associées : Heures, Dépenses, Frais et Article. Vous pouvez consulter et ajuster les catégories partagées en accédant à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Catégories partagées**.

## <a name="project-categories"></a>Catégories de projets

Les catégories de projet représentent le niveau le plus granulaire de configuration de catégorie et doivent être configurées séparément, et pour chaque entreprise, par un comptable de projet.

1. Accédez à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Catégories de projets**.
2. Cliquez sur **Nouveau**.
3. Sélectionnez l’**Identificateur de catégorie** de la catégorie partagée créée dans la section précédente. Project Operations permet d’utiliser uniquement les catégories partagées associées aux catégories de transaction.
4. Sélectionnez un groupe de catégories.

## <a name="category-groups"></a>Groupes de catégories

Les groupes de catégories sont utilisés pour partager des propriétés, principalement des profils de publication, entre des catégories de projet associées. Il doit y avoir au moins un groupe de catégories pour chaque type de transaction et chaque catégorie de projet se voit attribuer un groupe.

Les spécifications de validation dans Project Operations sont définies par les règles de profil de coût et de produit du projet, les catégories de projet et les groupes de catégories. Vous pouvez configurer des groupes de catégories en accédant à **Gestion de projets et comptabilité** \> **Configurer** \> **Catégories** \> **Groupes de catégories**.
