---
title: Créer et confirmer des journaux de correction
description: Cet article fournit des informations sur la création et la confirmation d’une feuille correction.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 70886aa5a3060fa58461ce215e4de3b7286093e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928061"
---
# <a name="create-and-confirm-correction-journals"></a>Créer et confirmer des journaux de correction

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Parfois, une entrée de temps ou de dépense peut être saisie de manière incorrecte. Par exemple, un consultant peut sélectionner la mauvaise date lorsqu’il crée une entrée de temps, ou il peut sélectionner le mauvais projet lorsqu’il saisit une dépense. Si un consultant ne peut pas mettre à jour les entrées envoyées, un administrateur principal peut corriger directement les chiffres réels d’un projet.

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

 
## <a name="correct-approved-expense-entries"></a>Corriger les entrées de dépense approuvées

Effectuez les étapes suivantes pour corriger une ou plusieurs entrées de dépense. 

1. Dans la zone **Ventes** du volet de navigation de gauche, sous **Transactions**, sélectionnez **Dépenses approuvées**.

2. Dans la liste **Dépenses approuvées**, sélectionnez le projet que vous souhaitez corriger, puis sélectionnez **Corriger les entrées**. Un nouveau journal de correction est automatiquement créé, avec le type **Correction de dépenses** attribué. 

3. Sur la page **Nouveau journal**, entrez une **Description** pour la correction, et sur l’onglet **Correction des dépenses** dans la section **Nouvelles valeurs pour les dépenses**, sélectionnez les champs de données à corriger pour les lignes de dépenses sélectionnées. Par exemple, vous pouvez affecter la dépense à un autre **Projet** ou corriger la **Catégorie de dépense**, la **Date de dépense**, ou la **Ressource réservable**.

4. Sélectionnez **Aperçu**. Sélectionnez **OK** dans la boîte de dialogue. 

5. Vérifiez les corrections sur l’onglet **Lignes de journal**. Vous pouvez afficher la liste des valeurs réelles d’origine liées aux entrées de dépense sélectionnées qui ont été annulées et les lignes correspondantes corrigées qui ont été créées.

6. Si les corrections sont correctes, sélectionnez **Confirmer**. Sélectionnez **OK** dans la boîte de dialogue. Si les valeurs ne s’affichent pas comme prévu, sélectionnez **Annuler** pour revenir à la liste **Dépenses approuvées**. Répétez les étapes 2 et 5. 

7. Après avoir confirmé le journal de correction, revenez au projet ou aux projets que vous avez mis à jour pour afficher vos modifications.

8. Sur la page du projet, sur l’onglet **Chiffres réels**, passez en revue la liste **Vue associée Chiffre réel**. Les entrées originales et les entrées corrigées sont répertoriées.


## <a name="correct-approved-material-usage-logs"></a>Corriger les journaux d’utilisation du matériel approuvés

Procédez comme suit pour corriger une ou plusieurs entrées du journal d’utilisation du matériel.

1. Dans la zone **Ventes**, dans le volet de navigation de gauche, sous **Transactions**, sélectionner **Chiffres réels**.

2. Dans la liste **Chiffres réels**, utilisez des filtres de colonne pour sélectionner la classe de transaction **Matériel**, de sorte que seuls les chiffres réels des matériaux sont affichés. Utilisez d’autres filtres de colonne pour limiter davantage les chiffres réels affichés. Une fois que vous avez trouvé l’ensemble des chiffres réels souhaité, sélectionnez les valeurs réelles, puis **Corriger les entrées**. Un nouveau journal de correction est automatiquement créé, et le type **Correction du matériel** est attribué.

3. Sur la page **Nouveau journal**, dans le champ **Description**, vous pouvez saisir une description pour la correction. Ensuite, sur l’onglet **Correction du matériel**, dans la section **Nouvelles valeurs pour le matériel**, sélectionnez les champs de données à corriger pour les lignes de matériel sélectionnées. Par exemple, vous pouvez affecter le matériel à un autre projet ou corriger le produit, la date du matériel ou le contrat de sous-traitance.

4. Cliquez sur **Aperçu**. Puis, dans la boîte de dialogue suivante, cliquez sur **OK**.

5. Sur l’onglet **Lignes de journal**, vérifiez les corrections. Vous pouvez afficher une liste des chiffres réels d’origine associés aux écritures de matériel sélectionnées qui ont été contrepassées et les lignes correspondantes corrigées qui ont été créées.

6. Si les corrections sont correctes, sélectionnez **Confirmer**. Puis, dans la boîte de dialogue suivante, cliquez sur **OK**. Si les valeurs ne sont pas celles attendues, sélectionnez **Annuler** pour revenir à la liste **Chiffres réels**. Puis répétez les étapes 2 à 5.

7. Après avoir confirmé le journal de correction, revenez au projet ou aux projets que vous avez mis à jour pour afficher vos modifications.

8. Sur la page du projet, sur l’onglet **Chiffres réels**, passez en revue la liste **Vue associée Chiffre réel**. Les entrées originales et les entrées corrigées sont répertoriées.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
