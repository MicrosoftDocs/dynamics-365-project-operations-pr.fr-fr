---
title: Enregistrement du temps, des dépenses et de l’utilisation du matériel pour les composants en sous-traitance
description: Cet article explique comment le temps, les dépenses et l’utilisation des matériels enregistrés sur les projets à partir de composants sous-traités sont suivis par Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 89fbbfcd1535660e92d0cc80beb91029331e990f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261133"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>Enregistrement du temps, des dépenses et de l’utilisation du matériel sur les projets pour les composants en sous-traitance

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cet article explique comment le temps, les dépenses et l’utilisation des matériels enregistrés sur les projets à partir de composants sous-traités sont suivis par Microsoft Dynamics 365 Project Operations.

## <a name="costing-for-subcontractor-time-on-projects"></a>Chiffrage du temps des sous-traitants sur les projets
Dans Project Operations, les contractuels peuvent enregistrer le temps sur les projets de la même manière que les employés. Lors de la saisie du temps sur des projets et/ou des tâches de projet, un collaborateur contractuel peut sélectionner un sous-contrat et une ligne de contrat de sous-traitance spécifiques.

Lorsque le temps soumis par les collaborateurs contractuels est approuvé, le coût du projet est enregistré à l’aide du taux de coût unitaire défini pour cette ressource de collaborateur contractuel dans la section **Tarif des rôles** de la liste des tarifs d’achat sur le contrat de sous-traitance.

## <a name="costing-for-subcontracted-expenses-on-projects"></a>Chiffrage des dépenses de sous-traitance sur les projets
Lors de la saisie des dépenses engagées sur les projets, vous pouvez sélectionner un contrat de sous-traitance et une ligne contrat de sous-traitance sur l’entrée de dépense. 

Lorsque cette entrée de dépense est soumise et approuvée, le coût de la dépense est enregistré dans le projet sur la base du taux de coût unitaire défini pour cette catégorie de transaction dans la section **Tarifs par catégorie** de la liste des tarifs d’achat sur le contrat de sous-traitance.

## <a name="costing-for-subcontracted-materials-on-projects"></a>Chiffrage des matériels en sous-traitance sur les projets
Lors de la saisie de l’utilisation des matériels sur les projets, vous pouvez sélectionner un contrat de sous-traitance et une ligne contrat de sous-traitance dans le journal d’utilisation des matériels. Lorsque le journal d’utilisation des matériels est soumis et approuvé, le coût du matériel est enregistré dans le projet sur la base du taux de coût unitaire défini pour ce produit dans la section **Éléments tarifaires** de la liste des tarifs du contrat de sous-traitance.

L’utilisation du matériel peut également être enregistrée pour les produits hors catalogue sur les projets. Ce type d’utilisation de matériel peut également être lié à un contrat de sous-traitance et à une ligne de contrat de sous-traitance. Lors de l’enregistrement de l’utilisation de matériel pour les produits hors catalogue, vous devez saisir le coût unitaire du produit hors catalogue. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
