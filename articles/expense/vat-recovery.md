---
title: Récupération de la TVA dans Gestion des dépenses
description: Cette rubrique explique comment recevoir des remboursements sur les transactions de taxe sur la valeur ajoutée (TVA) éligibles.
author: suvaidya
ms.date: 10/10/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7c961763d3d670117c5a576db485ebcfdcf9ec9f
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581143"
---
# <a name="vat-recovery-in-expense-management"></a>Récupération de la TVA dans Gestion des dépenses

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Pour recevoir des remboursements sur les transactions de taxe sur la valeur ajoutée (TVA) éligibles, une entreprise ou une organisation doit identifier, collecter, vérifier et soumettre des informations exactes. Ce processus comprend plusieurs tâches et, selon la taille de votre entreprise, peut inclure plusieurs employés ou rôles.

Pour récupérer la TVA dans le module **Gestion des dépenses**, les conditions préalables suivantes doivent être remplies :

- Les codes de taxe doivent être créés pour les pays/régions affectés aux catégories de dépenses.
- Un groupe taxe doit être créé pour chaque code taxe.
- Un code de groupe de taxe doit être créé pour chaque groupe de taxe.

Une fois les conditions préalables remplies, les étapes suivantes doivent être effectuées pour demander le remboursement des transactions de TVA.

1. Dans une note de frais, saisissez les informations fiscales relatives aux transactions par carte de crédit pour identifier les remboursements de TVA éligibles.
2. Vérifiez que toutes les informations fiscales sont complètes, puis validez la note de frais.
3. Traitez les dépenses éligibles à la récupération internationale de la TVA.
4. Envoyez les données de récupération de TVA au fournisseur tiers pour déposer des déclarations de récupération internationales.
5. Traiter les dépenses pour la récupération de la TVA nationale.

Les sections suivantes fournissent des exemples qui montrent comment les employés de Contoso effectuent chaque étape.

## <a name="enter-tax-information-about-credit-card-transactions-to-identify-eligible-vat-refunds"></a>Saisir les informations fiscales relatives aux transactions par carte de crédit pour identifier les remboursements de TVA éligibles

Geneviève, une représentante commerciale de Contoso basée aux États-Unis, est récemment revenue d’un voyage d’affaires au Royaume-Uni. Pendant le voyage, Geneviève a engagé des dépenses personnelles de carte de crédit pour les repas. Geneviève doit maintenant créer une note de frais pour rapprocher les dépenses.

Lorsque Geneviève entre des informations sur la note de frais, elle sélectionne **Royaume-Uni** dans le champ **Pays/région** sur la page **Modifier la note de frais**. La liste des groupes de taxe est ensuite filtrée afin qu’elle n’affiche que les groupes qui s’appliquent au Royaume-Uni. Geneviève sélectionne le groupe de taxe **Royaume-Uni 001**, puis sélectionne le groupe de taxe d’article **Repas**. Ensuite, Geneviève ajoute une nouvelle transaction d’hébergement. Comme il n’y a qu’un seul groupe de taxe et un seul groupe de taxe d’article pour l’hébergement au Royaume-Uni, ces informations sont automatiquement renseignées sur la note de frais de Geneviève.

Selon la stratégie Contoso, toutes les dépenses doivent avoir un reçu correspondant. Par conséquent, lorsque Geneviève enregistre la note de frais, elle reçoit un message indiquant qu’elle doit joindre un reçu pour chaque transaction qu’elle a inscrite sur sa note de frais. Geneviève vérifie qu’elle a joint une image numérique de chaque reçu de transaction à son rapport de dépenses, puis soumet son rapport pour approbation. Elle envoie ensuite les reçus papier à l’équipe de traitement du back-office. Cette équipe enverra les données de récupération de TVA au fournisseur tiers qui dépose les déclarations internationales de récupération de TVA pour Contoso.

## <a name="verify-tax-information-and-post-an-expense-report"></a>Vérifier les informations fiscales et publier une note de frais

Avant avril, la coordinatrice de la Comptabilité fournisseur de Contoso peut publier une note de frais, elle doit saisir toutes les informations fiscales qui lui sont manquantes. Elle ouvre la page **Détails de la note de frais** et voit la note de frais approuvée de Geneviève. April ouvre alors la note de frais pour afficher les détails des transactions. Elle constate que Geneviève n’a pas saisi de groupe de taxe d’article pour l’une des transactions. Étant donné que ces informations ne sont pas fournies, April ne peut pas publier la note de frais. Par conséquent, elle regarde la page **Configurations fiscales** dans Gestion des dépenses et trouve le groupe de taxe d’article approprié pour le pays/la région et le type de transaction. April peut désormais publier la note de frais dans la comptabilité.

Lorsque April publie la note de frais, un élément de travail de TVA récupérable est créé. Cet élément de travail est affecté à un membre de l’équipe de traitement du back-office. April reçoit un message confirmant que la validation a réussi. Ce message répertorie également le nombre de transactions de TVA identifiées pour la récupération.

## <a name="process-expenses-that-are-eligible-for-international-vat-recovery"></a>Traiter les dépenses éligibles à la récupération internationale de la TVA

Arnie, membre de l’équipe de traitement back-office de Contoso, est chargé de vérifier que toutes les informations requises pour la récupération de la TVA sont incluses dans les notes de frais. Il ouvre la page **Récupération de la taxe sur les dépenses** et sélectionne la note de frais que Geneviève a soumise. Arnie vérifie ensuite que tous les reçus requis sont joints et que le groupe de taxe et les codes de taxe d’article corrects ont été saisis.

Lorsque Arnie reçoit les reçus papier de Geneviève, il les vérifie par rapport aux reçus numériques, puis change le statut de la note de frais en **Prêt pour la récupération**.

## <a name="send-vat-recovery-data-to-the-third-party-vendor"></a>Envoyer les données de récupération de TVA au fournisseur tiers

Lorsque Arnie est prêt à envoyer les données des notes de frais au fournisseur tiers qui déposera les déclarations de récupération de TVA, il ouvre la page **Récupération de la taxe sur les dépenses**. Il filtre la page pour qu’elle n’affiche que les notes de frais marquées comme **Prêt pour la récupération**. Arnie sélectionne ensuite **Fichier** &gt; **Exporter vers Excel**. Les informations de TVA des notes de frais sont exportées vers une feuille de calcul Microsoft Excel. Arnie soumet cette feuille de calcul au fournisseur tiers et inclut un message indiquant que les reçus papier ont été envoyés par courrier.

## <a name="process-expenses-for-domestic-vat-recovery"></a>Traiter les dépenses pour la récupération de la TVA nationale

Arnie doit vérifier que les transactions des notes de frais sont éligibles à la récupération de la TVA et que les reçus numériques sont joints aux notes. Pour commencer à traiter les dépenses éligibles pour le recouvrement national, Arnie ouvre la page **Récupération de la taxe sur les dépenses** et sélectionne la note de frais à vérifier. Il vérifie que les reçus sont au nom de l’entreprise et non de l’employé. (Pour la récupération de la TVA, les reçus doivent être au nom de la société.) Arnie vérifie ensuite que tous les reçus requis sont joints et que le groupe de taxe et les codes de taxe d’article corrects ont été saisis.

Lorsque Arnie reçoit les reçus papier, il change le statut de la note de frais en **Prêt pour la récupération**. Il peut ensuite déposer la déclaration auprès de l’administration fiscale appropriée. Dans ce cas, l’autorité fiscale compétente aux États-Unis est l’IRS (Internal Revenue Service).


[!INCLUDE[footer-include](../includes/footer-banner.md)]