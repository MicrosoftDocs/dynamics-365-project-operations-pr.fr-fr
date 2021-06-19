---
title: Gérer les estimations de revenus
description: Cette rubrique fournit des informations sur la manière de gérer les estimations de revenus pour les projets.
author: sigitac
ms.date: 11/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e3cbaff18d8bd4d6f6a7577bba25b3e843b1757e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013844"
---
# <a name="manage-revenue-estimates"></a>Gérer les estimations de revenus

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Vous pouvez créer, calculer, valider, annuler ou éliminer des estimations de revenus. Vous pouvez le faire manuellement ou en utilisant un processus périodique. Cette rubrique fournit des informations sur la manière de gérer les estimations de revenus pour les projets.

### <a name="manage-revenue-estimates-manually"></a>Gérer les estimations de revenus manuellement

Sur le projet d’estimation des revenus à prix fixe ou la page **Demande d’estimation** (**Gestion et comptabilité des projets** > **Rapports et demandes** > **Demandes de devis et rapports**), sélectionnez **Estimations**.

### <a name="manage-revenue-estimates-using-a-periodic-process"></a>Gérer les estimations de revenus à l’aide d’un processus périodique

Accédez à **Gestion et comptabilité des projets** > **Périodique** > **Estimations** et sélectionnez le processus correspondant.

## <a name="create-a-revenue-estimate"></a>Créer une estimation de revenus

Pour créer une estimation de revenus, suivez les étapes suivantes. 

1. Accédez à **Gestion et comptabilité des projets** > **Périodique** > **Estimations**.
2. Cliquez sur **Nouveau**. Sur la page **Création d’une estimation**, sélectionnez les paramètres suivants :

   - **Code période** : ce code détermine la fréquence à laquelle les estimations sont validées.
   - **Date estimée** : date à laquelle l’estimation est traitée.
   - **Continu** : cochez cette case pour créer des estimations uniquement si les estimations ont été validées dans la période précédente, ou si l’estimation est la première estimation qui a été créée. Si cette option n’est pas sélectionnée, les estimations sont créées même si les estimations n’ont pas été validées au cours de la période précédente.
   - **Coût pour compléter les méthodes** : définissez comment estimer le travail de projet restant. Pour plus d’informations, voir [Coût pour compléter les méthodes](cost-complete-methods.md).
   - **Méthode d’achèvement** : sélectionnez une méthode d’achèvement parmi les options suivantes :
     - **Automatique** : le pourcentage d’achèvement est calculé automatiquement et basé sur les lignes de coût incluses dans le calcul. Le modèle de coût définit les lignes de coût incluses.
     - **Manuel** : le pourcentage d’achèvement est égal au pourcentage d’achèvement de la dernière estimation. Une fois l’estimation créée, vous pouvez modifier le **Calcul manuel** sur la page **Estimations**.
     - **À partir du modèle de coût** : une combinaison des méthodes automatique et manuelle. Cette option est définie automatiquement ou manuellement, en fonction de la valeur par défaut dans le modèle de coût.
   - **Modèle de prévision** : sélectionnez un modèle de prévision pour l’estimation.
   - **Imprimer la liste des estimations** : créez et affichez une liste d’estimations. La liste contient l’état de la fonction en cours. Vous pouvez imprimer tous les avertissements concernant l’estimation sur le rapport. Les conditions suivantes font apparaître des avertissements dans la liste des estimations :
     - Un pourcentage d’achèvement supérieur à 100 %%.
     - Un pourcentage d’achèvement inférieur à zéro %%.
     - Un montant négatif dans la colonne **À terminer**.
     - Une estimation sans montant de contrat correspondant.
     - Une estimation sans estimation de coût jointe.
   - **Afficher la fenêtre Infos** : sélectionnez cette option pour recevoir un message contenant des informations sur les projets d’estimation qui ont été traités lors de l’exécution du travail.


## <a name="post-wip-or-accruals"></a>Valider TEC ou régularisations

Une fois les estimations évaluées, elles sont maintenues, diminuées ou augmentées. Vous pouvez ensuite valider le TEC lorsque vous travaillez avec le principe d’évaluation **Contrat terminé**, ou valider les provisions lorsque vous travaillez avec le principe d’évaluation **Pourcentage terminé**.
  
Le statut de la période estimée change passe **Créé** à **Validé**.

## <a name="reverse-wip-or-accruals"></a>Inverser TEC ou régularisations

Utilisez l’option d’inversement pour créditer les TEC ou les provisions déjà validés, puis créez des estimations pour la période.

> [!NOTE]
> Pour inverser une période qui se situe entre d’autres périodes, inversez les périodes d’estimation nécessaires, puis revalidez-les. Étant donné que toutes les périodes suivantes dépendent des estimations de la période précédente, ne sautez aucune période.

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a>Éliminer le projet d’estimation et terminer le projet

La dernière étape du processus d’estimation consiste à éliminer le projet d’estimation et à mettre fin au projet à prix fixe lorsque le pourcentage d’achèvement atteint 100 %%.

Voici ce qui suit se produit lorsque vous exécutez l’élimination :

- Pour un projet à prix fixe avec un contrat achevé, les valeurs TEC sont effacées des comptes de bilan et validés dans les comptes de résultat.
- Pour un projet à prix fixe avec un pourcentage achevé, les provisions sont supprimées des comptes de résultat.

L’estimation fait passer le statut à **Éliminé**.

> [!NOTE]
> Dans des cas particuliers, le pourcentage peut dépasser 100 %%. Lorsque cela se produit, réduisez le pourcentage d’achèvement en utilisant la **Méthode Définir le coût à terminer à zéro** pour atteindre 100 pour cent.

## <a name="reverse-elimination"></a>Inverser élimination

1. Accéder à **Gestion et comptabilité des projets** > **Périodique** > **Estimations** > **Inverser élimination**. 
2. Dans le volet Actions, sur l’onglet **Processus**, dans le groupe **Maintenir**, sélectionnez **Estimation**. 
3. Sélectionnez **Inverser élimination**.

Utilisez cette page pour inverser toutes les éliminations avec une date d’estimation spécifiée et avec le statut d’estimation **Éliminé**. Le statut de la transaction change une fois que vous avez sélectionné les champs appropriés.

Cela change définit également automatiquement le projet sur le statut **En cours** si l’étape du projet est définie comme terminée. Le statut de l’estimation de la période du projet repasse au statut **Validé**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]