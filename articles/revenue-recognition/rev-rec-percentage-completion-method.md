---
title: Projets d’estimation de revenus à prix fixe
description: Cette rubrique fournit des informations sur les projets d’estimation de revenus à prix fixe.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 80fe1d4171d80ca39e8b7ebb1eefaa524a4f2b07
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531420"
---
# <a name="fixed-price-revenue-estimate-projects"></a>Projets d’estimation de revenus à prix fixe 

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Lorsque vous créez une ligne de contrat de projet avec les attributs suivants dans Dynamics 365 Project Operations sur Microsoft Dataverse, le système crée automatiquement un projet d'estimation des revenus à prix fixe. Les informations de ce projet reposent sur les éléments suivants :

  - Une méthode de facturation à prix fixe.
  - Un projet associé.
  - Au moins un jalon défini sur l'onglet **Calendrier de facturation** de la page **Ligne de contrat de projet**.

## <a name="review-fixed-price-revenue-estimates-projects"></a>Réviser des projets d’estimation de revenus à prix fixe
Pour réviser des projets d'estimation des revenus à prix fixe, procédez comme suit :

1. Dans l'environnement Dynamics 365 Finance, accédez à **Gestion et comptabilité des projets** > **Projets** > **Projets d'estimation de revenus à prix fixe**.
2. Sélectionnez le projet que vous souhaitez afficher et double-cliquez sur **ID projet d'estimation** pour ouvrir l'enregistrement et revoir les détails du projet.
3. Développez l'onglet **Projet**. Vous verrez un projet dans la grille **Projets sélectionnés**. Le système l'utilise comme projet par défaut car il s'agit du projet associé à la ligne de contrat de projet. 
4. Pour modifier l'association, sélectionnez des projets supplémentaires et ajoutez-les à la grille **Projets sélectionnés**. Si plusieurs projets sont sélectionnés dans cette grille, le pourcentage d'achèvement du projet et les estimations de revenus sont calculés ensemble pour tous les projets sélectionnés.

  Le coût du projet, le profil de revenu, le modèle de coût et le code de période peuvent être définis manuellement. S'ils ne sont pas définis manuellement, les valeurs sont définies par défaut lors du premier calcul d'estimation du projet à l'aide des règles configurées pour les profils de coût et de revenu du projet.

