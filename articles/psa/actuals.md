---
title: Vue d’ensemble des chiffres réels
description: Cette rubrique fournit des informations sur les chiffres réels du projet.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146120"
---
# <a name="actuals-overview"></a>Vue d’ensemble des chiffres réels

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les chiffres réels sont la quantité de travail effectuée sur un projet. Les chiffres réels du projet peuvent être retracés jusqu’à leurs documents origine. Ces documents origine incluent les écritures de temps, de dépenses et de journal, ainsi que les factures.

![Comment les chiffres réels du projet de planification sont retracés jusqu’aux documents origine](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Envoi d’une entrée de temps

Dans PSA, quand une entrée de temps est envoyée pour un projet qui est mappé à une ligne de contrat de durée et de matériaux, deux lignes du journal sont créées. Une ligne est pour le coût, tandis que l’autre est pour les ventes non facturées. Quand une entrée de temps est envoyée pour un projet qui est mappé à une ligne de contrat à prix fixe, une ligne de journal seulement est créée pour le coût. 

La logique d’entrée des prix par défaut se trouve sur la ligne de journal. Toutes les valeurs de champ d’une entrée de temps sont copiées sur la ligne de journal. Ces champs comprennent la date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que le résultat en devise dans les tarifs adéquats. 

Les champs qui touchent les prix par défaut, par exemple **Rôle** et **Unité d’organisation**, entraînent un tarif approprié à entrer par défaut sur la ligne de journal. Si vous ajoutez un champ personnalisé à l’entrée de temps, et que vous souhaitez que la valeur de champ soit propagée aux chiffres réels, créez un champ dans l’entité Chiffres réels, puis utilisez les mappages de champs pour copier le champ de l’entrée de temps dans les chiffres réels.

## <a name="submitting-an-expense-entry"></a>Envoi d’une entrée de dépenses

Dans PSA, quand une entrée de dépenses est envoyée pour un projet qui est mappé à une ligne de contrat de durée et de matériaux, deux lignes du journal sont créées. Une ligne est pour le coût, tandis que l’autre est pour les ventes non facturées. Quand une entrée de dépenses est envoyée pour un projet qui est mappé à une ligne de contrat à prix fixe, une ligne de journal seulement est créée pour le coût.

La logique d’entrée des prix par défaut pour les dépenses est basée sur la catégorie de dépenses sélectionnée sur la page **Entrée de dépense**. La date de la transaction, la ligne de contrat auquel le projet est mappé, ainsi que la devise sont tous utilisés pour déterminer les tarifs adéquats. Toutefois, pour le prix lui-même, le montant que l’utilisateur a entré est défini directement sur les lignes de journal relatives de dépenses pour le coût et les ventes par défaut.

Dans la version actuelle de PSA, l’entrée basée sur la catégorie des prix unitaires par défaut dans les entrées de dépense n’est pas disponible.

## <a name="using-entry-journals-to-record-costs"></a>Utilisation des journaux d’entrées pour enregistrer les coûts

Dans PSA, les journaux d’entrées vous permettent d’enregistrer les coûts ou les revenus dans les classes de transaction des matériaux, frais, durée, dépenses ou taxes. Un journal comporte un en-tête, des lignes, puis une action **Confirmer**. Voici quelques scénarios où vous pourriez utiliser un journal :

- Vous devez enregistrer les coûts et les ventes réels des matériaux sur un projet.
- Vous devez déplacer des chiffres réels de la transaction d’un autre système à PSA.
- Vous devez enregistrer les coûts qui se sont produits dans un autre système, tel que les coûts d’approvisionnement ou de sous-traitance.

> [!IMPORTANT]
> L’utilisation des journaux d’entrées pour créer des chiffres réels ne doit être effectuée que par un utilisateur qui est pleinement conscient de l’impact comptable des chiffres réels sur le projet. En effet, l’application ne valide pas le type de ligne de journal ou la tarification associée qui est entrée sur la ligne de journal. En raison de l’impact de ce type de journal, choisissez attentivement les personnes autorisées à créer des journaux d’entrées.     


## <a name="recording-actuals-based-on-project-events"></a>Enregistrement des chiffres réels en fonction des événements du projet

PSA enregistre les transactions financières qui se produisent pendant un projet. Ces transactions sont enregistrées comme **chiffres réels**. Les tableaux suivants illustrent les différents types de chiffres réels qui sont créés, selon qu’il s’agit d’un projet basé sur la durée et les matériaux ou d’un projet à prix fixe, se trouvant dans la phase préalable à la vente, ou d’un projet interne.

**La ressource appartient à la même unité d’organisation que l’unité contractuelle du projet**

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

**La ressource appartient à une unité d’organisation différente de l’unité contractuelle du projet**

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
