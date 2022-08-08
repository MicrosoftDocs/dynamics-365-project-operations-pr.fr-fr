---
title: Nouveautés ou modifications de Project Operations en octobre 2021 pour les scénarios basés sur les produits stockés/ordres de fabrication
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version d’octobre 2021 de Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication.
author: andchoi
ms.date: 11/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: aa36199c9e7b0a70307c5e9fb163d82554f6be16
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029940"
---
# <a name="whats-new-or-changed-in-project-operations-october-2021-for-stockedproduction-based-scenarios"></a>Nouveautés ou modifications de Project Operations en octobre 2021 pour les scénarios basés sur les produits stockés/ordres de fabrication

_**S’applique à :** Project Operations pour les scénarios basés sur le stock/la production_

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.22
 
## <a name="quality-updates"></a>Mises à jour qualité

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
|--------------|------------------|----------------|
| Gestion et comptabilité des projets | [557017](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557017) | Les travaux en cours (TEC) de projet et les montants des produits à recevoir ne sont pas correctement contrepassés lorsqu’une facture client intersociétés est validée. |
| Gestion et comptabilité des projets | [558232](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558232) | La fonctionnalité **Empêcher la clôture du projet si des transactions ouvertes existent** ne fonctionne pas. |
| Gestion et comptabilité des projets | [559271](https://fix.lcs.dynamics.com/Issue/Details/?bugId=559271) | La classification de facturation sur une facture financière ne remplit pas automatiquement les dimensions provenant des projets lorsque cette fonctionnalité est activée. |
| Gestion et comptabilité des projets | [574013](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574013) | Dans les scénarios non intersociétés, les travaux en cours (TEC) de projet et les montants des produits à recevoir ne sont pas correctement contrepassés lorsque la facture du projet est validée. |
| Gestion et comptabilité des projets | [577857](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577857) | Les valeurs de débit et de crédit sont inversées lorsque le complément Microsoft Excel est utilisé avec le journal des dépenses du projet et le champ **Type de compte de contrepartie** est défini sur **Projet**. |
| Gestion et comptabilité des projets | [577972](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577972) | Le montant qui est validé dans les transactions de projet est surestimé sur un bon de commande de projet qui comprend des articles stockés et qui comporte des montants de taxe non déductibles lorsque **UseTax** est marqué. |
| Gestion et comptabilité des projets | [581216](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581216) | Le système répartit le montant entre les états de résultat du projet et les états des travaux en cours du projet. |
| Gestion et comptabilité des projets | [582065](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582065) | L’inventaire disponible est incorrect après l’ajustement d’un besoin d’article partiellement retourné. |
| Gestion et comptabilité des projets | [582682](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582682) | Les noms de ressources sont dupliqués dans Project Operations lorsqu’ils sont modifiés dans Microsoft Project. |
| Gestion et comptabilité des projets | [583873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583873) | Les notes de frais intersociétés qui ont des coûts de facture fournisseur intersociétés en attente dans la comptabilité fournisseur sont d’abord validés dans le type de validation **Coût des TEC du projet**. Cependant, lors du traitement, les coûts liés au devis sont validés dans le type de validation **Coût du projet** au lieu du type de validation attendu **Coût intersociétés**. |
| Gestion et comptabilité des projets | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Cette retenue fournisseur a pour effet que les transactions de dépenses du projet ne sont pas affichées. |
| Gestion et comptabilité des projets | [587453](https://fix.lcs.dynamics.com/Issue/Details/?bugId=587453) | La feuille de temps doit arrondir le montant de la transaction dans la devise de la transaction à un nombre spécifié de décimales sur toutes les répartitions comptables et les écritures de répartition du journal général. |
| Gestion et comptabilité des projets | [589409](https://fix.lcs.dynamics.com/Issue/Details/?bugId=589409) | Les quantités des besoins d’articles du projet sont automatiquement mises à jour lorsque les commandes planifiées sont confirmées. |
| Gestion et comptabilité des projets | [590206](https://fix.lcs.dynamics.com/Issue/Details/?bugId=590206) | Le numéro de document, le solde fournisseur du type de transaction et le numéro de compte ne peuvent pas être annulés sur la facture d’acompte d’un bon de commande. |
| Gestion et comptabilité des projets | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | La facture fournisseur intersociétés est interrompue lorsque l’intégration de la facture fournisseur est activée. |
| Gestion et comptabilité des projets | [593335](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593335) | Lorsque vous créez un journal des dépenses du projet, le montant du coût est affiché dans le champ **Crédit**. |
| Gestion et comptabilité des projets | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Les conditions de paiement sur les factures de projet ne fonctionnent pas comme prévu. |
| Gestion et comptabilité des projets | [593565](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593565) | Les numéros document de feuille de temps peuvent être réutilisés lorsque la souche de numéros est configurée comme continue. |
| Gestion et comptabilité des projets | [593652](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593652) | FRANCE : La logique du **Montant de la rétention manuelle** ne correspond pas à la logique du **Montant de la rétention automatique** dans la proposition de facture de contrat de projet. |
| Gestion et comptabilité des projets | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Lorsque la rétention du fournisseur est libérée, la validation du numéro document comporte des lignes supplémentaires incorrectes. |
| Gestion et comptabilité des projets | [596650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596650) | Quand le champ **Date de la facture** sur la page **Créer une proposition de facture** est modifié, l’erreur suivante peut se produire : « Référence d’objet non définie sur une instance d’objet. » |
| Gestion et comptabilité des projets | [597679](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597679) | Une erreur se produit lorsque vous essayez d’approuver une feuille de temps à partir du workflow **TSLine**, et il existe une stratégie de feuille de temps pour le samedi et le dimanche. |
| Gestion et comptabilité des projets | [597801](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597801) | Le type d’élément de projet de solde d’ouverture est exclu des **Récapitulatifs des transactions de proposition de facture** lorsque le total de la facture de la proposition de facture est calculé. |
| Gestion et comptabilité des projets | [597886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597886) | Si le coût de consommation sur un ordre de fabrication de projet est 0 (zéro), l’erreur suivante se produit lorsque vous essayez de procéder à l’estimation : « Tentative de division par zéro. » |
| Gestion et comptabilité des projets | [598706](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598706) | L’application mobile Feuille de temps de projet sur Android cesse de répondre. Ce problème est lié à **TimeEntryDataManager ArgumentNullException**. |
| Gestion et comptabilité des projets | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Le journal d’intégration Project Operations échoue lorsque vous le validez, car il manque des dimensions à un compte. Cependant, le compte auquel il manque les dimensions n’est pas le compte sur lequel vous effectuez la validation. |
| Gestion et comptabilité des projets | [598929](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598929) | Le filtre **À ce jour** dans les recherches n’est pas effacé lorsqu’il est supprimé de la boîte de dialogue **Sélectionner** de la page **Valider les coûts**. |
| Gestion et comptabilité des projets | [599757](https://fix.lcs.dynamics.com/Issue/Details/?bugId=599757) | **Réinitialiser toutes les répartitions** échoue et affiche une erreur pour les feuilles de temps créées pour un projet du type **Temps uniquement**. |
| Gestion et comptabilité des projets | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | L’onglet **Projet** n’est pas modifiable sur une facture fournisseur en attente lorsque la catégorie d’approvisionnement est affectée à l’article. |
| Gestion et comptabilité des projets | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Le volet de navigation est absent si vous n’êtes pas connecté au Dataverse de Project Operations. |
| Gestion et comptabilité des projets | [546467](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546467) | Pour les transactions d’ajustement de projet intersociétés, il y a des problèmes dans la société de destination. |
| Gestion et comptabilité des projets | [563579](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563579) | Les coûts engagés pour un projet calculent la quantité et le prix de revient erronés si le bon de commande a été traité par la fonction **Processus de fin d’exercice des bons de commande** dans la comptabilité. |
| Gestion et comptabilité des projets | [581454](https://fix.lcs.dynamics.com/Issue/Details/?bugId=581454) | Lorsqu’un ordre de fabrication de projet comportant des ordres de qualité est signalé comme étant terminé, l’erreur suivante se produit : « Aucune transaction virtuelle marquée avec une transaction d’inventaire. » |
| Gestion et comptabilité des projets | [596408](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596408) | Lorsqu’une facture de comptabilité fournisseur liée au projet est validée, l’erreur suivante se produit : « Le texte de projet énuméré - coût - élément n’existe pas. » |
| Gestion et comptabilité des projets | [597237](https://fix.lcs.dynamics.com/Issue/Details/?bugId=597237) | Les coûts indirects sont doublés lorsque vous provisionnez manuellement le produit. |
| Gestion et comptabilité des projets | [601198](https://fix.lcs.dynamics.com/Issue/Details/?bugId=601198) | La validation des TEC et du produit provisionné ne produisent pas de transactions. |
| Gestion et comptabilité des projets | [602095](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602095) | L’activation du prix en attente échoue pour un poste de coût standard lorsqu’un bon de commande de projet reçu existe. |
| Gestion et comptabilité des projets | [602677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602677) | La valeur contrepassée des TEC à partir de la validation d’une facture est différente de la valeur des TEC validée originellement à partir d’une entrée de temps. |
| Gestion et comptabilité des projets | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Il existe un problème de validation du produit facturé d’un projet dans les cas d’application de provision où les transactions ne sont pas équilibrées sur la pièce justificative. |
| Gestion et comptabilité des projets | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | La création d’un devis après validation d’une proposition de facture bloque l’importation des lignes de correction dans Project Operations. |
| Gestion et comptabilité des projets | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | La modification d’un enregistrement de jalon entièrement facturé ne devrait pas être possible. |
| Gestion et comptabilité des projets | [611389](https://fix.lcs.dynamics.com/Issue/Details/?bugId=611389) | Lorsque les frais automatiques sont utilisés, la facture client intersociétés pour une feuille de temps ne peut pas être validée et un message d’erreur s’affiche. |
| Gestion et comptabilité des projets | [612991](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612991) | L’adresse d’un sous-projet n’est pas correctement mise à jour. |
| Gestion et comptabilité des projets | [613418](https://fix.lcs.dynamics.com/Issue/Details/?bugId=613418) | Le prix de revient sur les besoins d’articles est mis à jour avec le prix d’achat pour les bons de commande consolidés. |
| Gestion et comptabilité des projets | [614145](https://fix.lcs.dynamics.com/Issue/Details/?bugId=614145) | Le coût validé n’est pas correct après la mise à jour du prix d’achat et le paramètre **Activer la gestion des modifications** est activé. |
| Déplacement et dépenses | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Toutes les dépenses des utilisateurs sont visibles lorsque vous recherchez une catégorie dans l’application mobile Gestion des dépenses. |
| Déplacement et dépenses | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Des montants incorrects sur les transactions fournisseur et les transactions de taxe de vente sont validés à partir d’une dépense créée à partir d’une transaction par carte de crédit. |
| Déplacement et dépenses | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Un message d’avertissement non pertinent s’affiche lorsque vous actualisez les pages de notes de frais. |
| Déplacement et dépenses | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Le mauvais approbateur provisoire est utilisé lorsque vous supprimez un approbateur provisoire, puis soumettez à nouveau la demande via le workflow. |
| Déplacement et dépenses | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Une erreur de validation se produit, liée à la configuration du kilométrage. |
| Déplacement et dépenses | [620773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620773) | La distribution ne met pas à jour l’entité juridique lorsqu’une transaction non attachée est rajoutée à la note de frais sur une dépense intersociétés. |

### <a name="regulatory-updates"></a>Mises à jour réglementaires

Pour plus d’informations sur les mises à jour réglementaires pour les applications de finances et d’opérations, voir [Mises à jour réglementaires](/dynamics365/finance/localizations/regulatory-updates). Vous pouvez également vous connecter à Microsoft Dynamics Lifecycle Services (LCS) et utiliser l’outil Recherche de problèmes pour afficher les mises à jour réglementaires prévues. La recherche de problèmes vous permet de rechercher par pays ou région, type de fonctionnalité et version.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
