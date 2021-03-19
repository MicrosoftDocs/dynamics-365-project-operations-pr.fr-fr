---
title: Utiliser une catégorie de transaction comme dimension de tarification
description: Cette rubrique donne des informations sur l'utilisation d'une catégorie de transaction comme dimension de tarification.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ce878665384b75fc44bba2d413217857e0ee467c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281880"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utiliser une catégorie de transaction comme dimension de tarification

[!include [banner](../includes/psa-now-project-operations.md)]

Cette rubrique indique comment utiliser une catégorie de transaction comme dimension de tarification. Avant de commencer, si vos n'avez pas déjà créé une solution Dimension de tarification, vous devez en créer une. Si vous disposez déjà d'une solution Dimension de tarification, vous pouvez apporter vos modifications dans cette solution. Si vous n'avez pas créé de solution Dimension de tarification pour votre organisation, effectuez les procédures décrites dans la rubrique [Créer des champs et des entités personnalisés](create-custom-fields-entities.md).

## <a name="add-transaction-category-to-forms-and-views"></a>Ajouter une catégorie de transaction aux formulaires et vues
Pour rendre la catégorie de transaction visible dans l'interface utilisateur de la solution Dimension de tarification, vous devez parcourir tous les formulaires et vues des principales entités et ajouter ces champs aux formulaires et vues de ces entités.
Le tableau suivant présente une liste complète des formulaires et vues prédéfinis, répertoriés par entité, qui doivent être mis à jour avec les nouveaux champs. S'il existe des vues ou formulaires supplémentaires dans vos personnalisations de ces entités, ajoutez-y également les nouveaux champs.

|  Entité        | Formulaires     |Vues        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prix du rôle|• Informations |• Prix de la catégorie de ressource actifs<br> • Vue associée Prix de la catégorie de ressource|
|  Majoration du prix du rôle|• Informations|• Majorations du prix du rôle actives<br>• Vue associée Majoration du prix du rôle|
|  Détail de la ligne de devis|• Informations sur le projet<br>• Création rapide de projets|• Détail de la ligne de devis active<br>• Détails de la ligne de devis combinée<br>• Vue associée Détail de la ligne de devis|
|  Détail de la ligne de contrat du projet|• Informations sur le projet<br>• Création rapide de projets|• Détails de la ligne de contrat combinée<br>• Détails de la ligne de contrat active<br>• Vue associée Détails de la ligne de contrat|
|  Tâche du projet|• Informations<br>• Nouveau formulaire||
|  Membre de l'équipe du projet|• Informations<br>• Nouveau formulaire|• Membres de l'équipe du projet actifs<br>• Membres de l’équipe du projet<br>• Vue associée Membres de l’équipe du projet|
|  Entrée de temps|• Informations<br>• Créer une entrée de temps|• Mes entrées de temps par date<br>• Mes entrées de temps pour cette semaine<br>• Entrées des temps pour approbation|
|  Ligne de journal|• Informations<br>• Création rapide|• Lignes de journal actives<br>• Vue associée Ligne de journal|
|  Détail de la ligne de facture|• Informations<br>• Création rapide|• Détails de la ligne de facture active<br>• Transactions facturables<br>• Transactions gratuites<br>• Vue associée Détails de la ligne de facture<br>• Transactions non facturables|
|  Chiffre réel|• Informations<br>• Chiffres réels actifs|• Vue associée Chiffre réel|

## <a name="set-up-transaction-category-as-a-pricing-dimension"></a>Configurer une catégorie de transaction comme dimension de tarification

1. Dans l'interface Web, accédez à **Project Service** > **Paramètres** > **Paramètres**. 
2. Dans la page **Paramètres**, sous l'onglet **Dimensions de tarification basées sur le montant**, notez que la grille de l'onglet affiche les enregistrements de l'entité **Dimensions de tarification**.
3. Ajoutez **Catégorie de transaction** à cette liste et définissez les champs **Applicable aux coûts** et **Applicable aux ventes** sur **Oui**.
4. Dans le champ **Type de dimension**, sélectionnez **Basé sur le montant**, puis sélectionnez la priorité de la **Catégorie de transaction** pour les coûts et les ventes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]