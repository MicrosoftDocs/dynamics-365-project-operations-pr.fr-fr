---
title: Vue d’ensemble des approbations
description: Cette rubrique offre des informations sur l’utilisation des approbations dans Project Operations.
author: stsporen
ms.date: 03/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 735cd820011a4badb83dbf6540ffe9c49f960ca1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576175"
---
# <a name="approvals-overview"></a>Vue d’ensemble des approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les soumissions de temps, de dépenses et d’utilisation du matériel passent par un workflow d’approbation. Une fois les écritures approuvées, les transactions sont enregistrées en chiffres réels ou le temps est réservé dans le calendrier.

## <a name="approvals-workflow"></a>Workflow des approbations
Lorsque vous créez et soumettez une entrée de temps, de dépense ou d’utilisation du matériel, un enregistrement d’approbation est créé. L’approbateur ou le responsable du projet examine et approuve l’entrée. Si l’entrée est liée à un projet, les chiffres réels seront créés lors de son approbation. Cela permet de suivre le coût et la facturation.

## <a name="approve-an-entry"></a>Approuver une entrée
La page **Approbations** vous permet de basculer entre différentes vues afin de pouvoir afficher les différents types d’approbations.
  
1. Accédez à la page **Approbations** et sélectionnez **Dépenses**, **Temps**, **Utilisation du matériel** ou **Rappels**.
2. Passez en revue chaque approbation et sélectionnez celles que vous souhaitez approuver.
3. Sélectionnez **Approuver** pour approuver les entrées sélectionnées.
Le système traite ces entrées et crée des chiffres réels.

## <a name="reject-an-entry"></a>Refuser une entrée
En tant qu’approbateur de projet, vous devrez peut-être renvoyer une entrée à un utilisateur pour correction.
  
1. Accédez à la page **Approbations** et sélectionnez l’entrée à rejeter. 
2. Sélectionnez **Rejeter**.
3. Vous pouvez ajouter un commentaire dans la boîte de dialogue **Commentaires sur le rejet** pour informer l’utilisateur de la raison pour laquelle l’entrée est rejetée.
4. Cliquez sur **OK**. L’entrée sera retournée à l’utilisateur.
  
## <a name="cancel-approval"></a>Annuler l’approbation
Dans certains cas, vous devrez peut-être annuler une entrée précédemment approuvée. L’annulation d’une entrée précédemment approuvée aura un impact financier. 

## <a name="approving-recall-requests"></a>Demandes de rappel d’approbation
Dans certains cas, un consultant peut avoir besoin de rappeler une entrée précédemment approuvée. L’annulation d’une entrée précédemment approuvée aura un impact financier. L’approbateur de projet doit approuver le rappel pour annuler la transaction dans les chiffres réels.

## <a name="specify-project-approvers"></a>Spécifier des approbateurs de projet
Chaque projet dispose d’un certain nombre de membres de l’équipe de projet. Vous pouvez spécifier les membres de l’équipe qui sont également des approbateurs de projet.

1. Accédez à la page **Projets** et ouvrez le projet dans la liste.
2. Sur l’onglet **Équipe**, sélectionnez le membre de l’équipe qui sera un approbateur de projet, puis sélectionnez **Modifier**.
3. Définissez le champ **Approbateur du projet** sur **Oui**.
4. Sélectionnez **Enregistrer**.
5. Répétez les étapes 2 à 4 pour ajouter des approbateurs de projet supplémentaires.

## <a name="configure-the-users-manager"></a>Configurer le gestionnaire de l’utilisateur

1. Accédez à **Paramètres** > **Sécurité** > **Utilisateurs**.
2. Sélectionnez l’utilisateur auquel vous affectez un responsable et dans la zone **Informations sur l’organisation**, sélectionnez le responsable dans la liste. 
3. Sélectionnez **Enregistrer**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
