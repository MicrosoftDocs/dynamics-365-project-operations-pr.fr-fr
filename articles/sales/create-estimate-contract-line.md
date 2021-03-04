---
title: Estimer une ligne de contrat basée sur un projet
description: Cette rubrique fournit des informations sur les estimations d’une ligne de contrat basée sur un projet.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180459"
---
# <a name="estimate-a-projectbased-contract-line"></a>Estimer une ligne de contrat basée sur un projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_ 

Dans Dynamics 365 Project Operations, une ligne de contrat basée sur un projet contient des détails qui aident à estimer le coût et les revenus potentiels du travail impliqué pour fournir la ligne de contrat.

Pour estimer une ligne de contrat basée sur un projet, accédez à l’onglet **Détail de la ligne de contrat** sur la **Ligne de contrat** basée sur un projet.  Il existe deux façons de créer une estimation sur une ligne de contrat basée sur un projet :

   - Créer une estimation directement sur la ligne de contrat en ajoutant manuellement les détails de la ligne de contrat.
   - Créer un projet et un plan de projet, puis associer le projet et les tâches à la ligne de contrat du projet. Cela active le processus grâce auquel vous pouvez importer l’estimation du plan de projet dans la ligne de contrat en fonction des composants inclus dans la ligne de contrat.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Créer une estimation directement sur une ligne de contrat basée sur un projet

1. Accédez à la ligne du contrat et sélectionnez l’onglet **Détail de la ligne de contrat**. Les lignes créées dans cet onglet sont synthétisées et s’affichent comme **Valeur contractuelle** pour cette **Ligne de contrat**. 
2. Dans la sous-grille **Détails de la ligne de contrat**, sélectionnez **+ Nouveau détail de ligne de contrat**. Un curseur de création rapide s’ouvre. Les champs suivants sont disponibles sur le formulaire **Détails de la ligne de contrat** :

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| **Description** | **Création rapide** | Description d’estimation spécifique. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. |
| **Classe de transaction** | **Création rapide** | Cette liste déroulante est une liste des classes de transaction incluses dans l’onglet **Général** de la ligne de contrat basée sur un projet. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. |
| **Rôle** | **Création rapide** | Le rôle de la personne qui effectue ce travail ou qui engage cette dépense. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. |
| **Catégorie** | **Création rapide** | La catégorie du travail ou de la dépense. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. |
| **Date de début** | **Création rapide** | Date de début du travail. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. |
| **Date de fin** | **Création rapide** | Date de fin du travail. | Ce champ prend par défaut le détail de la ligne de contrat associée pour le coût qui est automatiquement créé. |
| **Société d’allocation de ressources** | **Création rapide** | La société d’allocation de ressources ou l’entité juridique qui supporte ce coût et fournit la ressource pour la tâche. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. Ce champ est également utilisé dans la recherche des prix de revient. |
| **Unité d’allocation des ressources** | **Création rapide** | L’unité d’allocation des ressources qui engage ce coût et fournit la ressource pour la tâche. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. Ce champ est également utilisé dans la recherche des prix de revient. |
| **Planification d’unités** | **Création rapide** | Le groupe d’unités du travail ou de la dépense. Les unités appartiennent à une nomenclature d’unités ou à un groupe d’unités. Par exemple, *miles* et *kilomètres (Kms)* sont des unités qui appartiennent à un groupe d’unités qui décrivent la distance. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. |
| **Unité** | **Création rapide** | L’unité du travail ou de la dépense. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. |
| **Quantité** | **Création rapide** | La quantité de travail ou de dépense. | Ce champ prend par défaut le détail de la ligne de contrat associée pour les coûts qui sont automatiquement créés. |
| **Prix unitaire** | **Création rapide** | Le taux de facturation du rôle qui exécute le travail ou le prix de vente de la catégorie de dépenses. Ce champ prend par défaut le **Temps** en fonction de la combinaison de rôle et unité d’allocation des ressources dans le tarif du projet valide à la date de début. Pour les dépenses, la valeur par défaut de ce champ provient de la configuration des prix pour la catégorie de transaction dans le tarif du projet valide à la date de début. Si la méthode de tarification pour la catégorie de transaction n’est pas le **prix unitaire**, il n’y a pas de valeur par défaut et ce champ est laissé vide. | Le taux de coût du rôle qui exécute le travail ou le coût par unité de la catégorie de dépenses. Ce champ prend la valeur par défaut pour **Temps basé sur le rôle** et la combinaison de l’unité d’allocation des ressources sur la ligne de prix du rôle de liste de prix de revient associée à l’unité contractuelle valide à la date de début. Pour les dépenses, la valeur par défaut de ce champ est basée sur la ligne de prix de la catégorie dans la liste de prix de revient associée à l’unité contractuelle valide à la date de début. Si la méthode de tarification pour la catégorie de transaction n’est pas le prix unitaire, il n’y a pas de valeur par défaut et ce champ est laissé vide. |
| **Estimation de taxe** | **Création rapide** | La taxe estimée pour ce travail ou cette dépense comme entrée par l’utilisateur. | La taxe estimée pour ce travail ou cette dépense comme entrée par l’utilisateur. |
| **Montant** | **Création rapide** | La valeur de ce champ peut être ajoutée par l’utilisateur si les champs **Quantité** et **Prix** sont laissés vides. Si les champs **Quantité** et **Prix** sont renseignés, le champs **Montant** est en lecture seule et est calculé comme **(Quantité\*Prix unitaire) + Taxe**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Mettre à jour les prix sur les détails de la ligne de contrat

Si vous modifiez les prix dans le tarif du projet associé au contrat ou la liste des prix de revient de l’unité contractuelle, vous pouvez actualiser les prix sur les détails de la ligne de contrat individuelle pour refléter cette modification. Sur la page **Contrat**, sélectionnez **Recalculer**. Un message d’avertissement s’ouvre pour vous informer que les prix de toutes les lignes de contrat de ce contrat sont réinitialisés. Sélectionnez **Oui** pour actualiser les détails de la ligne de contrat avec les prix de vente et les prix de revient.

## <a name="access-contract-line-details-for-cost"></a>Accéder aux détails de la ligne de contrat pour travailler sur les coûts

Sous l’onglet **Détails de la ligne de contrat**, sélectionnez une ligne dans la grille pour afficher les actions dans la barre d’outils de la sous-grille. La première action sur la barre d’outils de la sous-grille est **Ouvrir les détails du coût**. Pour afficher le taux de coûts et le montant associés à ces détails de ligne de contrat, sélectionnez **Ouvrir les détails du coût**. 

> [!NOTE]
> Modifier la société d’allocation de ressources, l’unité d’allocation des ressources, la quantité, les dates, le rôle ou les valeurs de catégorie dans les détails de la ligne de contrat pour **Coût** modifie également les valeurs correspondantes dans les détails de la ligne de contrat pour **Ventes**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Devise sur les détails de la ligne de contrat pour le coût et les ventes

Les détails de la ligne de contrat pour **Ventes** définit la devise par défaut à partir du tarif du projet valide à la date de début des détails de la ligne de contrat.

Les détails de la ligne de contrat pour **Coût** définit la devise par défaut à partir du tarif de l’unité contractuelle du contrat valide à la date de début des détails de la ligne de contrat pour **Coût**.

Les calculs de rentabilité convertissent les montants des détails de la ligne de contrat pour **Coût** et **Ventes** dans la devise de base de l’environnement pour créer un rapport sur les marges réelles et estimées globales du contrat.

> [!NOTE]
> Des erreurs d’arrondi des devises et de marges modifiées peuvent se produire en raison de l’absence date effective de taux de change. Utilisez ces calculs sur les contrats de projet uniquement pour obtenir des approximations et non pour les rapports statutaires ou autres qui nécessitent une plus grande précision d’arrondi et une prise de compte de la date effective des taux de change.


[!INCLUDE[footer-include](../includes/footer-banner.md)]