---
title: Annuler l’approbation des entrées précédemment approuvées
description: Cette rubrique explique comment un chef de projet peut annuler l’approbation d’entrées de temps, de dépense ou d’utilisation de matériel précédemment approuvées.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584777"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Annuler l’approbation des entrées précédemment approuvées

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Un chef de projet ou approbateur ayant déjà approuvé précédemment les entrées de temps, de dépense ou d’utilisation de matériel peut annuler leur approbation de ces entrées. 

Procédez comme suit pour annuler l’approbation d’une entrée de temps, de dépense ou d’utilisation de matériel précédemment approuvée.

1. Accédez à **Projets** \> **Mes tâches** \> **Approbations**.
2. La page de la liste **Approbations** affiche toutes les entrées de temps en attente d’approbation. Définissez la vue sur **Mes approbations passées**.
3. Sélectionnez les approbations de temps, de dépense ou de matériel à annuler. Puis, dans le volet Actions, sélectionnez **Annuler l’approbation**.
4. Dans la boîte de message de confirmation qui s’affiche, sélectionnez **OK** pour confirmer l’opération.

> [!IMPORTANT]
> Vous ne pouvez pas annuler l’approbation d’une entrée de temps, de dépense et d’utilisation de matériel précédemment approuvée qui a déjà été facturée au client. Si vous essayez, vous recevez un message indiquant que l’approbation ne peut pas être annulée, car elle a déjà été facturée. Dans ce cas, vous pouvez annuler l’approbation uniquement si une facture corrective est utilisée pour émettre un crédit ou un remboursement complet au client sur la facture d’origine.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Impact de l’annulation de l’approbation d’une entrée précédemment approuvée

Lorsqu’une approbation est annulée, il existe un impact opérationnel et un impact financier.

### <a name="operational-impact"></a>Impact opérationnel

Si l’approbation d’une entrée est annulée, l’enregistrement d’approbation est marqué comme **Envoyé**. Le statut de l’entrée passe sur **Envoyé**. À cette étape, un membre de l’équipe de projet peut rappeler l’entrée sans envoyer de demande de rappel.

L’approbateur peut modifier les valeurs **Quantité facturable** et **Type de facturation**, puis approuvez l’entrée une fois de plus.

### <a name="financial-impact"></a>Impact financier

Si l’approbation d’une entrée est annulée, les chiffres réels correspondants au coût et aux ventes sont mis à jour de la façon suivante :

- Le champ **Statut d’ajustement** est mis à jour sur **Ajusté**.
- Le champ **Statut de facturation** est mis à jour sur **Annulé**.

Ensuite, des entrées de contrepassation sont créées dans la table Chiffres réels. Pour créer des entrées de contrepassation, le système copie sur les valeurs de champ les chiffres réels initiaux. Les seules valeurs qui ne sont pas copiées sont les valeurs de quantité. Ces valeurs sont contrepassées à la place. Les chiffres réels contrepassés sont définis pour les chiffres réels **Coût** et **Ventes non facturées**. Le champ **Statut de l’ajustement** sur les chiffres réels contrepassés est défini sur **Non ajustable**, et le champ **Statut de facturation** est défini sur **Annulé**. En raison de ces modifications, la dépense enregistrée et l’arriéré de revenu du projet ne compteront plus dans les montants que ces chiffres réels représentent.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
