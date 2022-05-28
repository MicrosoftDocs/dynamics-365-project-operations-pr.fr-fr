---
title: Factures correctives basées sur un projet
description: Cette rubrique fournit des informations sur la création et la confirmation de factures correctives basées sur un projet dans Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 71bf10518c22ce2ad6aa43b710c68d0d46f93e77
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594621"
---
# <a name="corrective-project-based-invoices"></a>Factures correctives basées sur un projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une facture de projet confirmée peut être corrigée pour traiter les modifications ou les crédits négociés avec le client et le chef de projet.

Pour apporter des modifications à une facture confirmée, ouvrez la facture confirmée et sélectionnez **Corriger cette facture**. 

> [!NOTE]
> Cette sélection n’est pas disponible, sauf si une facture de projet est confirmée ou si la facture basée sur le projet comporte des avances, des provisions ou des rapprochements d’avances ou de provisions.

Un nouveau projet de facture est créé à partir de la facture confirmée. Tous les détails de la ligne de facture de la facture précédemment confirmée sont copiés dans le nouveau brouillon. Voici quelques-uns des points clés à comprendre concernant les détails de la ligne sur la nouvelle facture corrigée :

- Toutes les quantités sont mises à jour à zéro. Dynamics 365 Project Operations suppose que tous les articles facturés sont entièrement crédités. Si nécessaire, vous pouvez mettre à jour manuellement ces quantités pour refléter la quantité facturée et non la quantité créditée. En fonction de la quantité que vous saisissez, l’application calcule la quantité créditée. Ce montant est reflété dans les chiffres réels créés lorsque la facture corrigée est confirmée. Si vous apportez des modifications au montant de la taxe, vous devez entrer le montant de taxe correct et non le montant de taxe crédité.
- Les corrections d’étape sont toujours traitées comme des crédits complets.


> [!IMPORTANT]
> Pour les détails de la ligne de facture qui sont des corrections d’autres frais déjà facturés, le champ **Correction** est défini sur **Oui**. Pour les factures dont des détails de la ligne de facture sont corrigés, le champ **Contient des corrections** est défini sur **Oui**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Chiffres réels créés lorsqu’une facture corrective est confirmée

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
Facturation de l’intégralité du crédit d’une transaction de matériel déjà facturée.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une contrepassation des ventes facturées pour la quantité et le montant du détail de la ligne de facture d’origine du matériel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre réel des ventes facturées pour la quantité et le montant du détail de la ligne de facture d’origine du matériel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturation du crédit partiel sur une transaction de matériel.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une contrepassation des ventes facturées pour la quantité et le montant facturés sur le détail de la ligne de facture d’origine du matériel.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre réel de ventes non facturées qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation de celui-ci et un chiffre réel de ventes facturé équivalent.
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
Le statut de la facture du jalon <b>Facture client publiée</b> est remplacé par <b>Prêt pour la facturation</b>.
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
Ce scénario n’est pas pris en charge.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
