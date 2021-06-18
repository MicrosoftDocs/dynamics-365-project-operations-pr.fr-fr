---
title: Chiffres réels
description: Cette rubrique des informations sur l’utilisation de chiffres réels dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996608"
---
# <a name="actuals"></a>Chiffres réels 

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les chiffres réels représentent l’état d’avancement des finances et du calendrier révisé et approuvé d’un projet. Ils sont créés suite à l’approbation des entrées de temps, de dépenses, de l’utilisation du matériel ainsi que des écritures feuille et des factures.

## <a name="journal-lines-and-time-submission"></a>Lignes de journal et envoi de temps

Pour plus d’informations sur l’entrée de temps, voir [Vue d’ensemble des entrées de temps](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Temps et matériaux

Lorsqu’une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.

### <a name="fixed-price"></a>Prix fixe

Quand une entrée de temps envoyée est liée à un projet mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.

### <a name="default-pricing"></a>Tarification par défaut

La logique de création des prix par défaut se trouve sur la ligne de journal. Les valeurs de champ de l’entrée de temps sont copiées sur la ligne de journal. Ces valeurs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats.

Les champs qui affectent la tarification par défaut, par exemple **Rôle** et **Unité d’allocation des ressources**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal. Vous pouvez ajouter un champ personnalisé sur l’entrée de temps. Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**. Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions. Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Lignes de journal et envoi des dépenses de base

Pour plus d’informations sur l’entrée des dépenses, voir [Vue d’ensemble des dépenses](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Temps et matériaux

Lorsqu’une entrée de dépenses de base envoyée est liée à un projet mappé à une ligne de contrat temps et matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.

### <a name="fixed-price"></a>Prix fixe

Quand une entrée de dépenses de base envoyée est liée à un projet qui est mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.

### <a name="default-pricing"></a>Tarification par défaut

La logique de saisie des prix par défaut des dépenses est basée sur la catégorie de dépenses. La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats. Les champs qui affectent la tarification par défaut, par exemple **Catégorie de transaction** et **Unité d’allocation des ressources**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal. Cependant, cela ne fonctionne que lorsque la méthode de tarification dans les tarifs est **Prix unitaire**. Si la méthode de tarification est **À prix coûtant** ou **Majoration du coût**, le prix saisi lors de la création de l’entrée de dépense est utilisé pour le coût et le prix sur la ligne du journal des ventes est calculé en fonction de la méthode de tarification. 

Vous pouvez ajouter un champ personnalisé sur l’entrée des dépenses. Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**. Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions. Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Soumission des lignes de journal et du journal d’utilisation du matériel

Pour plus d’informations sur l’entrée des dépenses, voir [Journal d’utilisation des matériaux](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Temps et matériaux

Lorsqu’une entrée du journal d’utilisation du matériel envoyée est liée à un projet qui est mappé à une ligne de contrat de temps et de matériel, le système crée deux lignes de journal, une pour le coût et une pour les ventes non facturées.

### <a name="fixed-price"></a>Prix fixe

Quand une entrée du journal d’utilisation du matériel envoyée est liée à un projet qui est mappé à une ligne de contrat à prix fixe, le système crée une ligne de journal pour le coût.

### <a name="default-pricing"></a>Tarification par défaut

La logique d’entrée des prix par défaut pour le matériel est basée sur la combinaison de produit et d’unité. La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats. Les champs qui affectent la tarification par défaut, par exemple **ID produit** et **Unité**, sont utilisés pour déterminer le tarif approprié sur la ligne de journal. Cependant, cela ne fonctionne que pour les produits du catalogue. Pour les produits hors catalogue, le prix saisi lors de la création de l’entrée du journal d’utilisation du matériel est utilisé pour le prix de revient et le prix de vente sur les lignes de journal. 

Vous pouvez ajouter un champ personnalisé sur l’entrée **Journal d’utilisation des matériaux**. Si vous souhaitez que la valeur du champ soit propagée aux chiffres réels, créez le champ dans les tables **Chiffres réels** et **Ligne de journal**. Utilisez un code personnalisé pour propager la valeur du champ sélectionné de Entrée de temps à Chiffres réels via la ligne de journal à l’aide des origines des transactions. Pour plus d’informations sur les origines des transactions et les connexions, voir [Lier les chiffres réels aux enregistrements d’origine](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Utiliser des journaux pour enregistrer les coûts

Vous pouvez utiliser les journaux des entrées pour enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes. Les journaux peuvent être utilisés aux fins suivantes :

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
