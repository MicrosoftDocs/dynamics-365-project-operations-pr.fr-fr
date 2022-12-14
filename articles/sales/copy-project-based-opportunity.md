---
title: Copier des opportunités de projets
description: Cet article fournit des informations sur la copie d’opportunités basées sur un projet dans Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0fe29918e14a944de7277639f752ad53513a7589
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9826125"
---
# <a name="copy-project-opportunities"></a>Copier des opportunités de projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_


Les opportunités de projet peuvent facilement être copiées pour créer de nouvelles opportunités de projet. 

1. Accédez à la page de liste **Opportunités de projet** et sélectionnez une opportunité dans la liste. Ou ouvrez la page des détails d’une opportunité spécifique. 
2. Sur l’une ou l’autre page, sélectionnez **Copier**. Une page de dialogue s’ouvre et contient les informations de champ suivantes. Selon les valeurs sélectionnées dans cette page de dialogue, le processus de copie peut changer.

    | **Champ** | **Description** | **Impact en aval** |
    | --- | --- | --- |
    | Rubrique | Entrez la rubrique pertinente de l’opportunité cible. Lorsque la boîte de dialogue s’ouvre, le système le définira sur la rubrique de l’opportunité source avec **-copy** comme suffixe. | Il n’y a pas d’impact en aval pour ce champ. |
    | Compte | Références à la société ou à l’enregistrement de compte du client. Lorsque la boîte de dialogue s’ouvre, le système le définira sur le compte de l’opportunité source. | Ce champ est le client principal de l’opportunité. |
    | Unité contractuelle | Unité organisationnelle responsable de la livraison des projets associés à cette transaction. Lorsque la boîte de dialogue s’ouvre, le système le définira sur l’unité contractuelle de l’opportunité source. | L’unité contractuelle est la division de l’entreprise qui exécute les projets après la conclusion de la transaction. Chaque unité contractuelle dispose d’une devise, et cette devise est utilisée pour déclarer les coûts estimés et réels engagés pendant le projet. |
    | Devise | Devise dans laquelle la transaction est réalisée. Lorsque la page de dialogue s’ouvre, le système le définira sur la devise de l’opportunité source. | La devise est utilisée par défaut pour un tarif et pour construire des estimations financières sur le devis. Finalement, la devise est utilisée pour facturer le client lorsque la transaction est gagnée. |
    | Copier la tarification | Une valeur Oui/Non qui indique si la tarification de l’opportunité doit être copiée à partir de l’opportunité source. | Si **Oui** est sélectionné, les tarifs sont copiés de la source vers l’opportunité cible. Si **Non** est sélectionné, les tarifs sont définis par défaut sur la base des derniers tarifs configurés. |

3. Cliquez sur **OK**. Le système crée une copie de l’opportunité de projet en fonction des paramètres sélectionnés et la nouvelle opportunité de projet est ouverte.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
