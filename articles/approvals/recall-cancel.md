---
title: Rappel des entrées précédemment approuvées
description: Cet article explique comment un membre de l’équipe de projet peut demander le rappel des enregistrements de temps, de dépense et d’utilisation de matériaux précédemment soumis et approuvés, et comment un chef de projet peut approuver ou rejeter les demandes de rappel.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930361"
---
# <a name="recall-previously-approved-entries"></a>Rappel des entrées précédemment approuvées

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Un membre de l’équipe du projet qui envoie une entrée de temps, de dépense ou d’utilisation de matériel peut rappeler cette entrée après qu’elle a été approuvée. Le processus de rappel a deux étapes principales :

1. Un expéditeur demande un rappel.
2. Un approbateur approuve la demande de rappel.

## <a name="request-a-recall"></a>Demander un rappel

Procédez comme suit pour demander un rappel d’une entrée de temps, de dépense ou d’utilisation de matériel approuvée.

1. Procédez comme suit, selon le type d’entrée que vous souhaitez rappeler :

    - Pour les entrées de temps, accédez à **Projets** \> **Mon travail** \> **Entrée de temps** et sélectionnez toutes les entrées de temps pour une combinaison spécifique d’un projet et d’une tâche. Sinon, dans la grille, sélectionnez des cellules individuelles pour le temps à une date spécifique pour un projet spécifique.
    - Pour les entrées de dépense, accédez à **Projets** \> **Mon travail** \> **Dépenses**, et sélectionnez la ligne de l’entrée de dépense afin de faire le rappel.
    - Pour les entrées d’utilisation de matériel, accédez à **Projets** \> **Mon travail** \> **Journal d’utilisation des matériaux**, et sélectionnez la ligne de l’entrée de l’utilisation des matériaux afin de faire le rappel.

2. Cliquez sur **Rappeler**. Une boîte de dialogue de confirmation s’affiche. Si les entrées de temps, de dépense ou d’utilisation de matériel sélectionnées ont été déjà approuvées, vous êtes invité à indiquer une raison pour le rappel.
3. Entrez une raison pour le rappel, puis sélectionnez **OK** pour confirmer l’opération. Le système envoie à la personne ayant approuvé les entrées une demande d’approbation du rappel.

> [!IMPORTANT]
> Vous ne pouvez pas créer de demande de rappel pour une entrée de temps, de dépense et d’utilisation de matériel précédemment approuvée qui a déjà été facturée au client. Si vous essayez, vous recevez un message stipulant que l’entrée de temps, de dépense ou d’utilisation de matériel ne peut pas être rappelée, car elle a déjà été facturée. Dans ce cas, vous pouvez demander un rappel de l’entrée uniquement si une facture corrective est utilisée pour émettre un crédit ou un remboursement complet au client sur la facture d’origine.

## <a name="approve-or-reject-a-recall-request"></a>Approuver ou rejeter une demande de rappel

Procédez comme suit pour approuver ou rejeter une demande de rappel.

1. Accédez à **Projets** \> **Mes tâches** \> **Approbations**.
2. Dans la page de liste **Approbations**, modifiez la vue avec **Rappeler les demandes d’approbation**. Une liste des demandes de rappel envoyées s’affiche.
3. Sélectionnez une ou plusieurs entrées, puis sélectionnez **Approuver** ou **Rejeter**.
4. Si vous avez sélectionné **Approuver**, un message d’avertissement s’affiche qui explique l’impact de l’approbation. Sélectionnez **OK** pour confirmer l’opération. La demande de rappel est approuvée.

    -ou-

    Si vous avez sélectionné **Rejeter**, la demande de rappel est rejetée.

> [!IMPORTANT]
> Lorsqu’un rappel est approuvé, tout comme lorsqu’un rappel est demandé, le système vérifie l’activité de facturation sur les entrées de temps, de dépense ou d’utilisation de matériel. Si une entrée a déjà été facturée, ou si elle figure sur un brouillon de facture, l’approbateur reçoit un message d’erreur qui déclare que le temps ou les dépense ne peuvent pas être approuvé pour rappel, car ils ont déjà été facturés. Dans ce cas, l’approbateur peut approuver le rappel uniquement si une facture corrective est utilisée pour émettre un crédit ou un remboursement complet au client sur la facture d’origine.

## <a name="impact-of-a-recall-request"></a>Impact d’une demande de rappel

Lorsqu’une approbation est rappelée, il existe un impact opérationnel et un impact financier.

### <a name="operational-impact"></a>Impact opérationnel

Si une demande de rappel est approuvée, l’enregistrement de l’approbation est marqué comme **Rejeté**. Le statut de l’entrée passe à **Renvoyé** ou **Rejeté**, selon qu’il s’agit d’une entrée de temps ou d’une entrée de dépense ou d’utilisation de matériel.

Le membre de l’équipe du projet peut afficher les entrées, les modifier, puis renvoyer les entrées, ou supprimer des entrées entièrement.

Si une demande de rappel est rejetée, le statut de l’entrée reste **Approuvé**, et l’entrée ne peut pas être modifiée par le membre de l’équipe du projet ou l’approbateur du projet.

### <a name="financial-impact"></a>Impact financier

Si une demande de rappel est approuvée, les chiffres réels correspondants au coût et aux ventes sont mis à jour de la façon suivante :

- Le champ **Statut d’ajustement** est mis à jour sur **Ajusté**.
- Le champ **Statut de facturation** est mis à jour sur **Annulé**.

Ensuite, des entrées de contrepassation sont créées dans la table Chiffres réels. Pour créer des entrées de contrepassation, le système copie sur les valeurs de champ les chiffres réels initiaux. Les seules valeurs qui ne sont pas copiées sont les valeurs de quantité. Ces valeurs sont contrepassées à la place. Les chiffres réels contrepassés sont définis pour les chiffres réels **Coût** et **Ventes non facturées**. Le champ **Statut de l’ajustement** sur les chiffres réels contrepassés est défini sur **Non ajustable**, et le champ **Statut de facturation** est défini sur **Annulé**. En raison de ces modifications, la dépense enregistrée et l’arriéré de revenu du projet ne compteront plus dans les montants que ces chiffres réels représentent.

Si une demande de rappel est rejetée, il n’y a aucun impact financier sur le projet.

## <a name="changes-to-time-entry-records"></a>Modifications apportées aux enregistrements d’entrées de temps

L’illustration suivante montre les modifications qui se produisent pour des entrées de temps approuvées et les enregistrements d’approbation correspondants lorsqu’elles sont rappelées.

![Transitions d’état d’entrée de temps.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Modifications apportées aux enregistrements d’entrées de dépense et d’utilisation de matériel

L’illustration suivante montre les modifications qui se produisent pour des entrées de dépense et d’utilisation de matériel approuvées et les enregistrements d’approbation correspondants lorsqu’elles sont rappelées.

![Transitions d’état d’entrée de dépense.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
