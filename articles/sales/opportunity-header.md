---
title: En-tête/résumé de l’opportunité
description: Cette rubrique fournit des informations sur les transactions basées sur des projets et les lignes d’opportunités basées sur des projets.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c4e91c1a869347ac1182db2de1ab9244309eb856
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075615"
---
# <a name="opportunity-headersummary"></a>En-tête/résumé de l’opportunité

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_


L’en-tête, ou la résumé, Opportunité capture les informations globales sur une transaction basée sur un projet qui s’applique à toutes les lignes d’une opportunité basée sur un projet.

Les opportunités basées sur des projets dans Dynamics 365 Project Operations sont des extensions d’opportunités dans Dynamics 365 Sales. Ces extensions fournissent des fonctionnalités supplémentaires spécifiques et requises pour les opportunités basées sur des projets. Ces extensions peuvent inclure de nouveaux champs et actions de ruban disponibles dans les opportunités basées sur des projets. Il se peut que certains champs, fonctionnalités et logiques par défaut disponibles dans Sales ne soient pas disponibles dans Project Operations.

Le tableau suivant inclut les champs d’une opportunité basée sur un projet qui sont propres à Project Operations ou qui présentent des changements de comportement importants par rapport aux opportunités dans Sales.

| **Champ** | **Emplacement** | **Pertinence, objectif et conseils** | **Impact en aval** |
| --- | --- | --- | --- |
| Type | Onglet Général (masqué) | Ce champ de groupe d’options comporte les options suivantes :</br>- Basé sur le travail (disponible uniquement avec Project Operations)</br>- Basé sur l’article (disponible uniquement lorsque Project Operations et Sales sont installés)</br>- Service basé sur la maintenance (disponible lorsque Field Service est installé) | Lorsque vous utilisez Project Operations, la valeur de ce champ est automatiquement définie sur **Basé sur le travail** qui classifie l’opportunité comme basée sur un projet. Une opportunité doit être basée sur un projet pour activer toutes les extensions et fonctionnalités spécifiques au projet dans le processus de vente en aval pour cette transaction. |
| Société propriétaire | Onglet Général | Il s’agit de la société ou de l’entité juridique qui livrera le projet au client. | Ces informations de champ seront copiées dans le champ correspondant du devis de projet créé à partir de cette opportunité. |
| Contact | Onglet Général | Référence au contact principal du client pour cette offre. | |
| Compte | Onglet Général | Référence à la société ou à l’enregistrement de compte du client. | |
| Gestionnaire de comptes | Onglet Général | Nom du Gestionnaire de compte de cette opportunité basée sur un projet. | Le gestionnaire de compte est responsable de la gestion de la relation avec le client jusqu’à la réalisation de ce projet. En fonction de l’enregistrement de ressource réservable lié au gestionnaire du compte, l’unité contractuelle utilise par défaut. |
| Unité contractuelle | Onglet Général | Unité d’organisation responsable de la livraison du ou des projets associés à cette transaction. | L’unité contractuelle est la division de l’entreprise qui terminera les projets après la conclusion de la transaction. Chaque unité contractuelle dispose d’une devise, et cette devise est utilisée pour déclarer les coûts estimés et réels engagés pendant le projet. |

Pour tous les autres champs et sections de l’onglet **Résumé** de l’opportunité, voir [Créer ou modifier des opportunités (Ventes et Centre des ventes)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales).
