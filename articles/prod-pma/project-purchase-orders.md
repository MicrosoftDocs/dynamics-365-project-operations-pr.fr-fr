---
title: Commandes fournisseur pour un projet
description: Cet article décrit les différentes méthodes que vous pouvez utiliser pour créer des commandes fournisseur pour un projet. La méthode que vous utilisez dépend de l’objectif de la commande fournisseur et quand les articles achetés sont consommés et, par conséquent, facturés sur un projet.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd891aec5bcab66c5801a5d9ca8abbbf632d662d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075728"
---
# <a name="purchase-orders-for-a-project"></a>Commandes fournisseur pour un projet

[!include [banner](../includes/banner.md)]

Cet article décrit les différentes méthodes que vous pouvez utiliser pour créer des commandes fournisseur pour un projet. La méthode que vous utilisez dépend de l’objectif de la commande fournisseur et quand les articles achetés sont consommés et, par conséquent, facturés sur un projet.

### <a name="methods-for-creating-a-purchase-order"></a>Méthodes de création d’une commande fournisseur

Vous pouvez utiliser l’une des méthodes suivantes pour créer une commande fournisseur dans Gestion de projet et comptabilité. Le but de la commande fournisseur détermine quand la commande fournisseur est consommée et, par conséquent, quand les articles sont facturés vers un projet.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Méthode</th>
<th>Objectif</th>
<th>Consommation d’articles</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Créez une commande fournisseur directement à partir d’un projet.</td>
<td>Utilisez cette méthode pour acheter des articles auprès d’un fournisseur externe pour les consommer sur un projet. Vous pouvez créer la commande fournisseur de l’une des deux méthodes suivantes :
<ul>
<li>À partir du projet lui-même. Dans ce cas, le projet est déjà défini pour la commande fournisseur.</li>
<li>En accédant à la commande fournisseur du projet. Vous devez sélectionner à la fois le fournisseur et le projet pour lesquels créer la commande fournisseur.</li>
</ul></td>
<td>Les articles sont consommés lors de la mise à jour de la facture fournisseur.</td>
</tr>
<tr class="even">
<td>Créer une commande achat à partir d'une commande client.</td>
<td>Utilisez cette méthode pour acheter des articles lorsque vous créez une commande client à partir d’un projet.</td>
<td>Les articles sont consommés lorsque la commande client est facturée au client.</td>
</tr>
<tr class="odd">
<td>Créez une commande fournisseur à partir d’une exigence d’article.</td>
<td>Utilisez cette méthode pour acheter des articles lorsque vous créez une exigence d’article à partir d’un projet.</td>
<td>Les articles sont consommés lorsque le bon de livraison de l’exigence d’article est mis à jour.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Lorsque vous mettez à jour la facture fournisseur ou le bon de livraison, vous êtes invité à mettre à jour le bon de livraison sur l’exigence de l’article.

Pour plus d’informations, consultez [Recevoir les articles sur la commande fournisseur depuis l’exigence d’article](tasks/receive-items-purchase-order-item-requirement.md).

