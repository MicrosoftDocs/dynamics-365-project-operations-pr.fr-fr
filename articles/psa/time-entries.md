---
title: Créer des entrées de temps
description: Cet article donne des informations sur la création d’entrées de temps.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 1b707ccb970365ddbac75646da902733e2976d48
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930775"
---
# <a name="create-time-entries"></a>Créer des entrées de temps

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dans les versions précédentes de Dynamics 365 Project Service Automation, les entrées de temps étaient créées chaque semaine. Dans la version 3 de Project Service Automation, les entrées de temps sont créées chaque jour. Toutefois, une fois que quelques entrées de temps ont été créées, vous pouvez les copier en bloc ou en créer d’autres en bloc.

## <a name="create-a-time-entry"></a>Créer une entrée de temps

Pour créer une entrée de temps, procédez comme suit.

1. Dans la page **Entrées de temps**, sélectionnez **Nouveau**.
2. Dans la boîte de dialogue **Création rapide : Entrée de temps**, entrez la durée de l’entrée de temps en minutes, heures ou jours. La durée doit être entrée dans l’un des formats suivants : *x* minutes, *x* heures ou *x* jours. Les heures et les jours peuvent également être entrés sous forme de valeurs décimales, par exemple *x,x* heures » ou *x,x* jours.
3. Sélectionnez le type d’entrée de temps et le projet pour lequel vous créez l’entrée de temps.
4. Dans le champ **Tâche du projet**, recherchez la tâche pour cette entrée de temps.

    > [!NOTE]
    > Si vous créez une entrée de temps pour une tâche qui n’est pas affectée à un utilisateur, dans le champ **Tâche du projet**, sélectionnez le bouton **Rechercher**, sélectionnez **Modifier la vue**, puis sélectionnez **Toutes les tâches du projet actives** pour répertorier toutes les tâches.

5. Entrez une description, si nécessaire, puis sélectionnez **Enregistrer et fermer**.

Une fois l’entrée de temps créée et stockée, vous pouvez la modifier dans la grille d’entrée de temps. La grille d’entrée de temps prend en charge deux formats :

- Vous pouvez créer des entrées de temps au format **hh:mm**. Ce format est ensuite converti en heures et fractions.
- Vous pouvez entrer des heures et des fractions directement.

Notez que les fractions d’une heure ne sont pas des minutes. Par conséquent, 1,5 heure représente 1 heure et 30 minutes. La même règle s’applique aux fractions d’un jour. Un jour est égal à 24 heures, et 0,5 jour représente 12 heures.

## <a name="bulk-create-time-entries"></a>Création d’entrées de temps en bloc

Une fois que quelques entrées de temps ont été créées, vous pouvez les copier pour créer des entrées de temps supplémentaires en bloc.

1. Dans la page **Entrées de temps**, sélectionnez **Copier la semaine**.
2. Dans le groupe de champs **À partir de la période**, dans les champs **Date de début** et **Date de fin**, définissez la plage de dates à partir de laquelle copier les entrées de temps.
3. Dans le groupe de champs **Vers la période**, dans le champ **Date de début**, spécifiez la date pour laquelle créer des entrées de temps.
4. Sélectionnez **Copier** pour créer une copie des entrées de temps correspondant au jour de la semaine spécifiée dans le groupe de champs **Vers la période**. Par exemple, l’entrée de temps pour le lundi de la semaine dernière est copiée dans le lundi de la semaine spécifiée dans le groupe de champs **Vers la période**.

## <a name="import-data-for-time-entries"></a>Importer des données pour les entrées de temps

Vous pouvez importer des données à partir des réservations et des affectations du projet. Lorsque vous importez des données, vous pouvez spécifier la plage de dates des réservations à importer, puis sélectionner explicitement les réservations devant être créées comme entrées de temps **Brouillon**.

## <a name="group-by-sort-search-and-filter-capabilities"></a>Fonctionnalités de regroupement, de tri, de recherche et de filtrage

Vous pouvez regrouper et filtrer des entrées de temps en fonction des dimensions spécifiées dans les colonnes. Dans le champ **Regrouper par**, sélectionnez la dimension à utiliser pour filtrer des entrées de temps. Vous pouvez également trier les enregistrements d’entrée de temps dans l’ordre croissant ou décroissant à l’aide de la flèche de tri des en-têtes de colonne. En outre, vous pouvez afficher ou masquer les entrées en sélectionnant le bouton **Filtrer** sur les en-têtes de colonne, puis, dans la zone **Rechercher**, entrez le texte à utiliser pour rechercher des entrées de temps par nom de projet, tâche de projet, entrée de temps ou ressource.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
