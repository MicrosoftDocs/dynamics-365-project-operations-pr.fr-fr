---
title: Devis - Concepts clés
description: Cette rubrique fournit des informations sur les devis de projet et les devis de vente disponibles dans Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8d113111f5fbf6f5d23ef02cae36d85a27beed93
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121305"
---
# <a name="quotes---key-concepts"></a>Devis - Concepts clés

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, il existe deux types de devis : les devis de projet et de vente. Ces deux types de devis diffèrent des façons suivantes :

- **Grilles pour les lignes** : Dans un devis de vente, il n’existe qu’une grille pour les lignes. Dans un devis de projet, il y a deux grilles pour les lignes. L’une des grilles est destinée aux lignes de projet et l’autre aux lignes de produits.
- **Activation et révisions** : Les devis de vente prennent en charge l’activation et les révisions. Ces processus ne sont pas pris en charge sur un devis de projet.
- **Commandes jointes** : Vous pouvez joindre plusieurs commandes à un devis de vente. Un seul contrat de projet peut être joint à un devis de projet.
- **Gagner un devis** : Lorsque vous remportez un devis de vente, l’opportunité associée peut rester ouverte. Lorsqu’un devis de projet qui conclus, une opportunité associée est fermée.
- **Champs et concepts** : Un devis de vente ne comprend pas certains champs et les concepts qui se trouvent sur un devis de projet. Les champs incluent **Unité contractuelle**, **Gestionnaire de comptes** et **Nom du contact de facturation**.  
- **Type** : Les devis de vente et les devis de projet sont également identifiés par un champ basé sur un jeu de données nommé **Type**. Pour un devis de vente, ce champ a la valeur **Basé sur l’article**. Pour un devis de projet, il a la valeur **Basé sur le travail**.

Cette rubrique se concentre sur les détails des devis de projet.

Un devis de projet dans Project Operations peut avoir plusieurs lignes ou lignes de devis. En fait, un devis de projet a deux grilles pour les lignes. Une grille pour les lignes basées sur le projet qui permettent des estimations détaillées. L’autre grille est pour les lignes basées sur le produit qui utilisent un seul prix unitaire et une approche basée sur la quantité.

- **Basé sur le projet** : La valeur du devis est déterminée après avoir estimé le volume de travail requis. Vous pouvez estimer le travail à un niveau élevé, directement sous forme de détails de ligne sous chaque ligne de devis, ou sur la base d’estimations à la base, en utilisant un projet et un plan de projet. Les lignes de devis basées sur un projet sont disponibles uniquement dans les devis basés sur un projet créés à l’aide de Project Operations. Ce type de ligne de devis est un formulaire personnalisé des lignes de devis hors catalogue disponibles dans Microsoft Dynamics 365 Sales.

- **Basé sur le produit** : La valeur du devis est déterminée selon la quantité d’unités vendue et du prix de vente unitaire du produit. Le produit sur une ligne basée sur un produit peut provenir d’un catalogue de produits dans Sales, ou peut être un produit que vous définissez. Ce type de ligne de devis est également disponible sur les devis basés sur un projet créés à l’aide de Project Operations.

Le montant d’un devis est le total des lignes basées sur le produit et des lignes basées sur le projet.

> [!NOTE]
> Les devis et les lignes de devis ne sont pas nécessaires dans Project Operations. Vous pouvez commencer le processus de projet avec un contrat de projet (projet vendu). Toutefois, une opportunité est toujours nécessaire, indépendamment du fait que vous commencez par un devis ou un contrat de projet.

## <a name="project-based-quote-lines"></a>Lignes du devis selon les projets

Dans Project Operations, une ligne de devis basée sur un projet contient les modes de facturation suivants :

- Temps et matériel
- Prix fixe

### <a name="time-and-material"></a>Temps et matériel

Le mode de facturation du temps et du matériel dépend de la consommation. Lorsque vous sélectionnez ce mode de facturation, le client est facturé lorsque le projet engage des coûts. Les factures sont créées à une fréquence périodique basée sur la date. Durant le processus de vente, la valeur estimée dans le devis d’un composant de temps et de matériel ne donne qu’une estimation du coût final du client. Le fournisseur ne s’engage pas à terminer le projet à la valeur exacte du devis. Les composants de temps et de matériel augmentent le risque du client. Les clients peuvent souhaiter négocier des clauses supplémentaires de non dépassement pour réduire le risque. Project Operations ne prend pas en charge la configuration de clauses de non dépassement.

### <a name="fixed-price"></a>Prix fixe

Dans le mode de facturation à prix fixe, un fournisseur s’engage à livrer le projet à un coût fixe au client. Le client est facturé de la valeur estimée dans le devis de la ligne de devis à prix fixe, indépendamment des coûts que le fournisseur encourt pour livrer cette ligne de devis. La valeur de la ligne de devis à prix fixe est facturée de l’une des façons suivantes : 

- En tant que somme forfaitaire au début ou à la fin du projet, ou lorsqu’un des jalons du projet est atteint. 
- À une fréquence basée sur la date d’échelonnements égaux de la valeur fixe sur la ligne de devis. Ces échelonnements sont connus comme des jalons périodiques.
- Dans les échelonnements avec une valeur monétaire alignée sur l’avancement des travaux ou des jalons spécifiques exécutés dans le projet. Dans ce cas, la valeur de chaque échelonnement peut différer, mais la somme totale doit être égale à la valeur fixe de la ligne de devis.

Project Operations prend en charge les trois types de planifications de facture des lignes de devis à prix fixe.

## <a name="transaction-classification"></a>Classification de la transaction

Les organisations de services professionnels établissement des devis et facturent leurs clients généralement selon la classification des coûts. Les coûts sont représentés par les classifications de transaction suivantes :

- **Temps** : Cette classification représente le coût de temps de la main-d’œuvre ou des ressources humaines dans un projet.
- **Dépenses** : Cette classification représente tous les autres types de dépenses dans un projet. Étant donné que les dépenses peuvent être globalement classifiées, la plupart des organisations créent des sous-catégories, telles que le trajet, la location de voiture, l’hôtel ou les fournitures de bureau.
- **Frais** : Cette classification représente des dépassements, pénalités et autres postes divers qui sont imputés au client. 
- **Taxes** : Cette classification représentent les montants des taxes que les utilisateurs ajoutent lorsqu’ils entrer des dépenses.
- **Transaction matérielle** : Cette classification représente les chiffres réels des lignes de produits sur une facture de projet confirmée.
- **Jalon** : Cette classification est utilisée par la logique de facturation à prix fixe.

Une ou plusieurs de ces classifications de transactions peuvent être associées à chaque ligne de devis. Une fois que le devis est remporté, le mappage entre la classification des transactions et la ligne de devis est transmis à la ligne de contrat.
  
Par exemple, un devis peut contenir les deux lignes de devis suivantes : 

- Travail de conseil qui utilise un mode de facturation Heure et matériel où les classifications de temps et de frais sont applicables. Par exemple, toutes les transactions de temps et de frais pour l’exemple de projet **Mise en œuvre de Dynamics AX** sont appliquées au client selon le temps et le matériel utilisés. 
- Frais de votre voyage associés qui utilisent un mode de facturation à prix fixe. Par exemple, toutes les dépenses en voyage pour l’exemple de projet **Mise en œuvre de Dynamics AX** sont appliquées à une valeur monétaire fixe.

> [!NOTE]
> La combinaison des classifications de projet et de transaction **Temps**, **Dépenses** et **Frais** associées à une ligne de devis ou à une ligne de contrat doit être unique. Si la même combinaison de projet et de classe de transaction est associée à plusieurs lignes de contrat ou lignes de devis, Project Operations ne fonctionnera pas correctement.

## <a name="billing-types"></a>Types de facturations

Le champ **Type de facturation** définit le concept d’exigibilité. Il s’agit d’un groupe d’options avec les valeurs possibles suivantes :

- **Facturable** : Le coût cumulé par ce rôle/cette catégorie est un coût direct qui dirige la réalisation du projet, et le client payera pour ce travail. Le paiement peut être administré sous forme d’agencement Temps et matériel ou à prix fixe. Toutefois, l’employé qui consacre ce temps recevra le crédit correspondant pour son utilisation facturable.
- **Non facturable** : Le coût cumulé par ce rôle/cette catégorie est considéré comme un coût direct qui dirige la réalisation du projet, même si le client ne reconnaît pas ce fait et ne payera pas pour ce travail. L’employé qui consacre ce temps ne sera pas crédité de l’utilisation facturable à cet effet.
- **Gratuit** : Le coût cumulé par ce rôle/cette catégorie est considéré comme un coût direct qui dirige la réalisation du projet, et le client payera reconnaît ce fait. L’employé qui consacre ce temps sera crédité de l’utilisation facturable à cet effet. Toutefois, ce coût n’est pas imputé au client.
- **Non disponible** : Les coûts qui sont encourus dans les projets internes qui ne nécessitent pas de suivi du revenu sont suivis à l’aide de cette option.

## <a name="invoice-schedule"></a>Planification de facture

Une planification de facture est une série de dates auxquelles la facturation d’un projet se produit. Vous pouvez éventuellement créer une planification de facture dans une ligne de devis. Chaque ligne de devis peut posséder sa propre planification de facture. Pour créer une planification de facture, vous devez fournir les valeurs d’attribut suivantes :

- Une date de début de facturation 
- Une date de livraison qui représente la date de fin de facturation sur le projet
- Une fréquence de facture

Ces trois valeurs d’attribut permettent de générer un ensemble de dates provisoire sur lequel baser la facturation.

## <a name="invoice-frequency"></a>Fréquence de facture

La fréquence de facture est une entité qui stocke les valeurs d’attributs permettant d’exprimer la fréquence de la création de facture. Les attributs suivants expriment ou définissent l’entité de fréquence de facture :

- **Période** : Mensuelle, bihebdomadaire et hebdomadaire sont prises en charge. 
- **Exécutions par période** : Pour les périodes hebdomadaires et bihebdomadaires, vous pouvez définir une seul exécution par période. Pour les périodes mensuelles, vous pouvez définir entre une et quatre exécutions par période. 
- **Jours d’exécution** : Les jours où la facturation doit être exécutée. Vous pouvez configurer cet attribut de deux manières :
  - **Jours ouvrables** : Par exemple, vous pouvez spécifier que la facturation est exécutée chaque lundi ou un lundi sur deux. Les clients qui doivent définir la facturation à exécuter pendant un jour ouvrable peuvent préférer ce genre de configuration. 
  - **Jours civils** : Vous pouvez par exemple spécifier que la facturation est exécutée le septième et le vingt-et-unième jour de chaque mois. Certaines organisations peuvent préférer ce genre de configuration, car il permet de garantir que la facturation est exécutée à dates fixes tous les mois.
  
### <a name="invoice-schedule-for-a-fixed-price-quote-line"></a>Planification de facture pour une ligne de devis à prix fixe

Pour une ligne de devis à prix fixe, vous pouvez utiliser la grille **Planification de facture** pour créer des jalons de facturation égaux à la valeur de la ligne de devis.

- Pour créer des jalons de facturation divisés à parts égales, sélectionnez une fréquence de facturation, entrez la date de début de facturation sur la ligne de devis, et sélectionnez **Date de fin demandée** pour le devis dans la section **Résumé** de l’en-tête de devis. Ensuite, sélectionnez **Générer des jalons périodiques** afin de créer des jalons fractionnés à parts égales en fonction de la fréquence de facture sélectionnée. 
- Pour créer un jalon de facturation avec somme forfaitaire, créez un jalon, puis entrez la ligne de valeur du devis en tant que montant de jalon.
- Pour créer des jalons de facturation basés sur des tâches spécifiques dans le plan du projet, créez un jalon, et mappez-le à l’élément de la planification du projet dans l’interface utilisateur des jalons de facturation.
