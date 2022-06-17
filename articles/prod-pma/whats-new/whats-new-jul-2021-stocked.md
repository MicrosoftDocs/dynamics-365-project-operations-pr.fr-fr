---
title: Nouveautés ou modifications dans Project Operations de juillet 2021 pour les scénarios basés sur le stock/la production
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de juillet 2021 de Project Operations pour les scénarios basés sur la production/produits stockés.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: df9a68c5a12e6aec140867eb1db3d88279c05795
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933627"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Nouveautés ou modifications dans Project Operations de juillet 2021 pour les scénarios basés sur le stock/la production

_**S’applique à :** Project Operations pour les scénarios basés sur le stock/la production_

Cet article s’applique aux composants et versions de Microsoft Dynamics 365 Project Operations suivants :

- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.20
 
### <a name="quality-updates"></a>Mises à jour qualité
                                                                                                                                                                                  
| Fonctionnalités                      | Numéro de référence| Mise à jour qualité                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Gestion et comptabilité des projets | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Les enregistrements d’engagement de coûts d’une demande d’achat sont effacés dès que la commande fournisseur est libérée de l’émission de la demande d’achat.                                                                           |
| Gestion et comptabilité des projets | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | La validation du budget se produit deux fois dans une demande d’achat. Cette duplication signifie que la demande ne peut pas être fermée et que la commande fournisseur correspondante n’est pas créée.                                                                                                                        |
| Gestion et comptabilité des projets | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | La règle de facturation **Pourcentage à facturer** n’a pas pu être complétée en raison d’un problème d’arrondi.                                                                              |
| Gestion et comptabilité des projets | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Lorsque vous ajustez la transaction et que le pourcentage a des décimales, le prix de revient et de vente n’est pas ajusté correctement.                                      |
| Gestion et comptabilité des projets | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | L’explorateur de source comptable affiche les heures pour une seule ligne de la feuille de temps ou pour plusieurs lignes de la feuille de temps avec différentes activités.                                      |
| Gestion et comptabilité des projets | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Les vues enregistrées et la personnalisation des détails de la ligne de la feuille de temps font que le système ouvre toujours les détails de la première feuille de temps de la liste lorsqu’il essaie d’ouvrir une feuille de temps.  |
| Gestion et comptabilité des projets | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Le nœud racine du projet disparaît et les enregistrements de la structure de répartition du travail sont supprimés après l’importation.                                                                                             |
| Gestion et comptabilité des projets | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Lorsque les articles sont reçus et émis partiellement à partir de la demande d’articles, le système met à jour le solde de consommation budgétaire incorrect. |
| Gestion et comptabilité des projets | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Les commandes achat de retenue du projet n’affichent pas correctement les totaux dans le volet **Totaux** de la grille **Facture en attente**.                                                                  |
| Gestion et comptabilité des projets | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Lors de la clôture du stock, les ajustements du coût des articles du projet sont enregistrés dans le compte de bilan au lieu du compte de résultat.                                                            |
| Gestion et comptabilité des projets | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Un document de transaction validé et un document d’estimation utilisent USD comme devise comptable, mais le montant indique ce que serait l’équivalent en CAD.              |
| Gestion et comptabilité des projets | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Les coûts engagés avec une demande d’articles et une commande fournisseur sont incorrects dans le processus de facturation de la commande fournisseur avec l’accusé de réception de marchandises partielles et la facturation partielle.       |
| Gestion et comptabilité des projets | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | L’ajustement du projet ne met pas correctement à jour le montant des ventes avec les coûts indirects.                                                                                    |
| Gestion et comptabilité des projets | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | La table **Feuille de temps** n’a pas de relation définie avec la vue **Collaborateur/Ressource**.                                                                                   |
| Gestion et comptabilité des projets | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Impossible de remplir le champ **Numéro d’activité** lorsque vous le sélectionnez dans le menu déroulant d’une feuille de temps intersociétés.                                                                 |
| Gestion et comptabilité des projets | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Vous ne pouvez pas ajouter un champ **Finalité** ou **Description de l’activité** personnalisé aux pages suivantes : **Transaction de projet validée**, **Création de proposition de facture** ou **Proposition de facture**.  |
| Gestion et comptabilité des projets | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Un contrôle de date de livraison incorrect est fourni lorsque vous créez des demandes d’articles à l’aide de la gestion des données (**ProjSalesItemExigenceEntité**).                                              |
| Gestion et comptabilité des projets | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Lorsque vous sélectionnez un ID de contrat de projet dans Finance, l’environnement intégré Project Operations ouvre la page pour créer un nouvel enregistrement au lieu d’ouvrir le contrat de projet existant.                                                                                                                 |
| Gestion et comptabilité de projets | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  L’étiquette, « @SYS4083080 » (« Impossible de trouver un enregistrement de collaborateur unique correspondant aux valeurs entrées ») n’est pas traduite en danois.                                |
| Gestion et comptabilité des projets | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Le champ **Groupe de taxe d’article** n’est pas modifiable dans une proposition de facture.                                                                               |
| Gestion et comptabilité des projets | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Le coût engagé est surestimé avec des montants de taxe non déductibles.                                                                                                    |
| Gestion et comptabilité des projets | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | La validation d’une feuille de temps intersociétés avec plusieurs projets et différentes dimensions financières génère des valeurs inattendues dans la comptabilité générale.                             |
| Gestion et comptabilité des projets | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Les lignes de proposition de facture sont dupliquées en raison de plusieurs instances du processus périodique **Importer depuis la table intermédiaire** qui s’exécutent en même temps.                                      |
| Gestion et comptabilité des projets | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | Une erreur s’est produite dans la validation de la proposition de facture d’avoir, les transactions du document ne s’équilibrent pas.    |
| Gestion et comptabilité des projets | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Les coûts engagés du projet deviennent incorrects une fois que les factures en attente sont libérées.                                                                             |
| Gestion et comptabilité de projets | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Vous ne pouvez pas créer un avoir pour une commande client de projet lorsque la taxe est dans une devise différente de celle de la société.                                      |
| Gestion et comptabilité des projets | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | La suppression d’un contrat supprime également l’adresse associée au client.                                                                                     |
| Gestion et comptabilité des projets | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Une proposition de facture résultant d’une correction de transaction de temps négative ne peut pas être validée.                                                                    |
| Déplacement et dépenses                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | La taxe est calculée différemment dans les notes de frais.                                                                                                                  |
| Déplacement et dépenses                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | La mise à jour de la version **DB72_Expense.updateTrvExpTransProjTransId()** ne permet pas à **trvExpTrans.ReferenceDataAreaId** de créer la nouvelle souche de numéros.                    |
| Déplacement et dépenses                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Le montant indiqué ne s’affiche pas avec le champ obligatoire.                                                                                                             |
| Déplacement et dépenses                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Améliorations des performances d’ajout en pièce jointe d’une dépense à la note de frais à l’aide de l’interface utilisateur Notes de frais réinventées.                                                            |
| Déplacement et dépenses                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Vous pouvez supprimer les notes de frais validées.                                                                                           |
| Déplacement et dépenses                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Le message de stratégie de dépenses s’affiche plusieurs fois.                                                                                                       |
| Déplacement et dépenses                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Le champ **Mode de paiement** est inclus dans le volet **Nouvelle dépense**.                                                                                                      |
| Déplacement et dépenses                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | L’outil **Réinitialiser le statut du document de dépenses** doit réinitialiser le statut de la note de frais sur **Brouillon** si le flux de travail est introuvable. 

### <a name="regulatory-updates"></a>Mises à jour réglementaires
Pour plus d’informations sur les mises à jour réglementaires pour les applications de finances et d’opérations, voir [Mises à jour réglementaires](/dynamics365/finance/localizations/regulatory-updates). Vous pouvez également vous connecter à Lifecycle Services (LCS) et afficher les mises à jour réglementaires planifiées à l’aide de l’outil de recherche de problèmes. La recherche d’incidents vous permet d’effectuer une recherche par pays, type de fonctionnalité et version.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
