---
title: Impact des chiffres réels pour un projet interne
description: Cette rubrique offre des informations sur l’impact sur le tableau des chiffres réels lors de divers événements pour un projet interne dans Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579763"
---
# <a name="actuals-impact-for-an-internal-project"></a>Impact des chiffres réels pour un projet interne

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Le tableau suivant répertorie les chiffres réels des différents types de transaction créés lors de divers événements dans le cadre d’un engagement de projet interne.

| Événement | Coût réel | Exemple |
|---|---|---|
| L’heure est créée. | Non applicable | <p>Bob Kozack, de l’unité d’organisation Fabrikam US dont le coût est de 100 dollars américains (100 USD) par heure, travaille sur un projet intitulé « Arm Installation at Adatum ». Ce projet est mappé sur un mode de facturation à prix fixe sur la ligne de contrat. Voici un exemple d’entrée de temps de Bob Kozak :</p><p>Bob Kozack – 8 heures</p> |
| L’heure est envoyée. | Non applicable | Une ligne de journal des coûts est créée pour l’entrée de temps. Le coût par défaut est saisi dans l’entrée de journal. |
| L’entrée de temps est rappelée avant d’être approuvée. | Non applicable | |
| L’heure est approuvée. | Un chiffre réel du coût est créé. | <p>Nouveau chiffre réel créé :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, 8 heures, 800 USD</li></ul> |
| L’approbation de l’heure est annulée. | <p>Le statut d’ajustement du chiffre réel du coût d’origine est mis à jour avec la valeur **Ajusté**.</p><p>Un chiffre réel du coût de contrepassation est créé avec un statut d’ajustement défini sur **Non ajustable**.</p> | <p>Chiffre réel existant mis à jour :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, 8 heures, 800 USD, *Ajusté*</li></ul><p>Nouveau chiffre réel créé pour annuler le précédent impact financier :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, (8 heures), (800 USD), *Non ajustable*</li></ul> |
| L’entrée de temps est rappelée après être approuvée. | <p>Le statut d’ajustement du chiffre réel du coût d’origine est mis à jour avec la valeur **Ajusté**.</p><p>Un chiffre réel du coût de contrepassation est créé avec un statut d’ajustement défini sur **Non ajustable**.</p> | <p>Chiffre réel existant mis à jour :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, 8 heures, 800 USD, *Ajusté*</li></ul><p>Nouveau chiffre réel créé pour annuler le précédent impact financier :</p><ul><li>**Chiffre réel du coût :** Bob Kozack, (8 heures), (800 USD), *Non ajustable*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
