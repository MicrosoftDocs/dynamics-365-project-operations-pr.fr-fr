---
title: Nouveautés d’août 2021 – Project Operations pour les scénarios basés sur les ressources/hors stock
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version d’août 2021 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bd91f7f6b3a6f78161f8900aa06c810a58609b53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912283"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés d’août 2021 – Project Operations pour les scénarios basés sur les ressources/hors stock

*S’applique à : Project Operations pour les scénarios basés sur les ressources/hors stock*

Cet article s’applique aux composants et versions de Microsoft Dynamics 365 Project Operations suivants :

   - Project Operations dans l’environnement Microsoft Dataverse, version 4.13.0.152.
   - Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.20.

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- **Ensembles d’approbation** : Les ensembles d’approbation regroupent les demandes d’approbation de temps, de dépenses ou d’utilisation de matériel en sous-ensembles d’opérations plus petits. Ce regroupement permet de traiter les approbations par projet, dans un ordre spécifique et permet d’effectuer de nouvelles tentatives et de séquencer. Le regroupement des demandes améliore la fiabilité et la traçabilité du traitement de gros volumes d’approbations. Pour en savoir plus, consultez [Ensembles d’approbations](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations.

Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctionnalités et capacités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez voir la version active du mappage dans la page **Double écriture** dans la colonne **Version**. Activez une nouvelle version du mappage en sélectionnant **Versions de mappage de table**, en sélectionnant la version la plus récente, puis en enregistrant la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème au démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes dans les mappages](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du Guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2295625 | Le nom du jalon doit être copié du calendrier de facturation dans le détail de la ligne de facture. |
| Facturation et tarification | 2316323 | La remise ne doit pas être modifiable sur une facture proforma dans Project Operations pour les scénarios basés sur les ressources. |
| Gestion des opportunités | 2338619 | Les règles métier **Opportunité** et **Devis** doivent être invoquées uniquement sur les pages. |
| Gestion des ressources | 2316523 | Le fait d’utiliser **Envoyer une demande** à partir d’une exigence de ressource à laquelle est attaché un rôle ne doit pas afficher d’erreur. |
| Gestion des ressources | 2326885 | La création d’un besoin en ressources via un projet ne doit pas afficher d’erreur. |
| Temps et dépenses | 2335584 | Flux de tâches obsolètes dans l’entrée de temps. |
| Temps et dépenses | 2336884 | Le bouton d’entrée de temps **Copier la semaine** ne doit pas uniquement fonctionner pour l’utilisateur actuel. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets sur Dynamics 365 Finance

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Déplacement et dépenses | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Des montants de transaction fournisseur et de transaction de taxe incorrects sont enregistrés lorsqu’une dépense est créée à partir d’une transaction par carte de crédit. |
| Déplacement et dépenses | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Des lignes sont créées pour les règlements erronés lors de la génération du journal des paiements. |
| Déplacement et dépenses | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Des montants de transaction de taxe incorrects sont enregistrés lorsqu’une dépense est créée à partir d’une transaction par carte de crédit. |
| Déplacement et dépenses | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | La suppression d’une ligne de dépense peut prendre beaucoup de temps. |
| Comptabilité de projet | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Le système ne prend pas en charge la configuration du séquençage continu des numéros lorsque vous publiez un devis après avoir appliqué la base de connaissances 4619395. |
| Comptabilité de projet | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | La validation de la facture du fournisseur risque d’échouer avec le message d’erreur suivant : « Les transactions du justificatif ne s’équilibrent pas au 17/05/2021. (devise comptable : 0,00 - devise de déclaration : 0,01) » |
