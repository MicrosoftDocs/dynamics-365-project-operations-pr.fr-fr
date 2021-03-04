---
title: Contrats de projet
description: Cette rubrique offre des exemples des contrats de projet que vous pouvez créer pour différents types de projets et sources de financement et comment vous pouvez gérer les contrats et facturer les clients du projet.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075871"
---
# <a name="project-contracts"></a>Contrats de projet

[!include [banner](../includes/banner.md)]

Cet article offre des exemples des contrats de projet que vous pouvez créer pour différents types de projets et sources de financement et comment vous pouvez gérer les contrats et facturer les clients du projet.

Le type de projet que vous créez pour un contrat de projet détermine la méthode utilisée pour facturer les clients du projet. Vous pouvez modifier un contrat de projet et le projet associé, mais vous ne pouvez pas modifier le type de projet. 

En utilisant un contrat de projet, vous pouvez facturer un ou plusieurs projets en même temps. Le contrat de projet permet également de garantir une procédure de facturation cohérente pour chaque sous-projet d'une structure de projet. 

Chaque projet qui sera facturé doit être associé à un contrat de projet. Les paramètres d'un contrat de projet s'appliquent à tous les projets et sous-projets associés à ce contrat de projet. 

Un contrat de projet peut spécifier une ou plusieurs sources de financement. Par conséquent, vous pouvez répartir la facturation entre plusieurs bailleurs, définir des limites de financement afin que les sources de financement ne soient pas facturées plus qu’un montant spécifié et configurer des règles de financement pour la facturation des dépenses.

## <a name="funding-for-project-contracts"></a>Financement des contrats de projet
Certains contrats de projet précisent que plusieurs parties partagent la responsabilité de financer les coûts du projet. En voici quelques exemples :

-   Un gros client avec plusieurs divisions demande que le financement d’un projet soit réparti par division.
-   Votre entreprise partage les coûts d’un grand projet avec une organisation externe.
-   Un projet routier est cofinancé par deux municipalités.
-   Un projet de pont est financé par une subvention du gouvernement et une société privée.

Dans Dynamics 365 Finance, vous pouvez répartir la facturation d’une seule transaction ou d’un projet entier entre plusieurs clients, subventions ou organisations. 

Dans les projets qui ont plusieurs bailleurs, toutes les parties qui contribuent au financement d’un projet de financement avancé sont appelées sources de financement. Une fois qu’un client, une organisation ou une subvention est défini comme source de financement, il peut être affecté à une ou plusieurs règles de financement. Les règles de financement contiennent les critères qui déterminent la façon dont les frais sont répartis entre les différentes sources de financement d’un projet. 

Étant donné que les articles en stock, tels que ceux qui apparaissent sur les demandes d’achat et les bons de commande, ne peuvent pas être répartis, le montant du coût ne peut pas être réparti entre plusieurs sources de financement au moment de la distribution. Par conséquent, la valeur de la source de financement reste 0 (zéro) jusqu’à ce que la sortie de stock soit validée. Lorsque la sortie de stock est validée, le montant du coût est réparti selon les règles de répartition des comptes du projet.

Voici quelques étapes que vous pouvez suivre pour faciliter la répartition de la facturation entre plusieurs sources de financement :

-   Spécifiez que toutes les transactions saisies pour un projet utilisent la même devise de vente que le contrat de projet.
-   Définissez des limites de financement, de sorte qu’une source de financement ne soit pas facturée plus qu’un montant spécifié pour un projet.
-   Configurez les règles de financement et les limites de financement pour chaque employé, article, catégorie, groupe de catégories et type de transaction (ou pour tous les types de transaction).
-   Sélectionnez des dates de début et de fin facultatives pour définir la période pendant laquelle chaque règle de financement est valide.
-   Précisez le pourcentage dont chaque source de financement est responsable.
-   Spécifiez quelle source de financement est responsable des différences d’arrondi causées par les calculs d’allocation de financement.
-   Définissez des règles qui déterminent la manière dont les coûts du projet sont facturés aux clients externes et facturés aux organisations internes.
-   Enregistrez les transactions dans un compte de financement en attente jusqu’à ce qu’un financement supplémentaire puisse être obtenu, ou jusqu’à ce que vous décidiez de supporter les coûts en interne.

Pour déterminer le groupe de taxes à associer à une transaction, le projet est recherché pour une affectation de groupe de taxes. Si aucune affectation de groupe de taxe n’a été effectuée au niveau du projet, le contrat de projet est recherché.

### <a name="example-multiple-funding-sources-simple"></a>Exemple : plusieurs sources de financement (simple)

Le tableau suivant présente des scénarios de gestion de la répartition du financement entre plusieurs sources de financement. Ces scénarios reposent sur les hypothèses suivantes :

-   Les paramètres de priorité sont pris en compte dans l’allocation des fonds avant que d’autres critères de règle de financement ne soient appliqués.
-   Aucune plage de dates n’a été spécifiée pour définir la période d pendant laquelle la règle de financement est valide.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Scénario</strong></td>
<td><strong>Source de financement</strong></td>
<td><strong>Pourcentage d’allocation</strong></td>
<td><strong>Priorité d’allocation</strong></td>
</tr>
<tr class="even">
<td>Vous voulez affecter les coûts à une source de financement jusqu’à ce que ses fonds soient épuisés, allouer les coûts à une deuxième source de financement jusqu’à ce que ses fonds soient épuisés, et enfin allouer les coûts restants à une troisième source de financement.</td>
<td><ul>
<li>Source de financement 1</li>
<li>Source de financement 2</li>
<li>Source de financement 3</li>
</ul></td>
<td><ul>
<li>100%</li>
<li>100%</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
<li>3</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vous souhaitez affecter 75 % des coûts à une source de financement et 25 % à une deuxième source de financement. Lorsque l’une de ces sources de financement est épuisée, vous voulez payer les coûts restants à partir d’une troisième source de financement.</td>
<td><ul>
<li>Source de financement 1</li>
<li>Source de financement 2</li>
<li>Source de financement 3</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
<tr class="even">
<td>Vous souhaitez affecter 75 % des coûts à une source de financement et 25 % à une deuxième source de financement. Lorsque l’une de ces sources de financement est épuisée, vous voulez répartir les coûts restants entre une troisième source de financement et une quatrième source de financement.</td>
<td><ul>
<li>Source de financement 1</li>
<li>Source de financement 2</li>
<li>Source de financement 3</li>
<li>Source de financement 4</li>
</ul></td>
<td><ul>
<li>75 %</li>
<li>25 %</li>
<li>50 %</li>
<li>50 %</li>
</ul></td>
<td><ul>
<li>1</li>
<li>1</li>
<li>2</li>
<li>2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vous souhaitez affecter les premiers 25 % des coûts à une source de financement et le reste à une deuxième source de financement.</td>
<td><ul>
<li>Source de financement 1</li>
<li>Source de financement 2</li>
</ul></td>
<td><ul>
<li>25 %</li>
<li>100%</li>
</ul></td>
<td><ul>
<li>1</li>
<li>2</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a>Exemple : plusieurs sources de financement (complexe)

Vous disposez de trois sources de financement que vous souhaitez utiliser dans l’ordre suivant :

1.  Utilisez la source de financement 2 et la source de financement 3 de manière égale jusqu’à ce que la source de financement 2 soit épuisée.
2.  Continuez à utiliser la source de financement 3 jusqu’à ce qu’elle soit épuisée.
3.  Utilisez la source de financement 1 une fois la source de financement 3 épuisée.

Pour atteindre cet objectif, vous devez d’abord procéder comme suit :

-   Fixez des limites de financement pour la source de financement 2 et la source de financement 3, pour leurs montants respectifs.
-   Créez les règles de financement suivantes :
    -   Règle 1 (priorité 1) : attribuez 50 % des transactions à la source de financement 2 et 50 % à la source de financement 3.
    -   Règle 2 (priorité 2) : attribuez 100 % des transactions à la source de financement 3.
    -   Règle 3 (priorité 3) : attribuez 100 % des transactions à la source de financement 1.

Cette configuration fonctionne, car les transactions sont vérifiées par rapport aux règles et aux limites pour déterminer si l’une d’entre elles s’applique à la transaction. Si aucune règle ou limite spécifique ne s’applique à la transaction, la règle Toutes les transactions s’applique. La règle Toutes les transactions correspond à toutes les transactions. 

Si une règle correspond à une transaction, le pourcentage qui a été alloué dans cette règle est appliqué en premier, mais uniquement une fois que les correspondances ont été vérifiées par rapport aux limites définies. Si une limite a été atteinte et si les fonds d’une source de financement sont épuisés, la règle de financement associée à la limite de financement n’est pas respectée et le programme vérifie la règle suivante qui s’applique. 

Dans certains cas, seule une partie d’une transaction peut être allouée selon une règle. Cela peut se produire, car une limite est atteinte lorsque la transaction est allouée. Dans ce cas, seul un certain montant est alloué selon cette règle, par exemple 50 pour cent à chaque source de financement. C’est le cas de la règle 1, qui est décrite plus haut dans cette section. Le reste est alloué selon la règle suivante de la séquence. 

Le tableau suivant examine ce scénario en détail.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Focus</strong></td>
<td><strong>Détails</strong></td>
</tr>
<tr class="even">
<td>Règles de financement</td>
<td><ul>
<li>Règle 1 (priorité 1) : toutes les transactions. Allouez la source de financement 2 à 50 % et la source de financement 3 à 50 %.</li>
<li>Règle 2 (priorité 2) : toutes les transactions. Allouez la source de financement 3 à 100 %.</li>
<li>Règle 3 (priorité 2) : toutes les transactions. Allouez la source de financement 1 à 100 %.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Limites de financement</td>
<td><ul>
<li>Limite de la source de financement 1 = 10 000</li>
<li>Limite de la source de financement 2 = 500</li>
<li>Limite de la source de financement 3 = 750</li>
</ul></td>
</tr>
<tr class="even">
<td>Transaction 1</td>
<td><strong>Montant de la transaction :</strong>100<strong>Financement :</strong> la transaction est payée selon la règle 1 uniquement, car la transaction est entièrement payée après l’application de la règle 1. La transaction est financée à parts égales entre la source de financement 2 et la source de financement 3.
<ul>
<li>Source de financement 2 : 50</li>
<li>Source de financement 3 : 50</li>
</ul></td>
</tr>
<tr class="odd">
<td>Transaction 2</td>
<td><strong>Montant de la transaction :</strong>5 000<strong>Financement :</strong> la transaction est payée selon les trois règles. <strong>Règle 1</strong>
<ul>
<li>Source de financement 2 : 450</li>
<li>Source de financement 3 : 450</li>
</ul>
<strong>Règle 2</strong>
<ul>
<li>Source de financement 3 : 250 (= 750 - 50 - 450)</li>
</ul>
<strong>Règle 3</strong>
<ul>
<li>Source de financement 1 : 3 850 (= 5 000 - 450 - 450 - 250)</li>
</ul></td>
</tr>
<tr class="even">
<td>Total des fonds distribués pour chaque source de financement</td>
<td><ul>
<li>Source de financement 1 : 3 850</li>
<li>Source de financement 2 : 500</li>
<li>Source de financement 3 : 750</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a>Règles de facturation
Lorsque vous négociez un contrat de projet avec un client, vous définissez comment et quand vous pouvez facturer le client pour le travail sur un projet. Après avoir configuré le contrat de projet et le projet, vous pouvez définir des règles de facturation pour le projet. Les règles de facturation sont basées sur les conditions du projet qui sont spécifiées dans le contrat de projet. Les règles de facturation que vous pouvez créer dépendent des conditions du contrat de projet et du type de projet, tel que Temps et matériel ou Prix fixe, que vous associez à la règle de facturation. Vous pouvez créer plusieurs règles de facturation pour un contrat de projet. Vous pouvez également affecter une règle de facturation à plusieurs projets associés au même contrat de projet et ayant des conditions de facturation similaires. 

Vous pouvez configurer les types de règles de facturation suivants :

-   **Unité de livraison**  : facturer un client lorsque vous complétez une unité de livraison. Vous définissez les unités de livraison dans le contrat.
-   **Progression**  : facturer un client lorsque vous terminez un pourcentage spécifié du projet. Vous pouvez configurer une règle de facturation pour calculer automatiquement le pourcentage de travail achevé, ou vous pouvez calculer manuellement le pourcentage de travail achevé et le montant à facturer au client.
-   **Jalon**  : facturer un client pour le montant total d’un jalon de projet lorsque le jalon est atteint.
-   **Frais**  : facturez un client pour vos services plus des frais de gestion, qui correspondent généralement à un pourcentage du coût des services.
-   **Temps et matériel**  : facturez un client pour la valeur du temps et des matériaux utilisés sur un projet.

Pour tous les types de règles de facturation, vous pouvez spécifier un pourcentage de rétention qui est déduit des factures client jusqu’à ce qu’un projet atteigne une étape convenue. Le pourcentage de rétention de paiement est spécifié dans le contrat de projet. Le montant est calculé en fonction de la valeur totale des lignes d’une facture client et soustrait de celle-ci. 

Pour les règles de facturation **Temps et matériel** et **Progression** , vous pouvez attribuer des catégories facturables. Les catégories facturables indiquent les transactions à inclure dans les factures des clients. 

Lorsque vous êtes prêt à facturer le client, le montant à facturer pour le projet est calculé en fonction des règles de facturation et une proposition de facture de projet est générée. 

Les sections suivantes fournissent des exemples qui montrent comment configurer et gérer les règles de facturation pour un projet.

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a>Exemple : créer une règle de facturation basée sur le nombre d’unités livrées

Votre organisation conclut un accord pour fournir un total de cinq sessions de formation aux employés d’un client au coût de 10 000 par session de formation. Vous facturez le client après chaque session de formation. 

Lorsque vous configurez les règles de facturation pour le contrat, vous utilisez les valeurs suivantes :

-   L’unité de livraison est une session de formation.
-   Le prix unitaire est de 10 000 par session de formation.
-   Le nombre total d’unités est de cinq sessions de formation.

Lorsque vous avez terminé une session de formation, vous pouvez créer une facture de 10 000, pour la première unité livrée, et envoyer la facture au client.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a>Exemple : créer une règle de facturation basée sur un pourcentage spécifié d’achèvement du projet (calcul manuel)

Votre organisation, une société de conseil en logiciels, conclut un accord avec un client pour développer une partie d’un produit que le client développe. Votre organisation s’engage à livrer le code logiciel sur une période de six mois. Le client s’engage à payer à votre organisation un total de 100 000 pour les travaux. Vous créez une règle de facturation pour facturer le client en fonction du pourcentage de travail achevé sur le projet, comme spécifié dans le contrat.

-   À la fin du premier mois, vous rencontrez le client pour déterminer le pourcentage de travail réalisé. Une fois que vous et le client avez examiné le projet, vous décidez que le projet est achevé à 15 %.
-   Vous créez une facture pour 15 000 (15 pour cent de 100 000) et l’envoyez au client.

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a>Exemple : créer une règle de facturation basée sur un pourcentage spécifié d’achèvement du projet (calcul automatique)

Votre organisation, une entreprise de développement de logiciels, accepte de développer un progiciel de comptabilité de paie pour un client pour 30 000. Le client s’engage à payer à votre organisation selon le pourcentage de travail exécuté. Vous estimez que les coûts du projet sont de 20 000. Le contrat de projet spécifie les catégories de travail que vous utilisez dans le processus de facturation. Vous configurez des règles de facturation qui calculent automatiquement les montants de facture pour le pourcentage de travail achevé pour chaque catégorie. Vous définissez un budget pour chaque catégorie :

-   **Développement**  : coût de 15 000 et revenu de 20 000
-   **Installation**  : coût de 5 000 et revenu de 10 000

Lorsque vous créez une facture client pour la première fois, le montant de la facture est automatiquement calculé en fonction des informations suivantes :

-   Après un mois, l’employé du projet soumet une feuille de temps pour le projet. Le coût des heures d’employé est de 5 000 heures pour le développement et 1 000 pour l’installation. Les travaux de développement sont terminés à 33 % (5 000 coûts réels / 15 000 coûts budgétaires) et les travaux d’installation sont terminés à 20 % (1 000 coûts réels / 5 000 coûts budgétaires).
-   Le montant de la facture de 8 667 est calculé automatiquement (33 % de 20 000 + 20 % de 10 000).
-   Vous créez une facture pour 8 667 et l’envoyez au client.

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a>Exemple : créer une règle de facturation basée sur des jalon convenus

Votre organisation, une société de conseil en gestion, accepte de mener une étude de marché pour un produit de consommation que le client envisage de vendre. Le client s’engage à utiliser vos services pendant une période de trois mois, à compter du mois de mars, et s’engage à payer 50 000 à votre organisation. Le projet comporte trois étapes :

-   Jalon 1 : recueillir des données sur les consommateurs - 31 mars
-   Jalon 2 : analyser les données des consommateurs - 30 avril
-   Jalon 3 : présenter une proposition de viabilité du produit - 31 mai

Le client accepte de payer à votre organisation 10 000 pour le premier jalon, 20 000 pour le deuxième jalon et 20 000 pour le troisième jalon. 

Lorsque vous configurez le contrat de projet, vous acceptez de facturer le client en fonction du jalon qui a été atteint. La configuration de la règle de facturation comprend les étapes suivantes :

-   Définissez les jalons du projet.
-   Définissez le montant à facturer au client lorsque chaque jalon est atteint.

Lorsque le premier jalon est atteint le 31 mars, vous le marquer comme atteint, puis créez une facture pour 10 000 et l’envoyez au client. Vous ne pouvez pas créer une facture pour un jalon tant que vous ne l’avez pas marqué comme atteint.

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a>Exemple : Créer une règle de facturation basée sur des services plus des frais de gestion

Votre organisation, une société de conseil en gestion, accepte de mener des études de marché pour évaluer la viabilité d’un produit que le client, une entreprise de vente au détail, développe. Les termes de l’accord précisent que vous fournirez les services de vos trois principaux consultants en gestion, qui mèneront la recherche en fonction du temps et des matériaux. Le client accepte de payer 100 par heure, plus des frais de gestion de 10 % pour les heures de consultation qui sont facturées au projet. 

Lorsque vous configurez le contrat de projet, créez une règle de facturation pour ajouter des frais de gestion de 10 % aux heures de consultation facturées au projet. 

Lorsque vous créez une facture pour le client, le client reçoit des frais de gestion de 10 % plus le coût des heures de consultation. Par exemple, si les trois consultants ont travaillé un total de 200 heures sur le projet, une facture de 22 000 est créée sur la base du calcul suivant :

-   200 heures à 100 par heure = 20 000
-   10 pour cent de frais de gestion = 2000
-   Total du montant de la facture = 22 000

Si les frais sont taxables pour un client et si vous sélectionnez un groupe de taxe de vente dans le contrat de projet, le groupe de taxe de vente est automatiquement saisi dans une règle de facturation pour les frais.

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a>Exemple : Créer une règle de facturation pour la valeur du temps et des matériaux

Votre organisation, une société de conseil en logiciels, accepte de fournir cinq consultants techniques pour travailler sur un projet de développement logiciel pour un client pendant les six prochains mois. Le client s’engage à payer 150 pour chaque heure de consultation, plus le coût des fournitures de bureau. Votre organisation envoie une facture au client à la fin de chaque mois. 

Lorsque vous configurez le contrat de projet, vous acceptez de facturer le client chaque mois pour le temps et les matériaux du projet. Vous créez une règle de facturation qui comprend les informations suivantes :

-   La durée du contrat est de six mois.
-   Le temps de consultation est calculé à raison de 150 par heure.
-   Les fournitures de bureau sont facturées au prix coûtant et le coût total du projet ne doit pas dépasser 10 000.
-   Vous créez une facture client à la fin de chaque mois calendaire pendant le projet.

Au cours du premier mois, un total de 800 heures est enregistré par les consultants sur le projet. Le coût des fournitures de bureau imputées au projet est de 2 000. Par conséquent, à la fin du mois, vous créez une facture pour 122 000, qui est calculée comme 800 heures à 150 par heure, plus 2 000 pour les fournitures de bureau.





[!INCLUDE[footer-include](../includes/footer-banner.md)]