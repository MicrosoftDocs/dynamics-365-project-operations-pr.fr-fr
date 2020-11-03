---
title: Configurer les taux de facturation de la main-d’œuvre
description: Cette rubrique offre des informations sur la configuration des taux de facturation de la main-d’œuvre dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e6294895857442f3a24a9d73ee07d2b90926a4fb
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075802"
---
# <a name="setting-up-bill-rates-for-labor-rate-billing"></a>Configuration des taux de facturation pour la facturation du taux de main-d'œuvre 

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Chaque tarif a un ensemble de prix de rôle, ou taux de main-d'œuvre, qui sont effectifs pour le contexte et la plage de dates définie inclus dans l'en-tête du tarif. Les taux de facturation pour le temps dans Dynamics 365 Project Operations peuvent être configurés dans une seule devise, qui est la devise de l'en-tête du tarif.

1. Pour configurer les taux de facturation de la main-d'œuvre pour un tarif de vente, créez un tarif basé sur l'en-tête de tarif. 
2. Dans l'onglet **Prix du rôle** , dans la sous-grille, sélectionnez **+ Nouveau prix de rôle**. 
3. Dans le volet **Création rapide** , saisissez la combinaison du rôle et de l'unité d'organisation pour laquelle vous devez configurer le taux de facturation.

  Le tableau suivant inclut les champs de l'onglet **Général** et du volet **Création rapide** d'une ligne de prix de rôle que vous devez garder à l'esprit lorsque vous créez des prix de rôle sur un tarif de vente :

  | Champ | Emplacement | Pertinence, objectif et conseils | Impact en aval |
  | --- | --- | --- | --- |
  | Rôle | Onglet **Général** et volet **Création rapide** | Sélectionnez le rôle pour lequel vous configurez le taux de facturation. | Le rôle sur l'estimation ou les chiffres réels entrants sera mis en correspondance avec cette ligne pour établir le taux de facturation par défaut du rôle. |
  | Unité d’allocation des ressources | Onglet **Général** et volet **Création rapide** | Sélectionnez l'unité d'organisation ou la division de la société dont provient le rôle. Par exemple, un développeur de la division Robotique de Fabrikam Inde ou un développeur de la division Logiciel de Fabrikam États-Unis. | L'unité d’allocation de ressources sur l'estimation ou les chiffres réels entrants sera mise en correspondance avec cette ligne pour établir le taux de facturation par défaut du rôle. |
  | Tarif | Onglet **Général** et volet **Création rapide** | Configurez le taux de facturation pour la combinaison de rôle société d’allocation de ressources/unité d’allocation de ressources. Par exemple, un développeur de Fabrikam Inde a un taux de facturation de 100 USD ou un développeur de Fabrikam États-Unis a un taux de facturation de 150 USD. | Ce prix est le taux de tarification par défaut sur le prix unitaire de la ligne d'estimations ou de chiffres réels entrants pour la classe de transaction Temps. |
  | Devise | Onglet **Général** et volet **Création rapide**| Par défaut, la valeur de devise provient de la devise de l'en-tête du tarif de vente. Sur un tarif de vente, la devise ne peut pas être remplacée. | Cette devise est la devise par défaut sur le prix unitaire de la ligne de chiffres réels entrants pour la classe de transaction Temps. |
  | Planification d’unités | Onglet **Général** et volet **Création rapide** | Cette planification d'unité est définie par défaut sur Temps et ne peut pas être modifiée sur l'entité de prix de rôle car elle est utilisée pour exprimer les tarifs par unités de temps. | Il n'y a pas d'impact en aval pour ce champ. |
  | Unité | Onglet **Général** et volet **Création rapide** | La valeur d'unité provient du champ **Unité de temps** de l'en-tête du tarif de vente. Mais la valeur peut être remplacée. Par exemple, un développeur de Fabrikam Inde a un taux de facturation de 1 000 USD par **Jour en Inde**. Un développeur de Fabrikam États-Unis a un taux de facturation de 1500 USD par **Jour aux États-Unis**. | Lorsque le prix unitaire est défini par défaut sur une ligne d'estimation ou de chiffres réels entrants, le système utilise le système d'unités et de conversion en unités de base pour calculer un prix unitaire. Par exemple, l'estimation utilise l'équivalent de 10 **Jours en Inde** pour un développeur venant d'Inde, et l'unité Jour en Inde est définie à 10 heures. Lors de la tarification de cette ligne d'estimation, l'application calcule le prix unitaire de l'estimation de la manière suivante : 1 000 USD / 10 heures = 100 USD par heure. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Transférer la facturation ou configurer les taux de facturation pour les ressources d'autres unités d'organisation ou divisions 

Les sociétés basées sur des projets utilisent des employés de différentes divisions de la société pour travailler sur des projets. Les projets peuvent être exécutés à partir d'une division tandis que les employés ou consultants proviennent d'une division différente de la société. Le projet peut également être composé d'une combinaison de personnes de différentes divisions. Dans Project Operations, la société qui détient la livraison du projet est appelée **Unité contractuelle**. Toutes les autres divisions qui fournissent des ressources sont appelées **Unités d'allocation de ressources**. En raison des différences de coûts de main-d'œuvre entre les différentes régions et marchés du travail à travers le monde, les taux de facturation de la main-d'œuvre sont également définis différemment selon les régions.

Par exemple, un développeur de Fabrikam Inde travaillant sur un projet américain est facturé au taux de 100 USD par heure. Un développeur de Fabrikam États-Unis travaillant sur un projet américain est facturé au taux de 150 USD par heure.

### <a name="example-set-up-a-bill-rate"></a>Exemple : configurer un taux de facturation

1. Créez un tarif de vente appelé *Taux de facturation Fabrikam États-Unis* et définissez la date de validité.
2. Dans le tarif de vente, entrez les informations suivantes :

    | Rôle | Unité d’organisation | Taux de facturation |
    | --- | --- | --- |
    | Developer | Fabrikam Inde | 100 € |
    | Developer | Fabrikam Philippines | 90 USD |
    | Developer | Fabrikam États-Unis | 150 USD |

3. Attachez le tarif de vente, **Taux de facturation Fabrikam États-Unis** au tarif du projet du contrat de projet ou à un compte spécifique.
