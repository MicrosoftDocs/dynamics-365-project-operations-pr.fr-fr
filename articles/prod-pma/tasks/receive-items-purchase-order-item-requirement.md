---
title: Recevoir les articles sur la commande achat depuis le besoin d’article
description: Cette rubrique explique comment recevoir des articles sur une commande achat à partir d’un besoin d’article.
author: Yowelle
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e0c4a75f1d86538cc773af1f7c0ae3c83ef0ad5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011683"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>Recevoir les articles sur la commande achat depuis le besoin d’article

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]