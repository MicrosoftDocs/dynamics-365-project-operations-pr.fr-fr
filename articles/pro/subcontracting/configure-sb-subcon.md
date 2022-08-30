---
title: Configurer le tableau de planification pour afficher les sous-traitants et la capacité de sous-traitance
description: Cet article décrit comment configurer le Tableau de planification dans Microsoft Dynamics 365 Project Operations pour afficher la capacité des ressources sous-traitées lors de la dotation en personnel des besoins en ressources du projet.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262213"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Configurer le tableau de planification pour afficher les sous-traitants et la capacité de sous-traitance 

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Le tableau de planification dans Microsoft Dynamics 365 Project Operations peut être utilisé pour la recherche de ressources de deux manières :

- Recherche de ressources générales sans le contexte d’un besoin en ressource spécifique basé sur un projet.
- Recherche de ressources spécifiques à un besoin où le besoin du projet fournira le contexte pour les ressources suggérées.

Pour informer le tableau de planification de la capacité des ressources sous-traitées et des collaborateurs contractuels, vous devez mettre à jour les paramètres du tableau de planification. Ces mises à jour comprennent : 
- La mise à jour des paramètres du tableau de planification pour la recherche de ressources générales.
- La mise à jour des paramètres du tableau de planification pour la recherche de ressources basées sur les besoins.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Mise à jour des paramètres du tableau de planification pour la recherche de ressources générales
### <a name="update-filters-for-general-resource-search"></a>Mise à jour des filtres pour la recherche de ressources générales
Lorsque vous recherchez une ressource, les filtres disponibles sur le tableau de planification doivent être mis à jour afin que vous puissiez également rechercher des ressources externes en spécifiant tout ou partie des éléments suivants :
  - Type de collaborateur, si les ressources affichées doivent être des collaborateurs contractuels ou des employés.
  - Société fournisseur à laquelle doit appartenir une ressource.
  - Les ressources qui appartiennent à un contrat ou à une ligne de contrat de sous-traitance spécifique.
    
### <a name="update-retrieve-resource-query"></a>Mise à jour de la requête de récupération de ressources
La requête utilisée pour la recherche doit également être mise à jour pour utiliser ces attributs de filtre supplémentaires. Procédez comme suit pour mettre à jour la configuration du tableau de planification pour la recherche de ressources générales :  
1. Ouvrez les **Paramètres du tableau de planification** pour un tableau de planification spécifique.
2. Ouvrez l’onglet **Paramètres** et faites défiler jusqu’à **Autres paramètres**.
3. Dans la liste des paramètres de cette section, mettez à jour la **Disposition du filtre** en **Disposition du filtre par défaut pour Project Operations Lite**.
4. Mettez à jour la **Requête de récupération de ressources** en **Requête de récupération de ressources par défaut pour Project Operations Lite**.

![Mise à jour des paramètres du tableau de planification pour la recherche de ressources générales](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Mise à jour des paramètres du tableau de planification pour la recherche de ressources basées sur les besoins
### <a name="update-filters-for-requirement-specific-resource-search"></a>Mise à jour des filtres pour la recherche de ressources spécifiques à un besoin 
Lorsque vous recherchez une ressource, les filtres disponibles sur le tableau de planification doivent être mis à jour afin que vous puissiez également rechercher des ressources externes en spécifiant tout ou partie des éléments suivants :
 - Type de collaborateur, si les ressources affichées doivent être des collaborateurs contractuels ou des employés.
 - Société fournisseur à laquelle doit appartenir une ressource.
 - Les ressources qui appartiennent à un contrat ou à une ligne de contrat de sous-traitance spécifique.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Mise à jour de la requête de récupération de ressources pour la recherche de ressources spécifiques à un besoin 
La requête utilisée pour la recherche doit également être mise à jour pour utiliser ces attributs de filtre supplémentaires. Procédez comme suit pour mettre à jour la configuration du tableau de planification pour la recherche de ressources spécifiques à un besoin :

1. Ouvrez les **Paramètres du tableau de planification** pour un tableau de planification spécifique, puis sélectionnez **Ouvrir les paramètres par défaut** pour ouvrir les paramètres de recherche spécifique aux besoins.
2. Ouvrez l’onglet **Paramètres** et faites défiler jusqu’à **Autres paramètres**.
3. Dans la liste des paramètres de cette section, mettez à jour la **Disposition du filtre** en **Disposition du filtre par défaut pour Project Operations Lite**.
4. Mettez à jour la **Requête de récupération de ressources** en **Requête de récupération de ressources par défaut pour Project Operations Lite**.
5. Ouvrez l’onglet **Types de planification** et accédez à **Projet**.
6. Sous les paramètres de **Projet**, mettez à jour la **Requête de récupération de ressources de l’Assistant Planifier** en **Requête de récupération de ressources par défaut pour Project Operations Lite** et mettez à jour la **Requête de récupération des contraintes de l’Assistant Planifier** en **Requête de récupération des contraintes par défaut pour Project Operations Lite**.

![Mise à jour des paramètres du tableau de planification pour la recherche de ressources basées sur les besoins](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
