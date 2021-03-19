---
title: Annuler les entrées de temps et de dépenses précédemment approuvées
description: Cette rubrique explique comment annuler une transaction de temps et de dépenses de projet approuvée.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 40ac37c1070e1c4da01e96bbc4248977b2b6d284
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290851"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Annuler les entrées de temps ou de dépenses précédemment approuvées

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dans la dernière version de Dynamics 365 Project Service Automation, les approbateurs peuvent annuler les entrées de temps ou de dépenses qu’ils ont précédemment approuvées.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Annuler une entrée de temps ou de dépenses précédemment approuvée

Procédez comme suit pour annuler une entrée de temps ou de dépenses précédemment approuvée.

1. Accédez à **Projets** \> **Mes tâches** \> **Approbations**.
2. Dans la page de liste **Approbations**, modifiez la vue avec **Mes approbations passées**. Une liste des entrées de temps et de dépenses que vous avez précédemment approuvée s’affiche.
3. Sélectionnez une ou plusieurs entrées, puis sélectionnez **Annuler l’approbation**. Vous recevez un message d’avertissement.
4. Sélectionnez **OK** pour annuler l’approbation.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Comprendre l’impact de l’annulation d’une approbation d’entrée de temps ou de dépenses

Lorsqu’une approbation est annulée, il existe un impact opérationnel et un impact financier.

### <a name="operational-impact"></a>Impact opérationnel

Du côté des opérations, quand une approbation est annulée, le statut de l’enregistrement est réinitialisé sur **Brouillon**, et l’approbation ne s’affiche plus dans la vue **Mes approbations passées**. Au lieu de cela, l’approbation annulée apparaît dans la vue **Entrées de temps pour approbation** ou la vue **Entrées de dépenses pour approbation**, selon que c’était une entrée de temps ou une entrée de dépenses. En outre, le statut de l’entrée de temps ou de dépenses associée passe à **Envoyé**, afin que l’entrée associée soit cohérente avec les approbations ayant le statut **Brouillon**.

En tant qu’approbateur, vous pouvez modifier certains champs d’une approbation qui a le statut **Brouillon**. Ces champs incluent **Type de facturation** et **Heures facturables pour des entrées de temps**. Après avoir apporté vos modifications, vous pouvez approuver l’enregistrement. Sinon, vous pouvez rejeter l’entrée. Si vous rejetez l’approbation d’une entrée de temps, le statut de l’entrée passe à **Renvoyé**. Si vous rejetez l’approbation d’une entrée de dépenses, le statut passe à **Rejeté**. Fonctionellement, les entrées retournées et rejetées se comportent comme une entrée qui a le statut **Brouillon**. Un membre de l’équipe du projet peut apporter des modifications requises à l’entrée puis les envoyer pour approbation, ou supprimer entièrement l’entrée.

### <a name="financial-impact"></a>Impact financier

Un projet est également affecté financièrement lorsqu’une approbation est annulée. D’abord, les chiffres réels correspondants au coût et aux ventes sont mis à jour de la façon suivante :

- Le statut d’ajustement est défini sur **Ajusté**.
- Le statut de facturation est défini sur **Annulé**.

Ensuite, des entrées de contrepassation sont créées dans la table Chiffres réels. Pour créer des entrées de contrepassation, le système copie sur les valeurs de champ les chiffres réels initiaux. Les seules valeurs qui ne sont pas copiées sont les valeurs de quantité. Ces valeurs sont contrepassées à la place. Les chiffres réels contrepassés sont définis pour les chiffres réels **Coût** et **Ventes non facturées**. Le champ **Statut de l’ajustement** sur les chiffres réels contrepassés est défini sur **Non ajustable**, et le statut de facturation sur **Annulé**.

Une fois ces modifications effectuées, le montant enregistré comme dépensé dans le projet et l’arriéré de revenu du projet ne compteront plus dans les montants que ces chiffres réels représentent.


[!INCLUDE[footer-include](../includes/footer-banner.md)]