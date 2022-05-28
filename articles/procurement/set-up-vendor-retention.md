---
title: Configurer la rétention de fournisseurs
description: Cette rubrique explique comment configurer la rétention de fournisseurs.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e0cd7669c7d6b916261e2c85cce0f24ff241a075
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583701"
---
# <a name="set-up-vendor-retention"></a>Configurer la rétention de fournisseurs

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cette rubrique fournit des informations sur la configuration de la rétention de fournisseurs.

## <a name="set-up-a-vendor-retention-account-in-general-ledger"></a>Configurer un compte de rétention de fournisseurs dans la comptabilité

1. Dans Dynamics 365 Finance, accédez à **Comptabilité** > **Paramétrage de la validation** > **Comptes pour transactions automatiques**.
2. Ajoutez une nouvelle ligne.
3. Dans le champ **Type de validation**, sélectionnez **Rétention de fournisseurs**.
4. Sélectionnez le compte principal pour la validation de la rétention de fournisseurs.

## <a name="create-vendor-retention-terms"></a>Créer des conditions de rétention de fournisseurs

Utilisez la page **Conditions de rétention de fournisseurs** pour configurer et gérer les conditions de rétention pour les paiements fournisseur. Entrez le pourcentage du paiement fournisseur à retenir et le pourcentage des montants précédemment retenus à libérer. Les montants sont automatiquement conservés sur les factures des fournisseurs jusqu’à ce que le contrat atteigne l’état d’achèvement spécifié. Une fois les conditions de rétention définies pour un fournisseur, vous pouvez les appliquer à tout projet sur lequel travaille le fournisseur.

1. Dans Finance, accédez à **Gestion et comptabilité des projets** > **Configurer** > **Rétention** > **Conditions de rétention des paiements fournisseur**.
2. Sélectionnez **Nouveau** pour ajouter une nouvelle condition de rétention de fournisseur. La valeur du champ **ID règle** pour la nouvelle condition est entrée automatiquement. 
3. Dans le champ **Description**, saisissez un nom descriptif pour la nouvelle condition.
4. Dans l’onglet **Conditions**, sélectionnez **Ajouter une ligne** pour entrer une condition de rétention de fournisseurs.
5. Dans le champ **Pourcentage d’unités livrées**, entrez un pourcentage d’achèvement pour la règle. Les montants sont automatiquement retenus sur les factures fournisseur jusqu’à ce que l’état d’achèvement du projet soit égal au pourcentage entré. Par exemple, si vous entrez 50,00, les montants sont conservés jusqu’à ce que le projet soit achevé à 50 %%.
6. Dans le champ **Pourcentage à retenir**, entrez le pourcentage d’un montant de facture fournisseur à retenir. Par exemple, si vous entrez 10,00 dans ce champ, 10 % du montant des factures fournisseur est retenu jusqu’à ce que le projet atteigne le pourcentage d’achèvement que vous avez sélectionné dans le champ **Pourcentage d’unités livrées**.
7. Dans le champ **Pourcentage à libérer**, entrez le pourcentage des montants précédemment retenus à libérer au niveau sélectionné d’achèvement du projet.

> [!NOTE]
> Si vous avez plusieurs jalons pour différents niveaux d’achèvement du projet, entrez une ligne de condition de rétention de fournisseurs distincte pour chaque règle de rétention. Chaque ligne peut avoir un pourcentage différent à retenir ou à libérer par niveau d’achèvement de projet désigné.

## <a name="set-up-a-vendor-agreement-for-the-project"></a>Configurer un contrat fournisseur pour le projet

Configurez les conditions de rétention de fournisseurs qui s’appliquent au projet. Les conditions de rétention du fournisseur sont également affichées sur les bons de commande que vous créez pour le fournisseur.

1. Dans Finance, accédez à **Gestion et comptabilité des projets** > **Projets** > **Tous les projets**. 
2. Sélectionnez un projet et, dans le volet Actions, sélectionnez **Groupe de projets** > **Accords fournisseur**.
3. Dans la page **Accords fournisseur**, ajoutez une nouvelle ligne.
4. Dans le champ **Code de compte**, sélectionnez l’une des options suivantes :
   - **Table** : Les conditions de rétention des fournisseurs s’appliquent à un seul fournisseur.
   - **Groupe** : Les conditions de rétention des fournisseurs s’appliquent à tous les fournisseurs d’un groupe de fournisseurs.
   - **Tous** : Les conditions de rétention des fournisseurs s’appliquent à tous les fournisseurs.
5. Dans le champ **Fournisseur/Groupe de fournisseurs**, sélectionnez le fournisseur ou le groupe de fournisseurs auquel s’appliquent les conditions de rétention de fournisseurs. Si vous avez sélectionné **Tous** à l’étape précédente, ce champ n’est pas disponible.
6. Dans le champ **Conditions de rétention de fournisseurs**, sélectionnez l’ID règle pour les conditions de rétention à appliquer à ce fournisseur.

