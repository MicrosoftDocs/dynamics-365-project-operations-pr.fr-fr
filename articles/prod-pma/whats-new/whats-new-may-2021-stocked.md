---
title: Nouveautés ou modifications dans Project Operations de mai 2021 pour les scénarios basés sur le stock/la production
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de mai 2021 de Project Operations pour les scénarios basés sur la production/produits stockés.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: eff34a4e9fc1fc6429f1fa7a3e4b0d5b664222f9
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029389"
---
# <a name="whats-new-or-changed-in-project-operations-may-2021-for-stockedproduction-based-scenarios"></a>Nouveautés ou modifications dans Project Operations de mai 2021 pour les scénarios basés sur le stock/la production

_ **S’applique à :** Project Operations pour les scénarios basés sur le stock/la production

Cet article s’applique aux composants et versions de Microsoft Dynamics 365 Project Operations suivants :

- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.19
 
### <a name="quality-updates"></a>Mises à jour qualité
                                                                                                                                                                                  
| Fonctionnalités                      | Numéro de référence| Mise à jour qualité                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestion et comptabilité des projets | [529751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529751) | L’importation échoue lorsque les validations d’entité sont désactivées pour les lignes du journal d’articles du projet.                                                                                                                                                   |
| Gestion et comptabilité des projets | [550565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550565) | Un problème de performances se produit avec le rapport de comptes TEC lié à la recherche **GeneralJournalEntry**.                                                                                                                                  |
| Gestion et comptabilité des projets | [539044](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539044) | Les dimensions financières sont manquantes dans le projet TEC.                                                                                                                                                                                                    |
| Gestion et comptabilité des projets | [540903](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540903) | La validation d’une proposition de facture échoue, car le **ProjBudgetAllocationLineIdSales** incorrect est attribué à **ProjBudgetReductionHistory**.                                                                                                                           |
| Gestion et comptabilité des projets | [547090](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547090) | Après l’importation du fichier XML, le journal général affiche des numéros de document incorrects.                                                                                                                                                              |
| Gestion et comptabilité des projets | [552160](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552160) | Une erreur se produit dans le modèle de structure de répartition du travail.                                                                                                                                                                                          |
| Gestion et comptabilité des projets | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Notes de formulaire** et **Configuration de formulaire** ne sont pas visibles dans la configuration de la gestion des projets dans les entités juridiques de Finance lorsqu’elles sont intégrées à Project Operations.                                                                                                             |
| Gestion et comptabilité des projets | [553313](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553313) | L’annulation d’une commande client intersociétés échoue avec l’erreur suivante, « Impossible de modifier un enregistrement dans les lignes de commande fournisseur (PurchLine). Un conflit de mise à jour s’est produit, car un autre processus utilisateur a supprimé l’enregistrement ou modifié un ou plusieurs champs dans l’enregistrement. » |
| Gestion et comptabilité des projets | [553775](https://fix.lcs.dynamics.com/Issue/Details/?bugId=553775) | L’ajustement de la transaction du projet crée une dimension financière incorrecte pour le coût du projet.                                                                                                                                                          |
| Gestion et comptabilité des projets | [556751](https://fix.lcs.dynamics.com/Issue/Details/?bugId=556751) | La facture fournisseur a une invite supplémentaire lors du traitement d’une commande fournisseur connectée à un projet.                                                                                                                                                 |
| Gestion et comptabilité des projets | [557925](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557925) | Les lignes de la feuille de temps ne peuvent pas être approuvées et l’erreur suivante se produit : « La condition d’activation du flux de travail n’est pas valide. Signalez ce problème à l’administrateur système. »                                                                          |
| Gestion et comptabilité des projets | [559266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559266) | Si vous recevez l’erreur « Impossible de modifier le contrat de projet car il existe une transaction pour le projet associé XXXXXX », vous pouvez toujours modifier le contrat au niveau du projet.                                                                           |
| Gestion et comptabilité des projets | [560432](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560432) | Si vous recevez l’erreur « La quantité ne peut pas être facturée, car les transactions de stock avec le statut Déduit sont insuffisantes », une facture de commande fournisseur ne peut pas être validée après l’exécution du recalcul du stock.                             |
| Gestion et comptabilité des projets | [562013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=562013) | Lorsque le flux de travail de demande de ressources est activé, des problèmes de performances se produisent lorsque vous essayez d’ouvrir des pages avec le contrôle de disponibilité de ressources du projet.                                                                                                               |
| Gestion et comptabilité des projets | [488320](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488320) | Le statut de la facture passe à **Non facturable** une fois que vous ajoutez une règle de facturation pour spécifier un autre projet dans le contrat du projet.                                                                                                                                |
| Gestion et comptabilité des projets | [515219](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515219) | Une erreur se produit lorsque vous supprimez une facture d’acompte d’une commande fournisseur du projet et que le paramètre **Valider le coût d’acompte dans le projet** est activé.                                                                                                        |
| Gestion et comptabilité des projets | [526439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526439) | Lorsque vous validez une facture de commande founisseur du projet, une erreur se produit car le marquage automatique de l’article est manquant.                                                                                                                            |
| Gestion et comptabilité des projets | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | La description par défaut est vide pour la TVA lorsque le type de validation est égal à la taxe de vente pour les documents de facture du projet.                                                                                                                                           |
| Gestion et comptabilité des projets | [530352](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530352) | Une commande fournisseur de projet affichera une erreur si vous supprimez la commande client de demande d’articles annulée associée.                                                                                                                                 |
| Gestion et comptabilité des projets | [530651](https://fix.lcs.dynamics.com/Issue/Details/?bugId=530651) | Lorsque vous marquez et annulez le marquage des commandes fournisseur de demandes d’articles du projet, les références sont perdues.                                                                                                                                                               |
| Gestion et comptabilité des projets | [533023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=533023) | Un problème se produit avec la valeur par défaut de la quantité réduite lors de l’impression d’une liste de sélection pour les demandes d’articles du projet.                                                                                                                                                 |
| Gestion et comptabilité des projets | [535493](https://fix.lcs.dynamics.com/Issue/Details/?bugId=535493) | Le prix de vente calculé n’est pas correct en cas de livraison excessive.                                                                                                                                                                                 |
| Gestion et comptabilité des projets | [541329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541329) | L’engagement incorrect est validé lorsque la rétention est libérée sans quantité de facture dans une proposition de facture.                                                                                                                                                |
| Gestion et comptabilité des projets | [541997](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541997) | Lorsque vous générez une période de feuille de temps, la première période s’affiche en tant que semaine 53.                                                                                                                                                                         |
| Gestion et comptabilité des projets | [542043](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542043) | Les types de projet par défaut dans les paramètres d’intégration de Dynamics 365 Project Service Automation doivent être Temps et matériel et Prix fixe.                                                                                                         |
| Gestion et comptabilité des projets | [543096](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543096) | La suppression d’une proposition de facture avec des règles de facturation génère des validations.                                                                                                                                                                              |
| Gestion et comptabilité des projets | [543463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543463) | L’estimation finale du processus d’élimination qui utilise la méthode de pourcentage complet ne peut pas être éliminée, car le système ne reconnaît pas le produit.                                                                                                                                      |
| Gestion et comptabilité des projets | [543938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543938) | Lorsque vous validez une estimation de projet, l’enregistrement de validation de l’estimation n’est pas créé.                                                                                                                                                                            |
| Gestion et comptabilité des projets | [546885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546885) | Le compte principal d’une facture fournisseur en attente est introuvable pendant la facturation intersociétés.                                                                                                                                                               |
| Gestion et comptabilité des projets | [547885](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547885) | Si un contrat comprend des demandes d’articles, vous ne pouvez pas ajouter une deuxième source de financement.                                                                                                                                                         |
| Gestion et comptabilité des projets | [550379](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550379) | Le système crée des révisions dans le budget du projet pour tous les projets lorsque vous utilisez **Projet** > **Budget** > **Révisions** > **Nouveau** > **Importer**.                                                                                                                         |
| Gestion et comptabilité des projets | [550577](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550577) |  Si vous ajustez une transaction avec des devises de transaction et de comptabilité différentes, les écritures de validation et de comptabilité générale sont incorrectes.                                                                                                                                       |
| Gestion et comptabilité des projets | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Le coût engagé est surestimé avec des montants de taxe non déductibles.                                                                                                                                                                                   |
| Gestion et comptabilité des projets | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Aucune dimension n’est sélectionnée lorsque vous créez une facture de validation pour une transaction.                                                                                                                                                                  |
| Gestion et comptabilité des projets | [559416](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559416) | La méthode **PurchTotals.purchNewTotalAmount()** est appelée lorsque vous créez une facture fournisseur en attente qui n’est pas liée à une commande fournisseur, ce qui entraîne un problème de performances.                                                                                   |
| Gestion et comptabilité des projets | [563694](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563694) | Les colonnes **Budget consommé** et **Budget restant** affichent des montants incorrects dans les soldes budgétaires du projet.                                                                                                                                                |
| Gestion et comptabilité des projets | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Une transaction est validée deux fois lorsque la facturation basée sur les tâches est utilisée dans Dataverse avec Project Operations.                                                                                                                                         |
| Gestion et comptabilité des projets | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Le pourcentage terminé pour la constatation du produit est incorrect lors de l’utilisation de Project Operations.                                                                                                                                                  |
| Gestion et comptabilité des projets | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | La régularisation du produit est doublée lorsque vous utilisez une facture fournisseur en attente dans un scénario intégré de Project Operations.                                                                                                                                          |
| Gestion et comptabilité des projets | [569736](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569736) | La validation d’une feuille de temps du projet crée des transactions en double.                                                                                                                                                                        |
| Gestion et comptabilité des projets | [569819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569819) | Une erreur se produit lorsque vous validez le journal de consommation d’articles dans l’ordre de travail.                                                                                                                                  |
| Gestion et comptabilité des projets | [571197](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571197) | Un ordre de fabrication du projet ne peut pas être terminé en raison de l’erreur suivante : « Référence d’objet non définie sur une instance d’un objet. »                                                                                                                           |
| Gestion et comptabilité des projets | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Le journal d’intégration ne peut pas être validé si la règle du profil de produit est définie sur la **Configuration Groupe**.                                                                                                                                                           |
| Gestion et comptabilité des projets | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Une facture fournisseur ne peut pas être validée pour une commande fournisseur du projet comportant des lignes avec plusieurs unités de mesure.                                                                                                                                             |
| Gestion et comptabilité des projets | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | La dimension financière par défaut d’un projet ne peut pas être mise à jour à l’aide de l’entité de données **V2** du projet.                                                                                                                                                          |
| Gestion et comptabilité des projets | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Impossible de créer un avoir pour une commande client du projet lorsque la taxe est dans une devise différente de celle de la société.                                                                                                                     |
| Gestion et comptabilité des projets | [574104](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574104) | Un problème se produit lorsqu’une proposition de facture est créée avec plus de 100 règles de facturation.                                                                                                                                                                  |
| Gestion et comptabilité des projets | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | L’exécution du traitement par lots pour créer des estimations de projet prend trop de temps.                                                                                                                                                                      |
| Gestion et comptabilité des projets | [577785](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577785) | Lorsque vous exécutez la fonctionnalité **Remplir les ressources du projet dans toutes les sociétés**, l’erreur suivante se produit : « Nom d’objet non valide ResRollupCalendar. »                                                                                                                                   |
| Gestion et comptabilité des projets | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Lorsque vous supprimez un contrat, l’adresse associée au client est également supprimée.                                                                                                                                                                    |
| Déplacement et dépenses                  | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | La condition du flux de travail d’approbation de la note de frais n’est pas évaluée correctement.                                                                                                                                                                           |
| Déplacement et dépenses                  | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | La stratégie de la note de frais n’évalue pas correctement l’ID du projet.                                                                                                                                                                                   |
| Déplacement et dépenses                  | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | L’action **Fractionner en personnel** pour les transactions de dépenses intersociétés ne fonctionne pas correctement.                                                                                                                                                                |
| Déplacement et dépenses                  | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Parfois, les justifications d’une ligne de note de frais sont accidentellement supprimées lorsque des demandes de déplacement sont supprimées. Cela se produit lorsque le recid de la note de frais et de la demande de déplacement sont identiques.                                                            |
| Déplacement et dépenses                  | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Un problème se produit avec l’application mobile Dépenses lorsque le champ **ID du projet** est requis par les stratégies de la note de frais.                                                                                                                                                |
| Déplacement et dépenses                  | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Lorsque vous essayez de modifier une dépense intersociétés associée à un projet, le message d’erreur suivant s’affiche : « Référence d’objet non définie sur une instance d’un objet. »                                                                           |
| Déplacement et dépenses                  | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | La devise et le montant incorrects sont répertoriés dans la comptabilité auxiliaire de la banque une fois qu’une note de frais est validée.                                                                                                                                                                |
| Déplacement et dépenses                  | [555462](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5355462) | Le coût engagé pour un projet n’est pas libéré après la clôture d’une demande de déplacement avec un coût engagé.                                                                                                                                              |
| Déplacement et dépenses                  | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Des améliorations ont été apportées à la fonctionnalité Supprimer les transactions par carte de crédit.                                                                                                                                                                                           |
| Déplacement et dépenses                  | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | La taxe de vente incluse dans une note de frais n’est pas calculée de manière cohérente lorsqu’une devise de déclaration différente est spécifiée dans une entité juridique.                                                                                                         |
| Déplacement et dépenses                  | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Les performances sont affectées lors de l’ajout d’une nouvelle dépense de déplacement en espèces.                                                                                                                                                                                         |
| Déplacement et dépenses                  | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | La règle de la stratégie de dépenses n’est pas déclenchée dans la note de frais.                                                                                                                                                                                            |
| Déplacement et dépenses                  | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Le chargement d’une nouvelle catégorie partagée à l’aide de Data Management Framework supprime toutes les sous-catégories de toutes les catégories partagées.                                                                                                                         |
| Déplacement et dépenses                  | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Lorsque vous créez une ligne de dépense et sélectionnez une catégorie, l’erreur suivante s’affiche : « La combinaison du DOM du groupe de taxe et du STD du groupe de taxe d’article n’est pas valide ».                                                                  |
| Déplacement et dépenses                  | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Des problèmes de synchronisation se produisent avec l’application mobile Dépenses. 

### <a name="regulatory-updates"></a>Mises à jour réglementaires
Pour plus d’informations sur les mises à jour réglementaires pour les applications de finances et d’opérations, voir [Mises à jour réglementaires](/dynamics365/finance/localizations/regulatory-updates). Vous pouvez également vous connecter à Lifecycle Services (LCS) et afficher les mises à jour réglementaires planifiées à l’aide de l’outil de recherche de problèmes. La recherche d’incidents vous permet d’effectuer une recherche par pays, type de fonctionnalité et version.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]