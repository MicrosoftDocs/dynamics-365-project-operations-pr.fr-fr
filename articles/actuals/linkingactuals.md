---
title: Origines des transactions – Associer les chiffres réels à leur source
description: Cette rubrique explique comment le concept d’origine des transactions est utilisé pour associer les chiffres réels aux enregistrements source d’origine, tels que les journaux d’entrées de temps, de dépense ou d’utilisation de matériel.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584823"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Origines des transactions – Associer les chiffres réels à leur source

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Des enregistrements d’origine de transaction sont créés pour associer les chiffres réels à leur source, telles que les journaux d’entrées de temps, de dépense et d’utilisation de matériel et les factures de projet.

L’exemple suivant explique le traitement classique des entrées de temps dans un cycle de vie de projet Project Operations.

> ![Traitement des entrées de temps dans Project Operations.](media/basic-guide-17.png)
 
1. L’envoi d’une entrée de temps entraîne la création de deux lignes de journal : une pour le coût et une pour les ventes non facturées.
2. L’approbation finale de l’entrée de temps entraîne la création de deux chiffres réels : une pour le coût et une pour les ventes non facturées.
3. Lorsque l’utilisateur crée une facture de projet, la transaction de ligne de facture est créée en utilisant les données du chiffre réel des ventes non facturées.
4. Lorsque la facture est confirmée, deux nouveaux chiffres réels sont créés : une contrepassation de ventes non facturées et un chiffre réel de ventes facturées.

Chaque événement dans ce workflow de traitement déclenche la création d’enregistrements dans l’entité Origine de la transaction pour aider à faire le suivi des relations entre ces enregistrements créés dans chaque entrée de temps, la ligne du journal, le chiffre réel et les détails de la ligne de facture.

Le tableau suivant indique l’enregistrement dans l’entité Origine de la transaction pour le workflow précédent.

| Événement                        | Origine                   | Type d’origine                       | Transaction                       | Type de transaction         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Envoi d’entrée de temps        | GUID de l’enregistrement de l’entrée de temps   | Entrée de temps                        | GUID de l’enregistrement de la ligne de journal (coût)   | Ligne de journal             |
| GUID de l’enregistrement de l’entrée de temps       | Entrée de temps               | GUID de l’enregistrement de la ligne de journal (ventes)  | Ligne de journal                      |                          |
| Approbation du temps                | GUID de l’enregistrement de la ligne de journal | Ligne de journal                      | GUID de l’enregistrement des ventes non facturées        | Chiffre réel                   |
| GUID de l’enregistrement de l’entrée de temps       | Entrée de temps               | GUID de l’enregistrement des ventes non facturées        | Chiffre réel                            |                          |
| GUID de l’enregistrement de la ligne de journal     | Ligne de journal             | GUID de l’enregistrement du chiffre réel du coût           | Chiffre réel                            |                          |
| GUID de l’enregistrement de l’entrée de temps       | Entrée de temps               | GUID de l’enregistrement du chiffre réel du coût           | Chiffre réel                            |                          |
| Création d’une facture             | GUID de l’enregistrement de l’entrée de temps   | Entrée de temps                        | GUID de la transaction de ligne de facture     | Transaction de ligne de facture |
| GUID de l’enregistrement de la ligne de journal     | Ligne de journal             | GUID de la transaction de ligne de facture     | Transaction de ligne de facture          |                          |
| Confirmation de la facture         | GUID de la ligne de facture        | Ligne de facture                      | GUID de l’enregistrement des ventes facturées          | Chiffre réel                   |
| GUID de la facture                 | Facture                  | GUID de l’enregistrement des ventes facturées          | Chiffre réel                            |                          |
| GUID du détail de la ligne de facture     | Détail de la ligne de facture      | GUID de l’enregistrement des ventes facturées          | Chiffre réel                            |                          |
| GUID de l’enregistrement de l’entrée de temps       | Entrée de temps               | GUID de l’enregistrement des ventes facturées          | Chiffre réel                            |                          |
| GUID de l’enregistrement de la ligne de journal     | Ligne de journal             | GUID de l’enregistrement des ventes facturées          | Chiffre réel                            |                          |
| GUID de l’enregistrement de l’entrée de temps       | Entrée de temps               | GUID de libération des ventes non facturées      | Chiffre réel                            |                          |
| GUID de l’enregistrement de la ligne de journal     | Ligne de journal             | GUID de libération des ventes non facturées      | Chiffre réel                            |                          |
| Correction de facture en mode Brouillon     | Ancien GUID du détail de la ligne de facture             | Transaction de ligne de facture          | GUID du détail de la ligne de facture de correction               | Transaction de ligne de facture |
| Ancien GUID de la ligne de facture                  | Ligne de facture             | GUID du détail de la ligne de facture de correction               | Transaction de ligne de facture          |                          |
| Ancien GUID de facture             | Facture                  | GUID du détail de la ligne de facture de correction               | Transaction de ligne de facture          |                          |
| GUID de l’enregistrement de l’entrée de temps       | Entrée de temps               | GUID du détail de la ligne de facture de correction               | Transaction de ligne de facture          |                          |
| GUID de l’enregistrement de la ligne de journal     | Ligne de journal             | GUID du détail de la ligne de facture de correction               | Transaction de ligne de facture          |                          |
| Correction confirmée de facture | Ancien GUID du détail de la ligne de facture             | Transaction de ligne de facture          | GUID du chiffre réel de ventes facturée contrepassée | Chiffre réel                   |
| Ancien GUID de la ligne de facture                  | Ligne de facture             | GUID du chiffre réel de ventes facturée contrepassée | Chiffre réel                            |                          |
| Ancien GUID de facture             | Facture                  | GUID du chiffre réel de ventes facturée contrepassée | Chiffre réel                            |                          |
| GUID de l’enregistrement de l’entrée de temps       | Entrée de temps               | GUID du chiffre réel de ventes facturée contrepassée | Chiffre réel                            |                          |
| GUID de l’enregistrement de la ligne de journal     | Ligne de journal             | GUID du chiffre réel de ventes facturée contrepassée | Chiffre réel                            |                          |
| Ancien GUID du détail de la ligne de facture                 | Transaction de ligne de facture | Nouveau GUID du chiffre réel des ventes non facturées    | Chiffre réel                            |                          |
| Ancien GUID de la ligne de facture                  | Ligne de facture             | Nouveau GUID du chiffre réel des ventes non facturées    | Chiffre réel                            |                          |
| Ancien GUID de facture             | Facture                  | Nouveau GUID du chiffre réel des ventes non facturées    | Chiffre réel                            |                          |
| GUID de l’enregistrement de l’entrée de temps       | Entrée de temps               | Nouveau GUID du chiffre réel des ventes non facturées    | Chiffre réel                            |                          |
| GUID de l’enregistrement de la ligne de journal     | Ligne de journal             | Nouveau GUID du chiffre réel des ventes non facturées    | Chiffre réel                            |                          |
| GUID du détail de la ligne de facture de correction          | Transaction de ligne de facture | Nouveau GUID du chiffre réel des ventes non facturées    | Chiffre réel                            |                          |
| GUID de la ligne de facture de correction           | Ligne de facture             | Nouveau GUID du chiffre réel des ventes non facturées    | Chiffre réel                            |                          |
| GUID de facture de correction      | Facture                  | Nouveau GUID du chiffre réel des ventes non facturées    | Réel                            |                          |


L’illustration suivante montre les liens qui sont créés entre les chiffres réels et leurs sources lors de divers événements en utilisant l’exemple d’entrées de temps dans Project Operations.

> ![Comment les chiffres réels sont associés aux enregistrements source dans Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
