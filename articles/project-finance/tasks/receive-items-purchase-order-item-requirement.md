---
title: Recevoir les articles sur la commande achat depuis le besoin d’article
description: Cette rubrique explique comment recevoir des articles sur une commande achat à partir d’un besoin d’article.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3167967"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Recevoir les articles sur la commande achat depuis le besoin d’article

[!include [task guide banner](../../includes/task-guide-banner.md)]

Cette rubrique explique comment recevoir des articles sur une commande achat à partir d’un besoin d’article.

En utilisant une demande d’article au lieu d’une transaction d’article, vous pouvez planifier la livraison juste avant que l’article ne soit réellement utilisé, créer une commande d’achat, inclure l’article dans le cadre de l’accord commercial et inclure l’exigence d’article dans la planification de la production. 

Cette tâche utilise le jeu de données USSI.

1. Dans le volet de navigation, accédez à **Modules > Gestion de projet et comptabilité > Projets > Tous les projets**.
2. Dans la liste, sélectionnez le lien sur la ligne souhaitée.
3. Dans le volet Actions, sélectionnez **Planifier**.
4. Sélectionnez **Demandes d’article**.
5. Cliquez sur **Nouveau**.
6. Dans la nouvelle ligne, saisissez ou sélectionnez une valeur dans le champ **Numéro d’article**.
7. Dans le champ **Quantité**, tapez un nombre.
8. Sélectionnez **Enregistrer**.
9. Dans le volet Actions, sélectionnez **Gérer**.
10. Sélectionnez **Fonctions**.
11. Sélectionnez **Créer une commande achat**.
12. Cochez la case **Tout inclure**.
13. Dans le champ **Compte fournisseur**, tapez ou sélectionnez une valeur.
14. Cliquez sur **OK**.
15. Dans le volet de navigation, accédez à **Modules > Comptabilité fournisseur > Commandes fournisseur > Toutes les commandes fournisseur**.
16. Dans la liste, sélectionnez le lien sur la ligne souhaitée.
17. Dans le volet Actions, sélectionnez **Achat**.
18. Cliquez sur **Confirmer**.
19. Dans le volet Actions, sélectionnez **Recevoir**.
20. Sélectionnez **Accusé de réception de marchandises**.
21. Dans le champ **Accusé de réception de marchandises**, tapez une valeur.
22. Cliquez sur **OK**.

