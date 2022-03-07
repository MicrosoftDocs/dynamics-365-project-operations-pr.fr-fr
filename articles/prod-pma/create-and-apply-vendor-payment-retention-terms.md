---
title: Créer et appliquer les conditions de rétention des paiements des fournisseurs
description: Cette rubrique fournit des informations sur la configuration et la gestion des conditions de rétention pour les paiements des fournisseurs.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 4ff725512aa0bcc87ff4670d6bb072f3bf780786c1f71b332914887f4d4ccf13
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991213"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a>Créer et appliquer les conditions de rétention des paiements des fournisseurs

[!include [banner](../includes/banner.md)] 

La configuration des conditions de rétention des paiements fournisseur pour un projet est utile lorsque votre organisation souhaite conserver une partie des paiements effectués à un fournisseur. Par exemple, lorsque vous souhaitez suspendre le paiement à un fournisseur jusqu’à ce que les produits livrés répondent à vos attentes. Les conditions de rétention des paiements fournisseur peuvent être spécifiées lorsque vous négociez un contrat fournisseur.

## <a name="create-vendor-payment-retention-terms"></a>Créer les conditions de rétention des paiements des fournisseurs

Vous pouvez saisir le pourcentage du paiement fournisseur pour la rétention et le pourcentage des montants précédemment retenus à débloquer. Les montants sont automatiquement conservés sur les factures des fournisseurs jusqu’à ce que le contrat atteigne l’état d’achèvement spécifié. Après avoir configuré les conditions de rétention, vous pouvez les appliquer à n’importe quel projet pour ce fournisseur.

Procédez comme suit pour configurer et gérer les conditions de rétention des paiements fournisseurs. 

1. Accédez à **Gestion de projets et comptabilité** > **Rétention** > **Conditions de rétention des paiements fournisseur**.
2. Sélectionnez **Nouveau** pour ajouter une nouvelle condition de rétention de fournisseur. La valeur **ID de règle** du nouveau terme est automatiquement saisie. 
3. Entrez une brève description dans le champ **Description** et sur le raccourci **Termes**, sélectionnez **Ajouter une ligne** pour saisir des valeurs de terme pour les éléments suivants :

   - **Pourcentage d’unités livrées** : Saisissez un pourcentage d’achèvement pour la condition. Les montants sont automatiquement conservés sur les factures des fournisseurs jusqu’au stade d’achèvement du projet est égal au pourcentage spécifié. Par exemple, si vous entrez 50,00, les montants sont conservés jusqu’à ce que le projet soit achevé à 50 %%.
   - **Pourcentage de conservation** : Saisissez un pourcentage du montant de la facture fournisseur à conserver. Par exemple, si vous entrez 10,00, 10 %% du montant d’une facture fournisseur sont conservés jusqu’à ce que le projet atteigne le pourcentage d’achèvement défini dans le **champ Pourcentage d’unités livrées**.
   - **Pourcentage à libérer** : Sélectionnez **Ajouter une ligne** pour saisir un pourcentage de tout montant précédemment retenu à débloquer pour le niveau d’achèvement de projet sélectionné.

> [!NOTE]
> Si vous avez plusieurs jalons pour différents niveaux d’achèvement de projet, entrez une ligne de condition de rétention fournisseur distincte pour chaque règle de rétention. Chaque ligne peut spécifier un pourcentage de rétention et un pourcentage de publication différents pour chaque niveau désigné d’achèvement de projet.

Après avoir créé les conditions de rétention pour un fournisseur, vous pouvez les appliquer à un projet.

## <a name="apply-vendor-retention-terms-to-a-project"></a>Appliquer les conditions de rétention des fournisseurs à un projet

1. Accédez à **Gestion de projets et comptabilité** > **Projets** > **Tous les projets** et ouvrez un projet à partir de la page de liste des projets.
2. Dans le raccourci **Accords fournisseur**, cliquez sur **Ajouter une ligne**.
3. Dans le **champ Code compte**, sélectionnez l’une des options suivantes : 

   - **Table** : Les conditions de rétention des fournisseurs s’appliquent à un seul fournisseur.
   - **Groupe** : Les conditions de rétention des fournisseurs s’appliquent à tous les fournisseurs d’un groupe de fournisseurs.
   - **Tous** : Les conditions de rétention des fournisseurs s’appliquent à tous les fournisseurs.

4. Dans le **champ Fournisseur/Groupe de fournisseurs**, sélectionnez le fournisseur ou le groupe de fournisseurs auquel s’appliquent les conditions de rétention des fournisseurs. Si vous avez sélectionné **Tout** à l’étape précédente, ce champ n’est pas disponible.
5. Dans le champ **Conditions de rétention des fournisseurs**, sélectionnez les conditions de conservation que vous avez créées lors de la procédure précédente.
6. Si le projet a également des conditions de paiement au moment du paiement (PWP) définies pour le fournisseur, entrez le pourcentage de seuil pour le projet dans le champ **Pourcentage de seuil PWP**.

Les conditions de rétention du fournisseur sont également affichées sur les bons de commande que vous créez pour le fournisseur.


[!INCLUDE[footer-include](../includes/footer-banner.md)]