---
title: Synchronisation du statut du projet pour empêcher l’accès aux projets clôturés
description: Cet article explique comment synchroniser le statut du projet pour empêcher l’accès aux projets inactifs ou clôturés.
author: ryansandnessMSFT
ms.date: 08/09/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ryansandnessMSFT
ms.openlocfilehash: 7a306da164235f36d9ed5e69196508dce6d257de
ms.sourcegitcommit: 6b6c2bfd04e3e613ed1f38355c7cd47c3a56748d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2022
ms.locfileid: "9348021"
---
# <a name="sync-project-status-to-prevent-entry-against-closed-projects"></a>Synchronisation du statut du projet pour empêcher l’accès aux projets clôturés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

## <a name="scenario"></a>Scénario

Contoso est en ligne avec Microsoft Dynamics 365 Project Operations pour les scénarios basés sur les ressources/produits non stockés. Dans le cadre des activités opérationnelles normales, des projets peuvent être achevés ou mis en attente. Vous pouvez désactiver le projet pour vous assurer qu’aucune dépense ni facture n’est générée.

## <a name="solution"></a>Solution

### <a name="prerequisites"></a>Conditions préalables

-   Microsoft Dynamics 365 Finance 10.0.29 ou version ultérieure doit être installé.
-   Le mappage de double écriture 1.0.0.3 pour Projects V2 (msdyn\_projects) doit être installé ou configuré manuellement comme décrit ci-dessous.

### <a name="create-an-updated-version-of-the-project-operations-integration-projects-v2-dual-write-map"></a>Créer une version mise à jour du mappage de double écriture Projects V2 de l'intégration de Project Operations

Pour mettre à jour le mappage à double écriture Projects V2 de Project Operations :

1. Accédez à l’espace de travail **Gestion des données** et sélectionnez **Double écriture**.
2. Sélectionnez la vignette **Double écriture**.
3. dans la colonne **Mappage de table**, localisez et sélectionnez **Project V2 (msdyn\_projects)**, puis sélectionnez Arrêter.
4. Sélectionnez le nom du mappage pour l'ouvrir, puis sélectionnez **[Aucun]**.
5. Dans la boîte de dialogue Sélectionner une colonne, sélectionnez **statecode \[Statut du projet\]**, puis sélectionnez OK. Vous pouvez saisir **state** dans la valeur du filtre pour réduire la liste.
6.  Sélectionnez **Ajouter ou modifier une transformation** dans la colonne **type de mappage** pour modifier la transformation.
7.  Dans **Type de transformation**, sélectionnez **ValueMap**.
8.  Sélectionnez **Ajouter un mappage de valeurs**, puis ajoutez les **touches** et **valeurs** suivantes :

   Touche       | active 
   ----------|-------
   InProcess | 0     
   terminé | 1     

![Capture d'écran montrant le mappage en double écriture](media/projectstage-dw-mapping.png)

9. Cliquez sur **Enregistrer**.
10. Du haut de la page **Double écriture > Projects V2 (msdyn_projects)**, sélectionnez **Enregistrer sous**.
11. Dans **Ajouter une table**, dans le champ **Éditeur**, sélectionnez **Éditeur par défaut CDS**.
12. Définissez le champ **Version** sur 1.0.0.3.
13. Saisissez une **description**, puis cliquez sur **Enregistrer**.
14. Du haut de la page **Double écriture > Projects V2 (msdyn_projects)**, sélectionnez **Exécuter** pour démarrer le mappage, puis cliquez sur **Oui** si vous êtes invité à confirmer avant l’exécution. 

### <a name="close-a-newly-completed-project"></a>Clôturer un projet récemment terminé

Dynamics 365 Finance utilise le champ **étape de projet** pour différencier les projets **en cours** ou **terminés**. Les projets **terminés** ne peuvent pas entraîner de dépenses ni être facturés aux clients.

1. Ouvrez un projet à désactiver.
2. Dans le ruban, sélectionnez **Désactiver**.

> [!NOTE]
> Vous pouvez désactiver ou fermer un projet car ils se comporteront tous les deux de la même manière dans le contexte de Finance.

3. Dans Finance, ouvrez la page **Liste de tous les projets**.
4. Vérifiez que le projet désactivé n’apparaît pas dans la liste.
5. Dans le filtre **Afficher les projets** au-dessus de la liste, modifiez la valeur de **Actif** sur **Tout**.
6. Vous verrez maintenant le projet désactivé.

Si vous tentez d’enregistrer le temps ou les dépenses pour ce projet dans Finance, le projet ne devrait pas être disponible pour être sélectionné. Si vous entrez manuellement le numéro de projet sur une dépense, vous verrez un message du type « L’étape de projet Terminé ne permet pas d’enregistrement dans le projet ». La facturation et autres fonctions connexes doivent être désactivées car elles le seront dans le contexte d’un projet fermé.

