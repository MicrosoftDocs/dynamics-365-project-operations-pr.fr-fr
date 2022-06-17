---
title: Impact des chiffres réels pendant la phase de prévente d’un engagement
description: Cet article offre des informations sur l’impact sur le tableau des chiffres réels lors de divers événements lorsqu’un engagement est dans la phase de prévente dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922357"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Impact des chiffres réels pendant la phase de prévente d’un engagement

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Le tableau suivant répertorie les chiffres réels des différents types de transaction créés lors de divers événements pendant la phase de prévente d’un engagement de projet.

| Événement | Coût réel | Exemple |
|---|---|---|
| L’heure est créée. | Non applicable | <p>Bob Kozack, de l’unité d’organisation Fabrikam US dont le coût est de 100 dollars américains (100 USD) par heure, travaille sur un projet intitulé « Arm Installation at Adatum ». Ce projet est mappé sur un mode de facturation à prix fixe sur la ligne de contrat. Voici un exemple d’entrée de temps de Bob Kozak :</p><p>Bob Kozack – 8 heures</p> |
| L’heure est envoyée. | Non applicable | Une ligne de journal des coûts est créée pour l’entrée de temps. Le coût par défaut est saisi dans l’entrée de journal. |
| L’entrée de temps est rappelée avant d’être approuvée. | Non applicable | |
| L’heure est approuvée. | Un chiffre réel du coût est créé. | <p>Nouveau chiffre réel créé :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, 8 heures, 800 USD</li></ul> |
| L’approbation de l’heure est annulée. | <p>Le statut d’ajustement du chiffre réel du coût d’origine est mis à jour avec la valeur **Ajusté**.</p><p>Un chiffre réel du coût de contrepassation est créé avec un statut d’ajustement défini sur **Non ajustable**.</p> | <p>Chiffre réel existant mis à jour :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, 8 heures, 800 USD, *Ajusté*</li></ul><p>Nouveau chiffre réel créé pour annuler le précédent impact financier :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, (8 heures), (800 USD), *Non ajustable*</li></ul> |
| L’entrée de temps est rappelée après être approuvée. | <p>Le statut d’ajustement du chiffre réel du coût d’origine est mis à jour avec la valeur **Ajusté**.</p><p>Un chiffre réel du coût de contrepassation est créé avec un statut d’ajustement défini sur **Non ajustable**.</p> | <p>Chiffre réel existant mis à jour :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, 8 heures, 800 USD, *Ajusté*</li></ul><p>Nouveau chiffre réel créé pour annuler le précédent impact financier :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, (8 heures), (800 USD), *Non ajustable*</li></ul> |
| Le devis est gagné, et un contrat est créé. | <p>Le statut d’ajustement des anciens chiffres réels du coût est mis à jour avec la valeur **Ajusté**.</p><p>Les chiffres réels du coût de contrepassation sont créés avec un statut d’ajustement défini sur **Non ajustable**.</p><p>De nouveaux chiffres réels du coût sont créés après la réévaluation des règles contractuelles.</p> | <p>Chiffre réel existant mis à jour :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, 8 heures, 800 USD, *Ajusté*</li></ul><p>Nouveau chiffre réel créé pour annuler le précédent impact financier :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, (8 heures), (800 USD), *Non ajustable*</li></ul><p>Chiffres réels créés pour l’impact financier réévalué lorsque le devis est remporté et que le contrat est créé :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, 8 heures, 800 USD</li><li>**Chiffre réel de vente non facturé :** Bob Kozack, 8 heures, 1 600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
