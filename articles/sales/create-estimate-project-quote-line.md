---
title: Estimer une ligne de devis de projet
description: Cette rubrique fournit des informations sur la création d’une estimation sur une ligne de devis de projet.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: adb5a7f113b15abd2fe7364fa9b592d2c02db389
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000703"
---
# <a name="estimate-a-project-quote-line"></a>Estimer une ligne de devis de projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une ligne de devis selon les projets contient des détails qui aident à estimer le coût et les revenus potentiels du travail impliqué pour fournir la ligne de devis.

Pour estimer une ligne de devis basée sur un projet, sélectionnez l’onglet **Détail de la ligne de devis** sur la ligne de devis. Il existe deux façons de créer une estimation sur une ligne de devis basée sur un projet :

   - Créez manuellement l’estimation directement sur la ligne de devis en utilisant les détails de la ligne de devis. 
   - Créez un projet et un plan de projet, puis associez le projet et les tâches du projet à la ligne de devis. Le processus d’importation des estimations du plan de projet dans la ligne de devis en fonction des informations que vous avez fournies sera activé.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Créer des estimations directement à partir d’une ligne de devis selon les projets

Pour créer des estimations directement sur une ligne de devis basée sur un projet, procédez comme suit :

1. Pour créer une estimation sur une ligne de devis selon les projets, sélectionnez l’onglet **Détail de la ligne de devis**. L’élément de ligne que vous créez dans cet onglet résume la valeur citée pour cette ligne de devis. 
2. Pour créer les détails de la ligne de devis, sélectionnez **Nouveau détail de la ligne de devis** dans la sous-grille **Détails de la ligne de devis**. Un curseur de création rapide s’ouvrira. Les champs suivants sur la page **Ligne de devis**.

| **Champ** | **Emplacement** | **Description** | **Impact en aval** |
| --- | --- | --- | --- |
| Description | Création rapide | Description d’estimation spécifique. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Classe de transaction | Création rapide | Cette liste déroulante fournit les classes de transaction incluses dans l’onglet **Général** de la ligne de devis selon les projets.  | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Sélectionner un produit | Création rapide | S’applique lorsque la classe de transaction est **Matériel**. Vous pouvez choisir de spécifier que cette ligne d’estimation s’applique à un produit **Existant** (catalogue) ou à un produit **Hors catalogue**. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Produit | Création rapide | L’ID du produit du catalogue de produits. Ce champ n’est activé que lorsque vous sélectionnez **Existant** dans le champ **Sélectionner un produit**. L’ID est utilisé pour récupérer le tarif de vente à partir du tarif du projet sur le devis. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Produit hors catalogue | Création rapide | Une zone de texte pour écrire le nom du produit. Ce champ n’est activé que lorsque vous sélectionnez **Produit hors catalogue** dans le champ **Sélectionner un produit**.| Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Rôle | Création rapide | Le rôle de la personne qui effectuera ce travail ou encourra cette dépense. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Catégorie | Création rapide | La catégorie du travail ou de la dépense. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Date de début | Création rapide | Date de début du travail. | La valeur par défaut de ce champ est le détail de la ligne de devis pour le coût qui est automatiquement créé. |
| Date de fin | Création rapide | Date de fin du travail. | La valeur par défaut de ce champ est le détail de la ligne de devis pour le coût qui est automatiquement créé. |
| Société d’allocation de ressources | Création rapide | La société d’allocation de ressources ou l’entité juridique qui supporte ce coût et fournit la ressource pour l’utiliser. | Par défaut, la valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé et utilisé pour récupérer le prix de revient. |
| Unité d’allocation des ressources | Création rapide | L’unité d’allocation des ressources qui supporte ce coût et fournit la ressource pour l’utiliser. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé et utilisé pour récupérer le prix de revient. |
| Planification d’unités | Création rapide | Le groupe d’unités du travail, du produit ou de la dépense. Les unités appartiennent à une nomenclature d’unités ou à un groupe d’unités. Par exemple, miles et kilomètres sont des unités qui appartiennent à un groupe d’unités qui décrivent la distance. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Unité | Création rapide | L’unité du travail, du produit ou de la dépense. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Quantité | Création rapide | La quantité de travail, de produit ou de dépense. | Par défaut, cette valeur est le détail de la ligne de devis associé pour le coût qui est automatiquement créé. |
| Prix unitaire | Création rapide |Le taux de facturation du rôle qui effectue le travail, le prix unitaire du produit ou le prix de vente du produit ou de la catégorie de dépense. La valeur par défaut pour **Temps** est basée sur la combinaison des valeurs de dimension de tarification sur la ligne de prix du rôle du tarif du projet qui est en vigueur à la date de début. Pour **Dépenses**, la valeur par défaut provient de la configuration des prix pour la catégorie de transaction dans le tarif du projet en vigueur à la date de début. Si la méthode de tarification pour la catégorie de transaction n’est pas le prix unitaire, il n’y a pas de valeur par défaut et ce champ est laissé vide. Pour les produits, la valeur par défaut de ce champ est basée sur la ligne **Élément tarifaire** dans le tarif du projet qui est en vigueur à la date de début.| Le taux de coûts du rôle qui effectue le travail, le coût unitaire de la catégorie de dépense ou le coût unitaire du produit. La valeur par défaut pour **Temps** est basée sur la combinaison des valeurs de dimension de tarification sur la ligne de prix du rôle de la liste des prix de revient attachée à l’unité contractuelle qui est en vigueur à la date de début. Pour les dépenses, la valeur par défaut est basée sur la ligne du prix de la catégorie de la liste des prix de revient attachée à l’unité contractuelle qui est en vigueur à la date de début. Si la méthode de tarification pour la catégorie de transaction n’est pas le prix unitaire, il n’y a pas de valeur par défaut et ce champ est laissé vide. Pour les produits, la valeur par défaut de ce champ est basée sur la ligne **Élément tarifaire** de la liste des prix de revient attachée à l’unité contractuelle qui est en vigueur à la date de début.|
| Estimation de taxe | Création rapide | Vous pouvez saisir manuellement la taxe estimée pour ce travail ou cette dépense. | Il n’y a pas d’impact en aval pour ce champ. |
| Montant | Création rapide | Vous pouvez saisir manuellement des informations dans ce champ si les champs **Quantité** et **Prix** sont laissés vides. Si ces champs ne sont pas vides, ce champ devient en lecture seule et est calculé comme (Quantité \* Prix unitaire) + TVA. | Il n’y a pas d’impact en aval pour ce champ. |

## <a name="update-prices-on-quote-line-details"></a>Mettre à jour les prix sur les détails de la ligne de devis

Si vous avez modifié les prix sur la liste de prix du projet jointe au devis ou sur la liste de prix de revient de l’unité contractuelle, vous pouvez sélectionner **Recalculer** sur la page **Citation**, pour actualiser les prix sur les détails de la ligne de devis individuelle afin de refléter ce changement. Lorsque vous sélectionnez **Recalculer**, un avertissement apparaît pour vous informer que les prix sur les détails de la ligne de devis pour toutes les lignes de devis de ce devis seront réinitialisés. Sélectionnez **Oui** pour actualiser les prix des détails de la ligne de vente et des détails de la ligne de devis.

## <a name="access-quote-line-details-for-cost"></a>Accéder aux détails de la ligne de devis pour connaître le coût

Pour accéder aux détails de la ligne de devis pour le coût, procédez comme suit :

1. Dans l’onglet **Détails de la ligne de devis**, sélectionnez une ligne de la grille pour activer les actions dans la barre d’outils de la sous-grille. 
2. Sélectionnez **Ouvrir les détails du coût** pour afficher les tarifs et le montant associés pour cette ligne de devis.

> [!NOTE]
> La modification de l’unité d’allocation des ressources, de la quantité, des dates, du rôle ou des valeurs de catégorie dans le détail de la ligne de devis pour le coût modifiera les valeurs correspondantes dans les détails de la ligne de devis pour les ventes.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Devise sur les détails de la ligne de devis pour le coût et les ventes

La devise du détail de la ligne de devis pour les ventes est par défaut celle du tarif du projet qui est en vigueur à la date de début du détail de la ligne de devis.

La devise du détail de la ligne de devis pour les coûts est par défaut celle du tarif de l’unité contractuelle du devis qui est en vigueur à la date de début du détail de la ligne de devis pour les coûts.

> [!NOTE]
> Les calculs de rentabilité convertissent le montant des détails de la ligne de devis pour le coût et les ventes dans la devise de base de l’environnement pour indiquer la marge globale estimée sur le devis. Des erreurs d’arrondi des devises et de marges modifiées peuvent se produire en raison de l’absence date effective de taux de change. Utilisez ces calculs uniquement pour les devis de projet, car il s’agit d’approximations et non de rapports statutaires ou autres qui nécessitent une plus grande précision d’arrondi et une connaissance de la date de validité des taux de change.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
