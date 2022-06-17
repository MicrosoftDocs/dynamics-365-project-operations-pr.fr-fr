---
title: Nouveautés ou modifications de Project Operations en septembre 2021 pour les scénarios basés sur les produits stockés/ordres de fabrication
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de septembre 2021 de Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication.
author: andchoi
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: 1e99471b4338209c1f7fe411084d1745d74b2d2c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916515"
---
# <a name="whats-new-or-changed-in-project-operations-september-2021-for-stockedproduction-based-scenarios"></a>Nouveautés ou modifications de Project Operations en septembre 2021 pour les scénarios basés sur les produits stockés/ordres de fabrication

_**S’applique à :** Project Operations pour les scénarios basés sur le stock/la production_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.21
 
## <a name="quality-updates"></a>Mises à jour qualité

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
|---|---|---|
| Gestion et comptabilité des projets | [412077](https://fix.lcs.dynamics.com/Issue/Details/?bugId=412077) | Si le rôle de responsable des achats est autorisé à accéder à une entité juridique, il permet également d’accéder à tous les projets dans toutes les entités juridiques. |
| Gestion et comptabilité des projets | [537214](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537214) | Un problème d’arrondi de la taxe sur la valeur ajoutée (TVA) se produit lorsqu’un avoir est réglé par rapport à une facture de projet d’origine. |
| Gestion et comptabilité des projets | [538002](https://fix.lcs.dynamics.com/Issue/Details/?bugId=538002) | Utilisez un autre budget de projet pour la vérification du budget. |
| Gestion et comptabilité des projets | [546265](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546265) | Le groupe de prix **Prix de vente - heure** n’est pas calculé sur la structure de répartition du travail pour les devis de projet. |
| Gestion et comptabilité des projets | [555604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=555604) | L’élimination de l’estimation échoue si la fonctionnalité **Activer la devise du contrat de projet pour le calcul de l’estimation** est activée. |
| Gestion et comptabilité des projets | [563523](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563523) | La factorisation de la taxe de vente par la quantité est ajoutée au montant du prix de vente lorsque la taxe d’utilisation est utilisée sur le groupe de taxe de vente du journal des dépenses de projet. |
| Gestion et comptabilité des projets | [564701](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564701) | La taxe conditionnelle n’est pas calculée correctement pour le dernier paiement si la rétention de fournisseurs et l’acompte sont appliqués à des factures de commande fournisseur. |
| Gestion et comptabilité des projets | [565642](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565642) | La trace d’ajustement ne fonctionne pas pour les journaux de solde d’ouverture. |
| Gestion et comptabilité des projets | [568814](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568814) | La **Répartition de révision budgétaire du projet par période** est réparti sur toutes les périodes budgétaires. Lorsque la répartition est soumise, l’enregistrement n’est pas effacé. |
| Gestion et comptabilité des projets | [569250](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569250) | Les écritures des Travaux en cours (TEC) en comptabilité ont un montant incorrect. |
| Gestion et comptabilité des projets | [570731](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570371) | L’approbation du journal des heures du projet ne fonctionne pas. |
| Gestion et comptabilité des projets | [571391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571391) | Le prix de vente d’ajustement du projet n’est pas mis à jour avec les coûts indirects lorsque la limite de financement n’est pas marquée. |
| Gestion et comptabilité des projets | [575831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575831) | Un besoin d’article ne peut pas être créé lorsque l’en-tête de la table Ventes est facturé et que le bon de commande d’approvisionnement pour les lignes existantes a été finalisé. |
| Gestion et comptabilité des projets | [578036](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578036) | Le montant de rétention pour une règle de facturation qui comporte un jalon pour un projet différent n’est pas validé dans l’ID de projet correspondant qui a été sélectionné pour le jalon. Au lieu de cela, il est validé avec le premier projet. |
| Gestion et comptabilité des projets | [578327](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578327) | Lorsque vous sélectionnez **Ensemble de dimensions financières** sur une proposition de facture, l’erreur suivante se produit : « Impossible de lancer l’objet de type "Dynamics.AX.Application.FormIntControl" vers le type "Dynamics.AX.Application.FormStringControl". » |
| Gestion et comptabilité des projets | [581167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581167) | Le rapport **Facture de projet** saute des lignes. |
| Gestion et comptabilité des projets | [581489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581489) | Une erreur se produit lorsque vous calculez le contrôle de coût pour un projet d’investissement. |
| Gestion et comptabilité des projets | [590357](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590357) | La méthode **ProjTable::InitFromCustTable - canDeletePostalAddress** provoque un problème de performances. |
| Gestion et comptabilité des projets | [592493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=592493) | Le message d’erreur doit être plus clair que « Erreur inattendue. » |
| Gestion et comptabilité des projets | [598810](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598810) | La tâche de traitement par lots Validation de la facture de projet traite et valide la proposition de facture même si les lignes de facture n’ont pas été générées. |
| Gestion et comptabilité des projets | [574282](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574282) | Un problème d’arrondi se produit lorsque la clé de configuration de la licence du secteur public est désactivée. Un coût ou un prix de vente incorrect est généré sur les heures de la feuille de temps pour les contrats qui ont plusieurs sources de financement. |
| Gestion et comptabilité des projets | [577598](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577598) | Le prix de vente du projet sur un bon de commande de projet facturé est mal calculé lorsque le modèle de prix de vente est **Taux de contribution**. |
| Gestion et comptabilité des projets | [580784](https://fix.lcs.dynamics.com/Issue/Details/?bugId=580784) | Le système ne prend pas en compte les jours actifs entre les deux lorsqu’il calcule le taux de main-d’œuvre effectif pour un employé. |
| Gestion et comptabilité des projets | [584054](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584054) | Une erreur de validation se produit sur la feuille de temps intersociétés en raison de l’erreur de validation suivante : « Aucun partenaire commercial n’est configuré pour l’entité juridique ». |
| Gestion et comptabilité des projets | [586303](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586303) | La description provenant d’un bon de commande qui a une catégorie de dépenses n’est pas récupérée dans la liste des transactions de projet validées. |
| Gestion et comptabilité des projets | [590349](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590349) | Il existe une conversion incorrecte sur les journaux d’articles qui sont validés dans un projet. |
| Gestion et comptabilité des projets | [557294](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557294) | Vous pouvez confirmer un bon de commande même si la limite de financement a été dépassée. |
| Gestion et comptabilité des projets | [574162](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574162) | La section **Correction/Annuler la facture** d’une facture financière disparaît lorsqu’un ID de projet est sélectionné. |
| Gestion et comptabilité des projets | [575425](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575425) | Il y a des problèmes de performances lorsqu’une proposition de facture de projet est validée à partir d’une commande client de projet qui comprend un article stocké. |
| Gestion et comptabilité des projets | [575939](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575939) | Les factures d’achat de projet ne peuvent pas être validées car l’erreur suivante se produit : « La fonction AccDistProcessorProjectExtension.createForProjectRevenueLine a été appelée de manière incorrecte. » |
| Gestion et comptabilité des projets | [578970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=578970) | Mise à jour de la création de tâches par lots d’estimation de projet pour prendre en charge l’exécution de plusieurs sous-tâches. |
| Gestion et comptabilité des projets | [584519](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584519) | Le statut d’une feuille de temps ne peut pas être mis à jour sur **Brouillon** lorsque le workflow est bloqué dans un état **Annulé**. |
| Gestion et comptabilité des projets | [584757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584757) | Les montants de retenue ne sont pas calculés dans la proposition de facture d’avoir s’il existe plusieurs lignes. |
| Gestion et comptabilité des projets | [586034](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586034) | Lorsque vous essayez de modifier le montant d’une facture générée à partir d’un bon de commande, l’erreur suivante se produit : « Les transactions sur le bon ne s’équilibrent pas au XX/XX/XXXX. (devise comptable : 0,00 - devise de déclaration : 0,01). » |
| Gestion et comptabilité des projets | [588714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588714) | Il existe un problème de performances lorsqu’une proposition de facture de projet est publiée en mode de traitement par lots, en raison de la jointure avec **GeneralJournalAccountEntry**. |
| Gestion et comptabilité des projets | [588851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=588851) | Il y a des problèmes de performances lorsqu’une feuille de temps est validée. |
| Gestion et comptabilité des projets | [590535](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590535) | La hiérarchie des estimations de coûts de la structure de répartition du travail n’est pas correctement alignée après le développement de toutes les tâches ou après le développement manuel d’une seule tâche. |
| Gestion et comptabilité des projets | [593663](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593663) | Le modèle Excel de devis de projet ne peut pas être ajouté au menu **Ouvrir dans Excel**. |
| Gestion et comptabilité des projets | [596669](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596669) | Le numéro d’exonération de taxes d’une entité juridique n’est pas inclus sur la facture de projet imprimée. |
| Gestion et comptabilité des projets | [597563](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597563) | Aucune donnée financière n’est mise à jour dans l’erreur unité d’inventaire lorsqu’un projet est ajusté par rapport aux lignes d’avoir. |
| Gestion et comptabilité des projets | [598109](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598109) | Après avoir appliqué l’article de la base de connaissances KB 461935, vous ne pouvez pas valider d’estimations si vous passez à des séquences de nombres continues. |
| Gestion et comptabilité des projets | [598688](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598688) | **TimeEntryDataManager** provoque l’arrêt de l’application mobile de feuille de temps du projet pour Android. |
| Gestion et comptabilité des projets | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | La valeur contrepassée des TEC à partir de la validation d’une facture est différente de la valeur des TEC validée originellement à partir de l’entrée de temps. |
| Gestion et comptabilité des projets | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Dans les cas de provision appliquée, les pièces comptables ne sont pas correctement équilibrées lorsque le revenu facturé d’un projet est validé. |
| Gestion et comptabilité des projets | [603320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603320) | Quand la fonctionnalité **Amélioration des performances de planification des ressources du projet** est activée, les valeurs décimales sont incorrectement arrondies pour la disponibilité et la capacité des ressources. |
| Gestion et comptabilité des projets | [607324](https://fix.lcs.dynamics.com/Issue/Details/?bugId=607324) | Quand la fonctionnalité **Créer des estimations de projet à l’aide de plusieurs tâches par lots** est activée, la création d’estimations dans un lot comportant plusieurs sous-tâches ne fonctionne que pour la période en cours. |
| Déplacement et dépenses | [551911](https://fix.lcs.dynamics.com/Issue/Details/?bugId=551911) | Une stratégie de demande de trajet est ignorée, et le workflow est approuvé sans erreurs. |
| Déplacement et dépenses | [563752](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563752) | <p>L’application Mobile Gestion des dépenses n’enregistre pas les informations suivantes sur la ligne de dépenses :</p><ul><li>L’ID du projet</li><li>Si la dépense est facturable</li><li>Le numéro d’activité</li></ul> |
| Déplacement et dépenses | [569458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569458) | Le champ **Reçus joints** est défini sur **Oui** même si aucun reçu n’est joint à la ligne de dépense. |
| Déplacement et dépenses | [571334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571334) | Une erreur se produit si vous essayez de définir la catégorie de dépense sur **Personnel**. |
| Déplacement et dépenses | [572783](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572783) | Vous ne pouvez pas joindre de reçu et modifier la dépense parente après qu’une transaction par carte de crédit a été divisée en une dépense personnelle. |
| Déplacement et dépenses | [574252](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574252) | La stratégie de dépense pour les transactions intersociétés ayant un ID de projet ne fonctionne pas correctement. |
| Déplacement et dépenses | [574489](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574489) | L’information de la date de validation est manquante pour les notes de frais validées. |
| Déplacement et dépenses | [574504](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574504) | Des problèmes de mode de paiement existent dans l’application mobile Gestion des dépenses. |
| Déplacement et dépenses | [584799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584799) | Une demande de trajet créée pour un collaborateur peut être utilisée pour la note de frais d’un autre collaborateur avant la date déléguée. |
| Déplacement et dépenses | [586023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586023) | Lorsque vous créez une dépense les modifications des valeurs de dimension financière ne sont pas correctement mises à jour au niveau de la répartition comptable dans l’espace de travail **Gestion des dépenses**. |
| Déplacement et dépenses | [586081](https://fix.lcs.dynamics.com/Issue/Details/?bugId=586081) | Le statut d’approbation de la ligne de dépense principale n’est pas synchronisé avec le statut d’approbation du workflow de la ligne détaillée. |
| Déplacement et dépenses | [590544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590544) | Une erreur se produit si vous validez une note de frais et que le recouvrement fiscal est activé. |
| Déplacement et dépenses | [564851](https://fix.lcs.dynamics.com/Issue/Details/?bugId=564851) | Un délégué ne peut pas supprimer les notes de frais d’un employé licencié. |
| Déplacement et dépenses | [587306](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587306) | La suppression d’une ligne de dépense prend plus de temps que prévu et affecte les performances. |
| Déplacement et dépenses | [600455](https://fix.lcs.dynamics.com/Issue/Details/?bugId=600455) | **TrvExpTrans** provoque un enregistrement **TaxUncommitted** orphelin, parce que seul **SourceDocumentLine** est supprimé. |
| Déplacement et dépenses | [609918](https://fix.lcs.dynamics.com/Issue/Details/?bugId=609918) | **ReleaseUpdateDB72_Expense.updateTrvExpTransProjTransId()** ne respecte pas **trvExpTrans.ReferenceDataAreaId** pour créer la nouvelle souche de numéros. |

## <a name="regulatory-updates"></a>Mises à jour réglementaires

Pour plus d’informations sur les mises à jour réglementaires pour les applications de finances et d’opérations, voir [Mises à jour réglementaires](/dynamics365/finance/localizations/regulatory-updates). Vous pouvez également vous connecter à Microsoft Dynamics Lifecycle Services (LCS) et utiliser l’outil Recherche de problèmes pour afficher les mises à jour réglementaires prévues. La recherche de problèmes vous permet de rechercher par pays ou région, type de fonctionnalité et version.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
