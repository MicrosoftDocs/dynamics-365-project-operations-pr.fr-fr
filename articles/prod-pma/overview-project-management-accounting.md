---
title: Vue d‘ensemble de gestion de projets et compatibilité
description: La fonctionnalité Gestion de projets et comptabilité peut être utilisée dans plusieurs secteurs pour fournir un service, fabriquer un produit ou obtenir un résultat.
author: Yowelle
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable; ProjProjectManagementWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: intro-internal
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1465e68fb119927f474bf4d5b26cb0cd1d60824340a7d46e59d23036d99503f3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007503"
---
# <a name="project-management-and-accounting-overview"></a>Vue d‘ensemble de gestion de projets et compatibilité

[!include [banner](../includes/banner.md)]

La fonctionnalité Gestion de projets et comptabilité peut être utilisée dans plusieurs secteurs pour fournir un service, fabriquer un produit ou obtenir un résultat.  

Un projet est un groupe d’activités conçu pour fournir un service, fabriquer un produit ou atteindre un objectif. Les projets consomment des ressources et génèrent des résultats financiers sous forme de revenus ou d’actifs.

## <a name="projects-across-industries"></a>Projets dans plusieurs secteurs
Le module Gestion de projets et comptabilité peut être utilisé dans plusieurs secteurs, comme indiqué dans l’illustration suivante.

[![Projets dans plusieurs secteurs.](./media/projects-accross-industries.jpg)](./media/projects-accross-industries.jpg) 

Dans un centre d’appels, un ticket peut être utilisé pour décrire l’ensemble des actions requises pour résoudre un appel. Les sociétés de conseil, telles que les organisations de conseil en gestion ou de conseil technique ou encore les agences de publicité, font référence à leurs activités comme des projets. En marketing, une campagne représente un ensemble de travaux qui doivent être livrés. Dans la fabrication par projet, un ordre de fabrication fait référence aux tâches variées qui doivent être effectuées pour produire certains produits finis. Quel que soit le nom utilisé pour eux, ces projets impliquent des ressources, des calendriers et des coûts, et le module Gestion de projets et comptabilité permet la planification, l’exécution et l’analyse de ces projets.

## <a name="project-phases"></a>Phases du projet
Bien que le flux de processus suivant vise les projets externes, ou des projets qui sont exécutés pour un ou plusieurs clients, la fonctionnalité s’applique également aux projets internes, uniquement de coûts. 

![3 phases d’un projet.](./media/3-stages-of-a-project.png) 

Comme le montre l’illustration précédente, la fonctionnalité Gestion de projets et comptabilité peut être divisée en trois phases :

1.  Initialiser
2.  Exécuter
3.  Analyser

## <a name="initiate-the-project"></a>Lancer le projet
Lors du lancement du projet, plusieurs processus clés se produisent. Vous pouvez utiliser un devis de projet pour communiquer l’estimation de la main-d’œuvre, des dépenses et des matériaux au client. Vous pouvez enregistrer les conditions de facturation, les limites et les accords dans un contrat de projet. Une structure de répartition du travail (WBS) peut être utilisée pour planifier et estimer le travail. Vous pouvez configurer des prévisions et des budgets pour guider l’exécution du projet. L’illustration suivante présente la structure d’un projet.[![structure du projet.](./media/project-structure1.jpg)](./media/project-structure1.jpg)  

### <a name="create-project-quotations"></a>Créer des devis de projet

Durant la phase de vente initiale d’un projet, un devis de projet permet de proposer à un client une offre sans engagement. Un devis peut inclure des articles, tels que les articles et services proposés, les coordonnées de base, les accords commerciaux spéciaux et les remises, ainsi que les éventuelles taxes et surtaxes.

Vous pouvez également émettre une lettre de garantie pour une transaction de devis de projet entre votre organisation et le client. Une fois le devis de projet créé, vous pouvez créer la demande de lettre de garantie pour le client et la soumettre à la banque. Une fois que la banque a approuvé la demande, la lettre de garantie est délivrée au client. 

Pour plus d’informations, voir [Devis du projet](project-quotations.md).

### <a name="create-project-contracts"></a>Créer des contrats de projet

Lorsque vous concluez un contrat avec un client ou une autre source de financement pour terminer un projet, vous devez d’abord créer un contrat de projet. Ensuite, lorsque vous créez le projet, vous devez l’affecter au contrat correspondant. Le type de projet que vous créez pour un contrat de projet détermine la méthode utilisée pour facturer les clients du projet. Vous pouvez modifier un contrat de projet et le projet associé, mais vous ne pouvez pas modifier le type de projet. Pour plus d’informations sur les types de projets, consultez la section « Création de projets ».

Pour plus d’informations sur les contrats de projet, voir [Contrats de projet](project-contracts.md).

### <a name="create-work-breakdown-structures"></a>Créer des structures de répartition du travail

Le degré des détails dans une structure de répartition du travail dépend du niveau de précision requis dans les estimations et le niveau de suivi requis par rapport à ces estimations. Les projets qui ont une tolérance très faible pour les glissements dans le calendrier ou les coûts nécessitent généralement une structure de répartition du travail plus détaillée, et nécessitent également un suivi diligent de l’avancement des travaux et des coûts par rapport à la structure de répartition du travail. 

Pour plus d’informations, voir [Vue d’ensemble des structures de répartition du travail](work-breakdown-structures.md).

### <a name="create-project-forecasts-and-budgets"></a>Créer des prévisions et des budgets de projet

Vous pouvez utiliser les prévisions si votre organisation a une perspective opérationnelle et se concentre sur les revenus et les coûts dérivés de transactions spécifiques. Cependant, si votre organisation se concentre davantage sur les montants financiers, vous pouvez utiliser la budgétisation. Chaque méthode a ses propres avantages. Pour plus d’informations, voir [Prévisions de projet et budgets](project-forecasts-budgets.md).

### <a name="create-projects"></a>Créer des projets

Vous pouvez créer six types de projets dans Finance. Chaque type de projet est configuré différemment pour la constatation des coûts et du produit. Le type de projet que vous choisissez dépend de l’objectif du projet. Le tableau suivant décrit l’utilisation type de chaque type de projet.
                                                                                                            
<table>
  <tr>
    <td>Type de projet</th>
    <td>Description</th>
  </tr>
  <tr>
    <td>Temps et matériel</td>
    <td>Dans les projets Temps et matériel, le client est facturé pour tous les coûts encourus sur un projet. Ces coûts comprennent les heures, les dépenses, les articles et les frais.</td>
  </tr>
  <tr>
    <td>Prix fixe</td>
    <td>Dans les projets à prix fixe, les factures se composent de transactions en compte. Un projet à prix fixe est facturé selon un calendrier de facturation basé sur un contrat de projet. Le produit d’un projet à prix fixe peut être calculé et validé tout au long du projet à l’aide de la méthode Pourcentage d’achèvement. Sinon, les revenus peuvent être calculés et comptabilisés à l’issue du projet, via la méthode du contrat exécuté. Les entreprises peuvent souvent tirer profit de l’utilisation de la valeur des travaux en cours pour calculer le degré d’exécution d’un projet ou d’un groupe de projets.</td>
  </tr>
  <tr>
    <td>Investissement</td>
    <td>Les projets d’investissement sont des projets qui ne produisent pas de bénéfices immédiats. Ils sont généralement utilisés pour des projets internes à long terme où les coûts doivent être capitalisés. Seuls les coûts associés aux articles, heures et dépenses peuvent être enregistrés pour un projet d’investissement. Les coûts d’un projet d’investissement sont suivis et contrôlés à l’aide de la fonctionnalité d’estimation. Les projets d’investissement peuvent être configurés avec une capitalisation maximale facultative. Au fil de l’avancement d’un projet d’investissement, vous enregistrez ses coûts sur des comptes TEC, où les coûts sont conservés jusqu’à l’achèvement du projet. Une fois le projet éliminé, vous transférez la valeur des travaux en cours vers une immobilisation, un compte général ou un nouveau projet. <br></br> <strong>REMARQUE :</strong> Les transactions sur les projets d’investissement ne sont pas affichées sur la page <strong>Valider les coûts<strong>, <strong>Provisionner le produit</strong> ou <strong>Créer des propositions de facture</strong>.</td>
  </tr>
  <tr>
    <td>Projet de coût</td>
    <td>Comme les projets d’investissement, les projets de coût permettent généralement de suivre les projets internes, et seuls les heures, les dépenses et les articles peuvent être enregistrés pour eux. Cependant, la durée des projets de coût est généralement plus courte que celle des projets d’investissement. De plus, contrairement aux projets d’investissement, les projets de coût ne peuvent pas être capitalisés dans les comptes de bilan. À la place, leurs transactions de projet sont enregistrées uniquement dans les comptes de résultat. <br></br> <strong>REMARQUE :</strong> Les transactions sur les projets Coût ne sont pas affichées sur la page <strong>Valider les coûts</strong>, <strong>Provisionner le produit</strong> ou <strong>Créer des propositions de facture</strong>. Comme les projets de coût permettent généralement de suivre les projets internes, ils ne doivent généralement pas être associés à un compte client. Cependant, si votre configuration nécessite que des demandes d’articles soient créées pour des commandes fournisseur, vous devez associer le projet de coût concerné à un client. Cette association est obligatoire, car les demandes d’articles sont gérées en tant que lignes commande client et le système exige qu’un client soit spécifié. Cependant, cette configuration n’entraîne pas la création automatique des demandes d’articles à partir d’une commande fournisseur. Pour les projets Coût, le paramètre <strong>Créer une demande d’article</strong> est ignoré. Si vous avez besoin d’une demande d’article dans un projet de coût, vous pouvez la créer manuellement, à condition qu’un client soit associé au projet.</td>
  </tr>
  <tr>
    <td>Interne</td>
    <td>Les projets internes permettent de suivre les coûts d’un projet interne pour votre organisation. Les projets internes peuvent fournir un outil de planification pour gérer la consommation des ressources. <br></br><strong>REMARQUE :<strong> Les transactions sur les projets internes ne sont pas affichées sur la page <strong>Provisionner le produit</strong> ou <strong>Créer des propositions de facture</strong>.</td>
  </tr>
  <tr>
    <td>Temps</td>
    <td>Les projets de temps permettent de suivre la durée associé à des activités non facturables et non productives, comme un projet de suivi des congés de maladie des collaborateurs. Les transactions des projets de temps ne sont pas validées dans la comptabilité. À la place, elles sont incluses dans les états sur l’utilisation des collaborateurs. Seules les transactions d’heures peuvent être enregistrées pour les projets de temps. Vous utilisez un journal d’heures ou une feuille de temps pour enregistrer ces heures dans le projet. Une fois les heures enregistrées, elles apparaissent comme des transactions de projet, mais n’ont pas de transactions de bons correspondants. <br></br><strong>REMARQUE :</strong> Les transactions sur les projets Temps ne sont pas affichées sur la page <strong>Valider les coûts</strong>, <strong>Provisionner le produit</strong> ou <strong>Créer des propositions de facture</strong>.</td>
  </tr>
</table>


### <a name="assign-workers-categories-and-resources"></a>Attribuer des employés, des catégories et des ressources

Vous pouvez planifier les ressources de travail en fonction des exigences et du calendrier d’un projet ou des compétences et de la disponibilité des employés. En utilisant les fonctionnalités de planification des ressources, vous pouvez déployer les employés de votre organisation de manière efficace et efficiente. Vous pouvez rapidement trouver les employés les plus qualifiés disponibles pour travailler sur votre projet. Vous pouvez également voir facilement comment ces employés pourraient être utilisés plus efficacement au cours du projet. 

Voici des moyens d’utiliser la fonctionnalité de planification des ressources :

-   Utilisez des informations sur les caractéristiques d’un employé, telles que l’éducation, les compétences, les certifications et l’expérience du projet, pour faire correspondre l’employé aux besoins d’un projet.
-   Utilisez les informations sur le calendrier et la disponibilité d’un employé pour faire correspondre le calendrier de l’employé au calendrier du projet.
-   Examinez la capacité de chaque collaborateur et déterminez comment cette capacité est utilisée. Par exemple, si un employé est sous-utilisé, il peut être affecté à un projet qui correspond à sa disponibilité et à ses attributs.
-   Vérifiez la disponibilité d’un employé pour vous assurer qu’il n’y a pas de conflit de calendrier avec les affectations de l’employé.
-   Consultez les informations sur l’utilisation des collaborateurs dans une vue récapitulative (par exemple, par service ou par collaborateur) ou dans une vue détaillée (par exemple, par collaborateur d’un service ou par détail hebdomadaire pour chaque collaborateur).
-   Modifiez les affectations de ressources pour différentes unités de temps, telles que le jour, la semaine ou le mois, afin d’optimiser l’utilisation des employés.

## <a name="execute-the-project"></a>Exécuter le projet
Pendant l’exécution du projet, les membres de l’équipe ou les responsables enregistrent les tâches et les dépenses engagées à l’aide de feuilles de temps, de notes de frais et d’autres documents commerciaux. Les chefs de projet disposent d’outils qui leur permettent de suivre la consommation des montants budgétés pour le projet. Les chefs de projet peuvent également commander, prélever ou acheter des matériaux pour des projets à l’aide de commandes achat et autres documents commerciaux. Les factures sont préparées et approuvées, afin que les clients puissent être facturés pour les travaux en cours. Enfin, le produit est reconnu au cours de ce processus pour affecter les données financières de l’organisation.

### <a name="manage-work-breakdown-structures"></a>Gérer des structures de répartition du travail

Une structure de répartition du travail décrit le travail qui sera accompli pour un projet. Une structure de répartition du travail est une hiérarchie de tâches. Elle représente non seulement le travail pour chaque tâche, mais également la taille, le coût et la durée de la tâche. 

Pour plus d’informations, voir [Vue d’ensemble des structures de répartition du travail](work-breakdown-structures.md).

### <a name="manage-project-forecasts-and-budgets"></a>Gérer des prévisions et des budgets de projet

Il existe deux façons de gérer et de contrôler vos projets : les prévisions de projet et les budgets de projet. Vous pouvez utiliser les prévisions si votre organisation a une perspective opérationnelle et se concentre sur les revenus et les coûts dérivés de transactions spécifiques. Cependant, si votre organisation se concentre davantage sur les montants financiers, vous pouvez utiliser la budgétisation.

Pour plus d’informations, voir [Prévisions de projet et budgets](project-forecasts-budgets.md).

### <a name="create-production-orders"></a>Créer des ordres de fabrication

Un ordre de fabrication lié au projet peut être lié à une commande client ou à une demande d’article à l’aide de la méthode de l’article fini ou de la méthode de l’article consommé. De plus, si l’ordre de fabrication a été créé manuellement, il n’y a aucun lien entre l’ordre de fabrication et la commande client ou la demande d’article (aucun lien vers la commande). Cependant, si l’ordre de fabrication a été créé automatiquement pour répondre à une commande client ou à une demande d’article, il existe un lien entre l’ordre de fabrication et la commande client ou la demande d’article (lien vers la commande). 

Selon les combinaisons de ces facteurs, utilisez l’une des méthodes suivantes :

- **Article fini/lien vers la commande** : associez le projet à une commande client ou à une demande d’article. Lorsque vous utilisez cette méthode, les coûts réels du projet sont validés lorsque la commande client est facturée ou lorsque le bon de livraison est mis à jour pour la demande d’articles. Le coût est validé en tant qu’article fini.
- **Article fini/Sans lien avec la commande** : les coûts réels ne peuvent pas être validés tant que le cycle de production d’un article n’a pas le statut **Terminé**. Le coût de l’article fini est validé comme une seule transaction.
- **Article consommé/lier à la commande** : lie le projet à une demande d’articles. En utilisant cette méthode, vous pouvez afficher les coûts réels du projet lorsque la production a un statut **Commencé** ou est signalée comme étant terminée. Les coûts sont validés sous la forme de plusieurs transactions d’articles de projet pour les matières premières et les heures consommées pour la production. Lorsque le bon de livraison est mis à jour pour la demande d’articles, aucun coût de projet n’est validé. Vous pouvez également définir le niveau dans la hiérarchie de nomenclature (BOM) auquel les projets de la production sont suivis.
- *<strong><em>Article consommé/Aucun lien vers la commande</em></strong>*  : associez le projet à une demande d’article. En utilisant cette méthode, vous pouvez afficher les coûts réels du projet lorsque la production est définie sur le statut <strong>Commencée</strong> ou est signalée comme terminée. Les coûts sont validés sous la forme de plusieurs transactions d’articles de projet pour les matières premières et les heures consommées pour la production. Vous pouvez également définir le niveau dans la hiérarchie de nomenclature auquel les projets de la production sont suivis.

### <a name="procure-products-and-services"></a>Acheter des produits et des services

L’achat et la vente d’articles sont des activités courantes dans de nombreuses activités ciblées sur des projets.

#### <a name="purchase-orders-for-projects"></a>Commandes achat pour les projets

Le but de la commande achat détermine quand la commande achat est consommée et, par conséquent, quand les articles sont facturés sur un projet.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Méthode</th>
<th>Objectif</th>
<th>Consommation d’articles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Créez une commande achat directement.</td>
<td>Achetez des articles auprès d’un fournisseur externe pour les consommer sur un projet. Vous pouvez créer la commande fournisseur des manières suivantes :
<ul>
<li>Depuis le projet lui-même. Dans ce cas, le projet est déjà défini pour la commande fournisseur.</li>
<li>En accédant à la commande fournisseur du projet. Vous devez sélectionner à la fois le fournisseur et le projet pour lesquels créer la commande fournisseur.</li>
</ul></td>
<td>Les articles sont consommés lorsque la facture fournisseur est mise à jour.</td>
</tr>
<tr class="even">
<td>Créez une commande fournisseur à partir d’une commande client.</td>
<td>Achetez des articles lorsque vous créez une commande client à partir d’un projet.</td>
<td>Les articles sont consommés lorsque la commande client est facturée au client.</td>
</tr>
<tr class="odd">
<td>Créez une commande fournisseur à partir d’une demande d’articles.</td>
<td>Achetez des articles lorsque vous créez une demande d’articles à partir d’un projet.</td>
<td>Les articles sont consommés lorsque le bon de livraison de l’exigence d’article est mis à jour.</td>
</tr>
</tbody>
</table>

#### <a name="sales-orders-for-projects"></a>Commandes client pour les projets

Dans Gestion de projets et comptabilité, vous pouvez enregistrer la consommation d’articles de plusieurs manières. Vous pouvez vendre des articles ou acheter des articles d’un projet ou réserver des articles pour un projet. 

Vous pouvez commander des articles de l’inventaire de l’entreprise pour la consommation sur un projet. Vous pouvez également acheter des articles auprès d’un fournisseur externe. Les éléments peuvent être utilisés sur tous les types de projets à l’exception des projets Temps. 

La façon dont vous commandez les articles dépend de l’endroit où vous les commandez :

-   Pour commander des articles à partir de l’inventaire de la société, vous devez saisir la commande comme une demande d’article. Si vous utilisez la page **Demandes d’article**, vous pouvez configurer la demande de sorte à recevoir les articles sous forme de livraisons partielles. Par conséquent, vous pouvez reporter la consommation d’une quantité d’articles jusqu’à ce que les articles soient nécessaires.
-   Pour commander des articles auprès d’un fournisseur externe, vous devez créer la commande en tant que commande d’achat sur la page **Commande achat**.

> [!NOTE] 
> Le bordereau de livraison d’une commande client liée à un projet ne peut pas être annulé si les articles ont déjà été marqués pour emballage. 

Le tableau suivant répertorie les méthodes de commande d’articles et décrit la manière dont ceux-ci sont consommés.

| Méthode            | Objectif                                                                                                                                                        | Consommation de transactions d’articles                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| Commande client       | Saisissez une transaction directement sur un projet Temps et matériel.                                                                                                   | Les transactions d’article sont consommées lorsque la facture client est validée.                                                                               |
| Feuille stock | Saisissez et gérez rapidement les enregistrements d’articles. Si, par exemple, vous souhaitez saisir une demande d’articles basée sur une liste imprimée, la feuille stock peut être appliquée. | Les transactions d’articles sont consommées lorsque la feuille est validée.                                                                                        |
| Demande d’articles  | Saisissez des articles qui ne vont pas être consommés immédiatement. Cette méthode vous permet de suivre le nombre d’articles qui ont été consommés dans un seul enregistrement de demande d’articles.    | Les transactions d’articles sont consommées lorsque le bon de livraison est mis à jour. En d’autres termes, la demande d’articles est créée lorsque le bon de livraison est validé. |
| Commandes fournisseur   | Saisissez les transactions dans l’un des trois emplacements, selon la méthode d’achat.                                                                              | Les transactions d’article sont consommées lorsque le bordereau de livraison est mis à jour ou lorsque le client ou le fournisseur est facturé.                                      |

### <a name="process-project-invoices"></a>Traiter les factures du projet

Le type de projet détermine la procédure de facturation à appliquer. Seuls les deux types de projets externes (Temps et matériel et Prix fixe) peuvent être facturés. Les projets Temps et matériel et Prix fixe sont toujours liés à un contrat de projet. 

Avant de créer une facture client pour un projet, vous pouvez créer une facture préliminaire ou une proposition de facture. Dans une proposition de facture, vous pouvez sélectionner des transactions de projet à inclure dans une facture de projet. Vous pouvez ensuite consulter les détails de la facture avant de valider la facture du projet et de l’envoyer au client ou à une autre source de financement. 


Pour plus d’informations sur le traitement des factures d’un projet, consultez [Facturation du projet](/dynamics365/finance/accounts-payable/project-invoicing).


### <a name="calculate-the-cost-to-complete-a-project"></a>Calculer le coût pour terminer un projet

Lorsque vous créez une estimation, vous pouvez choisir la méthode utilisée pour calculer le coût pour terminer le projet. Vous sélectionnez une méthode dans le champ **Méthode Coût pour terminer** sur la page **Créer une estimation**. La méthode que vous choisissez est appliquée séparément à chaque ligne de coût dans l’estimation des coûts. Alors qu’une ligne a un statut défini sur **Créé**, vous pouvez modifier la méthode qui lui est appliquée sur la page **Estimation des coûts**. 

Le tableau suivant décrit les méthodes de calcul du coût pour terminer un projet.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Méthode</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Coût total - réel</td>
<td>Les coûts estimés doivent être saisis manuellement. Une fois la colonne <strong>Coût total</strong> ou <strong>Quantité totale</strong> sur la page <strong>Estimation des coûts</strong> terminée, les coûts réels sont soustraits des totaux saisis par l’utilisateur. Le résultat correspond au coût pour terminer le projet. En règle générale, la progression des coûts n’est pas suivie en fonction, par exemple, du nombre de séjours à l’hôtel et de repas enregistrés dans chaque période. À la place. Le suivi est généralement basé sur une comparaison avec le nombre total d’heures estimées. Cette approche ne nécessite pas de modèle de prévision et le coût total ou la quantité totale peut être modifié manuellement. Lorsqu’une valeur est saisie dans la colonne <strong>Coût total</strong> ou <strong>Quantité totale</strong>, Finance compare cette valeur aux transactions réelles qui sont validées dans la période, puis diminue la valeur dans la colonne <strong>Quantité pour terminer</strong> ou <strong>Coût pour terminer</strong>.</td>
</tr>
<tr class="even">
<td>Budget total - réel</td>
<td>Les coûts réels sont comparés au modèle de prévision que vous sélectionnez pour déterminer le coût. Cette méthode utilise un modèle de budget total qui inclut les transactions prévues. Pour obtenir une vue plus précise du projet, vous pouvez ajuster le modèle de budget lorsque le projet est en cours. Si vous devez ajuster la prévision, suivez ce processus général :
<ol>
<li>Copiez les transactions de prévision dans un autre modèle de prévision.</li>
<li>Comparez les transactions prévues avec les transactions réelles.</li>
<li>Maintenez, diminuez ou augmentez les estimations pour la période suivante.</li>
</ol>
Finance ne diminue pas automatiquement les estimations prévues. Par conséquent, il est judicieux de conserver un modèle de prévision original sur le projet à prix fixe, afin d’établir une base de référence à des fins de comparaison lorsque le projet est terminé. 
<br></br> <strong>REMARQUE :</strong> Lorsque vous sélectionnez cette méthode, utilisez au moins deux modèles de prévision. Un modèle doit contenir la prévision d’origine. Pour l’autre modèle, vous devez copier les transactions de prévision d’un autre modèle. Cette méthode n’est valable que pour les projets Prix fixe et Investissement.</td>
</tr>
<tr class="odd">
<td>Budget restant</td>
<td>Cette méthode utilise un modèle de budget restant pour calculer le coût de réalisation du projet. Lorsque vous utilisez cette méthode, les coûts réels et les montants prévus dans le modèle de budget restant sont additionnés. Le résultat est un coût total. Avant d’utiliser cette méthode, un modèle de budget restant doit être configuré pour déduire les transactions en fonction des transactions réelles enregistrées dans le système. Sur la page <strong>Modèles de prévision</strong>, veillez à ce que les champs soient marqués dans le groupe <strong>Réduction automatique des prévisions</strong>. En règle générale, un budget restant est copié à partir d’un budget d’origine. Au fur et à mesure que les transactions sont saisies, les transactions sur le budget restant sont diminuées. Au fur et à mesure de l’avancement du projet, si vous déterminez que le budget restant doit être ajusté, vous imputez les transactions de prévision au budget restant. <br></br> <strong>REMARQUE :</strong> Cette méthode ne peut être appliquée que si un modèle de prévision est associé à l’estimation.</td>
</tr>
<tr class="even">
<td>Comme estimation précédente</td>
<td>La même méthode d’estimation utilisée lors de la période précédente est appliquée. Cette méthode nécessite un modèle de prévision si la période précédente nécessitait un modèle de prévision.</td>
</tr>
<tr class="odd">
<td>Définir le coût pour terminer à zéro</td>
<td>En règle générale, cette méthode est utilisée avant l’élimination du projet d’estimation. Cette méthode fait correspondre les estimations totales avec les transactions réelles qui ont été validées et efface la colonne <strong>Coût pour terminer</strong>. Le pourcentage d’achèvement qui en résulte est toujours égal à 100 %%. Le champ <strong>Prévision</strong> n’est pas sélectionné pour chaque ligne de coût que vous créez et l’estimation totale est copiée à partir de l’estimation de coût précédente. La consommation réelle pour la période estimée est déduite du coût de réalisation du projet. Cette méthode ne nécessite pas de modèle de prévision.</td>
</tr>
<tr class="even">
<td>À partir du modèle de coût</td>
<td>La méthode de coût de réalisation qui est configurée dans le modèle de coût associé au projet d’estimation sélectionné est appliquée.</td>
</tr>
</tbody>
</table>

## <a name="analyze-the-project"></a>Analyser le projet
À son niveau le plus élémentaire, un projet est utilisé pour regrouper les transactions qui enregistrent les coûts, puis les enregistrer en comptabilité. 

En général, ces transactions résultent de documents commerciaux, tels que des feuilles de temps, des notes de frais, des factures fournisseurs ou des mouvements de stock. Le cycle de vie d’un projet commence généralement par des estimations, des prévisions et des budgets qui permettent de planifier et d’anticiper les travaux et l’impact financier du projet. Lorsque vous analysez un projet, vous pouvez évaluer non seulement les transactions qui se sont produites au cours du projet, mais également l’exactitude de vos estimations et prévisions, les taux d’utilisation des membres de l’équipe de projet et le succès global du projet.

### <a name="analyze-cash-flow"></a>Analyser les flux de trésorerie

Utilisez la surveillance des flux de trésorerie pour examiner à la fois les flux de trésorerie prévus et les flux de trésorerie réels d’un projet. Vous pouvez consulter les trésoreries pendant qu’un projet est en cours, ou vous pouvez afficher les trésoreries d’un projet terminé. 

En surveillant les flux de trésorerie, vous pouvez évaluer un seul projet, utiliser les rapports pour afficher plusieurs projets et transférer les flux de trésorerie du projet vers les prévisions de flux de trésorerie en comptabilité.

#### <a name="cash-inflow-forecasting"></a>Prévision de flux entrant de trésorerie

En fonction de votre configuration, vous pouvez prévoir les flux entrants de trésorerie pour un projet sélectionné. Par exemple, si la date du projet est le 5 mars 2012 et si vous facturez le 31 mars 2012, voici comment prévoir la date d’échéance et la date de règlement des ventes prévue :

-   **Date du projet :** 5 mars 2012.
-   **Date de facture :** 31 mars 2012. Cette date est déterminée en fonction de la fréquence de facturation. Pour cet exemple, vous définissez la fréquence de facturation sur le mois en cours. Par conséquent, toutes les transactions validées au mois de mars sont facturées le dernier jour du mois.
-   **Date d’échéance :** 14 avril 2012. Cette date est déterminée en fonction des conditions de paiement qui ont été fixées pour le projet. Pour cet exemple, vous avez sélectionné des conditions de paiement de 14 jours. Par conséquent, 14 jours sont ajoutés à la date de facturation pour arriver à une date d’échéance du 14 avril 2012.
-   **Date prévue de règlement des ventes :** 27 avril 2012. Cette date est calculée en ajoutant le nombre de jours dans le champ **Jours tampons généraux** sur la page **Gestion de projets et comptabilité** au nombre de jours dans le champ **Jours tampons individuels** sur la page **Contrats de projet**, puis en ajoutant le total au nombre de jours dans le champ **Date d’échéance**. Pour cet exemple, vous avez saisi **3** dans le champ **Jours tampons généraux** et **10** dans le champ **Jours tampons individuels**. Par conséquent, 13 jours sont ajoutés à la date d’échéance pour arriver à une date de paiement des ventes attendu du 27 avril 2012.

Les jours tampons généraux peuvent remplacer les jours tampons individuels ou être ajoutés aux jours tampons individuels :

-   Pour utiliser les jours tampons généraux en remplacement des jours tampons individuels, saisissez le nombre moyen de jours entre la date d’échéance et la date de paiement réelle pour les clients.
-   Pour ajouter les jours tampons généraux aux jours tampons individuels, dans le champ **Jours tampons généraux**, saisissez votre estimation pour le nombre de jours entre le jour où le client envoie le paiement et le jour où votre organisation reçoit le paiement.

Mettez en place des jours tampons individuels dans le contrat du projet. Les jours sont calculés en fonction de la date d’échéance de la facture de vente et de l’expérience de votre organisation avec le modèle de paiement d’un client.

#### <a name="actual-cash-inflow"></a>Flux entrant de trésorerie réelle

Les flux entrants de trésorerie réelles ressemblent aux prévisions, mais vous pouvez commencer vos calculs à partir de la première date de facturation. Prenons un exemple :

-   **Date de facture :** 2 mars 2012.
-   **Date d’échéance :** 16 mars 2012. Les conditions de paiement sont fixées à 14 jours.
-   **Date prévue de règlement des ventes :** 29 mars 2012. Le calcul comprend trois jours tampons généraux et 10 jours tampons individuels.

#### <a name="cost-forecasting"></a>Prévisions des coûts

En fonction des jours définis, la date de règlement des coûts peut différer de la date du projet. Dans ce cas, la date de paiement des coûts est calculée en ajoutant le nombre de jours à partir de la date du projet au nombre de jours dans les conditions de paiement. 

Par exemple, la date du projet de la transaction est le 5 mars 2012 et les conditions de paiement suivantes sont définies :

-   **Heures :** Mois en cours (**M**)
-   **Dépenses :** 14 jours (**J14**)
-   **Articles :** 30 jours (**J30**)

En fonction de ces paramètres, voici la date de paiement des coûts pour chaque type de transaction :

-   **Heures :** 31 mars 2012, dernier jour du mois sélectionné.
-   **Dépenses :** 19 mars 2012, soit 14 jours après la date de la transaction.
-   **Articles :** 4 avril 2012, soit 30 jours après la date de la transaction.

> [!NOTE] 
> La date d’échéance de la commande d’achat est basée sur la transaction fournisseur lors de la création de la commande achat du projet. La date d’échéance n’est déterminée par aucun paramètre par défaut. 

La date de paiement des coûts n’est pas calculée les jours tampons. Une fois qu’un projet est terminé, lorsque tous les coûts et la facturation sont terminés, le coût et les ventes sont enregistrés dans les comptes de résultat. 

Lorsque toutes les factures de vente et de fournisseur sont terminées, vous pouvez afficher la relation entre les champs sur la page **Trésorerie** et les champs sur la page **Instructions du projet**.

:::row:::
    :::column:::
        #### <a name="cash-flow-page"></a>Page de trésorerie
        - Flux entrants de trésorerie 
        - Sorties de trésorerie
        - Trésorerie nette
    :::column-end:::
    :::column:::
        #### <a name="project-statements-page"></a>Page des instructions de projet
        - Revenus
        - Coût total
        - Marge brute
    :::column-end:::
:::row-end:::

### <a name="review-costs"></a>Examiner les coûts

Vous pouvez surveiller les coûts encourus par votre organisation pendant un projet sur la page **Contrôle des coûts**. En comparant les coûts budgétés d’origine pour le projet avec les coûts réels actuels et les coûts engagés, vous pouvez déterminer si le projet est sur la bonne voie, en dépassement de budget ou en deçà du budget. 

> [!NOTE] 
> Lorsque vous utilisez la page **Contrôle des coûts** pour afficher l’état actuel des coûts du projet, utilisez les modèles de prévision sélectionnés pour le budget d’origine et le budget restant. Si vous sélectionnez d’autres modèles de prévision lors du calcul des coûts, les résultats du calcul ne seront pas précis.

#### <a name="viewing-the-remaining-budgeted-amounts"></a>Affichage des montants budgétés restants

Si **Budget restant** est sélectionné comme méthode de contrôle des coûts sur la page **Paramètres de gestion de projets et de comptabilité**, la page **Contrôle des coûts** calcule les coûts qui n’ont pas été validés comme réels ou marqués comme engagés. Plus précisément, les montants sur l’onglet **Général** dans le volet inférieur de la page **Contrôle des coûts** sont calculés comme suit :

-   **Coûts réels** : le montant total qui a été dépensé sur le projet pour la ligne de coût sélectionnée. Le montant réel du coût est calculé sur la page **Mises à jour de la comptabilité**.
-   **Coût engagé** : le montant supplémentaire des dépenses que l’entité juridique s’est engagée à payer. Les montants des coûts engagés spécifiques sont calculés sur la page **Coûts engagés**.
-   **Budget restant** : le montant du montant initialement budgété qui est encore disponible pour la ligne de coût sélectionnée. Le montant budgété restant est calculé sur la page **Aperçu de la comptabilité**.
-   **Coût total** : la somme du coût réel, du coût engagé et des montants budgétaires restants.

Sur la page **Contrôle des coûts**, sur l’onglet **Écart**, vous pouvez afficher une comparaison du coût total prévu avec le budget d’origine. Cette comparaison montre toutes les différences entre ces montants. Vous pouvez donc voir où les données ne correspondent pas. Les montants d’écart sont calculés de la manière suivante :

-   **Budget d’origine** : le montant initialement budgété pour la ligne de coût sélectionnée. Le montant budgété d’origine est calculé sur la page **Aperçu de la comptabilité**.
-   **Coût total** : la somme du coût réel, du coût engagé et des montants budgétaires restants, comme indiqué sur l’onglet **Général**.
-   **Écart** : la différence entre le coût total et le budget initial.
-   **Écart basé sur la quantité** : la différence totale entre la prévision d’origine et la prévision totale. Cette différence peut être exprimée mathématiquement par (Quantité totale prévue) × (Prix moyen d’origine - Prix moyen total). Ce calcul s’applique uniquement aux heures du projet.
-   **Écart basé sur le prix** : la différence totale entre la prévision d’origine et la prévision totale. Cette différence peut être exprimée mathématiquement par (Prix de prévision d’origine) × (Quantité de prévision d’origine - Quantité de prévision totale). Ce calcul s’applique uniquement aux heures du projet.

#### <a name="viewing-the-total-budgeted-amounts"></a>Affichage des montants budgétés totaux

Si **Budget total** est sélectionné comme méthode de contrôle des coûts sur la page **Gestion de projets et comptabilité**, la page **Contrôle des coûts** calcule les coûts réels et les coûts totaux du projet pour vous aider à détecter toute différence entre les deux. Plus précisément, sur la page **Contrôle des coûts**, les montants dans les colonnes du volet inférieur de l’onglet **Général** sont calculés de la manière suivante :

-   **Coût total budgété** : le montant total budgété pour la ligne de coût sélectionnée.
-   **Coût réel** : le montant total des coûts engagés sur le projet à ce jour pour les lignes de coût sélectionnées.
-   **Coût engagé** : le montant total qui a été engagé sur le projet pour la ligne de coût sélectionnée.
-   **Écart** : la différence entre la somme des coûts réels et engagés et le coût total. L’écart indique si des coûts supplémentaires doivent être spécifiés pour le budget total.

Sur la page **Contrôle des coûts**, sur l’onglet **Écart**, vous pouvez voir la différence entre le budget total et le budget d’origine en consultant les champs suivants :

-   **Budget d’origine** : le montant initialement budgété pour la ligne de coût. Le budget d’origine est calculé sur la page **Aperçu de la comptabilité**.
-   **Coût total budgété** : le coût total initialement budgété pour la ligne de coût sélectionnée. Le coût total budgété est calculé sur la page **Aperçu de la comptabilité**.
-   **Écart** : l’écart pour la ligne de coût. Ce montant est calculé en soustrayant le coût total du budget d’origine.
-   **Écart basé sur la quantité** : la différence totale entre le budget d’origine et le budget total. Ce montant est calculé en soustrayant le total des heures budgétaires des heures budgétaires d’origine, puis en multipliant la différence par le prix de revient budgété d’origine. Cette différence peut être exprimée mathématiquement par (Prix de revient budgété d’origine) × (Heures budgétaires d’origine - Heures budgétaires totales). Ce calcul s’applique uniquement aux heures du projet.
-   **Écart basé sur le prix** : ce montant est calculé en soustrayant le total des heures budgétaires des heures budgétaires d’origine, puis en multipliant la différence par le nombre total d’heures consommées. Cette différence peut être exprimée mathématiquement par (Heures totales consommées) × (Heures budgétaires d’origine - Heures budgétaires totales). Ce calcul s’applique uniquement aux heures du projet.

### <a name="analyze-utilization"></a>Analyser l’utilisation

Le taux d’utilisation est le pourcentage de temps pendant lequel un employé effectue un travail facturable ou productif pendant une période de travail spécifique. Les heures facturables sont les heures de l’employé qui peuvent être facturées à un client spécifique. 

Le taux d’utilisation d’un employé est calculé en divisant le nombre d’heures facturables par le nombre d’heures de travail dans une période donnée. Par exemple, si un collaborateur dispose de 30 heures facturables dans une période et que le nombre d’heures de travail dans la même période est de 40, son taux d’utilisation est de 75 %%. 

Lorsque vous calculez le taux d’utilisation d’un collaborateur, vous pouvez calculer soit le taux facturable, soit le taux d’efficacité :

-   **Taux facturable** : la différence entre les heures facturables et les heures non facturables ou les heures normales.
-   **Taux d’efficacité** : la différence entre les heures productives et les heures non productives ou les heures normales. Les heures productives sont les heures que le collaborateur consacre à un projet spécifique. Les heures productives sont généralement facturées aux clients, sauf dans le cas de projets internes. Les heures non productives ne sont jamais facturées à un client.

Vous calculez les taux d’utilisation sur la page **Utilisation horaire**. Les calculs sont basés sur les préférences par défaut. Ces préférences précisent également comment les heures sont calculées en attribuant **Utilisation** ou **Charges** à chaque type de projet. Cela s’applique aux calculs de taux facturables et aux calculs de taux d’efficacité.

-   **Utilisation** : les heures déclarées pour le type de projet sélectionné sont toujours prises en compte pour une utilisation facturable ou efficace.
-   **Charge** : les heures déclarées pour le type de projet sélectionné sont toujours prises en compte pour une utilisation non facturable ou non efficace.
-   **Selon la propriété de la ligne** : les propriétés de ligne d’une transaction d’heure particulière déterminent si les heures sont prises en compte pour une utilisation facturable ou efficace.
-   **Non incluses** : les heures ne sont pas prises en compte dans le calcul de l’utilisation facturable ou de l’efficacité.

Sur la page **Utilisation horaire**, outre le pourcentage du taux d’utilisation global pour un employé ou un projet, vous pouvez afficher le nombre d’heures qui ont été utilisées pour les calculs du taux d’utilisation pour chacun des types d’heures suivants :

-   **Heures non incluses** : ces heures ne sont pas incluses dans le taux d’utilisation horaire.
-   **Heures incluses** : ces heures sont calculées en additionnant les heures d’utilisation et les heures de charge. Ces heures sont incluses dans le taux d’utilisation.
-   **Heures de charge** : si vous calculez un taux facturable, ces heures sont identiques aux heures non facturables. Si vous calculez un taux d’efficacité, ces heures sont identiques aux heures non productives.
-   **Heures d’utilisation** : si vous calculez un taux facturable, ces heures sont identiques aux heures facturables. Si vous calculez un taux d’efficacité, ces heures sont identiques aux heures productives.

Lorsque vous calculez le taux d’utilisation d’un collaborateur, vous pouvez utiliser les heures normales ou les heures incluses. Si vous utilisez des heures incluses, vous devez vous assurer que les collaborateurs enregistrent tout leur temps de travail pour les périodes de la feuille de temps, car le calcul est exprimé en pourcentage des heures saisies. Lorsque vous calculez le taux d’utilisation horaire pour un projet, un contrat de projet, un enregistrement client ou une catégorie, vous devez utiliser les heures incluses pour votre calcul.

### <a name="review-project-statements"></a>Vérifier les instructions de projet

Vous pouvez créer une instruction de projet pour afficher un instantané rapide de la progression d’un projet. Lorsque vous exécutez une instruction de projet, vous pouvez spécifier les critères utilisés pour calculer l’instruction en effectuant des sélections sur l’onglet **Général** sur la page **Instructions du projet**. Vous pouvez choisir d’inclure ou d’exclure les informations suivantes :

-   Types de projets
-   Types de transactions
-   Date du projet/Date comptable
-   Données

Une fois le relevé calculé, vous pouvez afficher les informations suivantes dans les différents onglets de la page **Relevés de projet** :

-   **Général** : informations générales sur la structure de base du résultat du projet.
-   **Résultats** : les informations sur le produit provisionné.
-   **TEC** : informations sur les soldes de compte des travaux en cours.
-   **Consommation** : les informations sur la consommation d’heures, d’articles, de dépenses et de transactions de paie.
-   **Facture** : informations sur les factures et la facturation en compte.
-   **Taux horaire** : taux horaires des heures imputées sur les comptes de produit et de coût.


[!INCLUDE[footer-include](../includes/footer-banner.md)]