---
title: Configurer les taux de coûts de la main-d’œuvre – Simplifié
description: Cette rubrique offre des informations sur la configuration des taux de coût de la main-d’œuvre dans Project Operations.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 01e3b41ca5c8fcc9146186873e0f44daad020c6c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575669"
---
# <a name="set-up-labor-cost-rates---lite"></a>Configurer les taux de coûts de la main-d’œuvre – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Chaque tarif a un ensemble de taux de main-d’œuvre (prix de rôle) qui correspondent au contexte et à la plage de dates définie du tarif.

1. Créez un tarif et sous l’onglet **Prix de rôle**, dans la sous-grille, sélectionnez **Nouveau rôle**.
2. Sur la page **Création rapide**, sélectionnez le rôle et l’unité d’organisation.
3. Saisissez toutes les autres informations de champ nécessaires.

Le tableau suivant inclut certains des champs importants lors de la création de taux de main-d’œuvre sur un tarif de prix de revient.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| Rôle | Onglet **Général** et pages **Création rapide** | Sélectionnez le rôle auquel le taux de coût s’applique. | Le rôle sur l’estimation ou les chiffres réels entrants sera mis en correspondance avec cette ligne pour établir le coût par défaut du rôle. |
| Unité d’allocation des ressources | Onglet **Général** et pages **Création rapide** | Sélectionnez l’unité d’organisation ou la division de la société dont proviendra le rôle. Par exemple, un développeur de la division Robotique de Fabrikam Inde ou un développeur de la division Logiciel de Fabrikam États-Unis. | L’unité d’allocation de ressources sur l’estimation ou les chiffres réels entrants sera mise en correspondance avec cette ligne pour établir le taux de coût par défaut du rôle. |
| Tarif | Onglet **Général** et pages **Création rapide** | Configurez le taux de coût pour la combinaison rôle, société d’allocation de ressources et unité d’allocation de ressources. Par exemple, un développeur de Fabrikam Inde coûte 1 000 INR ou un développeur de Fabrikam États-Unis coûte 150 USD. | Le prix est le taux de coût établi par défaut sur le coût unitaire de la ligne d’estimations ou de chiffres réels entrants pour la classe de transaction **Temps**. |
| Devise | Onglet **Général** et pages **Création rapide** | Par défaut, la valeur de devise provient de la devise de l’en-tête du tarif de prix de revient, mais elle peut être remplacée. Par exemple, un développeur de Fabrikam Inde coûte 1 000 INR. Un développeur de Fabrikam États-Unis coûte 150 USD. | Cette devise est définie par défaut sur le coût unitaire de la ligne de coût des chiffres réels entrants pour la classe de transaction **Temps**. Sur une estimation de projet, la valeur de la devise est convertie dans la devise du projet et affichée dans la vue chronologique de l’estimation. |
| Planification d’unités | Onglet **Général** et pages **Création rapide** | La planification d’unité est définie par défaut sur Temps et ne peut pas être modifiée sur l’entité de prix de rôle car elle est utilisée pour exprimer les tarifs par unités de temps. | Il n’y a aucun impact en aval. |
| Unité | Onglet **Général** et pages **Création rapide** | Par défaut, la valeur provient du champ **Unité de temps** de l’en-tête du tarif de prix de revient. La valeur peut être remplacée. Par exemple, un développeur de Fabrikam Inde coûte 1 000 INR par **Jour en Inde**. Un développeur de Fabrikam États-Unis coûte 150 USD par **Jour aux États-Unis**. | Le système utilise le système d’unités et de conversion en unités de base pour calculer un prix unitaire destiné à calculer le prix unitaire par défaut sur une ligne d’estimation ou de chiffres réels entrants. Par exemple, une estimation utilise l’équivalent de 10 **Jours en Inde** pour un développeur venant d’Inde, et l’unité **Jour en Inde** est définie à 10 heures. Lors de la valorisation de cette ligne d’estimation, l’application calcule le coût unitaire sur l’estimation comme suit : 1 000 INR / 10 heures = 100 INR par heure qui est converti en USD et affiché comme coût unitaire sur la page **Estimations de projets**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Transférer la tarification et les coûts des ressources en dehors de votre division ou entité juridique

Dans les sociétés basées sur des projets, il est courant d’utiliser des employés de différentes entités juridiques ou divisions sur les projets. Un projet peut être exécuté par une entité juridique, alors que les employés ou consultants qui travaillent sur le projet peuvent provenir de la même entité juridique et/ou d’une autre entité juridique. Dans Dynamics 365 Project Operations, l’entité juridique propriétaire de la livraison du projet est la **Société propriétaire** et la division propriétaire de la livraison est l’**Unité contractuelle**. Les autres entités juridiques qui fournissent des ressources sont les **Sociétés d’allocation de ressources** et les divisions qui fournissent des ressources sont les **Unités d’allocation de ressources**. Dans la plupart des pays, les sociétés doivent garantir que l’entité juridique d’allocation de ressources ou la division d’allocation de ressources facture à la société propriétaire et à l’unité contractuelle l’utilisation des ressources.

Par exemple, la société Fabrikam doit s’assurer que Fabrikam Inde - Robotique a négocié une grille de tarifs des coûts avec Fabrikam États-Unis - Robotique ou Fabrikam Royaume-Uni - Robotique.

Un développeur de Fabrikam Inde - Robotique facture 100 USD lorsqu’il travaille pour Fabrikam États-Unis - Robotique et 150 USD lorsqu’il travaille pour Fabrikam Royaume-Uni - Robotique.

### <a name="set-up-costs-for-outside-resources"></a>Configurer les coûts des ressources externes

1. Créez un tarif de prix de revient appelé *Tarifs de coût Fabrikam États-Unis - Robotique* et définissez une plage de dates effective.
2. Dans le tarif des prix de revient, configurez les tarifs à l’aide des informations du tableau suivant. 

| Rôle | Société d’allocation de ressources | Unité d’allocation des ressources | Taux de coût |
| --- | --- | --- | --- |
| Developer | Fabrikam Inde | Fabrikam Inde - Robotique | 100 € |
| Developer | Fabrikam Philippines | Fabrikam Philippines - Robotique | 90 USD |
| Developer | Fabrikam États-Unis | Fabrikam États-Unis - Robotique | 150 USD |

3. Attachez ce tarif de prix de revient à l’unité d’organisation Fabrikam États-Unis - Robotique.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Configurer la tarification du transfert pour une ressource dans la devise appropriée 

Dans Project Operations, la tarification des ressources peut être configurée dans n’importe quelle devise. La devise par défaut correspond à ce qui figure sur l’en-tête du tarif, mais peut être modifiée.

En utilisant l’exemple de configuration du prix de transfert, les informations peuvent être remplacées par :

La société Fabrikam doit s’assurer que Fabrikam Inde - Robotique a négocié un taux de coût avec Fabrikam États-Unis - Robotique ou Fabrikam Royaume-Uni - Robotique.

Un développeur de Fabrikam Inde - Robotique coûte 5 000 INR lorsqu’il travaille pour Fabrikam États-Unis - Robotique et 5 500 INR lorsqu’il travaille pour Fabrikam Royaume-Uni - Robotique.

Dans le tarif des prix de revient de Fabrikam États-Unis - Robotique, les tarifs peuvent être exprimés de la manière suivante :

| Rôle | Société d’allocation de ressources | Coût |
| --- | --- | --- |
| Developer | Fabrikam Inde | 5 000 INR |
| Developer | Fabrikam États-Unis | 115 USD |

Dans le tarif des prix de revient de Fabrikam Royaume-Uni - Robotique, les tarifs peuvent être exprimés de la manière suivante :

| Rôle | Société d’allocation de ressources | Coût |
| --- | --- | --- |
| Developer | Fabrikam Inde | 5 500 INR |
| Developer | Fabrikam Royaume-Uni | 115 GBP |

Le tarif des prix de revient peut fournir des taux de main-d’œuvre dans plusieurs devises. Lors de la génération d’une estimation des coûts sur le projet, Project Operations convertira ces taux de coûts dans la devise du projet et les affichera à l’utilisateur. Lorsqu’une entrée de temps est approuvée et que les chiffres réels du coût sont créés, les chiffres réels du coût sont évalués dans la devise de cette ligne de prix de rôle correspondante dans le tarif des prix de revient. Les chiffres réels du coût pour le temps sur un même projet peuvent être enregistrés dans plusieurs devises. Cependant, lors du report ou de la synthèse des chiffres réels des coûts de main-d’œuvre au niveau du projet, Project Operations convertira tous les montants des coûts de main-d’œuvre dans la devise du projet, que l’utilisateur peut afficher.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]