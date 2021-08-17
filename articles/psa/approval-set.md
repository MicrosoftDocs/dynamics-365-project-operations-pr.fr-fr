---
title: Ensembles d’approbations
description: Cette rubrique fournit des informations sur l’ensemble d’approbation, les demandes et les sous-ensembles de ces opérations.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e57944b3031ff8b6da163125bb6668875ae77bd06f23a5b8c4ef06f396210e4f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995488"
---
# <a name="approval-sets"></a>Ensembles d’approbations

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les ensembles d’approbation regroupent les demandes d’approbation en sous-ensembles d’opérations plus petits. Ce regroupement permet à Project de traiter les approbations dans l’ordre et permet le séquençage et les nouvelles tentatives. Le regroupement améliore la fiabilité et la traçabilité du traitement des approbations pour de gros volumes d’approbations.

Les ensembles d’approbation indiquent l’état de traitement global de leurs enregistrements associés. Lorsqu’un enregistrement d’approbation est traité à l’aide d’un ensemble d’approbations, l’enregistrement passe de **Envoyé** à **Approuvé**, et est dissocié de l’ensemble d’approbations. Si un enregistrement échoue lorsqu’il est soumis à l’approbation, l’enregistrement conserve le statut **Envoyé** et l’ensemble d’approbations est marqué comme ayant échoué. L’ensemble d’approbations consigne le message d’erreur de l’échec.

## <a name="processing-approvals-and-approval-sets"></a>Traitement des approbations et des ensembles d’approbations
Les approbations mises en file d’attente pour traitement sont visibles dans la vue **Approbations en cours de traitement**. Le système essaie de traiter toutes les entrées plusieurs fois de manière asynchrone, y compris en retentant une approbation si les tentatives précédentes ont échoué.

Le champ **Durée de vie de l’ensemble d’approbations** consigne le nombre de tentatives restantes pour traiter l’ensemble avant qu’il ne soit marqué comme ayant échoué.

## <a name="failed-approvals-and-approval-sets"></a>Approbations et ensembles d’approbations ayant échoué
La vue **Approbations ayant échoué** répertorie toutes les approbations qui nécessitent une intervention de l’utilisateur. Ouvrez les journaux d’ensemble d’approbations associés pour identifier la cause de l’échec.
Le fait de sélectionner **Réessayer** incrémente le compteur de durée de vie de l’ensemble d’approbations, remet l’ensemble d’approbations au statut de **Traitement en cours**, et tente de traiter les enregistrements restants.

## <a name="configure-approval-sets"></a>Configurer les ensembles d’approbation

###  <a name="enable-the-approval-sets-feature"></a>Activer la fonctionnalité Ensembles d’approbation
Avant d’activer la fonctionnalité Ensembles d’approbations, vérifiez qu’aucune approbation n’est en cours de traitement.

- Accédez à la page **Paramètres du projet** et sélectionnez **Contrôle de fonctionnalité** > **Activer les approbations modernes**.

### <a name="turn-off-the-approval-sets-feature"></a>Désactiver la fonctionnalité Ensembles d’approbation
Avant de désactiver la fonctionnalité Ensembles d’approbations, vérifiez qu’aucune approbation n’est en cours de traitement.

- Accédez à la page **Paramètres du projet** et sélectionnez **Contrôle de fonctionnalité** > **Désactiver les approbations modernes**.

### <a name="configuring-the-asynchronous-threshold"></a>Configuration du seuil asynchrone 
Lorsque des ensembles d’approbation sont créés, le traitement passe à l’arrière-plan lorsque le nombre sélectionné d’enregistrements destinés à l’approbation dépasse le seuil indiqué. Utilisez le champ **Seuil asynchrone** pour configurer le moment où le traitement des approbations doit être exécuté de manière synchrone ou asynchrone.
Les valeurs valides sont :

  - Zéro : toutes les demandes doivent être traitées de manière asynchrone. 
  - Nombres supérieurs à zéro : les approbations sont traitées de manière asynchrone uniquement lorsque le nombre d’approbations soumises dépasse cette valeur.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
