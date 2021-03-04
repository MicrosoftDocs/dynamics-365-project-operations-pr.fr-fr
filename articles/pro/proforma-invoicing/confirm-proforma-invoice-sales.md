---
title: Confirmer une facture pro forma – Simplifié
description: Cette rubrique fournit des informations sur la confirmation des factures pro forma dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176518"
---
# <a name="confirm-a-proforma-invoice---lite"></a>Confirmer une facture pro forma – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_


Une fois la facture pro forma confirmée, le statut de la facture projet est mis à jour sur **Confirmé**. Lorsqu’une facture est confirmée, elle devient en lecture seule. À l’avenir, la facture ne pourra être corrigée que s’il y a des corrections ou des crédits initiés par le client, ou si la facture est marquée comme payée.

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
Un chiffre d’affaires non facturé réel d’un montant négatif de la provision ou de l’avance à utiliser pour le rapprochement.
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
Un nouveau réel de ventes non facturé qui n’est pas facturable pour les heures et le montant restants après déduction des chiffres corrects dans le détail de la ligne de facture modifiée, une contrepassation des chiffres réels des ventes facturées et un réel de ventes facturé équivalent.
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
Un chiffre réel de vente pour la quantité et le montant figurant sur l’approbation de dépense d’origine </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
Facturation d’une ligne de contrat selon les produits.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Un chiffre d’affaires facturé réel pour la ligne de produits avec la quantité et le montant provenant de la ligne de contrat basée sur le produit.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]