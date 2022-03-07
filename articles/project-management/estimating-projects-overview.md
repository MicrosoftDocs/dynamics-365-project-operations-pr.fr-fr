---
title: Concepts d’estimation financière
description: Cette rubrique fournit des informations sur les estimations financières de projets dans Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 74b2499cc706e03658cadeb088df154100051cbc7cce386b2e4d50dbdb5c197f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989188"
---
# <a name="financial-estimation-concepts"></a>Concepts d’estimation financière

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, vous pouvez estimer financièrement vos projets en deux étapes : 
1. Au cours de la phase de prévente avant que la transaction ne soit conclue. 
2. Pendant la phase d’exécution après la création du contrat de projet. 

Vous pouvez créer une estimation financière pour le travail basé sur un projet en utilisant l’une des 3 pages suivantes :
- La page **Ligne de devis**, en utilisant les détails de la ligne de devis.  
- La page **Ligne de contrat du projet**, en utilisant les détails de la ligne de contrat. 
- La page **Projet**, en utilisant les pages d’onglets **Tâches** ou **Estimations des dépenses**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Utiliser un devis de projet pour créer une estimation
Sur un devis basé sur un projet, vous pouvez utiliser l’entité **Détails de la ligne de devis** pour estimer le travail requis pour fournir un projet. Vous pouvez ensuite communiquer cette estimation au client.

Les lignes de devis basées sur un projet peuvent avoir de zéro à plusieurs détails de ligne de devis. Les détails de la ligne de devis sont utilisés pour estimer le temps, les dépenses ou les frais. Microsoft Dynamics 365 Project Operations ne permet pas des estimations matérielles sur les détails de la ligne de devis. Elles sont appelées Classes de transaction. Des montants d’estimation des taxes peuvent également être entrés dans une classe des transactions.

Outre les classes de transactions, les détails de ligne de devis sont associés à un type de transaction. Deux types de transaction sont pris en charge pour les détails de la ligne de devis : **Coût** et **Contrat du projet**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Utiliser un contrat de projet pour créer une estimation

Si vous avez utilisé un devis lorsque vous avez créé un contrat basé sur un projet, l’estimation effectuée pour chaque ligne de devis sur le devis est copiée dans le contrat du projet. La structure d’un contrat de projet est semblable à la structure du devis de projet contenant les lignes, les détails de ligne, et les planifications de factures.

Les estimations peuvent être effectuées directement dans un contrat de projet, comme dans un devis de projet. Pour un devis de projet, l’estimation est effectuée à l’aide de lignes de contrat et de détails de la ligne de contrat. Les détails de ligne de contrat peuvent également être générés à partir d’un plan de projet créé à l’aide de l’approche d’estimation ascendante.

Les détails de ligne de contrat permettent d’estimer le temps, les dépenses ou les frais. Les montants de taxe estimés peuvent également être saisis dans un détail de ligne de contrat.

Les estimations matérielles ne sont pas autorisées sur les détails de la ligne de contrat.

## <a name="use-a-project-to-create-an-estimate"></a>Utiliser un projet pour créer une estimation 

Vous pouvez évaluer le temps et les dépenses des projets. Project Operations ne prend pas en charge les estimations du matériel ou des frais des projets.

Les estimations de temps sont générées lorsque vous créez une tâche et identifiez les attributs d’une ressource générique qui est obligatoire pour effectuer la tâche. Les estimations du temps sont générées à partir des tâches de planification. Les estimations de temps ne sont pas créées si vous créez des membres d’équipe génériques en dehors du contexte de la planification.

Les estimations des dépenses sont entrées dans la grille de la page **Estimations des dépenses**.

La création d’une estimation pour un projet est considérée comme une meilleure pratique, car vous pouvez créer des estimations détaillées ascendantes pour la main-d’œuvre ou le temps et les dépenses pour chaque tâche du plan de projet. Vous pouvez ensuite utiliser cette estimation détaillée pour créer des estimations pour chaque ligne de devis et créer un devis plus crédible pour le client. Lorsque vous importez ou créez une estimation détaillée sur la ligne de devis à l’aide du plan de projet, Project Operations importe les valeurs de vente et les valeurs de coût de ces estimations. Après l’importation, vous pouvez afficher les mesures de rentabilité, de marges et de faisabilité sur le devis du projet.

## <a name="understanding-estimates"></a>Présentation des estimations

Utilisez le tableau suivant comme guide pour comprendre la logique métier dans la phase d’estimation.

| Scénario                                                                                                                                                                                                                                                                                                                                          | Enregistrement d’entité                                                                                                                                                                                                       | Type de transaction | Classe de transaction | Informations supplémentaires                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Lorsque vous devez estimer la valeur commerciale du temps sur un devis                                                                                                                                                                                                                                                                                    | L’enregistrement Détails de la ligne de devis est créé                                                                                                                                                                               | Contrat du projet | Temps        | Le champ Origine de la transaction des Détails de la ligne de devis coté ventes référence les Détails de la ligne de devis côté coût |
|                                                                                                                                                                                                                                                                                     | Un second enregistrement de Détails de la ligne de devis est créé par le système afin de stocker les valeurs des coûts. Tous les champs non monétaires sont copiés à partir des Détails de la ligne de devis de vente dans les Détails de la ligne de devis de coût par le système.                                                                                                                                                                               | Coût | Temps        | Le champ Origine de la transaction des Détails de la ligne de devis coté ventes référence les Détails de la ligne de devis côté coût |
| Lorsque vous devez estimer la valeur commerciale du temps sur un contrat                                                                                                                                                                                                                                                                                 | L’enregistrement Détails de la ligne de contrat de projet est créé                                                                                                                                                                    | Contrat du projet | Temps        | Le champ Origine de la transaction des Détails de la ligne de contrat de projet coté ventes référence les Détails de la ligne de contrat de projet côté coût      |
|                                                                                                                                                                                                                                                                                  | Un second enregistrement de Détails de la ligne de contrat de projet est créé par le système afin de stocker les valeurs des coûts. Tous les champs non monétaires sont copiés à partir des Détails de la ligne de contrat de projet de vente dans les Détails de la ligne de contrat de projet de coût par le système.                                                                                                                                                                    | Coût | Temps        | Le champ Origine de la transaction des Détails de la ligne de contrat de projet coté ventes référence les Détails de la ligne de contrat de projet côté coût      |
| Lorsque l’utilisateur décrit une ressource sur une tâche du projet                                                                                                                                                                                                                                                                                            | L’enregistrement de ligne d’estimation pour afficher la valeur commerciale de la tâche est créé lorsque la tâche est créée avec toutes les dimensions Tarification requises. Le rôle et les unités d’organisation sont les dimensions de tarification | Contrat du projet | Durée        |                                                                                   |
|     | L’enregistrement de ligne d’estimation pour afficher la valeur du coût de la tâche est créé lorsque la tâche est créée avec toutes les dimensions Tarification requises. Tous les champs non monétaires sont copiés à partir de la ligne d’estimation de vente dans la ligne d’estimation de coût par le système. Le rôle et l’unité d’organisation sont les dimensions de tarification pour les taux de coût et de facture.                                                                                                                                                                                                                | Coût             | Durée           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Personnaliser les entités Détails de la ligne de devis et Détails de la ligne de contrat

Si vous avez ajouté un champ personnalisé sur les détails de la ligne de devis et souhaitez que le système entre la valeur du champ comme valeur par défaut sur la ligne de coût associée qu’elle crée, utilisez les outils d’inscription du plug-in **PreOperationContractLineDetailUpdate** et **PreOperationQuoteLineDetailUpdate**. Ces plug-ins doivent être réenregistrés une fois les détails de la ligne de devis ou les détails de la ligne de contrat modifiés. Pour terminer le processus, procédez comme suit :

1. Ouvrez PluginRegistrationTool et connectez-vous à votre instance en ligne.
2. Sélectionnez **Rechercher** et recherchez le plug-in à mettre à jour.
3. Sélectionnez le plug-in, puis, dans la page principale, sélectionnez **Sélectionner**.
4. Sélectionnez l’étape du plug-in à mettre à jour, cliquez avec le bouton droit, puis sélectionnez **Mettre à jour**.
5. Dans la boîte de dialogue **Mettre à jour l’étape existante**, dans le champ **Attributs de filtrage**, sélectionnez le bouton de sélection (**...**) :
6. Dans la boîte de dialogue **Sélectionner les attributs**, activez les cases à cocher des attributs personnalisés.
7. Sélectionnez **OK** pour fermer la boîte de dialogue, puis sélectionnez **Mettre à jour l’étape**.
8. Répétez les étapes 1 à 7 pour le deuxième plug-in.
9. Fermez le **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
