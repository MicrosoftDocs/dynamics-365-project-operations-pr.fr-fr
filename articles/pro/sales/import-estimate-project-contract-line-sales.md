---
title: Importer une estimation vers une ligne de contrat basée sur un projet – Simplifié
description: Cet article fournit des informations sur l’importation d’estimations financières d’un projet à une ligne de contrat.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d6e3bdfeb1ea9de32d6712ac5671be39c243702a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924197"
---
# <a name="import-an-estimate-to-a-project-based-contract-line---lite"></a>Importer une estimation vers une ligne de contrat basée sur un projet – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, vous pouvez importer des estimations d’un projet vers une ligne de contrat basée sur un projet.

1. Vérifiez que le champ **Projet** de la ligne de contrat basé sur le projet a été rempli.
2. Dans l’onglet **Détails de la ligne de contrat**, dans la sous-grille, sélectionnez **Importer à partir de l’estimation du projet**. Une page de dialogue avec des options de synthèse s’ouvre. Les options de synthèse disponibles sont **Classe de transaction**, **Catégorie**, **Rôle** et **Tâche de projet**.
3. En fonction de votre sélection de synthèse, l’estimation du projet pour toutes les classes et tâches de transactions incluses dans cette ligne de contrat sont copiées. Pour vérifier quelles classes de transaction sont incluses, dans l’onglet **Général** sur la ligne de contrat selon les projets et vérifiez les valeurs des champs **Inclure le temps**, **Inclure les dépenses** et **Inclure les frais**. 
4. Pour voir quelles tâches sont incluses, sélectionnez l’onglet **Tâches facturables** sur la ligne de contrat. Basé sur les tâches associées qui ont le champ **Classes de transaction incluses** défini sur **Oui**, toutes les estimations pour ces combinaisons de tâches et de classes de transactions sont importées dans la ligne de contrat.

Lorsque vous importez des estimations, le système définit par défaut la tarification en fonction des listes de prix du projet jointes au contrat et du type de facturation configuré sur la ligne de contrat. Si une tâche, un rôle ou une catégorie est configuré(e) comme non facturable, la ligne d’estimation importée sera définie comme non facturable et ne s’ajoutera pas à la valeur contractée de la ligne de contrat.

Lorsqu’une ligne de contrat comporte des détails de ligne, les champs **Valeur du contrat** et **Taxe estimée** de la ligne de contrat sont résumés et ne peuvent pas être modifiés.

Lorsque plusieurs options de synthèse sont sélectionnées, le système tente de résumer par toutes les options sélectionnées. Le résultat de la synthèse entraîne plus de lignes de contrat importées que si vous sélectionnez une seule option de synthèse.

Par exemple, si le projet comporte les lignes d’estimation suivantes pour les dépenses :

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| Tâche B | Hôtel | 10/1/2020 | 4 | 200 | 800 |
| Tâche C | Hôtel | 11/1/2020 | 2 | 200 | 400 |

Lorsque l’utilisateur choisit de synthétiser par **classe de transaction**, les informations suivantes sont importées :

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 10/1/2020 | 3.34 | 840 | 2800 |

Lorsque l’utilisateur choisit de synthétiser par **classe de transaction** et **catégorie**, les informations suivantes sont importées :

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| &nbsp;| Hôtel | 10/1/2020 | 6 | 200 | 1200 |

Lorsque l’utilisateur choisit de synthétiser par **classe de transaction**, **catégorie** et **tâche de nœud terminal**, les informations suivantes sont importées. Notez que ce résultat est le même que ce qui est sur le projet :

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| Tâche B | Hôtel | 10/1/2020 | 4 | 200 | 800 |
| Tâche C | Hôtel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]