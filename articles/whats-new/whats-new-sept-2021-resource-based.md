---
title: Nouveautés de septembre 2021 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de septembre 2021 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923369"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de septembre 2021 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

*S’applique à : Project Operations pour les scénarios basés sur les ressources/hors stock*

Cet article s’applique aux composants et versions de Microsoft Dynamics 365 Project Operations suivants :

   - Project Operations dans l’environnement Microsoft Dataverse, version 4.14.0.99.
   - Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations. Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctionnalités et capacités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez voir la version active du mappage dans la page **Double écriture** dans la colonne **Version**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Temps et dépenses | 1811407 | Ajustement du rôle de sécurité Approbateur du projet pour les approbations d’entrée de dépense. |
| Temps et dépenses | 1811438 | Ajustement du rôle de sécurité Approbateur du projet pour l’annulation des approbations d’entrée de temps. |
| Temps et dépenses | 2370126 | Mise à jour des icônes **Tâche du projet** et **Rôle** dans l’entité **Entrée de temps**. |
| Temps et dépenses | 2379879 | Correction de la fonction **Copier la semaine** dans l’entrée de temps lors de l’utilisation de Dynamics 365 pour téléphone. |
| Facturation et tarification | 2371906 | Le montant total de la facture pro forma ne doit pas être ajustable dans Project Operations pour les déploiements basés sur les ressources. |
| Facturation et tarification | 2385802 | Correction de l’erreur qui se produit avec des heures réelles négatives lorsque les totaux du projet sont actualisés. |
| Facturation et tarification | 2389675 | Amélioration du comportement de confirmation de la facture pro forma. L’entité des tâches durables doit prendre en compte l’activité requise pour écrire les résultats de confirmation pour la comptabilité. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Dynamics 365 Finance

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Déplacement et dépenses | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Les montants sur les transactions fournisseur et taxe de vente validés à partir d’une dépense créée à partir d’une transaction par carte de crédit sont incorrects. |
| Déplacement et dépenses | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Des lignes de règlement erronées sont créées lors de la génération de la feuille paiement. |
| Déplacement et dépenses | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Les montants sur les transactions taxe de vente validés à partir d’une dépense créée à partir d’une transaction par carte de crédit sont incorrects. |
| Déplacement et dépenses | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | La suppression d’une ligne de dépense peut prendre beaucoup de temps. |
| Comptabilité de projet | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Après avoir appliqué la base de connaissances 4619395, changer la séquence de nombres et la définir sur **Continu** n’est pas pris en charge et, si vous validez une estimation, l’erreur suivante se produit : « Le système ne prend pas en charge la configuration « continue » de la séquence de numéros Proj_X. » |
| Comptabilité de projet | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | La validation d’une facture fournisseur peut échouer avec le message d’erreur suivant : « Les pièces comptables ne sont pas équilibrées au 17/05/2021. (devise comptable : 0,00 - devise de déclaration : 0,01). » |
