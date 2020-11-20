---
title: Contrats basés sur les avances et les provisions – Simplifié
description: Cette rubrique fournit des informations sur les modèles de contrats basés sur les provisions et les paiements anticipés dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 912b235af5e561349fdfb481e5f5b7c5514669c3
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180864"
---
# <a name="advances-and-retainer-based-contracts---lite"></a>Contrats basés sur les avances et les provisions – Simplifié


_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations prend en charge les contrats basés sur les provisions. Un contrat basé sur les provisions est un ensemble négocié de paiements équitablement répartis pour lesquels le client sera facturé pendant toute la durée d’un projet. Ce type de contrat est généralement utilisé pour les modèles de facturation basés sur le temps et le matériel ou basés sur la consommation, dans lesquels il est nécessaire de donner au client une planification de facture et un échéancier de paiement prévisibles. Les chiffres réels de revenus réels accumulés à chaque période sont rapprochés du paiement reçu du client au début de la période. Conformément au concept du modèle de facturation du temps et du matériel, les valeurs de revenus accumulées au cours de chaque période peuvent varier en fonction des coûts engagés. Si le revenu accumulé est supérieur au montant reçu au début de la période, la société de livraison du projet peut :

- Facturer le client uniquement pour l’excédent 
- Reporter le rapprochement des revenus à la période de facturation suivante et générer une facture finale à la fin du projet pour l’ensemble du revenu non rapproché restant

Voici la principale différence entre un modèle de contrat basé sur les provisions et un modèle de contrat à prix fixe dans Project Operations : dans le modèle de contrat à prix fixe, le montant de la facture n’est pas lié aux coûts engagés. La facturation suit une approche par étapes qui est alignée sur les coûts engagés pour cette période. Dans un contrat basé sur les provisions, les revenus qui peuvent être facturés sont enregistrés en fonction de la méthode de facturation sur la ligne de contrat. Lorsque la méthode de facturation est Temps et matériel, les revenus facturables sont liés aux coûts engagés au cours d’une période donnée et peuvent varier d’une période à l’autre. Cependant, le client n’est facturé que pour le montant de la provision périodique. Le système utilise une autre facture à la fin de la période pour rapprocher le revenu facturable enregistré pendant la période avec le montant qui a été facturé au client au début de la période.

Cette méthode présente l’avantage suivant : les coûts du client deviennent prévisibles dans la planification de la provision contrairement au modèle standard Temps et matériel. L’organisation qui livre le projet dispose également d’une certaine marge de manœuvre pour couvrir le risque de recouvrement des coûts engagés en raison d’une augmentation de la portée, ce que ne permet pas un modèle à prix fixe.

En plus d’une planification périodique basée sur les provisions, Project Operations peut enregistrer un paiement anticipé ponctuel d’un client et le rapprocher des différentes composantes de coût du projet.

La provision dans Project Operations ne peut pas être utilisée tant qu’elle n’est pas facturée au client. Cette information est indiquée par les champs suivants sur la sous-grille pour les paiements anticipés et les provisions.

| Champ | Description | Impact en aval |
| --- | --- | --- |
| Montant disponible | Montant disponible pour être utilisé sur l’enregistrement de provision ou de paiement anticipé. | Tant que le paiement anticipé ou la provision n’est pas facturé, il ne peut pas être utilisé, ce qui signifie que le montant disponible sera nul. |
| Montant utilisé | Montant disponible qui est déjà utilisé sur la provision ou le paiement anticipé. | Un paiement anticipé ou une provision peut être partiellement rapproché sur une facture avec les coûts réels, dont une partie sera marquée comme déjà utilisée ou consommée. Le reste du montant du paiement anticipé ou de la provision peut être rapproché sur une future facture avec les coûts réels. |
