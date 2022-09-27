---
title: Ensembles d’approbations
description: Cet article explique comment utiliser les ensembles d’approbation, les demandes et les sous-ensembles de ces opérations.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524913"
---
# <a name="approval-sets"></a>Ensembles d’approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Les ensembles d’approbation regroupent les demandes d’approbation en sous-ensembles d’opérations plus petits. Ce regroupement permet de traiter les approbations par projet, dans un ordre spécifique et permet de réessayer et de séquencer. Le regroupement des demandes d’approbation améliore la fiabilité et la traçabilité du traitement de gros volumes d’approbations.

Les ensembles d’approbation indiquent l’état de traitement global de leurs enregistrements associés. Lorsqu’un enregistrement d’approbation est traité à l’aide d’un ensemble d’approbations, l’enregistrement passe de **Soumis** à **Approuvé**, et n’est plus lié à l’ensemble d’approbations. Si un enregistrement échoue lorsqu’il est soumis à l’approbation, l’enregistrement conserve le statut **Envoyé** et l’ensemble d’approbations est marqué comme ayant échoué. L’ensemble d’approbations consigne le message d’erreur de l’échec.

## <a name="processing-approvals-and-approval-sets"></a>Traitement des approbations et des ensembles d’approbations
Les approbations mises en file d’attente pour traitement sont visibles dans la vue **Approbations en cours de traitement**. Le système traite toutes les entrées plusieurs fois de manière asynchrone, y compris en retentant une approbation si les tentatives précédentes ont échoué.

Le champ **Durée de vie de l’ensemble d’approbations** consigne le nombre de tentatives restantes pour traiter l’ensemble avant qu’il ne soit marqué comme ayant échoué.

Les ensembles d’approbations sont traités via l’activation périodique basée sur un **Flux de cloud** nommé **Project Service - Planifier de manière récurrente les ensembles d’approbations du projet**. Cela se trouve dans la **Solution** intitulée **Project Operations**. 

Veillez à ce que le flux soit activé en exécutant la procédure suivante.

1. En tant qu’administrateur, connectez-vous à [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Dans l’angle supérieur droit, basculez vers l’environnement que vous utilisez pour Dynamics 365 Project Operations.
3. Sélectionnez **Solutions** pour répertorier les solutions installées dans l‘environnement.
4. Dans la liste de solutions, sélectionnez **Project Operations**.
5. Remplacez le filtre **Tout** par **Flux de cloud**.
6. Vérifiez que le flux **Project Service – Planifier de manière récurrente les ensembles d’approbations du projet** est défini sur **Activé**. Si ce n’est pas le cas, sélectionnez le flux, puis **Activer**.
7. Vérifiez que le traitement a lieu toutes les cinq minutes en passant en revue la liste **Tâches système** dans la zone **Paramètrs** dans votre environnement Project Operations Dataverse.

## <a name="failed-approvals-and-approval-sets"></a>Approbations et ensembles d’approbations ayant échoué
La vue **Approbations ayant échoué** répertorie toutes les approbations qui nécessitent une intervention de l’utilisateur. Ouvrez les journaux d’ensemble d’approbations associés pour identifier la cause de l’échec.
Le fait de sélectionner **Réessayer** incrémente le compteur de durée de vie de l’ensemble d’approbations, remet l’ensemble d’approbations au statut de **Traitement en cours**, et tente de traiter les enregistrements restants.

## <a name="configure-approval-sets"></a>Configurer les ensembles d’approbation

### <a name="enable-the-approval-sets-feature"></a>Activer la fonctionnalité Ensembles d’approbation
Avant d’activer la fonctionnalité Ensembles d’approbations, vérifiez qu’aucune approbation n’est en cours de traitement. Une fois cette fonctionnalité activée, elle ne peut pas être désactivée.

- Accédez à la page **Paramètres du projet** et sélectionnez **Contrôle de fonctionnalité** > **Activer les approbations modernes**.

### <a name="configuring-the-asynchronous-threshold"></a>Configuration du seuil asynchrone 
Lorsque des ensembles d’approbation sont créés, le traitement passe à l’arrière-plan lorsque le nombre sélectionné d’enregistrements destinés à l’approbation dépasse le seuil indiqué. Utilisez le champ **Seuil asynchrone** pour configurer le moment où le traitement des approbations doit être exécuté de manière synchrone ou asynchrone. Sélectionnez l’une des valeurs suivantes :

  - Zéro : toutes les demandes doivent être traitées de manière asynchrone. 
  - Nombres supérieurs à zéro : les approbations sont traitées de manière asynchrone uniquement lorsque le nombre d’approbations soumises dépasse cette valeur.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
