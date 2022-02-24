---
title: Performances de la planification de ressources projet
description: Cette rubrique fournit des informations sur la manière d’améliorer les performances de la planification des ressources pour un grand nombre de projets.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075723"
---
# <a name="project-resource-scheduling-performance"></a>Performances de la planification de ressources projet

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Des problèmes de performances liés à la planification des ressources peuvent survenir lorsque le nombre de projets atteint des milliers. Pour améliorer les performances de planification des ressources, une fonctionnalité est disponible qui permet aux utilisateurs de réduire le temps nécessaire pour lancer le formulaire de disponibilité des ressources. Plus précisément, cela supprime le processus de synchronisation de cumul de capacité des ressources et utilise la table **ResProjectResource** pour accélérer la recherche de ressources. Notez que la table **ResRollup** ne sera plus utilisée.

> [!IMPORTANT]
> S’il existe une dépendance sur le processus de synchronisation de cumul de capacité des ressources ou sur la table **ResProjectResource**, n’utilisez pas cette fonctionnalité.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Activer l’amélioration des performances de planification des ressources
Pour activer l’amélioration des performances de planification des ressources, procédez comme suit.

1. Aller à **Gestion des fonctionnalités** > **Tout**, et dans la liste des fonctionnalités, recherchez **Activer la fonctionnalité d’amélioration des performances de planification des ressources de projet**.
2. Sélectionnez **Activer maintenant**.

> [!NOTE]
> Si vous ne trouvez pas la fonction dans la liste, sélectionnez **Rechercher des mises à jour** pour actualiser la liste.

3. Actualisez votre navigateur, puis accédez à **Gestion de projet et comptabilité** > **Périodique** > **Ressources du projet** > **Synchroniser la capacité des calendriers de ressources dans toutes les entreprises**.
4. Définissez **Supprimer les enregistrements de capacité existants** sur **Oui** pour supprimer les données précédentes. Si vous souhaitez générer des données incrémentielles, définissez-le sur **Non**.
5. Dans le champ **Code de période**, sélectionnez la période pendant laquelle les données doivent être générées. Si vous sélectionnez un code de période, il n’est pas nécessaire de définir une date de début et de fin.
6. Si vous laissez le champ **Code de période** vide, sélectionnez des dates de début et de fin spécifiques pour générer des données.
7. Cliquez sur **OK**.

 > [!NOTE]
 > Cela distribuera des données générales à la table **ResCalendarCapacity** dans toutes les entreprises de votre environnement, de sorte que le traitement par lots ne doive être exécuté que dans une seule entité juridique. Les données de ce traitement par lots sont nécessaires pour calculer la capacité des ressources par le biais du calendrier associé.

8. Aller à **Gestion de projet et comptabilité** > **Périodique** > **Ressources du projet** > **Remplir les ressources de projet dans toutes les entreprises**, puis sélectionnez **OK**. Il s’agit du script de mise à niveau des données pour les données générales dans les tables **ResProjectResource**, **ResCalendarDateTimeRange** et **ResEffectiveDateTimeRange**. Les valeurs du champ **PSAPRojSchedRole.RootActivity** sont également mises à jour. Si ce n’est pas exécuté, vous recevrez un avertissement lorsque vous essayez d’exécuter des opérations de planification des ressources.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Désactiver l’amélioration des performances de planification des ressources

1. Aller à **Gestion des fonctionnalités** > **Tout** et recherchez **Activer la fonctionnalité d’amélioration des performances de planification des ressources de projet**.
2. Sélectionnez la fonctionnalité, puis cliquez sur le bouton **Désactiver**.
3. Actualisez votre navigateur.
4. Accédez à **Gestion de projets et comptabilité** > **Périodique** > **Synchronisation des capacités** > **Synchroniser les reports de capacité des ressources**.
5. Sur la page **Synchronisation de cumul de capacité**, définissez **Supprimer les enregistrements de capacité existants** sur **Oui** pour supprimer les données précédentes. Si vous souhaitez générer des données incrémentielles, définissez-le sur **Non**.
6. Dans le champ **Code de période**, sélectionnez la période pendant laquelle les données doivent être générées. Si vous sélectionnez un code de période, il n’est pas nécessaire de définir une date de début et de fin.
7. Si vous laissez le champ **Code de période** vide, sélectionnez des dates de début et de fin spécifiques pour générer des données.
8. Cliquez sur **OK**.

> [!NOTE]
> Cela distribuera des données générales à la table **ResRollup** dans toutes les entreprises de votre environnement, de sorte que le traitement par lots ne doive être exécuté que dans une seule entité juridique. Ce traitement par lots est nécessaire pour toutes les vues **Disponibilité des ressources**. Si ce traitement par lots n’est pas exécuté, les données **ResRollup** seront générées à la volée, ce qui peut prendre du temps.
