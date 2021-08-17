---
title: Créer et confirmer des journaux de correction
description: Cette rubrique donne des informations sur la création et la confirmation d’un journal de correction.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: f12cdba286a9e29e2c4eb4041effbe779cba65f3562684d625b21bc3bae809d6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986713"
---
# <a name="create-and-confirm-correction-journals"></a>Créer et confirmer des journaux de correction

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Il peut arriver qu’une entrée de temps ou de dépense soit mal saisie. Un consultant peut par exemple sélectionner la mauvaise date lors de la création d’une entrée de temps ou transposer les chiffres lors de la saisie d’une dépense. Si un consultant ne peut pas mettre à jour les entrées soumises, un administrateur peut directement corriger l’entrée pour un projet.

Pour effectuer les procédures de cette rubrique, vous aurez besoin des autorisations Administrateur.

## <a name="correct-approved-time-entries"></a>Corriger les entrées d’heure approuvées     

Effectuez les étapes suivantes pour corriger des entrées de temps individuellement ou en masse pour un projet.

1. Dans la zone **Ventes**, sélectionnez **Transactions**, puis **Heure approuvée**. 

2. Dans la liste **Heure approuvée**, localisez et sélectionnez une ou plusieurs entrées d’heure approuvées à corriger. Vous pouvez utiliser le filtre pour localiser les entrées associées. Par exemple, vous pouvez filtrer sur un ID de projet et sélectionner toutes les entrées de temps approuvées ayant cet ID de projet.

3. Sélectionnez **Corriger les entrées**. Un nouveau journal de correction est automatiquement créé, avec le type **Correction de temps** attribué. Les entrées que vous avez sélectionnées sont ajoutées au journal. 

4. Sur la page **Nouveau journal**, entrez une **Description** pour votre journal de correction, puis sélectionnez l’onglet **Corrections d’entrée de temps**.  

5. Dans la section **Nouvelles valeurs pour les entrées des temps**, mettez à jour les champs avec les informations correctes si nécessaire. Par exemple, vous pouvez modifier le projet affecté ou la ressource réservable.

6. Sélectionnez **Aperçu**. Sélectionnez **OK** dans la boîte de dialogue. Sur l’onglet **Lignes de journal**, vous pouvez afficher la liste des valeurs réelles d’origine liées aux entrées de temps sélectionnées qui ont été annulées et les lignes correspondantes corrigées qui ont été créées. Si des corrections supplémentaires doivent être apportées, répétez les étapes 5 et 6. 

> [!NOTE]
> Tous les chiffres réels corrigés auront les mêmes valeurs que celles sélectionnées dans la section **Nouvelles valeurs pour les entrées des temps**.

7. Si les corrections sont correctes, sélectionnez **Confirmer**. Sélectionnez **OK** dans la boîte de dialogue.

8. Revenez dans la zone **Ventes** et sélectionnez **Projets**, puis ouvrez le projet pour lequel vous venez de mettre à jour les entrées d’heure. 

9. Sur la page **Projets**, dans l’onglet **Chiffres réels**, affichez les modifications que vous avez apportées. 

> [!NOTE]
> Si l’onglet **Chiffres réels** n’est pas visible, sélectionnez **Association** > **Chiffres réels**.  

10. Dans la liste **Vue associée Chiffre réel**, vous pouvez voir que les entrées d’heure d’origine qui ont été annulées sont toujours répertoriées, tout comme les entrées d’heure corrigées correspondantes. 

Par exemple, dans le graphique suivant, deux éléments de ligne dont la quantité est 8,00 ont des débits répertoriés dans la colonne Montant. En outre, deux éléments de ligne dont la quantité est -8,00 indiquent des montants crédités dans la colonne Montant. Ces corrections ramènent la quantité à zéro.

 
## <a name="correct-approved-expense-entries"></a>Corriger les entrées de dépense approuvées

Effectuez les étapes suivantes pour corriger une ou plusieurs entrées de dépense. 

1. Dans la zone **Ventes** du volet de navigation de gauche, sous **Transactions**, sélectionnez **Dépenses approuvées**.

2. Dans la liste **Dépenses approuvées**, sélectionnez le projet que vous souhaitez corriger, puis sélectionnez **Corriger les entrées**. Un nouveau journal de correction est automatiquement créé, avec le type **Correction de dépenses** attribué. 

3. Sur la page **Nouveau journal**, entrez une **Description** pour la correction, et sur l’onglet **Correction des dépenses** dans la section **Nouvelles valeurs pour les dépenses**, sélectionnez les champs de données à corriger pour les lignes de dépenses sélectionnées. Par exemple, vous pouvez affecter la dépense à un autre **Projet** ou corriger la **Catégorie de dépense**, la **Date de dépense**, ou la **Ressource réservable**.

4. Sélectionnez **Aperçu**. Sélectionnez **OK** dans la boîte de dialogue. 

5. Vérifiez les corrections sur l’onglet **Lignes de journal**. Vous pouvez afficher la liste des valeurs réelles d’origine liées aux entrées de dépense sélectionnées qui ont été annulées et les lignes correspondantes corrigées qui ont été créées.

6. Si les corrections sont correctes, sélectionnez **Confirmer**. Sélectionnez **OK** dans la boîte de dialogue. Si les valeurs ne s’affichent pas comme prévu, sélectionnez **Annuler** pour revenir à la liste **Dépenses approuvées**. Répétez les étapes 2 et 5. 

> [!NOTE]
> Les chiffres réels corrigés auront les mêmes valeurs que celles sélectionnées dans la section **Nouvelles valeurs pour les dépenses**.

7. Après avoir confirmé le journal de correction, revenez au projet ou aux projets que vous avez mis à jour pour afficher vos modifications.  

8. Dans la page du projet, sur l’onglet **Chiffres réels**, passez en revue **Vue associée Chiffre réel**. Les entrées originales et les entrées corrigées sont répertoriées. Le graphique suivant montre les montants d’entrée des dépenses d’origine et ceux des dépenses corrigées correspondants. 




[!INCLUDE[footer-include](../includes/footer-banner.md)]