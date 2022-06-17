---
title: Confirmer une facture pro forma basée sur un projet
description: Cet article fournit des informations sur la confirmation d’une facture proforma basée sur un projet.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a4ad243e8959af61993e2ff6ce89209be378f7df
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929441"
---
# <a name="confirm-a-proforma-project-based-invoice"></a>Confirmer une facture pro forma basée sur un projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une fois la facture pro forma confirmée, le statut de la facture projet est mis à jour sur **Confirmé**. Lorsqu’une facture est confirmée, elle devient en lecture seule. À partir de ce moment-là, la facture ne pourra être corrigée que s’il y a des corrections ou des crédits initiés par le client.

Le tableau suivant répertorie les chiffres réels créés par le système. Ces chiffres réels sont créés lorsque certaines opérations sont effectuées sur le projet de facture de projet avant sa confirmation.

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
Facturation d’une avance ou d’une provision </p>
            </td>
            <td width="408" valign="top">
                <p>
Un chiffre d’affaires facturé réel de type <strong>Provision</strong> est créé pour le montant de l’avance ou de la provision.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un chiffre réel de vente non facturé avec un montant négatif de la provision ou de l’avance à utiliser pour le rapprochement.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Après avoir entièrement rapproché une provision ou une avance sur une facture.
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
Les chiffres réels des ventes facturées pour le montant de cette facture.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Après avoir partiellement rapproché une provision ou une avance sur une facture.
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
Les chiffres réels des ventes facturées pour le montant de cette facture.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un chiffre d’affaires non facturé négatif d’un montant de la provision ou de l’avance restant à utiliser pour le rapprochement sur les prochaines factures.
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
Un nouveau réel de ventes qui est facturable pour les heures et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un nouveau chiffre réel de vente non facturé qui n’est pas facturable pour les heures restantes et le montant après déduction des chiffres corrigés sur le détail de la ligne de facture modifiée, une contrepassation des chiffres réels de vente et un chiffre réel de ventes facturées équivalent.
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
Un nouveau réel de ventes non facturé qui est facturable pour la quantité et le montant du détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes non facturées et un réel de ventes facturé équivalent. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Facturation d’une transaction de matériel sans aucune modification sur la facture provisoire.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une contrepassation des ventes non facturées pour la quantité et le montant de l’approbation d’utilisation du matériel d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Un chiffre réel de vente facturée pour la quantité et le montant de l’approbation d’utilisation du matériel d’origine.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Facturation d’une transaction de matériel qui a été modifiée pour réduire la quantité.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une contrepassation des ventes non facturées pour la quantité et le montant de l’approbation du temps d’origine.
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
Facturation d’une transaction de matériel qui a été modifiée pour augmenter la quantité.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Une contrepassation des ventes non facturées pour la quantité et le montant de l’approbation d’utilisation du matériel d’origine.
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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
