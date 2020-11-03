---
title: Corrections en masse des chiffres réels créés par des entrées de temps et de dépenses approuvées
description: Cette rubrique explique comment un administrateur peut apporter des corrections individuelles ou en masse aux entrées de temps ou de dépenses précédemment approuvées si la facturation n'a pas été effectuée.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075916"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>Corrections en masse des chiffres réels créés par des entrées de temps et de dépenses approuvées

Il peut arriver qu'une entrée de temps ou de dépense soit mal saisie. Un consultant peut par exemple sélectionner la mauvaise date lors de la création d'une entrée de temps ou transposer les chiffres lors de la saisie d'une dépense. Si un consultant ne peut pas mettre à jour les entrées soumises, un administrateur peut directement corriger l'entrée pour un projet.

Pour effectuer les procédures de cette rubrique, vous aurez besoin des autorisations Administrateur.

## <a name="correct-approved-time-entries"></a>Corriger les entrées d'heure approuvées     

Effectuez les étapes suivantes pour corriger des entrées de temps individuellement ou en masse pour un projet.

1. Dans la zone **Ventes** , sélectionnez **Transactions** , puis **Heure approuvée**. 

2. Dans la liste **Heure approuvée** , localisez et sélectionnez une ou plusieurs entrées d'heure approuvées à corriger. Vous pouvez utiliser le filtre pour localiser les entrées associées. Par exemple, vous pouvez filtrer sur un ID de projet et sélectionner toutes les entrées de temps approuvées ayant cet ID de projet.

3. Sélectionnez **Corriger les entrées**. Un nouveau journal de correction est automatiquement créé, avec le type **Correction de temps** attribué. Les entrées que vous avez sélectionnées sont ajoutées au journal. 

4. Sur la page **Nouveau journal** , entrez une **Description** pour votre journal de correction, puis sélectionnez l'onglet **Corrections d'entrée de temps**.  
5. Dans la section **Nouvelles valeurs pour les entrées des temps** , mettez à jour les champs avec les informations correctes si nécessaire. Par exemple, vous pouvez modifier le projet affecté ou la ressource réservable.

6. Sélectionnez **Aperçu**. Sélectionnez **OK** dans la boîte de dialogue. Sur l'onglet **Lignes de journal** , vous pouvez afficher la liste des valeurs réelles d'origine liées aux entrées de temps sélectionnées qui ont été annulées et les lignes correspondantes corrigées qui ont été créées. Si des corrections supplémentaires doivent être apportées, répétez les étapes 5 et 6. 

> [!NOTE]
> Tous les chiffres réels corrigés auront les mêmes valeurs que celles sélectionnées dans la section **Nouvelles valeurs pour les entrées des temps**.

7. Si les corrections sont correctes, sélectionnez **Confirmer**. Sélectionnez **OK** dans la boîte de dialogue.

8. Revenez dans la zone **Ventes** et sélectionnez **Projets** , puis ouvrez le projet pour lequel vous venez de mettre à jour les entrées d'heure. 

9. Sur la page **Projets** , dans l'onglet **Chiffres réels** , affichez les modifications que vous avez apportées. 

> [!NOTE]
> Si l'onglet **Chiffres réels** n'est pas visible, sélectionnez **Association** > **Chiffres réels**.  

10. Dans la liste **Vue associée Chiffre réel** , vous pouvez voir que les entrées d'heure d'origine qui ont été annulées sont toujours répertoriées, tout comme les entrées d'heure corrigées correspondantes. 

Par exemple, dans le graphique suivant, deux éléments de ligne dont la quantité est 8,00 ont des débits répertoriés dans la colonne Montant. En outre, deux éléments de ligne dont la quantité est -8,00 indiquent des montants crédités dans la colonne Montant. Ces corrections ramènent la quantité à zéro.

![Liste de la vue Chiffre réel associée](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>Corriger les entrées de dépense approuvées

Effectuez les étapes suivantes pour corriger une ou plusieurs entrées de dépense. 

1. Dans la zone **Ventes** du volet de navigation de gauche, sous **Transactions** , sélectionnez **Dépenses approuvées**.

2. Dans la liste **Dépenses approuvées** , sélectionnez le projet que vous souhaitez corriger, puis sélectionnez **Corriger les entrées**. Un nouveau journal de correction est automatiquement créé, avec le type **Correction de dépenses** attribué. 

3. Sur la page **Nouveau journal** , entrez une **Description** pour la correction, et sur l'onglet **Correction des dépenses** dans la section **Nouvelles valeurs pour les dépenses** , sélectionnez les champs de données à corriger pour les lignes de dépenses sélectionnées. Par exemple, vous pouvez affecter la dépense à un autre **Projet** ou corriger la **Catégorie de dépense** , la **Date de dépense** , ou la **Ressource réservable**.

4. Sélectionnez **Aperçu**. Sélectionnez **OK** dans la boîte de dialogue. 

5. Vérifiez les corrections sur l'onglet **Lignes de journal**. Vous pouvez afficher la liste des valeurs réelles d'origine liées aux entrées de dépense sélectionnées qui ont été annulées et les lignes correspondantes corrigées qui ont été créées.

6. Si les corrections sont correctes, sélectionnez **Confirmer**. Sélectionnez **OK** dans la boîte de dialogue. Si les valeurs ne s'affichent pas comme prévu, sélectionnez **Annuler** pour revenir à la liste **Dépenses approuvées**. Répétez les étapes 2 et 5. 

> [!NOTE]
> Les chiffres réels corrigés auront les mêmes valeurs que celles sélectionnées dans la section **Nouvelles valeurs pour les dépenses**.

7. Après avoir confirmé le journal de correction, revenez au projet ou aux projets que vous avez mis à jour pour afficher vos modifications.  

8. Dans la page du projet, sur l'onglet **Chiffres réels** , passez en revue **Vue associée Chiffre réel**. Les entrées originales et les entrées corrigées sont répertoriées. Le graphique suivant montre les montants d'entrée des dépenses d'origine et ceux des dépenses corrigées correspondants. 

![Expense_actuals](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
