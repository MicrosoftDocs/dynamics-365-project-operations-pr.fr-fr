---
title: Estimation du coût des attributions de ressources de sous-traitance
description: Cette rubrique explique comment Microsoft Dynamics 365 Project Operations calcule l’estimation de coût des affectations de ressources sous-traitées.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f276e12713261538d1e7520dac17243e578db433
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596691"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Estimation du coût des attributions de ressources de sous-traitance

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Les affectations de tâches des membres de l’équipe de projet en sous-traitance sont chiffrées à l’aide des tarifs **Achat** joints au contrat de sous-traitance dans l’enregistrement du membre de l’équipe concerné. Cela diffère de la façon dont les affectations de ressources d’employés sont évaluées lorsque les affectations de tâches de ressources d’employés sont évaluées à l’aide des tarifs **Coût** qui sont joints à l’unité contractante du projet. 

Pour les membres d’équipe génériques qui sont en sous-traitance, les affectations sont chiffrées à l’aide de tarifs basés sur les rôles qui sont configurés dans les tarifs d’achat joints au contrat de sous-traitance. Les tarifs d’achat peuvent également être paramétrés spécifiquement pour chaque ressource. Ces tarifs spécifiques aux ressources seront prioritaires lorsque les affectations de tâches de membres nommés de l’équipe de projet sont des collaborateurs sous contrat. 

La priorité d’utilisation du tarif d’achat spécifique au rôle par rapport au tarif spécifique à la ressource se détermine en configurant la priorité des dimensions de tarification dans **Paramètres > Dimensions de tarification basées sur le montant**.

Cette fonctionnalité permettant de dériver dynamiquement les prix en fonction de la configuration des dimensions pour les tarifs d’achat des sous-traitants est similaire à la façon dont les taux de coût et de facturation sont dérivés pour les employés à temps plein. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Création d’affectations de tâches pour obtenir des estimations de coût des ressources en sous-traitance

Les affectations de tâches des sous-traitants peuvent être créées de deux manières : 
- En utilisant l’onglet **Tâches**.
- En utilisant l’onglet **Équipe**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Création d’affectations de ressources à l’aide de l’onglet Tâches
En utilisant la liste **Ressources** de l’onglet **Tâches** pour une tâche spécifique, vous pouvez créer une affectation de tâche pour une ressource nommée ou une ressource générique. Si vous sélectionnez une ressource nommée dans la liste déroulante **Ressources affectées** sur la tâche, et que cette ressource est un collaborateur sous contrat, la ressource nommée est affectée à la tâche et un enregistrement de membre de l’équipe de projet correspondant est créé avec le type de collaborateur défini comme **Collaborateur sous contrat** et la **Validité** définie sur **Non valide**. À l’étape suivante, vous devrez ouvrir l’enregistrement du membre de l’équipe de projet et sélectionner un contrat de sous-traitance et une ligne de contrat de sous-traitance. Cela mettra à jour l’affectation des tâches pour qu’elle fasse référence au contrat de sous-traitance et à la ligne de contrat de sous-traitance, et cela mettra également à jour le statut du membre de l’équipe en **Valide**.

Si vous choisissez de créer un membre d’équipe générique à partir de la liste déroulante **Ressources affectées** sur la tâche, la boîte de dialogue **Création de membre générique de l’équipe** vous permettra de sélectionner un contrat de sous-traitance et une ligne de contrat de sous-traitance. Lorsque la ressource générique est affectée à la tâche et que l’enregistrement de membre de l’équipe de projet correspondant est créé, vous remarquerez que l’enregistrement de membre de l’équipe de projet est créé avec le type de collaborateur défini sur **Collaborateur sous contrat** et la **Validité** définie sur **Valide**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Création de membres d’équipe de projet à l’aide de l’onglet Équipe
À l’aide de l’onglet Équipe du projet, vous pouvez créer un membre d’équipe générique ou nommé. Lors de la création d’un membre de l’équipe, vous pouvez sélectionner le contrat de sous-traitance et la ligne du contrat de sous-traitance. Une fois le membre de l’équipe créé, vous devrez l’affecter à une tâche à l’aide de la liste déroulante **Ressources affectées** sur la tâche. 

## <a name="updating-estimates"></a>Mise à jour des estimations
Après avoir affecté des membres de l’équipe de projet à des tâches, vous devrez accéder à l’onglet **Estimations** sur le projet et sélectionner **Mettre à jour les prix** pour vous assurer que les taux de coût des affectations de ressources des sous-traitants sont mis à jour en fonction de la liste des tarifs d’achat jointe au contrat de sous-traitance. Les estimations ne sont pas générées pour les tâches non affectées dans Microsoft Dynamics 365 Project Operations. Par conséquent, vous devrez créer des affectations de tâches pour établir le tarif et le coût des diverses tâches de votre projet. 

> [REMARQUE !] Les membres de l’équipe de projet dont le **Type de collaborateur** est **Collaborateur sous contrat** mais n’ont pas de référence à un contrat de sous-traitance sont signalés comme **Non valide** dans la grille **Membres de l’équipe de projet**. S’il existe des membres de l’équipe de projet ayant ce statut, ouvrez l’enregistrement du membre de l’équipe de projet et mettez à jour manuellement les champs de contrat et de ligne de sous-traitance afin que l’estimation des coûts financiers reflète avec précision le coût du sous-traitant dans l’onglet **Estimations**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
