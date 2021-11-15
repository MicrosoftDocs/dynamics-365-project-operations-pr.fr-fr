---
title: Désinstallez Dynamics 365 Project Operations.
description: Cette rubrique fournit des informations sur la désinstallation de Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783640"
---
# <a name="uninstall-dynamics-365-project-operations"></a>Désinstallez Dynamics 365 Project Operations. 

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Pour désinstaller Dynamics 365 Project Operations, vous devez disposer du rôle d’administrateur.

1. Accédez à **Paramètres** > **Solutions**.

    ![Page Paramètres.](./media/uninstall-proj-ops-solutions.png)
  
2. Supprimez les solutions dans l’ordre exact dans lequel elles sont répertoriées dans le tableau suivant. 

    | Étape | Nom de la solution                                    | Note                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Si elle est introuvable, ignorez cette solution.                                                            |
    | 2 | ProjectOperations_Anchor                           | Si elle est introuvable, ignorez cette solution.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Si elle est introuvable, ignorez cette solution.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Si elle est introuvable, ignorez cette solution.                                                            |
    | 5 | ProjectService                                     | Aucune note supplémentaire.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Aucune note supplémentaire.                                                                         |
    | 7 | ProjectServiceCore                                 | Aucune note supplémentaire.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Si elle est introuvable, ignorez cette solution.                                                            |
    | 9 | FieldServiceCommon                                 | Requis pour la double écriture avec Dynamics 365 Finance ou Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Requis pour la double écriture avec Dynamics 365 Finance ou Dynamics 365 Supply Chain Management.   |
    | 11 | msdyn_TESA_Anchor                                  | Requis pour Dynamics 365 Field Service.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Requis pour Dynamics 365 Field Service.                                                     |
    | 13 | msdyn_TESA                                         | Requis pour Dynamics 365 Field Service.                                                     |
    | 14 | ResourceSchedulingControls                         | Requis pour Dynamics 365 Field Service.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Requis pour Dynamics 365 Field Service.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Requis pour Dynamics 365 Field Service.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Requis pour Dynamics 365 Field Service.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Si elle est introuvable, ignorez cette solution.                                                            |
    | 19 | Dynamics365Notes                                   | Si elle est introuvable, ignorez cette solution.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Si elle est introuvable, ignorez cette solution.                                                            |
    | 21 | DualWriteCore                                      | Si elle est introuvable, ignorez cette solution.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Si elle est introuvable, ignorez cette solution.                                                            |
    | 23 | Dynamics365AssetManagement                         | Si elle est introuvable, ignorez cette solution.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Si elle est introuvable, ignorez cette solution.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Si elle est introuvable, ignorez cette solution.                                                            |
    | 26 | HCMCommon                                          | Si elle est introuvable, ignorez cette solution.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Si elle est introuvable, ignorez cette solution.                                                            |
    | 28 | Partie                                              | Si elle est introuvable, ignorez cette solution.                                                            |
    | 29 | Dynamics365Company                                 | Si elle est introuvable, ignorez cette solution.                                                            |
    | 30 | CurrencyExchangeRates                              | Si elle est introuvable, ignorez cette solution.                                                            |
    | 31 | AssetCommon                                        | Si elle est introuvable, ignorez cette solution.                                                            |
