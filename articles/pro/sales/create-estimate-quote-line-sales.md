---
title: Estimation d’une ligne de devis selon les projets
description: Cette rubrique fournit des informations sur la façon de créer des estimations sur une ligne de devis selon les projets.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 65aee7238781ac90f603e57c6d9b0b92cabd6644
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966775"
---
# <a name="estimating-a-project-based-quote-line"></a>Estimation d’une ligne de devis selon les projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Une ligne de devis selon les projets contient des détails qui aident à estimer le coût et les revenus potentiels du travail impliqué pour fournir la ligne de devis.

Pour estimer une ligne de devis selon les projets, sur la ligne de devis selon les projets, sélectionnez l’onglet **Détail de la ligne de devis**. Il existe deux façons de créer une estimation sur une ligne de devis selon les projets :

- Créez manuellement le devis directement sur la ligne de devis en utilisant les détails de la ligne de devis 
- Créez un projet et un plan de projet, puis associez le projet et les tâches du projet à la ligne de devis. Le processus d’importation des estimations du plan de projet dans la ligne de devis en fonction des informations que vous avez fournies sera activé.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Créer des estimations directement à partir d’une ligne de devis selon les projets

Pour créer une estimation sur une ligne de devis selon les projets, sélectionnez l’onglet **Détail de la ligne de devis**. L’élément de ligne que vous créez dans cet onglet résume la valeur citée pour cette ligne de devis. 

Pour créer les détails de la ligne de devis, sélectionnez **+ Nouveau détail de la ligne de devis** sur la sous-grille **Détails de la ligne de devis**. Un curseur de création rapide s’ouvrira. Les champs suivants sur le formulaire **Ligne de devis** :

| **Champ** | **Emplacement** | **Pertinence, objectif et conseils** | **Impact en aval** |
| --- | --- | --- | --- |
| Description | Création rapide | Description d’estimation spécifique. | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Classe de transaction | Création rapide | Cette liste déroulante fournit les classes de transaction incluses dans l’onglet **Général** de la ligne de devis selon les projets.  | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Rôle | Création rapide | La personne qui effectuera ce travail ou encourra cette dépense. | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Catégorie | Création rapide | Catégorie de travail ou de dépense. | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Date de début | Création rapide | Date de début du travail. | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Date de fin | Création rapide | Date de fin du travail. | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Unité d’allocation des ressources | Création rapide | Unité d’allocation des ressources qui supportera ce coût et fournira la ressource pour y travailler. | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. Ce champ est également utilisé dans la recherche des prix de revient. |
| Planification d’unités | Création rapide | Groupe de base du travail ou de la dépense. Les unités appartiennent à une nomenclature d’unités ou à un groupe d’unités. Par exemple, les kilomètres (ou les miles) sont des unités qui appartiennent à un groupe d’unités qui décrit la distance. | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Unité | Création rapide | Unité du travail ou de la dépense. | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Quantité | Création rapide | Quantité de travail ou de dépense | Ce champ prend par défaut le détail de la ligne de devis associée pour le coût qui est automatiquement créé. |
| Prix unitaire | Création rapide | Taux de facturation du rôle qui exécute le travail ou Prix de vente de la catégorie de dépenses. Ce champ prend par défaut la valeur Heure en fonction de la combinaison de rôle et d’unité de ressources dans la liste de prix du projet qui est en vigueur pour la date de début. Pour les dépenses, ce champ correspond par défaut à la configuration de prix pour la catégorie de transaction dans la liste de prix du projet qui est en vigueur pour la date de début. Si la méthode de tarification pour la catégorie de transaction n’est pas le prix unitaire, il n’y a pas de valeur par défaut et ce champ est laissé vide. | Taux de coût du rôle qui exécute le travail ou coût unitaire de la catégorie de dépenses. Ce champ prend par défaut la valeur Heure en fonction de la combinaison de rôle et d’unité d’allocation des ressources sur le prix de l’Unité contractuelle des tarifs du devis qui est en vigueur pour la date de début. Pour les dépenses, ce champ correspond par défaut à la configuration de prix pour la catégorie de transaction dans le prix de revient de l’unité contractuelle qui est en vigueur pour la date de début. Si la méthode de tarification pour la catégorie de transaction n’est pas le prix unitaire, il n’y a pas de valeur par défaut et ce champ est laissé vide. |
| Estimation de taxe | Création rapide | Vous pouvez saisir manuellement la taxe estimée pour ce travail ou cette dépense. | Il n’y a pas d’impact en aval de ce champ. |
| Montant | Création rapide | Vous pouvez saisir manuellement des informations dans ce champ si les champs **Quantité** et **Prix** sont laissés vides. Si ces champs ne sont pas vides, ce champ devient en lecture seule et est calculé comme (Quantité \* Prix unitaire) + TVA. | Il n’y a pas d’impact en aval de ce champ. |

## <a name="update-prices-on-quote-line-details"></a>Mettre à jour les prix sur les détails de la ligne de devis

Si vous avez modifié les prix sur la liste de prix du projet jointe au devis ou sur la liste de prix de revient de l’unité contractuelle, vous pouvez sélectionner **Recalculer** sur la page **Citation**, pour actualiser les prix sur les détails de la ligne de devis individuelle afin de refléter ce changement. Lorsque vous sélectionnez **Recalculer**, un avertissement s’affiche et vous informe que les prix indiqués sur les détails de la ligne de devis pour toutes les lignes de devis de ce devis seront réinitialisés. Sélectionnez **Oui**, pour actualiser les prix des ventes et des détails des lignes de devis.

## <a name="access-quote-line-details-for-cost"></a>Accéder aux détails de la ligne de devis pour connaître le coût

Sur l’onglet **Détails de la ligne de devis**, sélectionnez une ligne dans la grille pour activer certaines actions dans la barre d’outils de la sous-grille. La première action de la barre d’outils de la sous-grille lorsqu’un détail de ligne de devis est sélectionné est **Ouvrir les détails du coût**. Sélectionnez **Ouvrir les détails du coût** pour afficher les tarifs et le montant associés pour cette ligne de devis.

> [!NOTE]
> La modification de l’unité d’allocation des ressources, de la quantité, des dates, du rôle ou des valeurs de catégorie dans le détail de la ligne de devis pour le coût modifiera les valeurs correspondantes dans les détails de la ligne de devis pour les ventes.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Devise sur les détails de la ligne de devis pour le coût et les ventes

La devise du détail de la ligne de devis pour les ventes par défaut provient de la liste de prix du projet qui est en vigueur pour la date de début du détail de la ligne de devis.

La devise du détail de la ligne de devis pour les coûts par défaut provient des tarifs de l’unité contractuelle du devis qui est en vigueur pour la date de début du détail de la ligne de devis pour les coûts.

Les calculs de rentabilité convertissent le montant des détails de la ligne de devis pour le coût et les ventes dans la devise de base de l’environnement pour indiquer la marge globale estimée sur le devis.

Cela pourrait entraîner des erreurs d’arrondi des devises et une modification des marges en raison de l’absence de taux de change effectifs de date. Utilisez ces calculs sur les devis du projet uniquement comme approximations et non comme des chiffre réels statutaires ou les autres états qui nécessitent une plus grande précision d’arrondi et une connaissance de la date d’entrée en vigueur pour les taux de change.
