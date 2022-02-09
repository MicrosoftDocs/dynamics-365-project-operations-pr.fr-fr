---
title: Créer des factures correctives basées sur un projet
description: Cette rubrique fournit des informations sur les factures correctives dans Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cde82bb3c5777458a63a44a131af284e6ed5d7532de6aacbb5eb860c1fcddebd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006191"
---
# <a name="create-corrective-project-based-invoices"></a>Créer des factures correctives basées sur un projet 

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une facture de projet confirmée peut être corrigée pour traiter les modifications ou les crédits négociés avec le client et le chef de projet.

Pour apporter des modifications à une facture confirmée, ouvrez la facture confirmée et sélectionnez **Corriger cette facture**. 

> [!NOTE]
> Cette sélection n’est disponible que si une facture de projet est confirmée.

Un nouveau projet de facture est créé à partir de la facture confirmée. Tous les détails de la ligne de facture de la facture précédemment confirmée sont copiés dans le nouveau brouillon. Voici quelques points clés pour vous aider à mieux comprendre les détails de la ligne sur la nouvelle facture corrigée :

- Toutes les quantités sont mises à jour à zéro. Cela suppose que tous les articles facturés sont entièrement crédités. Si nécessaire, vous pouvez mettre à jour manuellement ces quantités pour refléter la quantité facturée et non la quantité créditée. En fonction de la quantité que vous saisissez, l’application calcule la quantité créditée. Ce montant est reflété dans les chiffres réels créés lorsque la facture corrigée est confirmée. Si vous apportez des modifications au montant de la taxe, vous devez entrer le montant de taxe correct et non le montant de taxe crédité.
- Les corrections d’étape sont toujours traitées comme des crédits complets.
- Les montants de provision ou d’avance peuvent être corrigés si le client a été facturé pour un montant incorrect.
- Les rapprochements des provisions et avances peuvent être corrigés si un montant incorrect a été utilisé pour effectuer le rapprochement avec les frais sur une facture précédemment confirmée.

> [!IMPORTANT]
> Pour les détails de la ligne de facture qui sont des corrections d’autres frais déjà facturés, le champ **Correction** est défini sur **Oui**. Les factures dont les détails de ligne de facture ont été corrigés ont un champ appelé **Contient des corrections** qui est également défini sur **Oui**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Chiffres réels créés lors de la confirmation d’une facture corrective

Le tableau suivant répertorie les chiffres réels créés lorsqu’une facture corrective est confirmée.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Scénario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Confirmer la correction d’une avance ou d’une provision facturée.<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une contrepassation des ventes non facturées de la provision ou de l’avance qui a été créée pour le rapprochement. Ce montant est positif car il vise à annuler le négatif qui a été créé lors de la facturation de la provision ou de l’avance.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Une contrepassation de ventes facturée réelle est créée pour le montant de la provision ou de l’avance pour contrepasser les ventes facturées d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre d’affaires facturé réel est créé pour le montant corrigé sur la provision ou la ligne de facture corrigée basée sur l’avance.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un chiffre d’affaires non facturé réel d’un montant négatif de la provision ou une ligne de facture corrigée basée sur l’avance, qui sera utilisé pour le rapprochement.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Une confirmation de la correction d’une provision ou d’une avance préalablement rapproché.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une contrepassation des ventes non facturées de la provision ou de l’avance qui a été créée pour le rapprochement. Ce montant est positif et vise à annuler le négatif qui a été créé lors du rapprochement précédent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Une contrepassation de ventes facturée réelle pour le montant de la facture précédente.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre d’affaires facturé réel pour le montant de provision qui est appliqué sur la facture corrigée.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un chiffre d’affaires réel non facturé avec un montant négatif de la provision ou de l’avance restante corrigée, qui sera utilisé pour le rapprochement sur les factures ultérieures.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation de l’intégralité du crédit d’une transaction horaire déjà facturée.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes facturées pour les heures et le montant figurant sur la ligne de facture d’origine pour le temps.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre d’affaires non facturé réel pour les heures et le montant figurant sur la ligne de facture d’origine pour le temps.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturation du crédit partiel sur une opération de temps.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes facturées pour les heures et le montant facturé figurant sur la ligne de facture d’origine pour le temps.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre d’affaires réel non facturé qui est facturé pour les heures restantes et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation de l’intégralité du crédit d’une transaction de dépense déjà facturée.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d’origine pour la dépense.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre d’affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d’origine pour la dépense.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturation du crédit partiel d’une transaction de dépense déjà facturée.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d’origine pour une dépense.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrigée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre d’affaires réel non facturé qui est facturé pour la quantité restante et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation de l’intégralité du crédit d’une transaction avec frais déjà facturée.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes facturées pour les quantités et le montant figurant sur la ligne de facture d’origine pour les frais.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre d’affaires non facturé réel pour les quantités et le montant figurant sur la ligne de facture d’origine pour les frais.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation du crédit partiel d’une transaction avec frais déjà facturée.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes facturées pour les quantités et le montant facturé figurant sur la ligne de facture d’origine pour les frais.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture corrective modifiée, une contrepassation de ce chiffre et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturation de l’intégralité du crédit d’un jalon facturé.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes facturées pour le montant figurant sur la ligne de facture d’origine pour le jalon.
                </p>
                <p>
Le statut de la facture du jalon <b>Facture client validée</b> est remplacé par <b>Prêt pour la facturation</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturation du crédit partiel d’un jalon facturé.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Non pris en charge </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]