---
title: Scénarios à plusieurs devises (version 3.x)
description: Cette rubrique fournit des informations sur les scénarios à plusieurs devises.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 70f27d29c74a82f0307bd0724347960e5755e3a8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014788"
---
# <a name="multiple-currency-scenarios"></a>Scénarios à plusieurs devises

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 a deux concepts de devises :

- **Devise de transaction** - Devise dans laquelle une transaction est effectuée. 
- **Devise de base** - Devise de l’instance de Dynamics 365. Cette devise est configurée lorsqu’une instance de Dynamics 365 est mise en service. Elle ne peut pas être modifiée.

Par exemple, Contoso US a vendu 100 teeshirts à un client au Royaume-Uni pour 15 livres sterling (GBP) pièce. Le tableau suivant montre comment cette transaction est enregistrée dans l’entité Produit de la commande.

| Produit | Quantité | Prix unitaire | Devise | Amount | Taux de change | Prix unitaire (devise de base)| Montant (devise de base)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Teeshirt | 100      | 15             | GBP      | 1 500   | 0,94          | 17.25 $               | 1 725 $       |

La colonne **Devise** affiche la devise de la transaction, qui est la devise dans laquelle la vente a été effectuée. La colonne **Taux de change** est le taux de change entre la devise de la transaction et la devise de base. La devise de base est en dollars US (USD). Cette devise de base a été configurée lorsqu’une instance de Dynamics 365 a été mise en service.
Comme le montre le tableau, chaque transaction est enregistrée dans la devise de la transaction et la devise de base. Dynamics 365 utilise le taux de change de la devise pour calculer les montants en devise de base.

## <a name="project-service-automation-extensions"></a>Extensions de Project Service Automation

Dynamics 365 Project Service Automation influence la devise de transaction, car les transactions ont généralement deux aspects : les coûts et les ventes.

Les entités suivantes sont considérées comme des transactions :

- Détail de la ligne de devis
- Détail de la ligne de contrat du projet
- Ligne d’estimation
- Ligne de journal
- Détail de la ligne de facture
- Chiffre réel

Dans chacune de ces entités, un enregistrement représente le montant du coût ou le montant des ventes. Comme pour tes entités de Dynamics 365 avec un champ **Montant**, chaque enregistrement contient des montants dans la devise de la transaction et dans la devise de base. 

PSA étend le concept de devise de transaction au coût et aux ventes des manières suivantes :

- La devise de transaction du coût de transactions des transactions de temps est toujours issue de la devise de l’unité d’organisation qui possède ou gère le projet. Cette unité d’organisation est appelée l’unité contractuelle.
- La devise de transaction commerciale pour les transactions de temps et de dépenses est toujours issue de la devise du contrat du projet.
- La devise de coût de transaction pour les dépenses provient de la devise à partir de laquelle l’entrée des dépenses a été créée.

## <a name="multiple-currency-scenario"></a>Scénario à plusieurs devises

Cette section propose l’exemple d’un projet que Contoso UK fournit pour un client nommé Fabrikam, au Japon. Voici comment le scénario a été configuré :

1. La GBP et le yen japonais (JPY) sont configurés sous **Paramètres** \> **Gestion d’entreprise** \> **Devises**. 
2. Un compte client nommé **Fabrikam - Japon** est configuré, et le JPY est sélectionné comme devise sur le compte.
3. Une unité d’organisation nommée **Contoso UK** est configurée, et la GBP est sélectionnée comme devise.
4. Un contrat de projet est créé, où **Contoso UK** est spécifié comme unité contractuelle et **Fabrikam – Japon** est spécifié comme client.
5. Des lignes de contrat de projet sont créées, selon les agencements de facturation des différentes classes de transactions dans le projet, comme la facturation pour le temps et la facturation pour les dépenses.
6. Un projet est créé où **Contoso UK** est désigné comme unité contractuelle. Ce projet est créé et mappé aux lignes de contrat du projet.


Pendant l’estimation qui utilise les détails de la ligne du devis, les détails de la ligne du devis du projet, ou sur la ligne d’estimation de la planification, deux enregistrements sont toujours créés dans l’entité. Un enregistrement est pour le coût, tandis que l’autre est pour les ventes.

- Par défaut, la devise de transaction sur l’enregistrement du coût est définie sur la devise de l’unité contractuelle du projet. Dans cet exemple, la devise est la GBP.
- Par défaut, la devise de transaction sur l’enregistrement des ventes est définie sur la devise du contrat du projet. Dans cet exemple, la devise est le JPY.

Lorsque des chiffres réels sont créés à l’aide d’une entrée de temps ou de la ligne du journal, le comportement suivant survient :

- Par défaut, la devise de transaction sur l’enregistrement du coût est définie sur la devise de l’unité contractuelle du projet.
- Par défaut, la devise de transaction sur l’enregistrement des ventes est définie sur la devise du contrat du projet.

Lorsque des chiffres réels sont créés pour les dépenses par l’entrée de dépenses ou la ligne du journal, le comportement suivant survient :

- Vous pouvez enregistrer le montant des dépenses dans n’importe quelle devise. Sélectionnez la devise à l’aide du sélecteur de devise sur la page **Entrée de dépense** ou la page **Ligne du journal**. Par défaut, la devise de transaction pour l’enregistrement des coûts est définie sur la devise de l’entrée des dépenses. 
- Par défaut, la devise de transaction pour l’enregistrement des ventes est la devise du contrat du projet. Pour définir cette devise, le système convertit d’abord le montant de la transaction dans la devise que l’utilisateur a entrée comme devise de base. Il convertit ensuite le montant dans la devise du contrat du projet. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Reports de calcul lorsque les chiffres réels du projet sont enregistrés dans plusieurs devises de transaction

Dynamics 365 gère automatiquement les reports des montants dans différentes devises. Prenons un exemple.

| Classe de transaction | Type de transaction| Date   | Ressource | Catégorie de transaction | Quantité | Prix unitaire | Amount      | Taux de change | Montant dans la devise de base |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Durée              | Ventes non facturées   | 14 juin | Jérôme  |                      | 8 h    | 20 000 JPY    | 160 000 JPY | 123           | 1 300,81 USD    |
| Durée              | Ventes non facturées   | 15 juin | Jérôme  |                      | 8 h    | 20 000 JPY    | 160 000 JPY | 123           | 1 300,81 USD    |
| Dépenses           | Ventes non facturées   | 16 juin | Jérôme  | Hôtel                | 1 chaque     | 250 EUR      | 250 EUR     | 0,94          | 265,95 USD     |
| Dépenses           | Ventes non facturées   | 17 juin | Jérôme  | Location de voiture           | 1 chaque     | 150 EUR      | 150 EUR     | 0,94          | 159,57 USD     |

Pour exprimer la valeur totale des ventes non facturées sur le projet, vous pouvez créer un champ de report pour le champ **Montant** sur tous les chiffres réels de ventes non facturés associés. Le champ de report est une construction de Dynamics 365 qui autorise les formules rapide sur des enregistrements associés.


[!INCLUDE[footer-include](../includes/footer-banner.md)]