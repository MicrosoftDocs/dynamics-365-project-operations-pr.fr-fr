---
title: Utilisation des modèles de données Project Service Automation
description: Cette rubrique fournit des informations sur la façon d’utiliser le modèle de données.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8c212ef2c9fd9dcd6be0b8f0a31aa5a948176bc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147650"
---
# <a name="working-with-the-project-service-automation-data-model"></a>Utilisation des modèles de données Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Service Automation étend d’autres entités d’applications et intègre ses propres entités au modèle de données Common Data Service. Cette rubrique décrit certaines des entités que vous rencontrerez dans les scénarios courants de génération de rapports PSA.

## <a name="reporting-on-opportunities"></a>Génération de rapports sur les opportunités

Project Service Automation étend l’entité **Opportunité** de Dynamics 365 Sales en ajoutant des champs qui activent les scénarios basées sur un projet. Ces champs sont identifiés par un nom de schéma dont le préfixe est **msdyn\_**. Un nouveau champ important pour la génération de rapports sur les opportunités PSA est **Type de commande**. Une valeur de **Basée sur le travail** pour ce champ indique que l’opportunité est une opportunité PSA. Les autres champs qui ont été ajoutés à l’entité qui comprennent **Organisation contractuelle**, qui capture l’organisation qui gère l’opportunité, et **Gestionnaire de comptes**, qui capture le nom du gestionnaire de comptes, responsable de l’opportunité.

L’entité **Ligne de l’opportunité** inclut également des champs associés à Project Service. **Mode de facturation** indique si la ligne Opportunité doit être affichée sur une base de temps-et-matériaux ou une base à prix fixe, et **Projet** capture le nom du projet qui soutient l’opportunité. Les autres champs que vous pouvez rapporter sur les coûts de capture et les montants budgétaires client pour l’éléments de ligne.

## <a name="reporting-on-quotes"></a>Génération de rapports sur les devis

PSA étend l’entité **Devis** des ventes en ajoutant des champs associés au projet. **Type de commande** distingue les devis PSA des devis non PSA. Une valeur de **Basée sur le travail** pour ce champ indique que le devis est un devis PSA. D’autres champs pouvant être pertinents pour générer des rapports sur les devis PSA incluent des champs de montant, comme **Coûts facturables**, **Coûts non facturables**, **Marge brute**, **Estimations** et **Budget**. Les autres champs utiles indiquent si le devis est rentable, s’il sera terminé au moment prévu, et s’il satisfait aux exigences du budget client.

PSA étend également l’entité **Ligne de devis** des ventes. Un champ que PSA ajoute est **Mode de facturation**, qui indique la facturation de la ligne de devis (temps et matériaux ou prix fixe). Les autres champs qui ont été ajoutés à la capture d’entité associé du projet qui soutient la ligne de devis, la facturation, le coût, et le budget.

PSA ajoute également de nouvelles entités liées au devis au modèle de données Dynamics 365. Voici quelques exemples :

- **Détail de la ligne de devis** : cette entité contient les détails d’estimation du projet de la ligne de devis. Elle contient deux enregistrements pour chaque ligne de devis. Un enregistrement stocke le coût et les détails du coût de la ligne de devis, et les autres types d’enregistrements stockent le montant des ventes et les détails de ventes de la ligne de devis.
- **Planification de facture de la ligne de devis** : cette entité contient la planification de facturation de la ligne de devis. Cette planification est générée selon la périodicité de facturation attribuée à la ligne de devis.
- **Jalon de la ligne de devis** : cette entité contient les jalons de facturation des lignes de devis à prix fixe.
- **Répartition de l’analyse de ligne de devis** : cette entité contient les détails financiers de la ligne de devis. Ces détails peuvent être utiles pour générer de rapports sur les montants des ventes de devis et du coût estimé selon différentes dimensions.

D’autres entités que PSA ajoute aux devis sont **Tarifs du projet de la ligne de devis**, **Catégorie de ressource de ligne de devis**, **Catégorie de transaction de ligne de devis**.

![Graphique affichant le devis, la ligne de devis et les relations du projet](media/PS-Reporting-image2.png "Graphique affichant le devis, la ligne de devis et les relations du projet")

## <a name="reporting-on-project-contracts"></a>Génération de rapports sur les contrats de projet

PSA étend l’entité **Commande** des ventes qui s’utilise lorsque des contrats de projet sont enregistrés. Il ajoute un nouveau champ important, **Type de commande**, qui identifie le contrat comme un contrat de projet PSA, plutôt qu’une commande client. Une valeur de **Basée sur le travail** pour ce champ indique que la commande est une un contrat de projet PSA. D’autres nouveaux champs ajoutés aux détails de la capture d’entité **Commande** sur les coûts, le statut du contrat PSA et l’organisation qui possède le contrat.

PSA étend également l’entité **Ligne de commande client**. Vous constaterez que les champs qu’il ajoute sont destinés à capturer le mode de facturation (temps et matériaux ou à prix fixe), les montants budgétaires du client et le projet sous-jacent.

PSA ajoute également de nouvelles entités conçues pour les contrats de projet. Voici quelques exemples :

- **Détail de la ligne de contrat de projet** : cette entité contient les détails au niveau de la ligne qui sont reportés dans le montant de la ligne de contrat. Ils peuvent être aussi détaillés que les éléments de ligne qui sont générés à partir d’une planification de projet au niveau de la tâche.
- **Planification de factures de la ligne de contrat** : cette entité contient la planification de facturation qui est générée selon la fréquence de facture affectée à la ligne de contrat.
- **Jalon de contrat** : cette entité contient les jalons de facturation pour les lignes de contrat avec une condition de facturation à prix fixe.

D’autres entités que PSA ajoute aux contrats sont **Tarifs du projet de la ligne de contrat de projet**, **Catégorie de ressource de ligne de contrat de projet**, **Catégorie de transaction de ligne de contrat de projet**.

![Graphique affichant la commande, la ligne de commande et les relations du projet](media/PS-Reporting-image3.png "Graphique affichant la commande, la ligne de commande et les relations du projet")

## <a name="reporting-on-projects"></a>Génération de rapports sur les projets

L’entité **Projets** et ses entités associées sont exclusives à PSA. **Projet** est l’entité de niveau supérieur qui permet de capturer l’aspect du travail et des coûts des opérations. Voici la liste des entités associées :

- **Membre de l’équipe du projet** : cette entité contient des détails relatifs aux ressources pouvant être réservées qui sont affectées au projet. Ces ressources peuvent être des ressources génériques pouvant être réservées ou des ressources nommées pouvant être réservées entrées par le chef de projet ou générées par la planification du projet.
- **Tâche du projet** : cette entité contient les tâches qui composent le plan ou la planification de projet.
- **Attribution de ressource** : cette entité contient l’affectation de tâches pour la ressource réservable.
- **Besoin en ressources** : cette entité contient les besoins de tous les membres de l’équipe de ressources génériques.
- **Estimation** et **Ligne d’estimation** : ces entités ont une relation en-tête/ligne et contiennent des estimations des dépenses pour le projet. Les estimations de tâches sont stockées sur l’entité **Estimation des ressources**.

![Graphique affichant le besoin en ressources et les relations du projet](media/PS-Reporting-image4.png "Graphique affichant le besoin en ressources et les relations du projet")

## <a name="reporting-on-resources"></a>Génération de rapports sur les ressources

Les ressources du projet utilisent les entités **Ressource pouvant être réservée** de Universal Resource Scheduling (URS) qui sont partagées avec d’autres applications, telles que Microsoft Dynamics 365 Field Service. Voici la liste des entités que vous devrez utiliser lorsque vous générerez des rapports sur les ressources de projet :

- **Ressource pouvant être réservée** : cette entité représente l’utilisateur, le contact, la ressource générique, le compte, le groupe ou les équipements utilisés par l’équipe du projet.
- **Caractéristiques des ressources pouvant être réservées** : cette entité comprend les compétences, les certifications ou les études de la ressource. Les caractéristiques peuvent avoir des valeurs d’évaluation définies par le modèle d’évaluation.
- **Catégorie de ressources pouvant être réservées** : cette entité représente le rôle de la ressources réservables.
- **Réservations des ressources réservables** : cette entité représente le temps qui est réservé sur les projets pour la ressource. Chaque réservation a une entité d’en-tête et des entités de ligne, et chaque ligne possède un statut qui représente le statut de la réservation.

![Diagramme affichant les relations des caractéristiques des ressources réservables](media/PS-Reporting-image5.png "Diagramme affichant les relations des caractéristiques des ressources réservables")

## <a name="reporting-on-actual-transactions"></a>Génération de rapports sur les transactions réelles

Lorsque vous approuvez une feuille de présence ou une dépense, ou que vous facturez un contrat dans PSA, la transaction commerciales est capturée dans l’entité **Chiffre réel**. Cette entité peut servir de base à presque tous les rapports liés aux finances dans PSA. L’entité **Chiffre réel** capture le coût et les transactions commerciales pour l’événement commercial. Elle capture également un grand nombre d’attributs appropriés.

Lorsque vous utilisez l’entité **Chiffre réel**, il est important de bien comprendre quelle(s) transaction(s) est stockée dans l’entité, et quand les transactions sont enregistrées. Voici un flux standard lorsque vous utilisez des entrées de temps (le flux pour des entrées de dépenses est similaire) :

1. Lorsque l’entrée de temps est enregistrée, aucun enregistrement n’est créé dans l’entité **Chiffre réel**.
2. Lorsque l’entrée de temps est envoyée, aucun enregistrement n’est créé dans l’entité **Chiffre réel**.
3. Lorsque l’entrée de temps est approuvée, un enregistrement est créé dans l’entité **Chiffre réel**, et un deuxième enregistrement peut également être créé. Le premier enregistrement stocke le coût de l’entrée de temps. Le second enregistrement stocke le montant des ventes non facturées de l’entrée de temps. Le second enregistrement dépend du projet ayant un client, un devis ou une ligne de contrat attribuée à celui-ci.

    | Date du document | Type de transaction | Classe de transaction | Client         | Contrat   | Ressource     | Rôle de la ressource | Type de facturation | Quantité | Prix unitaire | Amount |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | 3/2/18        | Coût             | Temps              | Chalet alpin | CRM alpin | Astrid Lang | Chef de projet   | Facturable   | 8.0      | 50.00      | 400.00 |
    | 3/2/18        | Ventes non facturées   | Temps              | Chalet alpin | CRM alpin | Astrid Lang | Chef de projet   | Facturable   | 8.0      | 100.00     | 800.00 |

    Ces deux enregistrements sont séparés mais associés. Ils ne sont ni des débits ni des crédits.

4. Si un contrat est associé au projet, lorsque l’entrée de temps est facturée, deux autres enregistrements sont créés dans l’entité **Chiffre réel**. D’abord, un montant négatif pour l’enregistrement des ventes non facturées est créé. Cet enregistrement contrepasse essentiellement la vente non facturée. Ensuite, une transaction pour la vente facturée est créée. Ici aussi, ces enregistrements sont distincts mais associés, pas des débits et des crédits.

    | Date du document | Type de transaction | Classe de transaction | Client         | Contrat   | Ressource     | Rôle de la ressource | Type de facturation | Quantité | Prix unitaire | Amount   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | 4/2/18        | Ventes non facturées   | Time              | Chalet alpin | CRM alpin | Astrid Lang | Chef de projet   | Facturable   | - 8,0    | 100.00     | - 800,00 |
    | 4/2/18        | Ventes facturées     | Temps              | Chalet alpin | CRM alpin | Astrid Lang | Chef de projet   | Facturable   | 8.0      | 100.00     | 800.00   |

L’entité **Origine de la transaction** enregistre l’origine de l’enregistrement **Chiffre réel**, et l’entité **Connexion de la transaction** enregistre les enregistrements associés de l’enregistrement **Chiffre réel**. En outre, l’enregistrement **Chiffre réel** contient des références au projet, au contrat du projet (commande), aux ressources réservables, et au client.

![Diagramme affichant la connexion, l’origine et les relations réelles de la transaction](media/PS-Reporting-image6.png "Diagramme affichant la connexion, l’origine et les relations réelles de la transaction")
