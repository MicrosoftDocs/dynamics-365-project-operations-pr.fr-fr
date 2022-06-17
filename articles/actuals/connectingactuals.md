---
title: Connexions de transaction – Associer les chiffres réels de différents types de transaction
description: Cet article explique comment une connexion de transaction est utilisée pour associer les chiffres réels de différents types afin de faciliter le suivi de la rentabilité, de l’arriéré de facturation et des calculs de revenus facturés et non facturés.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926083"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Connexions de transaction – Associer les chiffres réels de différents types de transaction

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Des enregistrements de connexion de transaction sont créés pour associer les chiffres réels de différents types au fur et à mesure que le temps, les dépenses ou l’utilisation de matériel évoluent dans son cycle de vie, de l’étape du devis ou de la prévente à la phase contractuelle, des approbations et/ou des rappels, de la facturation et éventuellement de la facturation de crédit ou corrective.

L’exemple suivant explique le traitement classique des entrées de temps dans un cycle de vie de projet Project Operations.

> ![Traitement des entrées de temps dans Project Operations.](media/basic-guide-17.png)

L’exemple suivant explique le traitement des entrées de temps dans un cycle de vie de projet Project Operations : 

1. L’envoi d’une entrée de temps entraîne la création de deux lignes de journal : une pour le coût et une pour les ventes non facturées. 
2. L’approbation finale de l’entrée de temps entraîne la création de deux chiffres réels : une pour le coût et une pour les ventes non facturées. Ces 2 chiffres réels sont liés à l’aide de connexions de transaction.
3. Lorsque l’utilisateur crée une facture de projet, la transaction de ligne de facture est créée en utilisant les données du chiffre réel des ventes non facturées.
4. Lorsque la facture est confirmée, deux nouveaux chiffres réels sont créés : une contrepassation de ventes non facturées et un chiffre réel de ventes facturées. La contrepassation des ventes non facturées et le chiffre réel des ventes non facturées d’origine sont connectés à l’aide de connexions de transaction de contrepassation. Les ventes facturées et les ventes réelles non facturées d’origine sont également connectées pour montrer les liens entre ce qui était autrefois le revenu du carnet de commandes ou des travaux en cours et ce qui est maintenant le revenu facturé.   

Chaque événement du workflow de traitement déclenche la création d’enregistrements dans la table **Connexion de la transaction**. Cela permet de créer une trace de la relation entre les enregistrements créés dans les détails de ligne d’entrée de temps, de journal, de chiffre réel et de facture.

La table suivante indique l’enregistrement dans l’entité **Connexion de la transaction** pour le workflow précédent.

|Événement                   |Transaction 1                 |Rôle de la transaction 1 |Type de la transaction 1       |Transaction 2          |Rôle de la transaction 2 |Type de la transaction 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Envoi d’entrée de temps   |GUID de la ligne de journal (ventes)     |Ventes non facturées |msdyn_journalline            |GUID de la ligne de journal (coût)     |Coût            |msdyn_journalline  |
|Approbation du temps           |GUID du chiffre réel non facturé (ventes)  |Ventes non facturées |msdyn_actual                 |GUID du chiffre réel du coût (coût)       |Coût            |msdyn_actual       |
|Création d’une facture        |GUID du détail de la ligne de facture      |Ventes facturées   |msdyn_invoicelinetransaction |GUID du chiffre réel de ventes non facturées   |Ventes non facturées  |msdyn_actual       |
|Confirmation de la facture    |GUID du chiffre réel de contrepassation         |Contrepassation      |msdyn_actual                 |GUID des ventes non facturées d’origine |D’origine        |msdyn_actual       |
|                        |GUID des ventes facturées             |Ventes facturées   |msdyn_actual                 |GUID du chiffre réel de ventes non facturées   |Ventes non facturées  |msdyn_actual       |
|Correction de facture en mode Brouillon |GUID de la transaction de ligne de facture|Remplacement      |msdyn_invoicelinetransaction |GUID des ventes facturées            |D’origine        |msdyn_actual       |
|Confirmer la correction de la facture|GUID de contrepassation des ventes facturées  |Contrepassation      |msdyn_actual                 |GUID des ventes facturées            |D’origine        |msdyn_actual       |
|                        |Nouveau GUID des ventes non facturées |Remplacement            |msdyn_actual                 |GUID des ventes facturées            |D’origine        |msdyn_actual       |


L’illustration suivante montre les liens qui sont créés entre différents types de chiffres réels lors de divers événements en utilisant l’exemple d’entrées de temps dans Project Operations.

> ![Comment les chiffres réels de différents types sont associés les uns aux autres dans Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
