---
title: Transactions commerciales
description: Cette rubrique fournit des informations sur les transactions commerciales.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 048bd2d98e6332e6c48a24f4eacee5b937ef04a9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126975"
---
# <a name="business-transactions"></a>Transactions commerciales

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dans Dynamics 365 Project Service Automation, *transaction commerciale* est un concept abstrait qui n’est représenté par aucune entité. Toutefois, certains champs et processus communs dans les entités sont conçus pour utiliser le concept de transactions commerciales. Les entités suivantes utilisent ce concept :

- Détails de la ligne de devis
- Détails de la ligne de contrat
- Lignes d’estimation
- Lignes de journal
- Chiffres réels

Dans ces entités, Détails de la ligne de devis, Détails de la ligne de contrat et Lignes d’estimation sont mappés à la phase d’estimation au cours du cycle de vie du projet. Les entités Lignes de journal et Chiffres réels sont mappées à la phase d’exécution au cours du cycle de vie du projet.

PSA traite les enregistrements de ces cinq entités comme des transactions commerciales. La seule différence est que les enregistrements dans les entités mappées à la phase d’estimation sont considérés comme des prévisions financières, alors que les enregistrements dans les entités mappées à la phase d’exécution sont considérés comme des faits financiers qui se sont déjà produits.

Pour plus d’informations, voir [Estimations](estimates.md) et [Chiffres réels](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Concepts propres aux transactions commerciales
Les concepts suivants sont propres au concept des transactions commerciales :

- Type de transaction
- Classe de transaction
- Origine de la transaction
- Connexion de la transaction

### <a name="transaction-type"></a>Type de transaction

Le type de transaction représente la chronologie et le contexte de l’impact financier sur un projet. Il est représenté par un jeu d’options avec les valeurs suivantes prises en charge dans PSA :
- Coût
- Contrat du projet
- Ventes non facturées
- Ventes facturées
- Ventes entre organisations
- Coût unitaire d’allocation des ressources

### <a name="transaction-class"></a>Classe de transaction

La classe de transaction représente les différents types de coûts encourus dans des projets. Il est représenté par un jeu d’options avec les valeurs suivantes prises en charge dans PSA :

- Temps
- Dépenses
- Matériel
- Frais
- Jalon
- Taxes

La valeur **Jalon** est généralement utilisée par une logique métier pour la facturation à prix fixe dans PSA.

### <a name="transaction-origin"></a>Origine de la transaction

L’origine de la transaction est une entité qui stocke l’origine de chaque transaction commerciale. Au fur et à mesure de l’exécution du projet, chaque transaction commerciale donnera lieu à une autre transaction commerciale qui, à son tour, en créera une autre, etc. L’entité d’origine des transactions a été conçue pour stocker des données sur l’origine de chaque transaction afin de faciliter la génération de rapports et la traçabilité. 

### <a name="transaction-connection"></a>Connexion de la transaction

Connexion de la transaction est une entité qui stocke la relation entre deux transactions commerciales similaires, telles que le coût et les chiffres réels associés aux ventes, ou des contrepassations de transaction déclenchées par les activités de facturation, telles que la confirmation de facture ou les corrections de facture.

Ensemble, Origine de la transaction et Connexion de la transaction vous permettent de garder le suivi des relations entre les transactions commerciales et les actions qui ont entraîné la création d’une transaction commerciale spécifique.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Exemple : Comment Origine de la transaction fonctionne avec Connexion de la transaction

L’exemple suivant explique le traitement classique des entrées de temps dans un cycle de vie de projet PSA.

> ![Traitement des entrées de temps au cours du cycle de vie de Project Service](media/basic-guide-17.png)
 
1. L’envoi d’une entrée de temps entraîne la création de deux lignes de journal : une pour le coût et une pour les ventes non facturées.
2. L’approbation finale de l’entrée de temps entraîne la création de deux chiffres réels : une pour le coût et une pour les ventes non facturées.
3. Lorsque l’utilisateur crée une facture de projet, la transaction de ligne de facture est créée en utilisant les données du chiffre réel des ventes non facturées. 
4. Lorsque la facture est confirmée, deux nouveaux chiffres réels sont créés : une contrepassation de ventes non facturées et un chiffre réel de ventes facturées.

Chacun de ces événements déclenche la création d’enregistrements dans les entités Origine de la transaction et Connexion de la transaction pour aider à faire le suivi des relations entre ces enregistrements créés dans chaque entrée de temps, la ligne du journal, les chiffres réels, les détails de la ligne de facture.

Le tableau suivant indique l’enregistrement dans l’entité Origine de la transaction pour le workflow précédent.

| Événement                        | Origine                    | Type d’origine                       | Transaction                       | Type de transaction         |
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
| GUID de facture de correction      | Facture                  | Nouveau GUID du chiffre réel des ventes non facturées    | Chiffre réel                            |                          |

Le tableau suivant indique l’enregistrement dans l’entité Connexion de la transaction pour le workflow précédent.

| Événement                          | Transaction 1                 | Rôle de la transaction 1 | Type de la transaction 1           | Transaction 2                | Rôle de la transaction 2 | Type de la transaction 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Envoi d’entrée de temps          | GUID de la ligne de journal (ventes)     | Ventes non facturées     | msdyn_journalline            | GUID de la ligne de journal (coût)     | Coût               | msdyn_journalline  |
| Approbation du temps                  | GUID du chiffre réel non facturé (ventes)  | Ventes non facturées     | msdyn_actual                 | GUID du chiffre réel du coût (coût)       | Coût               | msdyn_actual       |
| Création d’une facture               | GUID du détail de la ligne de facture      | Ventes facturées       | msdyn_invoicelinetransaction | GUID du chiffre réel de ventes non facturées   | Ventes non facturées     | msdyn_actual       |
| Confirmation de la facture           | GUID du chiffre réel de contrepassation         | Contrepassation          | msdyn_actual                 | GUID des ventes non facturées d’origine | D’origine           | msdyn_actual       |
| GUID des ventes facturées              | Ventes facturées                  | msdyn_actual       | GUID du chiffre réel de ventes non facturées   | Ventes non facturées               | msdyn_actual       |                    |
| Correction de facture en mode Brouillon       | GUID de la transaction de ligne de facture | Remplacement          | msdyn_invoicelinetransaction | GUID des ventes facturées            | D’origine           | msdyn_actual       |
| Confirmer la correction de la facture     | GUID de contrepassation des ventes facturées    | Contrepassation          | msdyn_actual                 | GUID des ventes facturées            | D’origine           | msdyn_actual       |
| Nouveau GUID du chiffre réel des ventes non facturées | Remplacement                     | msdyn_actual       | GUID des ventes facturées            | D’origine                     | msdyn_actual       |                    |
