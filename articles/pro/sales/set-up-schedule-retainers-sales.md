---
title: Configurer une planification de la provision
description: Cette rubrique fournit des informations sur la façon de configurer une planification de provsions dans Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a1cfd83837a91a8d1b3db6df688da6e216a90ada4735e5909a7e8cb26b87247d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994363"
---
# <a name="set-up-a-retainer-schedule"></a>Configurer une planification de la provision

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les planification de provisions sont configurées dans la page **Contrat de projet** dans Dynamics 365 Project Operations.

1. Dans la page **Contrat de projet**, sous l’onglet **Avances et provisions**, sélectionnez **Configurer une planification de provisions**.
2. Sur la page de dialogue qui s’ouvre, les champs répertoriés dans le tableau suivant sont affichés. Le tableau donne une idée de la manière dont les valeurs saisies impactent la planification de provisions qui sera créée.

| Champ | Description | Impact en aval |
| --- | --- | --- |
| Client du contrat du projet | Le client sur le contrat qui sera facturé pour cette provision ou cette avance. | Dans le cas de la présence de plusieurs clients sur le contrat et que vous souhaitez facturer un acompte ou un montant d’avance spécifique à chacun d’entre eux, créez manuellement une facture pour chaque client. |
| Début de la planification de la provision | Saisissez la date de début de la planification de provisions. | Cette date peut ne pas être la date à laquelle la première provision ou avance est créée. La date à laquelle la première provision ou avance est créée varie également en fonction de la fréquence de facturation. |
| Fin de la planification de la provision | Saisissez la date de fin de la planification de provisions. | Cette date peut ne pas être la date à laquelle la dernière provision ou avance est créée. La date à laquelle la dernière provision ou avance est créée varie également en fonction de la fréquence de facturation. |
| Nombre de provisions à créer | Lorsque vous saisissez le nombre de provisions à créer, le système utilise la date de début et la fréquence pour générer le nombre dans ce champ. | Lorsque ce champ est mis à jour manuellement, le système ignore la valeur du champ **Fin de la planification de provisions** et la remplace par le nombre spécifique de provisions ou d’avances. |
| Fréquence de facture | Il s’agit de la fréquence à laquelle l’application créera des provisions et des avances. | Cette valeur a un impact direct sur le nombre de provisions et d’avances et les dates de création. |
| Montant total | Le montant total est le montant qui est fractionné en paiements des provisions individuelles ou des avances qui seront créés. | Il n’y a pas d’impact en aval pour ce champ. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]