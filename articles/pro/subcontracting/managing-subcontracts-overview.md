---
title: Gestion de la sous-traitance dans Project Operations
description: Cette rubrique présente le processus de gestion de la sous-traitance de bout en bout courant pour les organisations basées sur des projets.
author: rumant
ms.date: 08/02/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d595e948b7be9a6822827f4841e737d3c0e1476b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593011"
---
# <a name="subcontract-management-in-project-operations"></a>Gestion de la sous-traitance dans Project Operations

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique présente le processus de gestion de la sous-traitance de bout en bout pour les organisations basées sur des projets. La sous-traitance des services suit généralement le flux des processus d’entreprise illustré dans le schéma suivant.

![Flux de processus de sous-traitance](../media/SubcontractingProcessFlow.png)

La liste suivante fournit une description étape par étape du processus de sous-traitance.

1. Le chef de projet crée un contrat de sous-traitance avec un fournisseur. Par défaut, les tarifs joints à l′enregistrement fournisseur sont utilisés pour le contrat de sous-traitance. Le compte fournisseur a un type de relation **Vendeur** ou **Fournisseur**.
2. Le chef de projet peut ventiler tous les achats sous forme d′éléments de ligne dans le contrat de sous-traitance. Les lignes du contrat de sous-traitance peuvent concerner le temps, les dépenses ou les produits. La classe de transaction de la ligne du contrat de sous-traitance détermine l’objet de la ligne.
3. Le gestionnaire de compte fournisseur et le chef de projet peuvent itérer sur le contrat de sous-traitance. La tarification peut être ajustée au niveau des tarifs d′achat joints au contrat de sous-traitance.
4. À ce stade ou plus tard dans le processus, si la ligne du contrat de sous-traitance concerne le temps, le gestionnaire de compte fournisseur associe des contacts fournisseur à chaque ligne du contrat de sous-traitance. Cette association fournit des informations au chef de projet qui travaille sur le contrat de sous-traitance. Si un fournisseur est associé à une ligne d’un contrat de sous-traitance, le système crée automatiquement une ressource réservable à partir du contact, si une ressource réservable n’existe pas déjà.
5. Le mode de facturation sur chaque ligne du contrat de sous-traitance peut être **Prix fixe** ou **Temps et matériel**. Pour les lignes de contrat de sous-traitance à prix fixe, il est possible de configurer un échéancier de facturation basé sur des jalons.
6.  Une fois le contrat de sous-traitance mis en place et la négociation terminée, le contrat est confirmé. Les contrats de sous-traitance confirmés ne peuvent pas être modifiés. Toutefois, si des modifications surviennent, un contrat de sous-traitance peut être « rouvert à des fins de modifications », le statut **Confirmé** est alors remplacé par **Brouillon** et la négociation peut être rouverte. 
7.  Lors de la création d’un membre générique de l’équipe sur un projet, le membre de l’équipe peut être associé à une ligne du contrat de sous-traitance. Cela indique que le membre générique de l’équipe doit disposer d’une capacité de sous-traitance.
8.  Les membres de l’équipe nommés peuvent être créés directement sur un projet ou en les réservant à l’aide des expériences de planification des ressources. Si un membre de l’équipe de projet nommé est un sous-traitant, il est possible de l’associer à une ligne du contrat de sous-traitance. Cela entraînera une réduction de la capacité disponible sur une ligne du contrat de sous-traitance.
9.  Les ressources de sous-traitance peuvent enregistrer le temps, les dépenses et l’utilisation des matériaux sur les projets et les tâches du projet, puis les soumettre pour approbation. C’est la même chose pour les employés. Lors de l’enregistrement du temps, un sous-traitant peut sélectionner un contrat de sous-traitance et une ligne spécifiques.
10. Après approbation, le temps approuvé par les contrats de sous-traitance enregistre les coûts réels du projet en fonction du prix d’achat du sous-traitant ou du rôle qu’il a joué sur le projet.
11. Les factures fournisseur et les articles de facture fournisseur peuvent être enregistrés dans le système pour le travail effectué par les ressources fournisseur ou les produits livrés par le fournisseur. Les lignes de facture fournisseur doivent être spécifiques à un projet et pour une classe de transaction de temps, de dépenses, de produit/matériel, de jalon ou de frais. Les lignes de facture fournisseur peuvent éventuellement faire référence à une ligne du contrat de sous-traitance.
12. Le système associera automatiquement tous les coûts réels correspondant à la ligne du contrat de sous-traitance et au projet à la facture fournisseur. Cela facilitera une correspondance à trois facteurs et un processus de vérification.
13. Le chef de projet peut ensuite examiner les chiffres réels du projet automatiquement mis en correspondance, supprimer ou ajouter d’autres chiffres réels au projet et terminer le processus de vérification.
14. Une fois le processus de vérification effectué sur toutes les lignes, la facture fournisseur est alors marquée comme **Prête à être payée**. À ce stade, les lignes de facture du fournisseur peuvent être transférées vers un système comptable afin de traiter le paiement. Les coûts du projet précédemment enregistrés seront contrepassés et les coûts réels de la ligne de facture du fournisseur seront enregistrés sur le projet.

## <a name="quantity-based-subcontract-lines-and-work-based-subcontract-lines"></a>Lignes du contrat de sous-traitance basées sur la quantité et lignes du contrat de sous-traitance basées sur le travail

Une ligne du contrat de sous-traitance peut être basée sur la quantité ou sur le travail. 

Lorsqu’une ligne du contrat de sous-traitance est **basée sur la quantité**, la quantité achetée sur la ligne du contrat de sous-traitance pour le temps, les dépenses ou le matériel peut être utilisée sur n’importe quel projet.

Lorsqu’une ligne du contrat de sous-traitance est **basée sur le travail**, la ligne du contrat de sous-traitance correspond à un ensemble de travaux représenté par un nœud dans le plan de projet. La valeur de la ligne du contrat de sous-traitance est la somme de tous les composants nécessaires à la livraison de cet ensemble de travaux. Ils sont modélisés comme des détails de la ligne du contrat de sous-traitance et il peut s’agir d’un ensemble d’heures, de dépense ou de matériel. S’il s’agit d’une ligne du contrat de sous-traitance basée sur le travail, elle est en outre dédiée à un seul projet. Ces types de sous-contrats ne sont actuellement pas pris en charge par Project Operations.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

