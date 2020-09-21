---
title: Prévisions et budgets du projet
description: Microsoft Dynamics 365 Finance offre les prévisions de projet et les budgets de projet pour gérer et contrôler vos projets.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85a5577968024bf42449c50d72a11414f9207eec
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168077"
---
# <a name="project-forecasts-and-budgets"></a>Prévisions et budgets du projet

[!include [banner](../includes/banner.md)]

Il existe deux façons de gérer et de contrôler vos projets : les prévisions de projet et les budgets de projet. 

Utilisez les prévisions de projet si votre organisation a une perspective opérationnelle et se concentre sur les revenus et les coûts dérivés de transactions spécifiques. Utilisez la budgétisation de projet si votre organisation se concentre davantage sur les montants financiers. 

Les prévisions de projet et les budgets de projet utilisent des modèles de prévision pour contenir les montants de transaction projetés. 

Chaque méthode a ses propres avantages. Vous devez tenir compte des points suivants avant de sélectionner une méthode pour votre organisation.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Prévisions de projet**                  | **Budgétisation de projet**                              |
| **Attribution de période**     | Vous ne pouvez pas allouer explicitement des transactions sur un période fiscale. Au lieu de cela, la prévision et le contrôle de la prévision sont basés sur la durée de vie du projet. Les prévisions étant basées sur une date spécifique, vous devez déduire la période à partir de la date. | Vous pouvez allouer des transactions sur l’intégralité du projet ou une période fiscale. Si vous faite la répartition sur une période, vous pouvez reporter les montants inutilisés à la prochaine période fiscale. |
| **Affichage des transactions**  | Vous pouvez afficher les transactions dans les formulaires de prévision, où vous voyez les prévisions pour l’ensemble de l’entreprise et pour tous les projets, quelle que soit la hiérarchie. Pour vous concentrer sur un projet particulier, vous devez filtrer les données.                                       | Vous pouvez afficher les transactions budgétisées pour une seule hiérarchie de projet. Par conséquent, vous pouvez afficher les détails de la transaction pour un projet parent ou ses sous-projets.                 |
| **Variables de transaction** | Lorsque vous saisissez des transactions de prévision, vous pouvez utiliser chaque attribut existant pour une transaction réelle. Cela permet d’obtenir plus de détails dans les prévisions. Par exemple, vous pouvez entrer des détails pour les quantités, les employés, les articles ou les propriétés de ligne.         | Lorsque vous saisissez les détails du budget, vous ne pouvez utiliser que des montants, des catégories et des activités.                    |
| **Sécurité**              | La prévision est basée sur les transactions que vous saisissez dans les formulaires de prévision et n’implique aucun mécanisme de contrôle de processus. Tout employé disposant des autorisations pour un formulaire de prévision peut réviser les informations sans approbation.                                        | La budgétisation utilise le système de workflow, qui permet la gestion des changements et vous permet de conserver un historique des révisions.         |
| **Types d’entrée**           | Les écritures de transaction de prévision sont basées sur le nombre d’unités et sur les prix unitaires de coût et de vente.  | Les détails du budget sont basés sur des montants, qui sont répartis entre les coûts et les revenus.                                          |
| **Modèles de prévision**       | Puisque chaque prévision doit être associée à un modèle, vous pouvez créer plusieurs modèles de prévision et également configurer des sous-modèles.           | La budgétisation de projet limite les modèles de prévision utilisés pour la budgétisation. Moins de modèles de prévision peuvent contribuer à accroître la cohérence des projections.                           |
| **Dépassements de coûts**         | Vous pouvez uniquement autoriser ou interdire la saisie de transactions qui entraîneront un dépassement de coût.   | La budgétisation de projet fournit des options de contrôle supplémentaires pour les utilisateurs. Vous pouvez autoriser les avertissements et les dépassements.                    |
| **Contrôler**               | Le contrôle des prévisions est effectué en utilisant la réduction des prévisions. Les montants réels sont soustraits des soldes de transaction prévisionnels sans aucune piste d’audit. Cela peut rendre plus difficile la localisation des transactions réelles.                   | Dans le contrôle budgétaire du projet, les montants réels sont soustraits des montants du budget restant. Cela permet une piste d’audit plus claire.                                   |

## <a name="project-forecasts"></a>Prévisions de projet
Lorsque vous utilisez la prévision de projet, vous pouvez saisir des transactions de prévision dans des formulaires de prévision pour chaque type de transaction. Chaque attribut disponible pour une transaction réelle peut être utilisé pour une transaction de prévision, par exemple, rentabilité de ligne, attributs de ligne, employés ou descriptions. Vous pouvez également prévoir combien de temps après avoir engagé un coût vous facturerez un client. 

Les transactions de prévision de projet sont basées sur des unités et des montants. 

Vous devez associer chaque prévision de projet à un modèle de prévision. Lorsque vous saisissez une transaction de prévision, un modèle de prévision est automatiquement suggéré. Le modèle de prévision agit comme un conteneur pour les transactions de prévision. 

Vous pouvez désigner des modèles de prévision comme sous-modèles pour un modèle. Cela vous permet de prévoir par région, période ou service. Vous pouvez copier les transactions de prévision dans un modèle pour créer un nouveau modèle, et vous pouvez également transférer les transactions vers le grand livre. Comme il existe une relation univoque entre une prévision et un modèle, chaque modèle de prévision constitue un budget distinct pour un projet. 

Les modèles de prévision peuvent utiliser la réduction des prévisions comme mécanisme de contrôle des projets. Dans la réduction des prévisions, les transactions réelles réduisent les soldes des transactions prévisionnelles. Cependant, étant donné que la réduction des prévisions est appliquée au projet le plus élevé de la hiérarchie, elle fournit une vue limitée des modifications de la prévision. Par exemple, si un travailleur est associé à un sous-projet, les transactions réelles du travailleur sont enregistrées dans le projet parent. Cela peut rendre difficile le suivi des modifications, car vous ne pouvez pas facilement déterminer quelle transaction dans quel sous-projet a entraîné une réduction du montant prévu. Par conséquent, il est judicieux de créer une copie d’un modèle de prévision à utiliser pour la réduction des prévisions. Vous pouvez ensuite utiliser des rapports pour afficher ce qui était initialement prévu. 

Vous pouvez réviser, copier, supprimer ou transférer des prévisions de projet dans un budget du grand livre. Cependant, il n’y a pas de contrôle de processus. Tout employé disposant des autorisations pour un formulaire de prévision peut réviser les informations sans examen.

-   **Réviser** : vous pouvez réviser une transaction de prévision sous les mêmes formes que celles où les écritures d’origine ont été effectuées.
-   **Copier ou supprimer** : lorsque vous copiez des transactions de prévision, vous copiez les lignes de transaction d’un modèle de prévision dans un autre modèle de prévision. Lorsque vous supprimez une prévision, vous supprimez les transactions de prévision d’un modèle de prévision. Pour limiter les transactions de prévision qui sont copiées ou supprimées, sélectionnez des types et des dates de transaction spécifiques. Cela vous permet de copier ou de supprimer uniquement des parties spécifiques d’une prévision.
-   **Transfert** : lorsque vous transférez une prévision de projet vers un budget du grand livre, vous transférez les transactions de prévision d’un modèle de prévision vers un budget du grand livre. Vous pouvez remplacer toutes les transactions précédemment transférées dans le budget du grand livre vers lequel vous transférez vos prévisions de projet.

## <a name="project-budgets"></a>Budgets de projet
La budgétisation de projet est une méthode plus simple que la prévision, même si elle s’intègre aux modèles de prévision. Elle utilise un formulaire de saisie unique pour les détails et les révisions du budget d’origine, et permet des projections basées uniquement sur le montant, la catégorie ou l’activité. 

Dans la budgétisation de projet, tous les budgets et révisions d’origine doivent être envoyés à un workflow de projet pour approbation. Les workflows vous donnent un contrôle accru sur le processus et créent un enregistrement d’historique des modifications. 

La budgétisation de projet ressemble à la budgétisation du grand livre, mais elle est plus rapide et plus facile à mettre en place. De nombreuses options de la budgétisation du grand livre, telles que les séquences de numéros ou la devise, ne doivent pas être configurées séparément pour les projets.

Les budgets de projet sont automatiquement associés à deux modèles de prévision, un pour le budget d’origine et un pour le budget restant. Par conséquent, les rapports basés sur des modèles de prévision peuvent utiliser des données budgétaires. Lorsqu’un budget de projet est engagé, le système crée des transactions de prévision basées sur les modèles associés, qui sont utilisés à des fins de reporting et de contrôle.

## <a name="forecast-models"></a>Modèles de prévision
Les modèles de prévision ont une hiérarchie à un seul niveau. Cela signifie qu’une prévision de projet doit être associée à un modèle de prévision.

Si vous utilisez la prévision de projet, vous pouvez identifier les modèles comme sous-modèles. Vous pouvez ensuite créer des prévisions par service, période ou région. Par exemple, vous pouvez créer un modèle de prévision pour un an, puis créer des sous-modèles pour les prévisions régionales du Nord-Est, du Sud-Est, du Nord-Ouest et du Sud-Ouest que les responsables régionaux soumettent. En sélectionnant différentes options dans les rapports disponibles, vous pouvez afficher les informations par prévision totale ou par sous-modèle.



