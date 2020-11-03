---
title: Copier des opportunités basées sur des projets
description: Cette rubrique offre des informations sur la copie des devis selon les opportunités dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 89f5a63581f36b30634bdd302a6d360d6b5e75bd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075679"
---
# <a name="copy-project-based-opportunities"></a>Copier des opportunités basées sur des projets

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_


Les opportunités de projet peuvent facilement être copiées pour créer de nouvelles opportunités de projet. 

1. Accédez à la page de liste **Opportunités de projet** et sélectionnez une opportunité dans la liste. Ou ouvrez la page des détails d'une opportunité spécifique. 
2. Sur l'une ou l'autre page, sélectionnez **Copier**. Une page de dialogue s'ouvre et contient les informations de champ suivantes. Selon les valeurs sélectionnées dans cette page de dialogue, le processus de copie peut changer.

    | **Champ** | **Pertinence, objectif et conseils** | **Impact en aval** |
    | --- | --- | --- |
    | Rubrique | Entrez la rubrique pertinente de l'opportunité cible. Lorsque la boîte de dialogue s'ouvre, le système le définira sur la rubrique de l'opportunité source avec **-copy** comme suffixe. | Il n'y a pas d'impact en aval pour ce champ. |
    | Compte | Références à la société ou à l'enregistrement de compte du client. Lorsque la boîte de dialogue s'ouvre, le système le définira sur le compte de l'opportunité source. | Ce champ est le client principal de l'opportunité. |
    | Unité contractuelle | Unité organisationnelle responsable de la livraison des projets associés à cette transaction. Lorsque la boîte de dialogue s'ouvre, le système le définira sur l'unité contractuelle de l'opportunité source. | L'unité contractuelle est la division de l'entreprise qui exécute les projets après la conclusion de la transaction. Chaque unité contractuelle dispose d’une devise, et cette devise est utilisée pour déclarer les coûts estimés et réels engagés pendant le projet. |
    | Devise | Devise dans laquelle la transaction est réalisée. Lorsque la page de dialogue s'ouvre, le système le définira sur la devise de l'opportunité source. | La devise est utilisée par défaut pour un tarif et pour construire des estimations financières sur le devis. Finalement, la devise est utilisée pour facturer le client lorsque la transaction est gagnée. |
    | Copier la tarification | Une valeur Oui/Non qui indique si la tarification de l'opportunité doit être copiée à partir de l'opportunité source. | Si **Oui** est sélectionné, les tarifs sont copiés de la source vers l'opportunité cible. Si **Non** est sélectionné, les tarifs sont définis par défaut sur la base des derniers tarifs configurés. |

3. Cliquez sur **OK**. Le système crée une copie de l'opportunité de projet en fonction des paramètres sélectionnés et la nouvelle opportunité de projet est ouverte.
