---
title: Confirmer une facture pro forma
description: Cette rubrique offre des informations sur la confirmation d’une facture pro forma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128100"
---
# <a name="confirm-a-proforma-invoice"></a>Confirmer une facture pro forma

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une fois la facture pro forma confirmée, le statut de la facture projet est mis à jour sur **Confirmé**. Lorsqu’une facture est confirmée, elle devient en lecture seule. À l’avenir, la facture ne pourra être corrigée que s’il y a des corrections ou des crédits initiés par le client, ou lorsqu’elle est marquée comme payée.

Le tableau suivant répertorie les chiffres réels créés par le système. Ces chiffres réels sont créés lorsque certaines opérations sont effectuées sur le projet de facture de projet avant sa confirmation.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Scénario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Rapports réels créés lors de la confirmation</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation d’une transaction de temps sans aucune modification sur le projet de facture.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes non facturées pour les heures et le montant figurant sur l’approbation du temps d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un chiffre réel de vente facturée pour les heures et le montant figurant sur l’approbation du temps d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturation d’une transaction de temps qui a été modifiée pour réduire la quantité.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes non facturées pour les heures et le montant figurant sur l’approbation du temps d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui n’est pas facturable pour les heures et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation d’une opération de temps qui a été modifiée pour augmenter la quantité.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes non facturées pour les heures et le montant figurant sur l’approbation du temps d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation d’une transaction de dépense sans aucune modification sur le projet de facture.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes non facturées pour la quantité et le montant figurant sur l’approbation de dépense d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un chiffre réel de vente pour la quantité et le montant figurant sur l’approbation de dépense d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturation d’une transacton de dépense qui a été modifiée pour réduire la quantité.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes non facturées pour la quantité et le montant figurant sur l’approbation de dépense d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui n’est pas facturable pour la quantité et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation d’une transacton de dépense qui a été modifiée pour augmenter la quantité.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes non facturées pour la quantité et le montant figurant sur l’approbation de dépense d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation des frais.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une annulation des ventes non facturées pour le montant des frais sur la ligne de journal d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un chiffre réel de vente pour la quantité et le montant figurant sur la ligne de journal d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Facturation d’un jalon.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Un chiffre réel de vente facturée pour le montant du jalon sur le jalon d’origine dans la ligne de contrat de projet.
                </p>
            </td>
        </tr>
    </tbody>
</table>
