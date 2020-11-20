---
title: Configurer une création de facture automatisée
description: Cette rubrique fournit des informations sur la façon de configurer le système pour générer automatiquement des factures.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 295c3b099c9670c930fb2ba2fd208be63a77217f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122430"
---
# <a name="configure-automatic-invoice-creation"></a>Configurer une création de facture automatisée

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_


Effectuez les étapes suivantes pour configurer une exécution de facture automatisée dans Dynamics 365 Project operations.

1. Accédez à **Paramètres** > **Traitements par lots**.
2. Créez un traitement par lots, et nommez-le **Créer des factures dans Project Operations**. Le nom du traitement par lots doit inclure les mots « Créer des factures ».
3. Dans le champ **Type de tâche**, sélectionnez **Aucun**. Par défaut, les options **Fréquence quotidienne** et **Est actif** sont définies sur **Oui**.
4. Sélectionnez **Exécuter le flux de travail**. Dans la boîte de dialogue **Rechercher un enregistrement**, vous verrez trois workflows :

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Sélectionnez **ProcessRunCaller**, puis **Ajouter**.
6. Dans la boîte de dialogue suivante, sélectionnez **OK**. Un workflow **Veille** est suivi d’un workflow **Processus**.

  > [!NOTE]
  > Vous pouvez également sélectionner **ProcessRunner** à l’étape 5. Ensuite, lorsque vous sélectionnez **OK**, un workflow **Processus** est suivi d’un workflow **Veille**.

Les workflows **ProcessRunCaller** et **ProcessRunner** créent des factures. **ProcessRunCaller** appelle **ProcessRunner**. **ProcessRunner** est le workflow qui crée en fait les factures. Il traverse toutes les lignes de contrat pour lesquelles des factures doivent être créées, et crée des factures pour ces lignes. Pour déterminer les lignes de contrat pour lesquelles des factures doivent être créées, la tâche recherche les dates d’exécution de factures des lignes de contrat. Si des lignes de contrat qui appartiennent à un contrat disposent de la même date d’exécution de factures, les transactions sont combinées en une seule facture avec deux lignes de facture. S’il n’existe pas de transaction pour créer des factures, la tâche ignore la création de facture.

Une fois que **ProcessRunner** a fini de s’exécuter, il appelle **ProcessRunCaller**, fournit l’heure de fin, et est fermé. **ProcessRunCaller** lance alors une minuterie qui s’exécute pendant 24 heures à partir de l’heure de fin spécifiée. À la fin de la minuterie, **ProcessRunCaller** est fermé.

La tâche de traitement par lots pour la création de factures est une tâche périodique. Si ce traitement par lots est exécuté de nombreuses fois, plusieurs instances de la tâche sont créées et entraînent des erreurs. Par conséquent, vous devez démarrer le traitement par lots une seule fois, et vous devez le redémarrer uniquement s’il cesse de s’exécuter.

> [!NOTE]
> La facturation par lots ne s’exécute que pour les lignes de contrat de projet qui sont configurées par des calendriers de facturation. Une ligne de contrat avec une méthode de facturation à prix fixe doit avoir des jalons configurés. Une ligne de contrat de projet avec une méthode de facturation en régie nécessite la configuration d’un calendrier de facturation basé sur la date. Il en va de même pour une ligne de contrat basée sur un projet.     
