---
title: Correction de factures
description: Cette rubrique fournit des informations sur la correction de factures.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898078"
---
# <a name="corrected-invoices"></a>Correction de factures

_**S'applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les factures confirmées peuvent être modifiées. Lorsque vous modifiez une facture confirmée, un brouillon de la facture corrigée est créé. Comme la supposition est que vous souhaitez contrepasser toutes les transactions et quantités de la facture d'origine, cette facture corrigée inclut toutes les transactions de la facture d'origine, et toutes les quantités sont de zéro (0).

Si aucune transaction ne nécessite de correction, vous pouvez la supprimer du brouillon de facture corrective. Pour contrepasser ou ne retourner qu'une quantité partielle, vous pouvez modifier le champ Quantité sur le détail de la ligne. Si vous ouvrez le détail de ligne de facture, la quantité de la facture d'origine s'affiche. Vous pouvez ensuite modifier la quantité actuelle de la facture afin qu'elle soit inférieure ou supérieure à la quantité de la facture d'origine.

Lorsque vous confirmez une facture corrective, le chiffre réel facturé d'origine est contrepassé et un chiffre réel de ventes facturées est créé. Si la quantité a été réduite, la différence aura pour effet la création d'un chiffre réel de ventes non facturées. Par exemple, si la vente facturée d'origine était de huit heures, et que le détail de la ligne de facture corrigée dispose d'une quantité réduite de six heures, la ligne de vente facturée d'origine est contrepassée et deux chiffres réels sont créés :

- Un chiffre réel de vente facturée de six heures.
- Un chiffre réel de ventes non facturées de deux heures restantes. Cette transaction peut être facturée ultérieurement ou marquée comme non facturable, selon les négociations avec le client.
