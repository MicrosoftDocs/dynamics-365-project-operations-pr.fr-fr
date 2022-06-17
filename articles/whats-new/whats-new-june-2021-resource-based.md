---
title: Nouveautés de juin 2021 – Project Operations pour les scénarios basés sur les ressources/hors stock
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de juin 2021 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bc8475554c4348fa1e88b9090450bd3bfaa924e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910581"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de juin 2021 – Project Operations pour les scénarios basés sur les ressources/hors stock

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions de Microsoft Dynamics 365 Project Operations suivants :

- Project Operations dans l’environnement Dynamics 365 Dataverse, version 4.11.0.156 ou 4.11.0.164.
- Gestion de projet et comptabilité dans les environnements d’applications de finances et d’opérations version 10.0.19.

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- Possibilité de supprimer les [Lignes de proposition de facture du projet pour les scénarios d’ajustement](../invoicing/correct-project-invoice-proposals.md).
- Les lignes de dépenses détaillées reflètent les noms des sous-catégories dans la note de frais [Notes de frais réinventées - Nouvelles fonctionnalités](../expense/expense-reports-reimagined.md#new-features).
- Le mode de paiement est disponible dans le volet de nouvelles dépenses lors de la création d’une nouvelle dépense.
- Disponibilité générale des API de planification de projets. Cette nouvelle fonctionnalité permet aux clients d’effectuer par programme des opérations de création, de mise à jour et de suppression sur les tâches du projet, les affectations de ressources, les dépendances de tâche et les enregistrements des membres de l’équipe du projet. Pour plus d’informations, consultez [Utiliser les API de planification de projets pour effectuer des opérations avec les entités de planification](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages de double écriture de Project Operations

Cette version ne contient aucune mise à jour pour les mappages de double écriture de Project Operations. 

Pour obtenir une liste actuelle et les versions des mappages de double écriture de Project Operations, consultez [Versions de mappage de double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution des applications de finances et d’opérations. Certaines fonctionnalités et capacités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez voir la version active du mappage dans la page **Double écriture** dans la colonne **Version**. Activez une nouvelle version du mappage en sélectionnant **Versions de mappage de table**, en sélectionnant la version la plus récente, puis en enregistrant la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème au démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes dans les mappages](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du Guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2281417 | Correction du problème concernant l’échec de l’action de création automatique de factures par le biais de la planification de factures. |
| Facturation et tarification | 2287835 | Amélioration des performances de confirmation de factures. |
| Gestion des opportunités | 2222555 | L’imputabilité des estimations de matériel doit être correctement copiée dans les détails de la ligne de devis lors de l’utilisation de l’option **Importer à partir de l’estimation du projet**. |
| Gestion des opportunités | 2223427 | Les personnalisations sont désormais autorisées pour l’action, **GenerateRetainersFromRetainerScheduleOptions**. |
| Gestion des opportunités | 2277528 | Correction du calcul de la valeur du jalon de facturation pour les lignes de contrat du projet avec plusieurs clients. |
| Planification et suivi de projets | 2226110 | Correction du problème intermittent avec la fonction **Générer une demande** dans la grille **Équipe du projet**. |
| Planification et suivi de projets | 2208109 | Les utilisateurs ne peuvent pas créer un projet dans une devise avec des tâches associées dans une autre devise. |
| Planification et suivi de projets | 2258228 | La liste de champs autorisés à modifier avec les entités de **Planification** qui utilisent l’API de planification a été mise à jour. |
| Planification et suivi de projets | 2293989 | Les paramètres de langue et régionaux corrects doivent être transmis à la grille **Tâches du projet**. |
| Gestion des ressources | 2220493 | Correction de l’expérience utilisateur dans la grille **Tâche** lorsque vous marquez rapidement une demande de ressource comme terminée. |
| Gestion des ressources | 2330496 | Correction du problème de chargement du **Tableau de planification**. (La mise à jour de qualité est disponible dans la version 4.11.0.164) |
| Temps et dépenses | 2194431 | La grille **Entrée de temps** doit respecter le début de la semaine comme défini dans les **Paramètres du système**. |
| Temps et dépenses | 2277311 | Une fois que vous supprimez la valeur dans une cellule de la grille **Entrée de temps**, le curseur reste dans la grille. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets sur Dynamics 365 Finance

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Gestion et comptabilité des projets | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notes de formulaire** et **Configuration de formulaire** ne sont pas visibles dans **Configuration de la gestion des projets** dans les entités juridiques de Finance qui sont intégrées à Project Operations. |
| Gestion et comptabilité des projets | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | La description par défaut de la TVA est vide lorsque le **Type de validation** = **Taxe de vente** pour les documents de facture du projet. |
| Gestion et comptabilité des projets | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Les transactions en double sont validées lorsque la facturation basée sur les tâches est utilisée dans Dataverse avec l’intégration de Project Operations. |
| Gestion et comptabilité des projets | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Le pourcentage terminé dans la constatation du produit est incorrect lors de l’utilisation de l’intégration de Project Operations. |
| Gestion et comptabilité des projets | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | La régularisation du produit est doublée dans une facture fournisseur en attente dans un scénario intégré de Project Operations. |
| Gestion et comptabilité des projets | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Impossible de valider le journal d’intégration lorsque la règle du profil de produit est définie sur la configuration **Groupe**. |
| Gestion et comptabilité des projets | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Une facture fournisseur ne peut pas être validée pour les commandes fournisseur de projet comportant des lignes avec plusieurs unités de mesure. |
| Gestion et comptabilité des projets | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | La dimension financière par défaut d’un projet ne peut pas être mise à jour à l’aide de l’entité de données **V2** du projet. |
| Gestion et comptabilité des projets | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | L’exécution du traitement par lots pour créer des estimations de projet prend trop de temps. |
| Gestion et comptabilité des projets | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | La suppression d’un contrat supprime également l’adresse associée au client. |
| Déplacement et dépenses | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | La condition du flux de travail d’approbation de la note de frais n’est pas évaluée correctement. |
| Déplacement et dépenses | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | La stratégie de la note de frais n’évalue pas correctement l’ID du projet. |
| Déplacement et dépenses | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | L’action **Fractionner en personnel pour les transactions de dépenses intersociétés** ne fonctionne pas correctement. |
| Déplacement et dépenses | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Les justifications de la ligne de note de frais sont accidentellement supprimées lorsque certaines demandes de déplacement sont supprimées. Cela se produit lorsque le recID de la note de frais et de la demande de déplacement sont identiques. |
| Déplacement et dépenses | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Un problème se produit dans l’application mobile Dépenses lorsque le champ **ID du projet** est obligatoire dans les stratégies de note de frais. |
| Déplacement et dépenses | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Les dépenses intersociétés associées à un projet ne peuvent pas être modifiées. À la place, le message d’erreur suivant s’affiche : « Référence d’objet non définie sur une instance d’un objet ». |
| Déplacement et dépenses | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Une fois la note de frais validée, la devise et le montant incorrects sont répertoriés dans la comptabilité auxiliaire de la banque. |
| Déplacement et dépenses | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Des améliorations ont été apportées à la fonctionnalité *Supprimer les transactions par carte de crédit*.  |
| Déplacement et dépenses | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | La taxe de vente incluse dans une note de frais n’est pas calculée de manière cohérente lorsqu’une devise de déclaration différente est spécifiée dans une entité juridique. |
| Déplacement et dépenses | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Les performances sont affectées lors de l’ajout d’une nouvelle dépense de déplacement en espèces. |
| Déplacement et dépenses | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Les règles de la stratégie de dépenses ne sont pas déclenchées dans une note de frais. |
| Déplacement et dépenses | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Le chargement d’une nouvelle catégorie partagée à l’aide de Data Management Framework supprime toutes les sous-catégories de toutes les catégories partagées. |
| Déplacement et dépenses | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Lorsque vous créez une ligne de dépense, puis sélectionnez une catégorie, le message d’erreur suivant s’affiche : « La combinaison du DOM du groupe de taxe et du STD du groupe de taxe d’article n’est pas valide ». |
| Déplacement et dépenses | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Des problèmes de synchronisation se produisent dans l’application mobile Dépenses. |
