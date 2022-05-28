---
title: Estimer une ligne de contrat basée sur un projet– Simplifié
description: Cette rubrique fournit des informations sur les estimations d’une ligne de contrat basée sur un projet.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 179994a2515686bce2370964121cbdca08a9d085
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597335"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Estimer une ligne de contrat basée sur un projet– Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, une ligne de contrat basée sur un projet contient des détails qui aident à estimer le coût et les revenus potentiels du travail impliqué pour fournir la ligne de contrat.

Pour estimer une ligne de contrat basée sur un projet, accédez à l’onglet **Détail de la ligne de contrat** sur la **Ligne de contrat** basée sur un projet.  Il existe deux façons de créer une estimation sur une ligne de contrat basée sur un projet :

   - Créer une estimation directement sur la ligne de contrat en ajoutant manuellement les détails de la ligne de contrat.
   - Créer un projet et un plan de projet, puis associer le projet et les tâches à la ligne de contrat du projet. Cela active le processus grâce auquel vous pouvez importer l’estimation du plan de projet dans la ligne de contrat en fonction des composants inclus dans la ligne de contrat.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Créer une estimation directement sur une ligne de contrat basée sur un projet

Pour créer une estimation directement sur une ligne de contrat basée sur un projet, procédez comme suit :

1. Accédez à la ligne du contrat et sélectionnez l’onglet **Détail de la ligne de contrat**. Les lignes créées dans cet onglet sont synthétisées et s’affichent comme **Valeur contractuelle** pour cette **Ligne de contrat**. 
2. Dans la sous-grille **Détails de la ligne de contrat**, sélectionnez **Nouveau détail de ligne de contrat**. Un curseur de création rapide s’ouvre. Les champs suivants sont disponibles sur la page **Détails de la ligne de contrat**.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| **Description** | **Création rapide** | Description d’estimation spécifique. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Classe de transaction** | **Création rapide** | Il s’agit d’une liste de classes de transaction incluse dans l’onglet **Général** de la ligne de contrat basée sur un projet. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Sélectionner un produit** | **Création rapide** | S’applique lorsque la classe de transaction est **Matériel**. Vous pouvez spécifier si cette ligne d’estimation s’applique à un produit **Existant** (catalogue) ou à un produit **Hors catalogue**. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Produit** | **Création rapide** | L’ID du produit du catalogue de produits. Ce champ n’est activé que lorsque vous sélectionnez **Produit existant** dans le champ **Sélectionner un produit**. L’ID est utilisé pour récupérer le tarif de vente à partir du tarif du projet sur le contrat. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Produit hors catalogue** | **Création rapide** | Un champ de texte pour saisir le nom du produit. Ce champ n’est activé que lorsque vous sélectionnez **Produit hors catalogue** dans le champ **Sélectionner un produit**.| Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Rôle** | **Création rapide** | Le rôle de la personne qui effectue ce travail ou qui engage cette dépense. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé.|
| **Catégorie** | **Création rapide** | La catégorie du travail ou de la dépense. |Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé.|
| **Date de début** | **Création rapide** | Date de début du travail. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Date de fin** | **Création rapide** | Date de fin du travail. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Unité d’allocation des ressources** | **Création rapide** | L’unité d’allocation des ressources qui supporte ce coût et fournit la ressource pour l’utiliser. |Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé et utilisé pour récupérer le prix de revient. |
| **Planification d’unités** | **Création rapide** | Le groupe d’unités du travail, du produit ou de la dépense. Les unités appartiennent à une nomenclature d’unités ou à un groupe d’unités. Par exemple, *miles* et *kilomètres (km)* sont des unités qui appartiennent à un groupe d’unités qui décrivent la distance. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Unité** | **Création rapide** | L’unité de travail, de produit ou de dépense. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Quantité** | **Création rapide** | La quantité de travail, de produit ou de dépense. | Par défaut, cette valeur est le détail de la ligne de contrat associé pour le coût qui est automatiquement créé. |
| **Prix unitaire** | **Création rapide** | Le taux de facturation du rôle qui effectue le travail, le prix unitaire du produit ou le prix de vente du produit ou de la catégorie de dépense. La valeur par défaut de ce champ pour **Temps** est basée sur la combinaison des valeurs de dimension de tarification sur la ligne de prix du rôle du tarif du projet qui est en vigueur à la date de début. Pour **Dépenses**, la valeur par défaut de ce champ provient de la configuration des prix pour la catégorie de transaction dans le tarif du projet en vigueur à la date de début. Si la méthode de tarification pour la catégorie de transaction n’est pas le **prix unitaire**, il n’y a pas de valeur par défaut et ce champ est laissé vide. Pour les produits, la valeur par défaut de ce champ est basée sur la ligne **Élément tarifaire** dans le tarif du projet qui est en vigueur à la date de début.| Le taux de coûts du rôle qui effectue le travail, ou le coût unitaire de la catégorie de dépense ou le coût unitaire du produit. La valeur par défaut de ce champ pour **Temps** est basée sur la combinaison des valeurs de dimension de tarification sur la ligne de prix du rôle de la liste des prix de revient attachée à l’unité contractuelle qui est en vigueur à la date de début. Pour les dépenses, la valeur par défaut de ce champ est basée sur la ligne de prix de la catégorie dans la liste de prix de revient associée à l’unité contractuelle valide à la date de début. Si la méthode de tarification pour la catégorie de transaction n’est pas le prix unitaire, il n’y a pas de valeur par défaut et ce champ est laissé vide. Pour les produits, la valeur par défaut de ce champ est basée sur la ligne **Élément tarifaire** de la liste des prix de revient attachée à l’unité contractuelle qui est en vigueur à la date de début.|
| **Estimation de taxe** | **Création rapide** | La taxe estimée pour ce travail ou cette dépense. | La taxe estimée pour ce travail ou cette dépense. |
| **Montant** | **Création rapide** | Vous pouvez ajouter la valeur de ce champ si les champs **Quantité** et **Prix** sont laissés vides. Si les champs **Quantité** et **Prix** sont renseignés, le champ **Montant** est en lecture seule et est calculé comme **(Quantité \* Prix unitaire) + Taxe**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Mettre à jour les prix sur les détails de la ligne de contrat

Si vous modifiez les prix dans le tarif du projet associé au contrat ou la liste des prix de revient de l’unité contractuelle, vous pouvez actualiser les prix sur les détails de la ligne de contrat individuelle pour refléter cette modification. Sur la page **Contrat**, sélectionnez **Recalculer**. Un avertissement apparaît pour vous informer que les prix de toutes les lignes de contrat de ce contrat sont réinitialisés. Sélectionnez **Oui** pour actualiser les détails de la ligne de contrat avec les prix de vente et les prix de revient.

## <a name="access-contract-line-details-for-cost"></a>Accéder aux détails de la ligne de contrat pour travailler sur les coûts

Sous l’onglet **Détails de la ligne de contrat**, sélectionnez une ligne dans la grille pour afficher les actions dans la barre d’outils de la sous-grille. La première action sur la barre d’outils de la sous-grille est **Ouvrir les détails du coût**. Pour afficher le taux de coûts et le montant associés à ces détails de ligne de contrat, sélectionnez **Ouvrir les détails du coût**. 

> [!NOTE]
> Modifier la société d’allocation de ressources, l’unité d’allocation des ressources, la quantité, les dates, le rôle ou les valeurs de catégorie dans les détails de la ligne de contrat pour **Coût** modifie également les valeurs correspondantes dans les détails de la ligne de contrat pour **Ventes**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Devise sur les détails de la ligne de contrat pour le coût et les ventes

Les détails de la ligne de contrat pour **Ventes** définit la devise par défaut à partir du tarif du projet valide à la date de début des détails de la ligne de contrat.

Les détails de la ligne de contrat pour **Coût** définit la devise par défaut à partir du tarif de l’unité contractuelle du contrat valide à la date de début des détails de la ligne de contrat pour **Coût**.

Les calculs de rentabilité convertissent les montants des détails de la ligne de contrat pour **Coût** et **Ventes** dans la devise de base de l’environnement pour créer un rapport sur les marges réelles et estimées globales du contrat.

> [!NOTE]
> Des erreurs d’arrondi des devises et de marges modifiées peuvent se produire en raison de l’absence date effective de taux de change. Utilisez ces calculs uniquement pour les contrats de projet, car il s’agit d’approximations qui ne sont pas destinées à des rapports statutaires ou autres qui nécessitent une plus grande précision d’arrondi et une connaissance de la date de validité des taux de change.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
