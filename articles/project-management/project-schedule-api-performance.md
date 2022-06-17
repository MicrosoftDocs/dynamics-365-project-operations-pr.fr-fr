---
title: Performances de l’API de planification de projets
description: Cet article fournit des informations sur les benchmarks de performance des API de planification de projets et identifie les pratiques recommandées pour une utilisation optimale.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911179"
---
# <a name="project-schedule-api-performance"></a>Performances de l’API de planification de projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés, déploiement simplifié : traiter la facturation pro forma, Project for the Web_

Cet article fournit des informations sur les benchmarks de performance des interfaces de programmation d’applications (API) de planification de projets et identifie les pratiques recommandées pour optimiser l’utilisation.

## <a name="project-scheduling-service"></a>Service de planification de projets
Le service de planification de projets est un service multiclient qui s’exécute dans Microsoft Azure. Il est conçu pour améliorer l’interaction en offrant une expérience rapide et fluide lorsque les utilisateurs travaillent sur des projets. Cette amélioration est obtenue en acceptant les demandes de modification, en les traitant, puis en renvoyant immédiatement le résultat. Le service persiste de manière asynchrone dans Dataverse et n’empêche pas les utilisateurs d’effectuer d’autres opérations.

Les API de planification de projets s’appuient sur le service de planification de projets pour exécuter des demandes qui sont décrites plus en détail dans les sections suivantes de cet article.

Les API de planification de projets sont conçues pour fonctionner avec les entités de structure de répartition du travail (WBS) suivantes :

  - Project
  - Tâche du projet
  - Dépendance de la tâche du projet
  - Membre de l’équipe du projet
  - Attribution de ressource
  
Les champs prédéfinis et les champs personnalisés sont pris en charge. Sauf indication contraire, toutes les opérations courantes sont prises en charge, comme la création, la mise à jour et la suppression. Pour plus d’informations, consultez [Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification](schedule-api-preview.md).

Dans le cadre des API de planification de projets, un modèle d’unité de travail a été ajouté. Ce modèle est appelé OperationSet et peut être utilisé lorsque plusieurs demandes doivent être traitées dans une seule transaction.

L’illustration suivante montre le flux qu’un partenaire expérimentera lorsque cette fonctionnalité est utilisée.

![Dataverse et le flux du service de planification de projets.](./media/dataverse-project-scheduling-service-flow.png)

**Étape 1** : un client effectue un appel d’API à un point de terminaison Open Data Protocol (OData) dans Dataverse pour créer un OperationSet.

**Étape 2** : une fois le nouvel OperationSet créé, une valeur **OperationSetId** est renvoyée.

**Étape 3** : le client utilise la valeur **OperationSetId** pour créer une autre demande d’API de planification de projets. Le résultat est une demande de création, de mise à jour ou de suppression sur une entité de planification. Lorsque cette demande est créée, la validation des métadonnées est effectuée. Si la validation échoue, la demande est terminée et une erreur est renvoyée.

**Étapes 4a à 4c** : ces étapes représentent la phase ACCEPTER. Le client appelle l’API **ExécuteOperationSetV1**, qui envoie toutes les modifications au service de planification de projets en un seul lot. Le service de planification de projets exécute ses propres validations sur les demandes du lot. Tout échec de validation annule le lot et renvoie une exception à l’appelant. Si le lot est accepté avec succès par le service de planification de projets, le statut d’OperationSet est mis à jour pour refléter le fait qu’OperationSet est en cours de traitement par le service de planification de projets.

**Étape 5** : cette étape représente la phase PERSISTER. Le service de planification de projets écrit de manière asynchrone le lot dans Dataverse dans une transaction. Si l’opération d’écriture réussit, OperationSet est marqué comme **Terminé**. Toute erreur restaure la transaction et le lot, et OperationSet est marqué comme **Échec**.

## <a name="performance-methodology"></a>Méthodologie de performances
Le temps d’exécution est défini comme le temps entre l’appel à l’API **ExecuteOperationSetV1** et le moment où le service de planification de projets a terminé d’écrire dans Dataverse. Toutes les opérations s’exécutent 2 200 fois au total et les mesures du temps d’exécution P99 sont spécifiées. Les opérations à enregistrement unique et en bloc sont mesurées.

Pour une opération à enregistrement unique, OperationSet contient une demande. Pour les opérations en bloc, il contient 20, 50 ou 100 demandes. Chaque taille en bloc est spécifiée séparément.

Ces opérations s’exécutent sur un déploiement UR 15 Project Operations Lite en Amérique du Nord.

## <a name="results"></a>Résultats
### <a name="create-operations"></a>Opérations de création
#### <a name="single-record-create-operations"></a>Opérations de création d’un enregistrement unique
Le tableau suivant présente les temps d’exécution pour la création d’un enregistrement unique. Les temps sont exprimés en secondes.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Type&nbsp;&nbsp;&nbsp;d’enregistrement</th>
    <th class="tg-0lax" colspan="2">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax">Champs obligatoires</th>
    <th class="tg-0lax">Tous les champs pris en charge</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tâche</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Affectation</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membre d’équipe</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dépendance</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Opérations de création en bloc
Le tableau suivant présente les temps d’exécution pour la création de nombreux enregistrements. Plus précisément, Microsoft a mesuré les temps d’exécution pour la création de 20, 50 et 100 enregistrements dans un seul OperationSet. Les temps sont exprimés en secondes.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Type&nbsp;&nbsp;&nbsp;d’enregistrement</th>
    <th class="tg-0lax" colspan="6">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 enregistrements</th>
    <th class="tg-0lax" colspan="2">50 enregistrements</th>
    <th class="tg-0lax" colspan="2">100 enregistrements</th>
  </tr>
  <tr>
    <th class="tg-0lax">Champs obligatoires</th>
    <th class="tg-0lax">Tous les champs pris en charge</th>
    <th class="tg-0lax">Champs obligatoires</th>
    <th class="tg-0lax">Tous les champs pris en charge</th>
    <th class="tg-0lax">Champs obligatoires</th>
    <th class="tg-0lax">Tous les champs pris en charge</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tâche</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Affectation</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dépendance</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Les opérations de création en bloc sur les entités **Projet** et **Membre de l’équipe** ne sont pas incluses dans ce tableau, car le temps d’exécution pour ces opérations ressemble au temps d’exécution lorsque l’API de création d’un enregistrement unique est appelée plusieurs fois. Ces API sont exécutées immédiatement dans Dataverse.

L’illustration suivante montre un tracé des temps d’exécution pour les entités **Tâche**, **Affectation** et **Dépendance** lorsque 20, 50 et 100 enregistrements sont créés et tous les champs pris en charge sont utilisés.

![Graphique des temps d’exécution pour la création d’un enregistrement.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Opérations de mise à jour
#### <a name="single-record-update-operations"></a>Opérations de mise à jour d’un enregistrement unique
Le tableau suivant présente les temps d’exécution pour les mises à jour d’un enregistrement unique. Les temps sont exprimés en secondes.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Type&nbsp;&nbsp;&nbsp;d’enregistrement</th>
    <th class="tg-0lax" colspan="2">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax">Champs obligatoires </th>
    <th class="tg-0lax">Tous les champs pris en charge</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tâche</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membre d’équipe</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Les opérations de mise à jour sur les entités **Affectations de ressources** et **Dépendance entre les tâches d’un projet** ne sont pas prises en charge.

#### <a name="bulk-update-operations"></a>Opérations de mise à jour en bloc
Le tableau suivant montre les temps d’exécution pour les mises à jour de nombreux enregistrements. Plus précisément, Microsoft a mesuré les temps d’exécution pour les mises à jour de 20, 50 et 100 enregistrements dans un seul OperationSet. Les temps sont exprimés en secondes.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Type&nbsp;&nbsp;&nbsp;d’enregistrement</th>
    <th class="tg-0lax" colspan="6">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 enregistrements</th>
    <th class="tg-0lax" colspan="2">50 enregistrements</th>
    <th class="tg-0lax" colspan="2">100 enregistrements</th>
  </tr>
  <tr>
    <th class="tg-0lax">Champs obligatoires</th>
    <th class="tg-0lax">Tous les champs pris en charge</th>
    <th class="tg-0lax">Champs obligatoires</th>
    <th class="tg-0lax">Tous les champs pris en charge</th>
    <th class="tg-0lax">Champs obligatoires</th>
    <th class="tg-0lax">Tous les champs pris en charge</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tâche</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membre d’équipe</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Les opérations de mise à jour sur les entités **Affectations de ressources** et **Dépendance entre les tâches d’un projet** ne sont pas prises en charge.

L’illustration suivante montre un tracé des temps d’exécution pour les entités Tâche et Membre de l’équipe lorsque 20, 50 et 100 enregistrements sont mis à jour et tous les champs pris en charge sont utilisés.

![Graphique des temps d’exécution pour la mise à jour d’un enregistrement.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Opérations de suppression
#### <a name="single-record-delete-operations"></a>Opérations de suppression d’un enregistrement unique
Le tableau suivant présente les temps d’exécution pour la suppression d’un enregistrement unique. Les temps sont exprimés en secondes.

| Type d’enregistrement | Temps  |
|-------------|-------|
| Tâche        | 20.12 |
| Affectation  | 10.86 |
| Membre d’équipe | 12.52 |
| Dépendance  | 20.89 |

> [!NOTE]
> Les opérations de suppression sur l’entité **Projet** ne sont pas prises en charge.

#### <a name="bulk-delete-operations"></a>Opérations de suppression en bloc
Le tableau suivant présente les temps d’exécution pour la suppression de nombreux enregistrements. Plus précisément, Microsoft a mesuré les temps d’exécution pour la suppression de 20, 50 et 100 enregistrements dans un seul OperationSet. Les temps sont exprimés en secondes.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Type&nbsp;&nbsp;&nbsp;d’enregistrement</th>
    <th class="tg-0lax" colspan="3">Temps</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 enregistrements</th>
    <th class="tg-0lax">50 enregistrements</th>
    <th class="tg-0lax">100 enregistrements</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tâche</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Affectation</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Membre d’équipe</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dépendance</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Les opérations de suppression sur l’entité **Projet** ne sont pas prises en charge.

L’illustration suivante montre un tracé des temps d’exécution pour les entités **Tâche**, **Affectation**, **Membre de l’équipe** et **Dépendance** lorsque 20, 50 et 100 enregistrements sont supprimés.

![Graphique des temps d’exécution pour la suppression d’un enregistrement.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Observations
Pour chaque opération d’enregistrement, l’API **ExecuteOperationSet** met environ 800 millisecondes pour envoyer une demande au service de planification de projets. Le service de planification de projets met ensuite environ cinq secondes pour traiter la charge utile et appeler Dataverse. Le reste du temps d’exécution est consacré à l’exécution de la logique métier et à l’écriture des données dans la base de données de Dataverse.

Lorsque 100 enregistrements sont créés, mis à jour ou supprimés, l’API **ExecuteOperationSet** met environ trois secondes pour envoyer la demande au service de planification de projets. Le service de planification de projets met ensuite environ cinq secondes pour traiter les demandes et appeler Dataverse. Les opérations en bloc doivent payer une **Taxe du service de planification de projets** une seule fois, pour tous les enregistrements d’OperationSet. Par conséquent, les opérations en bloc ont un temps d’exécution moyen nettement inférieur à celui des opérations à enregistrement unique.

## <a name="scenarios"></a>Scénarios
Le tableau suivant montre les temps d’exécution lorsque les API de planification de projets sont utilisées pour accomplir des scénarios spécifiques. Les temps sont exprimés en secondes.

| Scénario                                                                   | Temps  |
|----------------------------------------------------------------------------|-------|
| Créez un projet comportant 40 tâches.                                      | 36.01 |
| Créez un projet comportant 40 tâches et 20 dépendances.                  | 38.11 |
| Créez un projet comportant 40 tâches et 30 affectations.                   | 60.17 |
| Créez un projet comportant 40 tâches, 20 dépendances et 30 affectations. | 60.27 |

## <a name="best-practices"></a>Meilleures pratiques
En fonction des résultats du scénario précédent, les API fonctionnent mieux dans les conditions suivantes :

  - Regroupez autant d’opérations que possible. Le temps d’exécution moyen pour les opérations en bloc est meilleur que le temps d’exécution moyen pour les opérations à enregistrement unique. Plus le nombre d’OperationSets en cours d’utilisation est petit, plus le temps d’exécution moyen sera rapide.
  - Définissez uniquement les attributs minimaux nécessaires pour accomplir votre scénario. Soyez sélectif pour les types de champs non obligatoires inclus dans une demande OperationSet. Les champs qui contiennent des clés étrangères ou des champs de cumul affecteront négativement les performances.
