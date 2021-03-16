---
title: Utiliser une catégorie de transaction comme dimension de tarification
description: Cette rubrique donne des informations sur la manière d'utiliser le champ Catégorie de transaction comme dimension de tarification.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513980"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Utiliser une catégorie de transaction comme dimension de tarification


_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_


Cette rubrique explique comment utiliser le champ **Catégorie de transaction** comme dimension de tarification. 

## <a name="prerequisites"></a>Conditions préalables
Avant de suivre les procédures décrites dans cette rubrique, vous devez disposer d'une nouvelle solution de dimension de tarification pour votre organisation. Si vous n'en avez pas déjà créé une, voir [Créer des champs et des entités personnalisés comme dimensions de tarification](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Ajouter le champ Catégorie de transaction aux formulaires et vues
Pour que le champ **Catégorie de transaction** soit visible dans la solution de dimension de tarification, vous devez ajouter le champ à tous les formulaires et vues en tant qu'entité.

Le tableau suivant répertorie tous les formulaires et vues prêts à l'emploi, par entité. Vous devrez également ajouter le nouveau champ à tous les formulaires ou vues supplémentaires dans vos entités personnalisées.

|  Entity        | Formulaires     |Vues        |
| ------------------------------|---------------------------------|----------------------------------|
|  Prix du rôle| Information |- Prix de la catégorie de ressource actifs<br> - Associé au prix de la catégorie de ressource |
|  Majoration du prix du rôle| Information|- Majorations du prix du rôle actives<br>- Associé à la majoration du prix du rôle |
|  Détail de la ligne de devis|- Informations sur le projet<br>- Création rapide de projets| - Détail de la ligne de devis actif<br>- Détails de la ligne de devis combinée<br>- Associé au détail de la ligne de devis |
|  Détail de la ligne de contrat du projet|- Informations sur le projet<br>- Création rapide de projets|- Détails de la ligne de contrat combinée<br>- Détails de la ligne de contrat active<br>- Associé aux détail de la ligne de contrat |
|  Tâche du projet|- Information<br>- Nouveau formulaire| &nbsp; |
|  Membre de l'équipe du projet|- Information<br>- Nouveau formulaire|- Membres de l’équipe du projet actifs<br>- Membres de l’équipe de projet<br>- Associé aux membres de l’équipe du projet |
|  Entrée de temps|- Information<br>- Créer une entrée de temps|- Mes entrées de temps par date<br>- Mes entrées de temps pour cette semaine<br>- Entrées de temps pour approbation|
|  Ligne de journal|- Information<br>- Création rapide|- Lignes de journal actives<br>- Associé à une Ligne de journal|
|  Détail de la ligne de facture|- Information<br>- Création rapide|- Détails de la ligne de facture actifs<br>- Transactions facturables<br>- Transactions gratuites<br>- Associé au détail de la ligne de facture <br>- Transactions non facturables|
|  Réel|- Information<br>- Chiffres réels actifs| Associé au chiffre réel |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Configurer le champ Catégorie de transaction comme dimension de tarification

1. Accédez à **Paramètres** > **Paramètres**. 
2. Dans la page **Paramètres**, sous l'onglet **Dimensions de tarification basées sur le montant**, vérifiez que la grille affiche les enregistrements de l'entité **Dimensions de tarification**.
3. Ajoutez **Catégorie de transaction** à cette liste et définissez les champs **Applicable aux coûts** et **Applicable aux ventes** sur **Oui**.
4. Dans le champ **Type de dimension**, sélectionnez **Basé sur le montant**, puis sélectionnez la priorité de la **Catégorie de transaction** pour les coûts et les ventes.


[!INCLUDE[footer-include](../includes/footer-banner.md)]