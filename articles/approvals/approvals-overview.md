---
title: Vue d’ensemble des approbations
description: Cette rubrique offre des informations sur l’utilisation des approbations dans Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 37994422e9146765076fdbb77f5c763b4f1d0802
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961163"
---
# <a name="approvals-overview"></a>Vue d’ensemble des approbations

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les envois de temps et de dépenses passent par un workflow d’approbation. Une fois les écritures approuvées, les transactions sont enregistrées en chiffres réels ou le temps est réservé dans le calendrier.

## <a name="approvals-workflow"></a>Workflow des approbations
Lorsque vous créez et envoyez une entrée de temps ou de dépense, une entrée d’approbation est créée. L’approbateur de projet ou votre responsable examine et approuve votre saisie. Si l’entrée est liée à un projet, lorsqu’elle est approuvée, les chiffres réels seront créés. Cela permet de suivre le coût et la facturation. 

## <a name="approve-an-entry"></a>Approuver une entrée
Le formulaire **Approbations** vous permet de basculer entre différentes vues afin de pouvoir afficher les différents types d’approbations.
  
1. Accédez au formulaire **Approbations** et sélectionnez **Dépenses**, **Temps**, ou **Rappels**.
2. Passez en revue chaque approbation et sélectionnez celles que vous souhaitez approuver.
3. Sélectionnez **Approuver** pour approuver les entrées sélectionnées.
Le système traitera ces entrées et créera des chiffres réels ou une réservation.

## <a name="reject-an-entry"></a>Refuser une entrée
En tant qu’approbateur de projet, vous devrez peut-être renvoyer une entrée à un utilisateur pour correction.
  
1. Accédez au formulaire **Approbations** et sélectionnez l’entrée à rejeter. 
2. Sélectionnez **Rejeter**.
3. Facultatif – Ajoutez un commentaire dans la boîte de dialogue **Commentaires de rejet** pour informer l’utilisateur de la raison pour laquelle l’entrée est rejetée.
4. Cliquez sur **OK**. L’entrée sera retournée à l’utilisateur.
  
## <a name="recall-entries"></a>Rappeler des entrées
À un moment donné, vous devrez peut-être rappeler une entrée soumise. Si l’entrée n’a pas été approuvée, elle sera retournée immédiatement. Une entrée approuvée peut cependant avoir un impact matériel. L’approbateur de projet doit approuver le rappel afin d’annuler la transaction dans les chiffres réels.

## <a name="specify-project-approvers"></a>Spécifier des approbateurs de projet
Chaque projet dispose d’un certain nombre de membres de l’équipe de projet. Vous pouvez spécifier les membres de l’équipe qui sont également des approbateurs de projet.

1. Accédez au formulaire **Projets** et ouvrez le projet dans la liste.
2. Sur l’onglet **Équipe**, sélectionnez le membre de l’équipe qui sera un approbateur de projet, puis sélectionnez **Modifier**.
3. Définissez le champ **Approbateur du projet** sur **Oui**.
4. Sélectionnez **Enregistrer**.
5. Répétez les étapes 2 à 4 pour ajouter des approbateurs de projet supplémentaires.

## <a name="configure-the-users-manager"></a>Configurer le gestionnaire de l’utilisateur

1. Accédez à **Paramètres** > **Sécurité** > **Utilisateurs**.
2. Sélectionnez l’utilisateur auquel vous affectez un responsable et dans la zone **Informations sur l’organisation**, sélectionnez le responsable dans la liste. 
3. Sélectionnez **Enregistrer**.


