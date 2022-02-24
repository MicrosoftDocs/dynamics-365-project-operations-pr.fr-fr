---
title: Estimations
description: Cette rubrique fournit des informations sur les estimations dans Dynamics 365 Project Service Automation.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 1/31/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2fa81067ad6e7c291b9ad9468db051e8f6187da9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151430"
---
# <a name="estimates"></a>Estimations

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Sur un devis basé sur un projet, vous pouvez utiliser l’entité Détails de la ligne de devis pour estimer le travail requis pour fournir un projet. Vous pouvez ensuite partager cette estimation avec le client.

les lignes de devis basées sur un projet n’ont aucun détail de ligne de devis. Par ailleurs, elles peuvent avoir plusieurs détails de la ligne de devis. Les détails de la ligne de devis sont utilisés pour estimer le temps, les dépenses ou les frais. PSA ne permet pas des estimations matérielles sur les détails de la ligne de devis. Elles sont appelées Classes de transaction. Des montants d’estimation des taxes peuvent également être entrés dans une classe des transactions.

Outre les classes de transaction, les détails de la ligne de devis ont un type des transactions. PSA prend en charge deux types de transaction pour les détails de la ligne de devis : **Coût** et **Contrat du projet**.

## <a name="estimate-by-using-a-contract"></a>Estimation à l’aide d’un contrat

Si vous avez utilisé un devis PSA lorsque vous avez créé un contrat basé sur un projet, l’estimation effectuée pour chaque ligne de devis sur le devis est copiée dans le contrat du projet. La structure d’un contrat de projet est semblable à la structure du devis de projet contenant les lignes, les détails de ligne, et les planifications de factures.

Les estimations peuvent être effectuées directement dans un contrat de projet, comme dans un devis de projet. Pour un devis de projet, l’estimation est effectuée à l’aide de lignes de contrat et de détails de la ligne de contrat. Les détails de la ligne de contrat peuvent également être générés depuis un plan de projet créé à l’aide de l’approche d’estimation ascendante.

Les détails de la ligne de contrat peuvent être utilisés pour estimer le temps, les dépenses ou les frais. Des montants d’estimation des taxes peuvent également être entrés dans un détail de la ligne de contrat.

PSA ne permet pas des estimations matérielles sur les détails de la ligne de contrat.

Les processus pris en charge sur un contrat de projet sont la création et la confirmation de facture. La création de facture crée un brouillon d’une facture basée sur un projet qui inclut tous les chiffres réels vente non facturés jusqu’à la date du jour.

La confirmation rend le contrat en lecture seule et remplace le statut **Brouillon** par **Confirmé**. Une fois que vous prenez cette mesure, vous ne pouvez pas l’annuler. Cette action étant définitive, il est d’usage de conserver le contrat dans un état **Brouillon**.

Les uniques différences entre les projets de contrat et les contrats confirmés sont leur statut et le fait que les brouillons de contrat peuvent être modifiés alors que les contrats confirmés ne peuvent pas. La création de facture et le suivi des chiffres réels peuvent être réalisés sur les brouillons de contrats et contrats confirmés.

PSA ne prend pas en charge les ordres de modifications dans les contrats ou les projets.

## <a name="estimating-projects"></a>Estimations de projets

Vous pouvez évaluer le temps et les dépenses des projets. PSA ne permet pas les estimations de matériaux ou de frais sur des projets.

Les estimations de temps sont générées lorsque vous créez une tâche et identifiez les attributs d’une ressource générique qui est obligatoire pour effectuer la tâche. Les estimations de temps sont générées par les tâches de planification. Les estimations de temps ne sont pas créées si vous créez des membres d’équipe génériques en dehors du contexte de la planification.

Les estimations des dépenses sont entrées dans la grille de la page **Estimations**.

## <a name="understanding-estimation"></a>Compréhension les estimations

Utilisez le tableau suivant comme guide pour comprendre la logique métier dans la phase d’estimation.

| Scénario                                                                                                                                                                                                                                                                                                                                          | Enregistrement d’entité                                                                                                                                                                                                       | Type de transaction | Classe de transaction | Informations supplémentaires                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Lorsque vous devez estimer la valeur commerciale du temps sur un devis                                                                                                                                                                                                                                                                                    | L’enregistrement Détails de la ligne de devis est créé                                                                                                                                                                               | Contrat du projet | Temps        | Le champ Origine de la transaction des Détails de la ligne de devis coté ventes référence les Détails de la ligne de devis côté coût |
|                                                                                                                                                                                                                                                                                     | Un second enregistrement de Détails de la ligne de devis est créé par le système afin de stocker les valeurs des coûts. Tous les champs non monétaires sont copiés à partir des Détails de la ligne de devis de vente dans les Détails de la ligne de devis de coût par le système.                                                                                                                                                                               | Coût | Temps        | Le champ Origine de la transaction des Détails de la ligne de devis coté ventes référence les Détails de la ligne de devis côté coût |
| Lorsque vous devez estimer la valeur commerciale du temps sur un contrat                                                                                                                                                                                                                                                                                 | L’enregistrement Détails de la ligne de contrat de projet est créé                                                                                                                                                                    | Contrat du projet | Temps        | Le champ Origine de la transaction des Détails de la ligne de contrat de projet coté ventes référence les Détails de la ligne de contrat de projet côté coût      |
|                                                                                                                                                                                                                                                                                  | Un second enregistrement de Détails de la ligne de contrat de projet est créé par le système afin de stocker les valeurs des coûts. Tous les champs non monétaires sont copiés à partir des Détails de la ligne de contrat de projet de vente dans les Détails de la ligne de contrat de projet de coût par le système.                                                                                                                                                                    | Coût | Temps        | Le champ Origine de la transaction des Détails de la ligne de contrat de projet coté ventes référence les Détails de la ligne de contrat de projet côté coût      |
| Lorsque l’utilisateur décrit une ressource sur une tâche du projet                                                                                                                                                                                                                                                                                            | L’enregistrement de ligne d’estimation pour afficher la valeur commerciale de la tâche est créé lorsque la tâche est créée avec toutes les dimensions Tarification requises. Le rôle et les unités d’organisation sont les dimensions Tarification Project Service OOB | Contrat du projet | Time        |                                                                                   |
|     | L’enregistrement de ligne d’estimation pour afficher la valeur du coût de la tâche est créé lorsque la tâche est créée avec toutes les dimensions Tarification requises. Tous les champs non monétaires sont copiés à partir de la ligne d’estimation de vente dans la ligne d’estimation de coût par le système. Le rôle et l’unité d’organisation sont les dimensions Tarification PSA OOB pour les taux de coût et de facture.                                                                                                                                                                                                                | Coût             | Temps           |                                                                                   |



## <a name="customizing-the-quote-line-detail-and-contract-line-detail-entities"></a>Personnalisation des entités Détails de la ligne de devis et Détails de la ligne de contrat

Si vous avez ajouté un champ personnalisé sur les détails de la ligne de devis et souhaitez que le système entre la valeur du champ comme valeur par défaut sur la ligne de coût associée qu’elle crée, utilisez les outils d’inscription du plug-in PreOperationContractLineDetailUpdate et PreOperationQuoteLineDetailUpdate. Ces plug-ins doivent être réenregistrés une fois les détails de la ligne de devis ou les détails de la ligne de contrat modifiés. Pour terminer le processus, procédez comme suit :

1. Ouvrez PluginRegistrationTool et connectez-vous à votre instance en ligne.
2. Sélectionnez **Rechercher** et recherchez le plug-in à mettre à jour.

    ![Boîte de dialogue Rechercher dans l’arborescence](media/basic-guide-19.png)

3. Sélectionnez le plug-in, puis, dans la page principale, sélectionnez **Sélectionner**.
4. Sélectionnez l’étape du plug-in à mettre à jour, cliquez avec le bouton droit, puis sélectionnez **Mettre à jour**.

    ![Sélectionner une étape du plug-in](media/basic-guide-20.png)

5. Dans la boîte de dialogue **Mettre à jour l’étape existante**, dans le champ **Attributs de filtrage**, sélectionnez le bouton de sélection (**...**) :
 
    ![Boîte de dialogue Mettre à jour l’étape existante](media/basic-guide-21.png)

6. Dans la boîte de dialogue **Sélectionner les attributs**, activez les cases à cocher des attributs personnalisés.

    ![Boîte de dialogue Sélectionner les attributs](media/basic-guide-22.png)

7. Sélectionnez **OK** pour fermer la boîte de dialogue, puis sélectionnez **Mettre à jour l’étape**.
 
    ![Bouton Mettre à jour l’étape](media/basic-guide-23.png)

8. Répétez les étapes 1 à 7 pour le deuxième plug-in.
9. Fermez PluginRegistrationTool.
