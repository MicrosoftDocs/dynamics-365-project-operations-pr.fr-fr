---
title: Devise
description: Cette rubrique fournit des informations sur l’ajout et la suppression de types de devises dans Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 8d4e1d73dc183ed572fb5099d055d2fbe0c08746
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121215"
---
# <a name="currency"></a>Devise

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les devises déterminent les prix des produits dans le catalogue de produits et le coût des transactions, telles que les bons de commande. Si vos clients sont répartis dans différentes zones géographiques, ajoutez leurs devises pour gérer vos transactions. Ajoutez les devises les plus adaptées aux besoins actuels et futurs de votre entreprise.  

> [!NOTE]
> Si votre environnement est un environnement Common Data Service, dans le centre d’administration Power Platform, sélectionnez la page **Devises** (**Environnements** > [sélectionner un environnement] > **Paramètres** > **Entreprise** > **Devises**), la page sera vierge. En effet définir une devise n’est pas pris en charge dans les environnements Common Data Service.

## <a name="add-a-currency"></a>Ajouter une devise  
Avant de commencer cette procédure, vérifiez que votre rôle de sécurité inclut les autorisations d’administrateur système. 

1. Connectez-vous en tant qu’administrateur au centre d’administration Power Platform. 
2. Sélectionnez **Paramètres** > **Entreprise**.
3. Sélectionnez **Devises**.  
4. Sélectionnez **Nouveau**.  
5. Complétez les informations comme requis.  


   |          Champ          |                                                                                                                                                                                                                                                                                                                                                                            Description                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Type de devise**    | - **Système** : sélectionnez cette option si vous souhaitez utiliser les devises disponibles dans les applications pilotées par modèle dans Dynamics 365. Sélectionnez le bouton **Recherche** pour rechercher une devise. Lorsque vous sélectionnez un code devise, **Nom de la devise** et **Symbole monétaire** sont automatiquement ajoutés pour la devise sélectionnée.<br />- **Personnalisé** : sélectionnez cette option si vous souhaitez ajouter une devise qui n’est pas disponible dans les applications pilotées par modèle dans Dynamics 365. Dans ce cas, vous devez entrer manuellement les valeurs pour **Code devise**, **Précision de la devise**, **Nom de la devise**, **Symbole de la devise** et **Conversion monétaire**. |
   |    **Code devise**    |                                                                                                                                                                                                                                                                                                                                            Forme abrégée de la devise. Par exemple, **USD** pour dollar américain.                                                                                                                                                                                                                                                                                                                                            |
   | **Précision de la devise**  |                                                                                                                                                                                  Tapez le nombre de décimales que vous souhaitez utiliser pour la devise.  Vous pouvez ajouter une valeur comprise entre 0 et 4. **Remarque :** si vous avez défini une valeur de précision dans la boîte de dialogue **Paramètres du système**, cette valeur s’affiche ici.                                                                                                                                                                                  |
   |    **Nom de la devise**    |                                                                                                                                                                                                                                         Si vous avez sélectionné un code devise dans la liste des devises disponibles dans les applications pilotées par modèle dans Dynamics 365, le nom de la devise pour le code sélectionné s’affiche ici. Si vous avez sélectionné **Personnalisé** comme type de devise, tapez le nom de la devise.                                                                                                                                                                                                                                          |
   |   **Symbole monétaire**   |                                                                                                                                                                                                                                                                      Si vous avez sélectionné un code devise dans la liste des devises disponibles, le symbole de la devise sélectionnée s’affiche ici. Si vous avez sélectionné **Personnalisé** comme type de devise, tapez le symbole pour la nouvelle devise.                                                                                                                                                                                                                                                                       |
   | **Conversion de devise** |                                                                                                                                                                                                                                     Tapez la valeur de la devise sélectionnée sous la forme d’un dollar américain. Il s’agit du taux de conversion de la devise sélectionnée dans la devise de base. **Important :** assurez-vous de mettre à jour cette valeur aussi souvent que nécessaire pour éviter des calculs inexacts dans vos transactions.                                                                                                                                                                                                                                      |


6. Lorsque vous avez terminé, dans la barre des commandes, sélectionnez **Enregistrer** ou **Enregistrer et fermer**.  

   > [!TIP]
   >  Pour modifier une devise, cliquez sur la devise, puis entrez ou sélectionnez les nouvelles valeurs.  

## <a name="delete-a-currency"></a>Supprimer une devise  

1. Connectez-vous en tant qu’administrateur au centre d’administration Power Platform. 
2. Sélectionnez **Paramètres** > **Entreprise**.
3. Sélectionnez **Devises**.  
4. Dans la liste des devises affichées, sélectionnez la devise à supprimer.  
5. Sélectionnez **Supprimer**.  
6. Confirmez la suppression.  

> [!IMPORTANT]
>  Il est impossible de supprimer les devises en cours d’utilisation par d’autres enregistrements ; vous pouvez uniquement les désactiver. La désactivation des enregistrements de devise ne supprime pas les informations de devise stockées dans les enregistrements existants, tels que les opportunités ou les commandes. Toutefois, vous ne pourrez pas sélectionner la devise désactivée pour de nouvelles transactions.  
