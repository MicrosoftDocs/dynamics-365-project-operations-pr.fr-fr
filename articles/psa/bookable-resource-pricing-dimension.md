---
title: Utiliser une ressource réservable comme dimension de tarification
description: Cette rubrique donne des informations sur l’utilisation d’une ressource réservable comme dimension de tarification.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0ffbb1f7aa25e723c7842259f1c0127b3d2e26d6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012088"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a>Utiliser une ressource réservable comme dimension de tarification

[!include [banner](../includes/psa-now-project-operations.md)]

Cette rubrique donne des informations sur l’utilisation d’une ressource réservable comme dimension de tarification. Avant de commencer, si vos n’avez pas déjà créé une solution Dimension de tarification, vous devez en créer une. Si vous disposez déjà d’une solution Dimension de tarification, vous pouvez apporter vos modifications dans cette solution. Si vous n’avez pas créé de solution Dimension de tarification pour votre organisation, effectuez les procédures décrites dans la rubrique [Créer des champs et des entités personnalisés](create-custom-fields-entities.md).

## <a name="add-bookable-resource-to-forms-and-views"></a>Ajouter une ressource réservable aux formulaires et vues
Pour rendre les champs visibles dans l’interface utilisateur de la solution Dimension de tarification, vous devrez parcourir tous les formulaires et vues des entités Project Service clés et ajouter ces champs aux formulaires et vues de ces entités.
Le tableau suivant présente une liste complète des formulaires et vues prédéfinis, répertoriés par entité, qui doivent être mis à jour. S’il existe des vues ou formulaires supplémentaires dans vos personnalisations de ces entités, ajoutez également les nouveaux champs à ceux-ci.
Ouvrez l’Explorateur de solutions pour la solution de dimension de tarification puis cliquez sur **Publier toutes les personnalisations**.


|   Entité        | Formulaires   |Vues        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prix du rôle|• Informations |• Prix de la catégorie de ressource actifs<br> • Vue associée Prix de la catégorie de ressource|
|  Majoration du prix du rôle|• Informations|• Majorations du prix du rôle actives<br>• Vue associée Majoration du prix du rôle|
|  Détail de la ligne de devis|• Informations sur le projet<br>• Création rapide de projets|• Détail de la ligne de devis active<br>• Détails de la ligne de devis combinée<br>• Vue associée Détail de la ligne de devis|
|  Détail de la ligne de contrat du projet|• Informations sur le projet<br>• Création rapide de projets|• Détails de la ligne de contrat combinée<br>• Détails de la ligne de contrat active<br>• Vue associée Détails de la ligne de contrat|
|  Tâche du projet|• Informations<br>• Nouveau formulaire||
|  Membre de l’équipe du projet|• Informations<br>• Nouveau formulaire|• Membres de l’équipe du projet actifs<br>• Membres de l’équipe du projet<br>• Vue associée Membres de l’équipe du projet|
|  Entrée de temps|• Informations<br>• Créer une entrée de temps|• Mes entrées de temps par date<br>• Mes entrées de temps pour cette semaine<br>• Entrées des temps pour approbation|
|  Ligne de journal|• Informations<br>• Création rapide|• Lignes de journal actives<br>• Vue associée Ligne de journal|
|  Détail de la ligne de facture|• Informations<br>• Création rapide|• Détails de la ligne de facture active<br>• Transactions facturables<br>• Transactions gratuites<br>• Vue associée Détails de la ligne de facture<br>• Transactions non facturables|
|  Chiffre réel|• Informations<br>• Chiffres réels actifs|• Vue associée Chiffre réel|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a>Configurer une ressource réservable comme dimension de tarification

1. Dans l’interface Web, accédez à **Project Service** > **Paramètres** > **Paramètres**. Dans la page **Paramètres**, sous l’onglet **Dimensions de tarification basées sur le montant**, notez que la grille de l’onglet affiche les enregistrements de l’entité Dimensions de tarification. 
2. Ajoutez la **Ressource pouvant être réservée** à cette liste de dimensions de tarification comme **msdyn_bookableresource**. 
3. Indiquez le contexte dans lequel la ressource réservable s’exécute en tant que dimension de tarification et définissez les valeurs **Applicable aux coûts** et **Applicable aux ventes**.
4. Dans le champ **Type de dimension**, sélectionnez **Basé sur le montant**. 
5. Sélectionnez la priorité du coût et des ventes pour la ressource réservable. Généralement, si inclus comme dimension de tarification, une ressource réservable présente la priorité la plus élevée, définir cela sur **1** (ou **0** en fonction de la façon dont vous comptez la priorité) garantit ce comportement.

## <a name="set-up-pricing-dimension-field-names"></a>Configurer les noms de champs de dimension de tarification

Lorsque le nom du champ d’une dimension de tarification dans la table **Prix du rôle** est différent de son nom de champ dans toute autre entité où la valeur par défaut du prix doit fonctionner, l’enregistrement de dimension de tarification doit être mis au fait des différents noms.    
Pour une ressource réservable, l’entité **Membres de l’équipe du projet** a un nom de champ un peu différent (**msdyn_bookableresourceid**) dans ce qui est appelé sur l’entité **Prix de rôle** (**msdyn_bookableresource**). L’enregistrement de la dimension de tarification pour **msydn_bookableresource** doit être mise au fait de cela. 
1. Pour ce faire, double-cliquez sur la ligne dans la grille **Dimensions de tarification** pour ouvrir la page de dimension **msdyn_bookableresource**.
2. Sur la page Dimension, dans l’onglet **Association**, cliquez sur **Noms des champs Dimension de tarification**.

 ![Onglet Noms des champs Dimension de tarification](media/PD-fieldname.png)

4. Dans la vue associée qui apparaît, cliquez sur **Ajouter le nouveau nom de champ Dimension de tarification**.

 ![Ajouter le nouveau nom de champ Dimension de tarification](media/Add-NewPD-fieldname.png)


Cela ouvre la page **Nouveau nom du champ Dimension de tarification** pour **msdyn_bookableresource**. 

5. Ajoutez **msdyn_projectteam** au champ **Nom logique de l’entité** et **msdyn_bookableresourceid** au champ **Nom du champ**. Enregistrez l’enregistrement.

 ![Formulaire Nouveau nom de champ Dimension de tarification](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]