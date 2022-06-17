---
title: Groupes d’unités et unités
description: Cet article fournit des informations sur les groupes d’unités et les unités.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: ed413cc927901308a111263dbad1a59af8fce620
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933397"
---
# <a name="unit-groups-and-units"></a>Groupes d’unités et unités

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les groupes d’unités et les unités sont des entités de base dans Microsoft Dynamics 365. Une unité est une unité de mesure unique, et plusieurs unités peuvent être regroupées en groupes d’unités. Un groupe d’unités est parfois appelé une planification d’unités dans l’interface utilisateur (UI) de Dynamics 365. 

Voici quelques exemples d’unités et de groupes d’unités :
 
- **Groupe d’unités** : Distance 
    - **Unités** : Mile, kilomètre, etc.
- **Groupe d’unités** : Temps
    - **Unités** : Heure, jour, semaine, etc. 

Lorsque vous définissez plusieurs unités dans un groupe d’unités, vous devez également configurer un facteur de conversion entre eux en indiquant la première unité que vous avez configurée comme valeur par défaut ou unité principale du groupe d’unités. 

Par exemple, dans un groupe d’unités **Temps**, si vous configurez **Heure** comme première unité, le système indique **Heure** comme unité par défaut. Si la prochaine unité que vous définissez est **Jour**, vous devez configurer un facteur de conversion pour **Jour** sur **Heure**. Si vous ajoutez ensuite **Semaine** comme troisième unité, vous devez configurer un facteur de conversion pour **Semaine** en termes de **Jour** ou d’**Heure**. 

L’image suivante propose un exemple de configuration pour l’unité **Jour**, où le champ **Quantité** affiche le nombre d’heures dans une journée, et **Semaine**, où le champ **Quantité** affiche le nombre de jours dans une semaine.

> ![Groupe d’unités : page d’informations.](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Utilisation d’unités et de groupes d’unités

Dynamics 365 Project Service Automation utilise les unités et les groupes d’unités pour traiter les estimations et les entrées des deux dépenses et du temps. 

Pour les dépenses, chaque catégorie de dépense a un groupe d’unités une unité par défaut. Ces valeurs sont entrées en tant que valeurs par défaut sur les entrées de tarifs pour les catégories de dépenses. 

Par exemple, vous avez une catégorie de dépense nommée **Kilométrage**. Il possède un groupe d’unités appelé **Distance** et une unité par défaut nommée **Mile**. Si vous configurez le groupe d’unités **Distance** de sorte qu’il ait deux unités (**Mile** et **Kilomètre**), vous pouvez définir deux prix pour la catégorie **Kilométrage** sur un tarif : prix par mile et prix par kilomètre.

| Catégorie de dépense  | Groupe d’unités  | Unité      | Mode de tarification  | Prix unitaire  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilométrage           | Distance      | Mile      | Prix unitaire    | 10 USD            |
| Kilométrage           | Distance      | Kilomètre | Prix unitaire    |  6 USD            |

Lorsque vous entrez une dépense dans un projet, le système détermine le prix via la combinaison entre la catégorie et l’unité sur les dépenses. 

| Description de la dépense        | Catégorie de dépense  | Unité  | Quantité  | Prix unitaire   |
|----------------------------|---------------------|-------|-----------|----------------|
| Trajet en voiture vers l’emplacement du client | Kilométrage             | Mile  | 10        | 10 USD         |

Pour le temps, chaque en-tête de tarifs comporte un champ **Unité de temps par défaut**. La valeur est définie lorsque vous créez un en-tête de tarifs. Cette unité est ensuite utilisée pour définir tous les prix basés sur les rôles de ces tarifs.

Les lignes d’estimation pour le champ **Temps sur le devis** peuvent être exprimées dans n’importe quelle unité de temps. Toutefois, les lignes d’estimation sur les projets et les entrées de temps pour les projets peuvent utiliser uniquement l’unité de temps **Heure**. Si l’unité sur l’entrée de temps ou la ligne d’estimation ne correspond pas à l’unité sur la ligne des tarifs pour ce rôle, le système convertit le prix dans les unités définies dans l’estimation du projet ou la transaction réelle du projet.

L’exemple suivant montre comment PSA utilise le groupe d’unités, les unités et les facteurs de conversion.
- Unités

   - **Groupe d’unités** : Temps 
   - **Unités** : Heure 
    
    - **Jour** - Facteur de conversion : 8 heures       
    - **Semaine** - Facteur de conversion : 40 heures  
        
- Configuration des tarifs sur le projet A :

    - **Nom** : Tarifs R.-U. 2016 
    - **Unité de temps par défaut** : Jour 
    - **Devise** : GBP

| Rôle      | Groupe d’unités | Unité | Unité d’organisation | Prix   |
|-----------|------------|------|---------------------|---------|
| Développeur | Time       | Day  | Contoso UK          | 800 GBP |

### <a name="time-entry"></a>Entrée de temps

Le tableau suivant indique la transaction en résultant côté ventes créée par PSA pour un projet de trois heures.


| Projet   | Tâche    | Rôle      | Quantité | Unité  | Prix unitaire | Montant des ventes non facturé |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Projet A | Création  | Développeur | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>FAQ sur l’unité de temps

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>PSA convertit-elle dans différentes unités en cas de dépenses ?
Non. La conversion d’unités s’exécute uniquement pour le temps. Pour des dépenses, si le système ne parvient pas à trouver de prix pour la combinaison entre la catégorie et l’unité de dépenses, le prix est défini sur 0,00 par défaut.

### <a name="why-does-psa-convert-time-units"></a>Pourquoi PSA convertit-elle les unités de temps ?
Dans certains pays ou régions, il existe une obligation juridique de configuration des taux de factures en jours. La négociation de tarifs et les remises au cours du cycle du devis sont effectuées au moyen des taux de jour pour chaque rôle à facturer. L’estimation de la planification et l’entrée de temps sont effectuées en heures. Pour prendre en charge cette différence entre les unités de temps, PSA convertit les unités de temps.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Les unités de temps peuvent-elles être modifiées sur des estimations de projet ?
Non. L’estimation de la planification est actuellement limitée aux heures et ne peut pas être modifiée.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Les unités et les groupes d’unités peuvent-ils être édités, supprimés et ajoutés ?
Oui. À l’exception du groupe d’unités **Heure** et de l’unité **Heure**, toutes les unités peuvent être supprimées ou modifiées, et de nouvelles unités peuvent être ajoutées. Dans PSA, le groupe d’unités **Heure** et l’unité **Heure** ne peuvent pas être supprimés. En revanche, ils peuvent être mis à jour avec un texte traduit pour le champ **Nom**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
