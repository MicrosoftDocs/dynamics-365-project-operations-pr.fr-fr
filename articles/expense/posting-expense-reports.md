---
title: Publier des notes de frais
description: Cet article explique comment publier des notes de frais.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524866"
---
# <a name="post-expense-reports"></a>Publier des notes de frais

Une fois qu’une note de frais a été approuvée et transférée dans la feuille comptabilité, elle peut être affichée. Lorsque vous publiez une note de frais, les dépenses éligibles au recouvrement de la taxe sur la valeur ajoutée (TVA) sont identifiées. La tâche de vérification et de récupération des paiements de TVA est confiée au salarié qui est chargé de vérifier la note de frais.

Si les dépenses sur une note de frais sont imputées à une entreprise autre que l’entreprise qui emploie l’employé, vous devez vérifier à la fois l’entreprise à laquelle ces dépenses sont dues et l’entreprise à laquelle elles sont dues. Par exemple, l’employé qui a soumis une note de frais travaille pour la société DAT mais a facturé une dépense à la société DIR. Dans ce cas, DAT est l’entreprise à laquelle la dépense est due et DIR est l’entreprise à laquelle la dépense est due. Après avoir vérifié ces lignes de journal, vous pouvez enregistrer les lignes de dépenses dans la comptabilité.

Pour valider une note de frais, sur la page **Notes de frais approuvées**, sélectionnez la note de frais, puis, dans le volet Actions, sélectionnez **Valider**.

Vous pouvez également valider toutes les notes de frais de la liste en même temps. Sélectionnez toutes les notes de frais, puis sélectionnez **Valider**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Activer la possibilité d’afficher le passif des dépenses dans la devise du fournisseur pour la fonctionnalité de mode de paiement en espèces

La fonctionnalité **Possibilité d’afficher le passif des dépenses dans la devise du fournisseur pour la fonctionnalité de mode de paiement en espèces** permet aux notes de frais d’être publiées dans une devise fournisseur pour le mode de paiement en espèces.

Actuellement, lorsque vous soumettez des dépenses en espèces, les notes de frais sont comptabilisées dans la devise comptable. En raison de la conversion du montant entre la devise de la transaction, la devise comptable et la devise du fournisseur, un montant incorrect est payé aux fournisseurs si la date de transaction de la dépense et la date de paiement réelle ont des taux de change différents.

Cette fonctionnalité garantit que le solde du fournisseur est enregistré dans la devise du fournisseur lorsque la note de frais est publiée.

1. Accédez à **Espaces de travail** \> **Gestion des fonctionnalités**.
2. Dans la liste, recherchez et sélectionnez **Possibilité d’afficher le passif des dépenses dans la devise du fournisseur pour le mode de paiement en espèces**, puis sélectionnez **Activer maintenant**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
