---
title: Corriger la comptabilité dans les propositions de facture de projet provisoires
description: Cet article explique comment ajuster les informations liées à la comptabilité sur une ébauche de proposition de facture.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921207"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Corriger la comptabilité dans les propositions de facture de projet provisoires

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les *Détails opérationnels* des factures de projet sont maintenus par le chef de projet dans une facture pro forma. Ces détails comprennent la décision concernant les heures, dépenses, matériaux ou jalons à facturer, les tarifs et l’application des montants d’acompte et de provision. Une fois que vous avez confirmé la facture pro forma d’origine, vous pouvez ajuster les détails opérationnels en créant et en confirmant une [facture pro forma corrective](../proforma-invoicing/corrective-invoices.md).

Les *Détails comptables* des factures de projet sont maintenus dans un document de facture destiné au client. Ces détails comprennent le calcul de la taxe de vente et les dimensions financières appliquées à la facture. Cet article fournit des détails sur la façon dont ces détails comptables peuvent être ajustés sur une ébauche de proposition de facture de projet.

## <a name="adjust-sales-tax"></a>Ajuster la taxe

Les groupes de taxe de facturation et les groupes de taxe d’article par défaut peuvent être ajustés directement dans le document de proposition de facture. Pour ajuster ces groupes, sélectionnez **Modifier**, puis, sur chaque ligne de proposition de facture de projet, entrez une nouvelle valeur dans le champ **Groupe de taxe** ou **Groupe de taxe d’article**.

## <a name="adjust-financial-dimensions"></a>Ajuster les dimensions financières

### <a name="header-dimensions"></a>Dimensions de l’en-tête

Par défaut, les dimensions financières de la facture sont dérivées des enregistrements de transactions de projet non facturées qui sont en cours de facturation. Toutefois, les paramètres système vous permettent d’utiliser des dimensions financières dans l’en-tête des propositions de facture de projet pour publier les soldes des clients. Pour activer cette fonctionnalité, sélectionnez **Autoriser les mises à jour des dimensions du projet pour la comptabilité client** sur l’onglet **Finances** de la page **Paramètres de gestion et comptabilité des projets**.

Les dimensions financières des en-têtes de facture peuvent être modifiées avant la publication d’une facture. Sur la page **Proposition de facture de projet**, passez à la vue **En-tête**, puis modifiez les valeurs sur l’onglet **Dimensions financières**.

La vue **En-tête** n’est disponible qu’après que l’administrateur système a activé la fonctionnalité **Utiliser les formulaires de proposition de facture et de journal des factures de projet avec la vue En-tête et Lignes** dans l’espace de travail **Gestion des fonctionnalités**. Cette fonctionnalité nécessite la mise à jour Finance 10.0.25 ou ultérieure.

### <a name="line-dimensions"></a>Dimensions de ligne

Les dimensions financières ne peuvent pas être modifiées directement sur une ligne de proposition de facture de projet. À la place, suivez ces étapes pour ajuster les dimensions financières dans une proposition de facture de projet.

1. Dans la proposition de facture du projet, sélectionnez **Supprimer tout** pour supprimer les lignes de proposition de facture du projet.

    Le bouton **Supprimer tout** n’est disponible que lorsque l’administrateur système a activé la fonctionnalité **Supprimer les lignes de proposition de facture lors de l’utilisation de Project Operations pour les scénarios basés sur des ressources/hors stock** dans l’espace de travail **Gestion des fonctionnalités**.

2. Ajustez les dimensions financières :

    - **Transactions en compte (jalons de facturation) :** accédez à **Tous les projets** \> **Gérer** \> **Opérations en compte** et sélectionnez le jalon qui doit être ajusté. Puis, dans l’onglet **Dimensions financières**, mettez à jour les valeurs selon les besoins.
    - **Transactions de temps, dépenses et matériaux :** dans la page **Transactions de projet validées**, sélectionnez **Ajuster la comptabilité** pour mettre à jour les dimensions financières.

3. Une fois que vous avez terminé d’ajuster les valeurs de la dimension financière, accédez à **Gestion et comptabilité de projets** \> **Périodique** \> **Intégration de Project Operations** et sélectionnez **Importer à partir de la table intermédiaire** pour exécuter le processus périodique. Ce processus utilise les valeurs de dimension financière mises à jour pour recréer les lignes de proposition de facture du projet. Les valeurs mises à jour sont ensuite utilisées dans la comptabilité auxiliaire et la comptabilité générale du projet lorsque la facture du projet est validée.
