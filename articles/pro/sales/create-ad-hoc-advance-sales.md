---
title: Créer une avance ad hoc sur un contrat
description: Cette rubrique fournit des informations sur la création d’une avance sur un contrat, le cas échéant.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273594"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Créer une avance ad hoc sur un contrat

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Microsoft Dynamics 365 Project Operations prend en charge les scénarios de facturation qui impliquent des acomptes et des avances. Le processus d’utilisation des **Avances** dans **Project Operations** est le même que pour les **Provisions** des contrats. 

Effectuez les étapes suivantes pour facturer une avance au client.

1. Accédez à la page **Contrat du projet**, puis sélectionnez l’onglet **Avances et provisions**.
2. Dans la sous-grille qui répertorie tous les acomptes et les avances précédemment enregistrés, sélectionnez **+ Nouvelle provision du contrat de projet**. 

    Le formulaire **Création rapide** s’ouvre pour enregistrer un acompte ou une avance.
    
3. Le tableau ci-dessous répertorie les champs d’enregistrement d’une avance et les éléments dont vous devez tenir compte lorsque vous en créez de nouvelles :

    | Champ | Description | Impact en aval |
    | --- | --- | --- |
    | **Client du contrat du projet** | Ce champ indique quel client sur le contrat sera facturé pour cette avance. | Si vous avez plusieurs clients sur le contrat et que vous souhaitez facturer un acompte ou un montant d’avance spécifique à chacun d’entre eux, créez une avance pour chaque client individuellement. |
    | **Description** | La description du motif ou du moment de l’avance pour aider à identifier cette avance. | Cette description est affichée sur la ligne de facture de cette avance. |
    | **Montant** | Le montant de l’acompte ou de l’avance. | Ce montant est affiché sur la ligne de facture de cette avance. |
    | **Date de facture** | La date à laquelle cette avance est facturée au client. | Il s’agit de la date à laquelle le processus de création de facture automatisé crée une ligne de facture pour cette avance. |
    | **Statut de la facture** | Il s’agit d’un paramètre d’option qui indique si cette avance est ajoutée à une facture en mode brouillon pour ce client. Les valeurs possibles sont :</br>- **Non prêt(e) pour la facturation**</br>- **Prêt(e) pour la facturation** | Lorsqu’une avance ou un acompte est marqué comme **Prêt à facturer**, il est ajouté comme ligne Temps sur une facture en mode brouillon. Seule une avance entièrement facturée peut être utilisée pour effectuer un rapprochement avec les coûts du projet pour la période de facturation suivante. |

4. Sélectionnez **Enregistrer et fermer** dans la boîte de dialogue Création rapide pour enregistrer l’avance ou l’acompte.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]