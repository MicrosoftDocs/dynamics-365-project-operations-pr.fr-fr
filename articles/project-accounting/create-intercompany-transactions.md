---
title: Créer des transactions intersociétés
description: Cette rubrique fournit des informations sur la manière de créer des transactions intersociétés.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0e396f0d08fd166e7acd6f8ec8f32353a7679dd8
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013348"
---
# <a name="create-intercompany-transactions"></a>Créer des transactions intersociétés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les transactions intersociétés sont des transactions de temps et de dépenses d’un contrat de projet qui appartiennent à une société ou une unité d’organisation, tandis que les ressources du contrat de projet font partie d’une société ou d’une unité d’organisation différente.

Lorsqu’une transaction intersociétés est approuvée, les transactions réelles suivantes sont créées

| **Type de transaction** | **Tarifs appliqués** | **Devise de transaction** |
| --- | --- | --- |
| Coût | Tarifs de prix de revient unitaire contractuel | Devise sur la ligne de prix |
| Ventes non facturées. Celles-ci sont créés uniquement pour les chiffres réels associés à une ligne de contrat avec le type de facturation, l’heure et l’article. | Tarifs de ventes du projet de contrat | Devise du contrat |
| Coût unitaire d’allocation des ressources | Tarifs de prix de revient unitaire des ressources | Devise sur la ligne de prix |
| Ventes entre unités d’organisation | Tarifs de prix de revient unitaire contractuel | Devise sur la ligne de prix |

Le coût, le coût unitaire des ressources ainsi que la tarification et la devise des transactions de vente entre les unités d’organisation sont déterminés par **unité d’organisation**. Il est important de s’en souvenir lorsque vous décidez de la manière de structurer les entreprises et les unités d’organisation dans votre implémentation.

Lorsque vous créez des enregistrements d’opportunité, de devis, de contrat de projet et de projet, le système vérifie que la devise de l’unité contractante correspond à la devise comptable de la société contractante. Lorsqu’ils ne sont pas identiques, ces enregistrements ne peuvent pas être créés. La devise de l’unité d’organisation est définie dans Dynamics 365 Project Operations en accédant à **Dataverse** > **Paramètres** > **Unités d’organisation**. La devise comptable d’une entreprise est définie dans Dynamics 365 Finance en accédant à **Comptabilité** > **Paramétrage de la comptabilité** > **Registre**. La devise est synchronisée avec votre environnement Dataverse en utilisant la carte Ledgers Dual Write.

Le système crée le coût unitaire des ressources et les chiffres réels des ventes entre unités d’organisation dans les situations suivantes :

  - Lorsque l’unité de ressources diffère de l’unité contractante
  - Lorsque la société de ressources diffère de la société contractante

Cependant, seules les transactions qui ont une société de ressources différente de la société contractante seront transférées vers l’environnement Dynamics 365 Finance pour une comptabilité supplémentaire.

La comptabilité des chiffres réels du projet est enregistrée dans le journal d’intégration Project Operations de Finance. Le système crée les lignes de journal suivantes.

| **Type de transaction** | **Entité juridique** | **Il crée une transaction de projet lors de la validation** | **Valeur par défaut d’une dimension financière** | **Facturation du groupe de taxes de vente et Facturation du groupe de taxe de vente d’articles** |
| --- | --- | --- | --- | --- |
| Coût | Il n’est pas ajouté au journal d’intégration | S. O. | S. O. | S. O. |
| Ventes non facturées | Le journal d’intégration des entités juridiques emprunteuses | Oui | Project | **Groupe de taxe de vente de facturation** : basé sur le **client de contrat** <br/> **Groupe de taxe de vente des éléments de facturation** : à partir de la catégorie de projet d’entité juridique actuelle sur la ligne de journal |
| Coût unitaire d’allocation des ressources | Le journal d’intégration des entités juridiques prêteuses | No | Client intersociétés | **Groupe de taxe de vente de facturation** : basé sur le **client intersociétés** <br/> **Groupe de taxe de vente des éléments de facturation** : à partir de la catégorie de projet d’entité juridique actuelle sur la ligne de journal |
| Ventes entre organisations | Le journal d’intégration des entités juridiques prêteuses | No | Client intersociétés | **Groupe de taxe de vente de facturation** : basé sur le **client intersociétés** <br/> **Groupe de taxe de vente des éléments de facturation** : à partir de la catégorie de projet d’entité juridique actuelle sur la ligne de journal |

### <a name="example-intercompany-transactions"></a>Exemple : transactions intersociétés

Molly Clark, développeuse employée chez GBPM enregistre 10 heures de travail sur un projet USPM Adventure Works, qui est approuvé par le chef de projet. Le coût développeur dans GBPM est de 88 GBP par heure. GBPM facturera USPM 120 USD par heure de développeur. USPM facturera le client Adventure Works, 200 USD, pour le travail effectué par la ressource GBPM. Pour plus d’informations, voir [Configurer la facturation intersociétés](configure-intercompany-invoicing.md).

1. Dans Project Operations, accédez à **Ressources** et sélectionnez **Molly Clark** dans la liste. Dans l’onglet **Planification**, dans le champ **Société**, sélectionnez **GBPM**.
2. Accédez à **Ventes** > **Clients** et sélectionnez **Nouveau** pour créer un nouvel enregistrement client pour Adventure Works.
    1. Définissez la société sur **USPM**.
    2. Définissez **Type de relation** sur **Client**.
    3. Sélectionnez **Groupe de clients 10 - Domestique**.
    4. Définissez la devise sur **USD**.
    5. Enregistrez l’enregistrement.
3. Accédez à **Ventes** > **Contrats de projet** et créez un nouveau contrat de projet pour Adventure Works.
    1. Définir la société propriétaire sur **USPM** et l’unité contractuelle sur **Contoso Robotics États-Unis**.
    2. Sélectionnez Adventure Works comme client.
    3. Sélectionnez des tarifs de produit et enregistrez l’enregistrement.
    4. Sur l’onglet **Lignes de contrat**, créez une nouvelle ligne de contrat. Définissez n’importe quel nom et sélectionnez **Temps et matériaux** comme méthode de facturation.
    5. Créez un nouveau projet et associez-le à cette ligne de contrat.
4. Connectez-vous en tant que ressource, **Molly Clark**. Accédez à **Projets** > **Entrées de temps** et créez une entrée de temps pour le projet Adventure Works.
5. Connectez-vous en tant que chef de projet. Accédez à **Projets** > **Approbations** et approuvez la transaction de saisie de temps enregistrée par Molly Clark.
6. Accédez au projet Adventure Works et sélectionnez **Association** > **Réels**. Les transactions réelles suivantes sont créées.

| **Type de transaction** | **Tarif** | **Devise de transaction** | **Montant** |
| --- | --- | --- | --- |
| Coût | 120 | USD | 1200 |
| Ventes non facturées | 200 | USD | 2000 |
| Coût unitaire d’allocation des ressources | 88 | GBP | 880 |
| Ventes entre unités d’organisation | 120 | USD | 1200 |

7. Connectez-vous en tant que comptable USPM. Ouvrez l’instance Finance de Project Operations et sélectionnez la société **USPM**. 
8. Accédez à **Gestion et comptabilité des projets** > **Périodique** > **Project Operations sur Customer Engagement** > **Importer depuis la table intermédiaire** et choisissez d’exécuter le processus périodique. Ce processus périodique remplira le journal d’intégration de Project Operations.
9. Accédez à **Gestion et comptabilité des projets** > **Journaux** > **Journal d’intégration de Project Operations** et passez en revue les lignes de journal. Le système crée la ligne suivante.

    | **Type de transaction** | **Tarif** | **Devise de transaction** | **Montant** |
    | --- | --- | --- | --- |
    | Ventes non facturées | 200 | USD | 2000 |

    Si le système est configuré pour générer des revenus pour ce projet, les éléments suivants sont validés :

    - Débit : Projet - Valeur des ventes TEC 200 USD
    - Crédit : Projet - Produit à recevoir 200 USD

    Cette vente non facturée est maintenant prête pour la facturation. La facture du client Adventure Works peut être validée financièrement en cas de besoin.

10. Connectez-vous en tant que comptable **GBPM**. Ouvrez l’instance Finance de Project Operations et ouvrez la société **GBPM**. 
11. Accédez à **Gestion de projet et comptabilité** > **Périodique** > **Intégration Project Operations** > **Importer depuis la table intermédiaire** et exécutez le processus périodique pour remplir la feuille intégration de Project Operations.
12. Accédez à **Gestion et comptabilité des projets** > **Journaux** > **Journal d’intégration de Project Operations** et passez en revue les lignes. Le système crée les lignes suivantes.

    | **Type de transaction** | **Tarif** | **Devise de transaction** | **Montant** |
    | --- | --- | --- | --- |
    | Coût unitaire d’allocation des ressources | 88 | GBP | 880 |
    | Ventes entre unités d’organisation | 120 | USD | 1200 |

    La validation de ces enregistrements produit les pièces comptables suivantes :

    - Débit : coût du projet 88 GBP
    - Crédit ; Répartition de la paie 88 GBP

    Si le système est configuré pour générer des revenus intersociétés, les éléments suivants sont validés :

    - Débit : Projet - Valeur des ventes TEC 120 USD
    - Crédit : Projet - Produit à recevoir 120 USD

    Le système est maintenant prêt à créer une facture client intersociétés.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
