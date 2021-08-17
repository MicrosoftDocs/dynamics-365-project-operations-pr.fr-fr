---
title: Utiliser une ressource réservable comme dimension de tarification
description: Cette rubrique donne des informations sur la manière d’utiliser une ressource réservable comme dimension de tarification.
author: Rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e8487d3d32acab294bb2de16fb0278f357f774e62b553eb0c1ebd5b6246e332
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996253"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a>Utiliser une ressource réservable comme dimension de tarification

 _**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_ 

Cette rubrique donne des informations sur la manière d’utiliser une ressource réservable comme dimension de tarification. Si votre stratégie de tarification est configurée de sorte que chaque ressource réservable doit avoir un prix ou un taux de coût spécifique, utilisez une ressource réservable comme dimension de tarification.

## <a name="prerequisites"></a>Conditions préalables
Avant de suivre les procédures décrites dans cette rubrique, vous devez disposer d’une nouvelle solution de dimension de tarification pour votre organisation. Si vous n’en avez pas déjà créé une, voir [Créer des champs et des entités personnalisés](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a>Ajouter le champ Ressource réservable aux formulaires et vues
Pour que le champ **Ressource réservable** soit visible dans la solution de dimension de tarification, vous devez ajouter le champ à tous les formulaires et vues en tant qu’entité.

Le tableau suivant répertorie tous les formulaires et vues prêts à l’emploi, par entité. Vous devrez également ajouter le nouveau champ à tous les formulaires ou vues supplémentaires dans vos entités personnalisées.

|   Entity        | Formulaires   |Vues        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prix du rôle| Information | - Prix de la catégorie de ressource actifs<br> - Associé au prix de la catégorie de ressource |
|  Majoration du prix du rôle| Information| - Majorations du prix du rôle actives<br>- Associé à la majoration du prix du rôle |
|  Détail de la ligne de devis| - Informations sur le projet<br>- Création rapide de projets| - Détail de la ligne de devis actif<br>- Détails de la ligne de devis combinée<br>- Associé au détail de la ligne de devis |
|  Détail de la ligne de contrat du projet| - Informations sur le projet<br>- Création rapide de projets| - Détails de la ligne de contrat combinée<br>- Détails de la ligne de contrat active<br>- Associé aux détail de la ligne de contrat |
|  Tâche du projet| - Information<br>- Nouveau formulaire| &nbsp; |
|  Membre de l’équipe du projet| - Information<br>- Nouveau formulaire| - Membres de l’équipe du projet actifs<br>- Membres de l’équipe de projet<br>- Associé aux membres de l’équipe du projet |
|  Entrée de temps| - Information<br>- Créer une entrée de temps| - Mes entrées de temps par date<br>- Mes entrées de temps pour cette semaine<br>- Entrées de temps pour approbation|
|  Ligne de journal| - Information<br>- Création rapide| - Lignes de journal actives<br>- Associé à une Ligne de journal |
|  Détail de la ligne de facture| - Information<br>- Création rapide| - Détails de la ligne de facture actifs<br>- Transactions facturables<br>- Transactions gratuites<br>- Associé au détail de la ligne de facture <br>- Transactions non facturables|
|  Réel| - Information<br>- Chiffres réels actifs| Associé au chiffre réel |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a>Configurer une ressource réservable comme dimension de tarification
Pour configurer une ressource réservable comme dimension de tarification, procédez comme suit :

1. Accédez à **Paramètres** > **Paramètres**. 
2. Dans la page **Paramètre**, sous l’onglet **Dimensions de tarification basées sur le montant**, vérifiez que la grille affiche les enregistrements de l’entité **Dimensions de tarification**. 
2. Ajoutez la **Ressource pouvant être réservée** à cette liste de dimensions de tarification comme **msdyn_bookableresource**. 
3. Dans **Applicable au coût** et **Applicable aux ventes**, sélectionnez une valeur.
4. Dans le champ **Type de dimension**, sélectionnez **Basé sur le montant**. 
5. Sélectionnez la priorité du coût et des ventes pour la ressource réservable. En règle générale, une ressource réservable a la priorité la plus élevée lorsqu’elle est incluse en tant que dimension de tarification. Définissez la priorité sur **1** (ou **0** selon la façon dont vous comptez la priorité) pour garantir ce comportement.

## <a name="set-up-pricing-dimension-field-names"></a>Configurer les noms de champs de dimension de tarification

Lorsque le nom du champ d’une dimension de tarification dans la table **Prix du rôle** est différent de son nom de champ dans toute autre entité où le prix par défaut est utilisé, l’enregistrement de dimension de tarification doit être informé des différents noms.  

Pour une ressource réservable, l’entité **Membres de l’équipe du projet** a un nom de champ un peu différent dans ce qui est appelé sur l’entité **Prix de rôle**. 

 - **Membres de l’équipe de projet** entité = **msdyn_bookableresourceid**
 - **Prix du rôle** entité = **msdyn_bookableresource**

L’enregistrement de la dimension de tarification pour **msydn_bookableresource** doit être informé de cette différence.

1. Double-cliquez sur la ligne dans la grille **Dimensions de tarification** pour ouvrir la page de dimension **msdyn_bookableresource**.
2. Sur la page Dimension, dans l’onglet **Association**, sélectionnez **Noms des champs Dimension de tarification**.

  ![Onglet Noms des champs Dimension de tarification.](media/PD-fieldname.png)

3. Dans la vue associée qui apparaît, sélectionnez **Ajouter le nouveau nom de champ Dimension de tarification**.

  ![Ajoutez les nouveaux noms de champ Dimension de tarification.](media/Add-NewPD-fieldname.png)

  Cela ouvre la page **Nouveau nom du champ Dimension de tarification** pour **msdyn_bookableresource**. 

4. Sur la page **Nouveau nom de champ de dimension de tarification**, ajoutez **msdyn_projectteam** à **Nom logique d’entité**.
5. Ajoutez **msdyn_bookableresourceid** à **Nom de domaine**.

 ![Formulaire Nouveau nom de champ Dimension de tarification.](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]