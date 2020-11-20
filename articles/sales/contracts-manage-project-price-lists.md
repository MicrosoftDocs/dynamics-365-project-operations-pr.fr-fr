---
title: Gérer les tarifs des projets sur les contrats de projet
description: Cette rubrique fournit des informations sur la gestion des tarifs de projet sur les contrats de projet.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 030684576e1f53d27921907b07c9e5e0c5efe612
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133330"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Gérer les tarifs des projets sur les contrats de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les contrats de projet dans Dynamics 365 Project Operations sont conçus pour prendre en charge des tarifs de vente valides à plusieurs dates sur un contrat. Dans Project Operations, il existe une nouvelle entité associée appelée **Tarifs du projet**. Cette entité a une relation un-à-plusieurs avec un contrat de projet.

Les tarifs de projet sont utilisés pour évaluer les transactions de temps et de dépenses sur un projet. Lorsqu’un contrat comporte un ou plusieurs tarif(s) de projet, ces derniers sont utilisées pour tarifier les estimations de temps et de dépenses et les chiffres réels des projets associés au contrat via la ligne de contrat.

en cas d’absence de tarifs de projet pour un contrat de projet, un message d’avertissement s’affiche indiquant qu’il n’y a pas de tarif de projet et vos estimations, travaux de projet réels et dépenses ne seront pas tarifés. Les valeurs de vente ne comporteront pas de prix.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Associer ou dissocier un tarif de projet sur un contrat de projet

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Créer ou associer un tarif spécifique pour estimer le travail et les dépenses basés sur un projet

1. Dans le contrat de projet, accédez à l’onglet **Tarifs du projet**.
2. Dans la sous-grille, sélectionnez **+ Ajouter de nouveaux tarifs de projet**.
3. Sur le curseur **Création rapide**, sélectionnez un tarif. 

  La liste déroulante affiche tous les tarifs dont le contexte est défini sur **Ventes**, pour lesquels la devise du tarif correspond à la devise du contrat.
  
4. Saisissez une description de l’association du tarif du projet, sélectionnez **Enregistrer**, puis fermez le curseur **Création rapide**.

   Une association de tarif du projet est créée.
   
5. Répétez les étapes 1 à 4 pour associer plusieurs tarifs de projet au contrat de projet. Ne créez plusieurs tarifs de projet seulement si la date de validité est différente sur chacun des tarifs de projet associé.

> [!NOTE]
> Project Operations ne prend pas en charge le chevauchement de dates de validité de tarifs de projet. S’il existe plusieurs tarifs de projet pour une transaction avec une date donnée, le prix de cette transaction sera défini sur zéro par défaut.

### <a name="remove-a-project-price-list-association"></a>Supprimer l’association de tarifs de projet

- Sélectionnez le tarif de projet, puis **Supprimer le tarif de projet de contrat** de la sous-grille. 

  Le tarif est supprimé des tarifs de projet sur le contrat. Le tarif lui-même ne sera pas supprimé. Seule l’association au contrat sera supprimée.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Configurer la valeur par défaut automatique des tarifs de projet sur un contrat

Un tarif de projet peut être configuré comme le tarif par défaut sur un contrat de projet. Cette configuration permet de garantir que tous les contrats de votre organisation commencent toujours par un tarif standard pour cette période tarifaire.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Configurer la valeur par défaut de l’organisation des tarifs de projet

1. Accédez à **Paramètres** > **Général**, puis sélectionnez **Paramètres**.
2. Dans la page de la liste **Paramètres actifs**, sélectionnez et double-cliquez sur l’enregistrement pour l’ouvrir. Lorsque vous double-cliquez, veillez à ne pas cliquer sur une valeur de champ qui est un lien hypertexte. 
3. Sur la page **Paramètres actifs**, sélectionnez l’onglet **Tarifs**. Une sous-grille affiche une liste de tarifs par défaut. Il s’agit d’une liste de coûts standard et de tarifs de vente. Disposer d’un tarif **Ventes** associé ici pour chaque devise dans laquelle vous vendez, garantit que le tarif de ventes est la valeur par défaut sur tout contrat créé pour les clients qui effectuent des transactions dans cette devise.

### <a name="set-up-a-customer-specific-project-price-list"></a>Configurer un tarif de projet spécifique pour un client

Vous pouvez également configurer des tarifs de projet spécifiques pour des clients lorsque vous avez négocié un accord de tarification principal avec vos clients.

1. Accédez à **Ventes** > **Clients**.
2. À partir de la liste des comptes actifs, sélectionnez le client ayant un tarif spécial.
3. Sélectionnez l’enregistrement de client pour l’ouvrir, puis sélectionnez l’onglet **Tarifs de projet**. Une sous-grille affiche une liste de tarifs de projet spécifiques à ce client. 
4. Créez une association de tarifs ici pour obtenir un tarif de projet spécifique à ce client.

## <a name="custom-pricing-on-a-project-contract"></a>Tarification personnalisée sur un contrat de projet

Une fois que vous disposez de tarifs de projet par défaut pour l’organisation et spécifiques au client, vos contrats de projet sont créés automatiquement avec ces associations de tarifs de projet. Cependant, les tarifs de projet sur un contrat de projet sont toujours copiés avec la date et le nom du contrat qui leur sont ajoutés. Les gestionnaires de compte et de projet peuvent alors commencer à modifier les prix de ces copies. Ces prix modifiés s’appliqueront à ce contrat de projet uniquement.
