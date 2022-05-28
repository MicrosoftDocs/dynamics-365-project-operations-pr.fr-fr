---
title: Importer une estimation vers une ligne de contrat basée sur un projet
description: Cette rubrique fournit des informations sur le mode d’importation des estimations à partir d’un projet vers une ligne du contrat.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8e03a384e401331aea6e65881b4ecc88da77d737
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8601613"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Importer une estimation vers une ligne de contrat basée sur un projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Dans Dynamics 365 Project Operations, vous pouvez importer des estimations d’un projet vers une ligne de contrat basée sur un projet.

1. Vérifiez que le champ **Projet** de la ligne de contrat basé sur le projet est rempli.
2. Dans l’onglet **Détails de la ligne de contrat**, dans la sous-grille, sélectionnez **Importer à partir de l’estimation du projet**. Une page de dialogue avec des options de synthèse s’ouvre. Les options de synthèse disponibles sont **Classe de transaction**, **Catégorie**, **Rôle** et **Tâche de projet**. En fonction des sélections de synthèse, l’estimation du projet pour toutes les classes de transactions incluses dans cette ligne de contrat sont copiées. 
3. Pour vérifier quelles classes de transaction sont incluses, dans l’onglet **Général** sur la ligne de contrat et vérifiez les valeurs des champs **Inclure le temps**, **Inclure les dépenses** et **Inclure les frais**.

Lorsque vous importez des estimations, l’application définit par défaut la tarification en fonction des listes de prix du projet jointes au contrat et du type de facturation configuré sur la ligne de contrat. Si un rôle ou une catégorie est configuré(e) sur la ligne de contrat comme non facturable, la ligne d’estimation importée sera définie comme non facturable et ne s’ajoutera pas à la valeur contractée de la ligne de contrat.

Lorsqu’une ligne de contrat comporte des détails de ligne, les champs **Valeur du contrat** et **Taxe estimée** de la ligne de contrat sont résumés et ne peuvent pas être modifiés.

Lorsque plusieurs options de synthèse sont sélectionnées, le système tente de résumer par toutes les options sélectionnées. Le résultat de la synthèse entraîne plus de lignes de contrat importées que si vous sélectionnez une seule option de synthèse.

Par exemple, si le projet comportait les lignes d’estimation suivantes pour les dépenses :

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| Tâche B | Hôtel | 10/1/2020 | 4 | 200 | 800 |
| Tâche C | Hôtel | 11/1/2020 | 2 | 200 | 400 |

Lorsque l’utilisateur choisit de synthétiser par **classe de transaction**, les informations suivantes sont importées :

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 10/1/2020 | 3.34 | 840 | 2800 |

Lorsque l’utilisateur choisit de synthétiser par **classe de transaction** et **catégorie**, les informations suivantes sont importées :

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hôtel | 10/1/2020 | 6 | 200 | 1200 |

Lorsque l’utilisateur choisit de synthétiser par **classe de transaction**, **catégorie** et **tâche de nœud terminal**, les informations suivantes sont importées. Notez que ce résultat est le même que ce qui était sur le projet :

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| Tâche B | Hôtel | 10/1/2020 | 4 | 200 | 800 |
| Tâche C | Hôtel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]