---
title: Rappeler les entrées de temps ou de dépenses approuvées
description: Cette rubrique explique comment rappeler une transaction de temps et de dépenses approuvée précédemment.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e90b84bbfcd007e97e96b294144f058ac73746e3d358437692f0a8e6e92b8de3
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998323"
---
# <a name="recall-approved-time-or-expense-entries"></a>Rappeler les entrées de temps ou de dépenses approuvées

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Un membre de l’équipe du projet ou une autre personne qui envoie une entrée de temps ou de dépenses peut rappeler cette entrée de temps ou de dépenses après qu’elle a été approuvée. Le processus de rappel d’une entrée de temps ou de dépenses approuvée se fait en deux étapes :

1. Un expéditeur demande un rappel.
2. Un approbateur approuve le rappel.

## <a name="request-a-recall"></a>Demander un rappel

Procédez comme suit pour demander un rappel d’une entrée de temps ou de dépenses approuvée.

1. Pour les entrées de temps, accédez à **Projets** \> **Mes tâches** \> **Entrée de temps**.

    -ou-

    Pour les entrées de dépenses, accédez à **Projets** \> **Mes tâches** \> **Dépenses**.

2. Pour les entrées de temps, sélectionnez toutes les entrées de temps pour une combinaison spécifique d’un projet et d’une tâche. Sinon, dans la grille, sélectionnez des cellules individuelles pour le temps à une date spécifique pour un projet spécifique.

    -ou-

    Pour les entrées de dépenses, sélectionnez la ligne de l’entrée de dépenses afin de faire le rappel.

3. Sélectionnez **Rappeler**. Une boîte de dialogue de confirmation s’affiche. Si les entrées de temps et de dépenses sélectionnées ont été déjà approuvées, vous êtes invité à indiquer une raison pour le rappel.
4. Entrez une raison pour le rappel, puis sélectionnez **OK** pour confirmer l’opération. Le système envoie à la personne ayant approuvé les entrées une demande d’approbation du rappel.

> [!NOTE]
> Bien que des entrées de temps et de dépenses approuvées puissent être rappelées, si une entrée de temps ou de dépenses approuvée a déjà été facturée au client, aucune demande de rappel ne peut être créée. Un utilisateur qui tente de créer une demande de rappel reçoit un message qui déclare que l’entrée de temps ou de dépenses ne peut pas être rappelée, car elle a déjà été facturée.

## <a name="approve-or-reject-a-recall-request"></a>Approuver ou rejeter une demande de rappel

Procédez comme suit pour approuver ou rejeter une demande de rappel.

1. Accédez à **Projets** \> **Mes tâches** \> **Approbations**.
2. Dans la page de liste **Approbations**, modifiez la vue avec **Rappeler les demandes d’approbation**. Une liste des demandes de rappel envoyées s’affiche.
3. Sélectionnez une ou plusieurs entrées, puis sélectionnez **Approuver** ou **Rejeter**.
4. Si vous avez sélectionné **Approuver**, un message d’avertissement s’affiche qui explique l’impact de l’approbation. Sélectionnez **OK** pour confirmer l’opération. La demande de rappel est approuvée.

    -ou-

    Si vous avez sélectionné **Rejeter**, la demande de rappel est rejetée.

> [!NOTE]
> comme quand un rappel est demandé, lorsqu’un rappel est approuvé, le système vérifie l’activité de facturation sur les entrées de temps ou de dépenses. Si une entrée a déjà été facturée, ou si elle figure sur un brouillon de facture, l’approbateur reçoit un message d’erreur qui déclare que le temps ou les dépenses ne peuvent pas être approuvé pour rappel, car ils ont déjà été facturés.

## <a name="impact-of-a-recall-request"></a>Impact d’une demande de rappel

Lorsqu’une approbation est rappelée, il existe un impact opérationnel et un impact financier.

### <a name="operational-impact"></a>Impact opérationnel

Si une demande de rappel est approuvée, l’enregistrement de l’approbation est marqué comme **Rejeté**. Le statut de l’entrée passe à **Renvoyé** ou **Rejeté**, selon qu’il s’agit d’une entrée de temps ou d’une entrée de dépenses.

Le membre de l’équipe du projet peut afficher les entrées, les modifier, puis renvoyer les entrées, ou supprimer des entrées entièrement.

Si une demande de rappel est rejetée, le statut de l’entrée reste **Approuvé**, et l’entrée ne peut pas être modifiée par le membre de l’équipe du projet ou l’approbateur du projet.

### <a name="financial-impact"></a>Impact financier

Si une demande de rappel est approuvée, les chiffres réels correspondants au coût et aux ventes sont mis à jour de la façon suivante :

- Le champ **Statut d’ajustement** est mis à jour sur **Ajusté**.
- Le champ **Statut de facturation** est mis à jour sur **Annulé**.

Ensuite, des entrées de contrepassation sont créées dans la table Chiffres réels. Pour créer des entrées de contrepassation, le système copie sur les valeurs de champ les chiffres réels initiaux. Les seules valeurs qui ne sont pas copiées sont les valeurs de quantité. Ces valeurs sont contrepassées à la place. Les chiffres réels contrepassés sont définis pour les chiffres réels **Coût** et **Ventes non facturées**. Le champ **Statut de l’ajustement** sur les chiffres réels contrepassés est défini sur **Non ajustable**, et le champ **Statut de facturation** est défini sur **Annulé**. En raison de ces modifications, la dépense enregistrée et l’arriéré de revenu du projet ne compteront plus dans les montants que ces chiffres réels représentent.

Si une demande de rappel est rejetée, il n’y a aucun impact financier sur le projet.

## <a name="changes-to-time-entry-records"></a>Modifications apportées aux enregistrements d’entrées de temps

L’illustration suivante montre les modifications qui se produisent pour des entrées de temps approuvées lorsqu’elles sont rappelées.

![Transitions d’état d’entrée de temps.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Modifications apportées aux enregistrements d’entrées de dépenses

L’illustration suivante montre les modifications qui se produisent pour des entrées de dépenses approuvées lorsqu’elles sont rappelées.

![Transitions d’état d’entrée de dépense.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]