---
title: Importer des estimations pour un projet vers une ligne de devis de projet
description: Cette rubrique fournit des informations sur l’importation d’estimations d’un projet sur une ligne de devis de projet.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a9ac27b7694927f9cea88b49310f3106fbc6542cc0f7f1756744b970358c1057
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993508"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Importer des estimations pour un projet vers une ligne de devis de projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_


Si un projet est créé pendant la phase de prévente, vous pouvez choisir d’importer l’estimation financière du projet vers la ligne de devis selon les projets.

1. Assurez-vous que la ligne de devis selon les projets contient les informations sur le projet dans le champ **Projet**.
2. Sur l’onglet **Détails de la ligne de devis**, sélectionnez **Importer à partir des estimations de projets**.
3. Dans la boîte de dialogue qui s’ouvre, sélectionnez l’une des options de synthèse suivantes :

  - **Classe de transaction**
  - **Catégorie**
  - **Rôle** 
  - **Tâche du projet**

En fonction de votre sélection, l’estimation du projet pour toutes les classes de transactions incluses dans cette ligne de devis est copiée. Pour vérifier quelles classes de transaction sont incluses, sélectionnez l’onglet **Général** sur la ligne de devis selon les projets et vérifiez les valeurs de **Inclure le temps**, **Inclure les dépenses**, et **Inclure les frais**.

Lorsque vous importez des estimations, le système définit par défaut la tarification en fonction des listes de prix du projet jointes au devis et du type de facturation configuré sur la ligne de devis selon les projets. Si un rôle ou une catégorie est configurée sur la ligne de devis selon les projets comme non facturable, la ligne d’estimation importée sera définie comme non facturable et ne s’ajoutera pas à la valeur citée de la ligne de devis.

Lorsqu’une ligne de devis comporte des détails de ligne, les champs **Valeur du devis** et **Taxe estimée** de la ligne de devis sont résumés et ne peuvent pas être modifiés.

Lorsque plusieurs options de synthèse sont sélectionnées, le système tente de résumer par toutes les options sélectionnées. Il en résulte que la sortie des lignes de devis importées sera plus importante que si vous ne sélectionniez qu’une seule option de synthèse.

Par exemple, si le projet comporte les lignes d’estimation suivantes pour les dépenses.

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| Tâche B | Hôtel | 10/1/2020 | 4 | 200 | 800 |
| Tâche C | Hôtel | 11/1/2020 | 2 | 200 | 400 |

Lorsque l’utilisateur choisit de synthétiser par classe de transaction, les informations suivantes sont importées.

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| | | 10/1/2020 | 3.34 | 840 | 2800 |

Lorsque l’utilisateur choisit de synthétiser par classe de transaction et catégorie, les informations suivantes sont importées.

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| | Hôtel | 10/1/2020 | 6 | 200 | 1200 |

Lorsque l’utilisateur choisit de synthétiser par classe de transaction, catégorie et tâche de nœud terminal, les informations suivantes sont importées. Notez que ce résultat est le même que ce qui était sur le projet.

| Tâche | Catégorie | Date | Quantité | Prix unitaire | Montant |
| --- | --- | --- | --- | --- | --- |
| Tâche A | Billets d’avion | 10/1/2020 | 4 | 400 | 1600 |
| Tâche B | Hôtel | 10/1/2020 | 4 | 200 | 800 |
| Tâche C | Hôtel | 11/1/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
