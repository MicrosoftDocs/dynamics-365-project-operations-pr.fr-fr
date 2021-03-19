---
title: Chiffres réels
description: Cette rubrique des informations sur l’utilisation de chiffres réels dans Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291796"
---
# <a name="actuals"></a>Chiffres réels 

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les chiffres réels sont la quantité de travail effectuée sur un projet. Ils sont créés à la suite d’écritures de temps et de dépenses, d’écritures de journal et de factures.

## <a name="journal-lines-and-time-submission"></a>Lignes de journal et envoi de temps

Pour plus d’informations sur l’entrée de temps, voir [Vue d’ensemble des entrées de temps](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Temps et matériaux

Lorsqu’une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.

### <a name="fixed-price"></a>Prix fixe

Quand une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.

### <a name="default-pricing"></a>Tarification par défaut

La logique de création des prix par défaut se trouve sur la ligne de journal. Les valeurs de champ de l’entrée de temps sont copiées sur la ligne de journal. Ces valeurs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.

Les champs qui affectent la tarification par défaut, par exemple **Rôle** et **Unité d’organisation**, sont utilisés pour déterminer le tarif approprié à entrer par défaut sur la ligne de journal. Vous pouvez ajouter un champ personnalisé sur l’entrée de temps. Si vous souhaitez que la valeur de champ soit propagée aux chiffres réels, créez un champ dans l’entité Chiffres réels, puis utilisez les mappages de champs pour copier le champ de l’entrée de temps dans les chiffres réels.

## <a name="journal-lines-and-basic-expense-submission"></a>Lignes de journal et envoi des dépenses de base

Pour plus d’informations sur l’entrée des dépenses, voir [Vue d’ensemble des dépenses](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Temps et matériaux

Lorsqu’une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.

### <a name="fixed-price"></a>Prix fixe

Quand une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.

### <a name="default-pricing"></a>Tarification par défaut

La logique de saisie des prix par défaut des dépenses est basée sur la catégorie de dépenses. La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats. Toutefois, par défaut, le montant entré pour le prix lui-même est défini directement sur les lignes de journal relatives de dépenses pour le coût et les ventes.

L’entrée basée sur la catégorie des prix unitaires par défaut dans les entrées de dépense n’est pas disponible.

## <a name="use-entry-journals-to-record-costs"></a>Utiliser des journaux pour enregistrer les coûts

Vous pouvez utiliser les journaux des entrées pour enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes. Les journaux peuvent être utilisés aux fins suivantes :

- Enregistrer les coûts réels du matériel et les ventes sur un projet.
- Déplacer les chiffres réels de transactions d’un autre système vers Microsoft Dynamics 365 Project Operations.
- Enregistrer les coûts survenus dans un autre système. Ces coûts peuvent inclure des coûts d’approvisionnement ou de sous-traitance.

> [!IMPORTANT]
> L’application ne valide pas le type de ligne de journal ou la tarification associée qui est saisie sur la ligne de journal. Par conséquent, seul un utilisateur pleinement conscient de l’impact comptable des chiffres réels sur le projet doit utiliser des journaux d’entrées pour créer des chiffres réels. En raison de l’impact de ce type de journal, vous devez choisir soigneusement qui a accès pour créer des journaux d’entrées.
## <a name="record-actuals-based-on-project-events"></a>Enregistrer des chiffres réels en fonction des événements du projet

Project Operations enregistre les transactions financières qui se produisent pendant un projet. Ces transactions sont enregistrées comme chiffres réels. Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu’il s’agit d’un projet basé sur la durée et les matériaux ou d’un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d’un projet interne.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>La ressource appartient à la même unité d’organisation que l’unité contractuelle du projet

<table>
<thead>
<tr>
<th rowspan="3">Event</th>
<th colspan="4">Projet facturable ou vendu</th>
<th rowspan="3">Projet dans la phase préalable à la vente</th>
<th rowspan="3">Projet interne</th>
</tr>
<tr>
<th colspan="2">Temps et matériaux</th>
<th colspan="2">Prix fixe</th>
</tr>
<tr>
<th>Chiffres réels</th>
<th>Devise de transaction</th>
<th>Prix fixe</th>
<th>Devise de transaction</th>
</tr>
</thead>
<tbody>
<tr>
<td>Une entrée de temps est créée.</td>
<td colspan="6">Aucune activité dans l’entité Chiffres réels</td>
</tr>
<tr>
<td>Une entrée de temps est envoyée.</td>
<td colspan="6">Aucune activité dans l’entité Chiffres réels</td>
</tr>
<tr>
<td rowspan="2">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</td>
<td>Coût réel</td>
<td>Devise de l’unité contractuelle</td>
<td rowspan="2">Coût réel</td>
<td rowspan="2">Devise de l’unité contractuelle
<td rowspan="2">Coût réel</td>
<td rowspan="2">Coût réel</td>
</tr>
<tr>
<td>Chiffre réel des ventes non facturées - Facturable</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="3">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</td>
<td>Coût réel</td>
<td>Devise de l’unité contractuelle</td>
<td rowspan="3">Coût réel</td>
<td rowspan="3">Devise de l’unité contractuelle</td>
<td rowspan="3">Coût réel</td>
<td rowspan="3">Coût réel</td>
</tr>
<tr>
<td>Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Chiffre réel des ventes non facturées - Non facturable pour la différence</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="2">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</td>
<td>Libération des ventes non facturées</td>
<td>Devise du contrat du projet</td>
<td rowspan="2">Ventes facturées pour le jalon</td>
<td rowspan="2">Devise du contrat du projet</td>
<td rowspan="2">Non applicable</td>
<td rowspan="2">Non applicable</td>
</tr>
<tr>
<td>Ventes facturées</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="3">Une facture est confirmée, et une diminution des heures facturables survient.</td>
<td>Libération des ventes non facturées</td>
<td>Devise du contrat du projet</td>
<td rowspan="3">Non applicable</td>
<td rowspan="3">Non applicable</td>
<td rowspan="3">Non applicable</td>
<td rowspan="3">Non applicable</td>
</tr>
<tr>
<td>Ventes facturées - Facturable pour la nouvelle quantité</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Ventes facturées - Non facturable pour la différence</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="2">Une facture est corrigée pour augmenter la quantité facturable.</td>
<td>Ventes facturées - Libération</td>
<td>Devise du contrat du projet</td>
<td rowspan="5">
<ul>
<li>Libération des ventes facturées pour le jalon</li>
<li>Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></li>
</ul>
</td>
<td rowspan="5">Devise du contrat du projet</td>
<td rowspan="5">Non applicable</td>
<td rowspan="5">Non applicable</td>
</tr>
<tr>
<td>Ventes facturées</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="3">Une facture est corrigée pour diminuer la quantité facturable.</td>
<td>Ventes facturées - Libération</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Ventes facturées pour la nouvelle quantité</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Ventes non facturées - Facturable pour la différence</td>
<td>Devise du contrat du projet</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>La ressource appartient à une unité d’organisation différente de l’unité contractuelle du projet

<table>
<thead>
<tr>
<th rowspan="3">Event</th>
<th colspan="4">Projet facturable ou vendu</th>
<th rowspan="3">Projet dans la phase préalable à la vente</th>
<th rowspan="3">Projet interne</th>
</tr>
<tr>
<th colspan="2">Temps et matériaux</th>
<th colspan="2">Prix fixe</th>
</tr>
<tr>
<th>Chiffres réels</th>
<th>Devise de transaction</th>
<th>Prix fixe</th>
<th>Devise de transaction</th>
</tr>
</thead>
<tbody>
<tr>
<td>Une entrée de temps est créée.</td>
<td colspan="6">Aucune activité dans l’entité Chiffres réels</td>
</tr>
<tr>
<td>Une entrée de temps est envoyée.</td>
<td colspan="6">Aucune activité dans l’entité Chiffres réels</td>
</tr>
<tr>
<td rowspan="4">Le temps est approuvé, et aucune modification ou augmentation des heures facturables ne survient au cours de l’approbation.</td>
<td>Coût réel</td>
<td>Devise de l’unité contractuelle</td>
<td rowspan="4">Coût réel</td>
<td rowspan="4">Devise de l’unité contractuelle</td>
<td rowspan="4">Coût réel</td>
<td rowspan="4">Coût réel</td>
</tr>
<tr>
<td>Chiffre réel des ventes non facturées - Facturable</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Coût unitaire d’allocation des ressources</td>
<td>Devise de l’unité d’allocation des ressources</td>
</tr>
<tr>
<td>Ventes entre organisations</td>
<td>Devise de l’unité contractuelle</td>
</tr>
<tr>
<td rowspan="5">Le temps est approuvé, et une diminution des heures facturables survient au cours de l’approbation.</td>
<td>Coût réel</td>
<td>Devise de l’unité contractuelle</td>
<td rowspan="5">Coût réel</td>
<td rowspan="5">Devise de l’unité contractuelle</td>
<td rowspan="5">Coût réel</td>
<td rowspan="5">Coût réel</td>
</tr>
<tr>
<td>Coût unitaire d’allocation des ressources</td>
<td>Devise de l’unité d’allocation des ressources</td>
</tr>
<tr>
<td>Ventes entre organisations</td>
<td>Devise de l’unité contractuelle</td>
</tr>
<tr>
<td>Chiffre réel des ventes non facturées - Facturable pour la nouvelle quantité</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Chiffre réel des ventes non facturées - Non facturable pour la différence</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="2">Une facture est confirmée, et aucune modification ou augmentation des heures facturables ne survient.</td>
<td>Libération des ventes non facturées</td>
<td>Devise du contrat du projet</td>
<td rowspan="2">Ventes facturées pour le jalon</td>
<td rowspan="2">Devise du contrat du projet</td>
<td rowspan="2">Non applicable</td>
<td rowspan="2">Non applicable</td>
</tr>
<tr>
<td>Ventes facturées</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="3">Une facture est confirmée, et une diminution des heures facturables survient.</td>
<td>Libération des ventes non facturées</td>
<td>Devise du contrat du projet</td>
<td rowspan="3">Non applicable</td>
<td rowspan="3">Non applicable</td>
<td rowspan="3">Non applicable</td>
<td rowspan="3">Non applicable</td>
</tr>
<tr>
<td>Ventes facturées - Facturable pour la nouvelle quantité</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Ventes facturées - Non facturable pour la différence</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="2">Une facture est corrigée pour augmenter la quantité facturable.</td>
<td>Ventes facturées - Libération</td>
<td>Devise du contrat du projet</td>
<td rowspan="5">
<ul>
<li>Libération des ventes facturées pour le jalon</li>
<li>Passez dans le statut du jalon de <strong>Facturé</strong> à <strong>Prêt pour la facturation</strong></li>
</ul>
</td>
<td rowspan="5">Devise du contrat du projet</td>
<td rowspan="5">Non applicable</td>
<td rowspan="5">Non applicable</td>
</tr>
<tr>
<td>Ventes facturées</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td rowspan="3">Une facture est corrigée pour diminuer la quantité facturable.</td>
<td>Ventes facturées - Libération</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Ventes facturées pour la nouvelle quantité</td>
<td>Devise du contrat du projet</td>
</tr>
<tr>
<td>Ventes non facturées - Facturable pour la différence</td>
<td>Devise du contrat du projet</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]