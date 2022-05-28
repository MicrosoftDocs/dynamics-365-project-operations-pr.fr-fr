---
title: Configurer des rôles sur des modèles de structure de répartition du travail
description: Cette rubrique fournit des informations sur la configuration des informations de rôle sur les modèles de structure de répartition du travail.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 35ab88d61c9b1e9d9aebeb776d6a7783b96c62f6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682845"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Configurer des rôles sur des modèles de structure de répartition du travail

[!include [banner](../includes/banner.md)]

Les chefs de projet peuvent configurer des modèles de structure de répartition du travail qu’ils peuvent appliquer lorsqu’ils créent une structure de répartition du travail pour de nouveaux projets. Les chefs de projet peuvent ajouter des rôles lorsqu’ils créent un modèle. Utilisez la procédure suivante pour attribuer un rôle à un modèle de structure de répartition du travail.

1. Sélectionnez **Gestion de projets et comptabilité** > **Paramétrage** > **Projets** > **Modèles de structure de répartition du travail**.
2. Sélectionnez **Détails** pour un modèle de structure de répartition du travail sélectionné.
3. Sélectionnez une tâche dans la liste, puis, dans le champ **Rôle**, sélectionnez un rôle à attribuer à la tâche.

## <a name="work-with-a-wbs"></a>Utiliser une structure de répartition du travail

Vous pouvez créer une nouvelle structure de répartition du travail ou copier une structure de répartition du travail à partir d’un modèle de structure de répartition du travail existant. Un chef de projet peut facilement gérer les ressources en attribuant des rôles à de nouvelles tâches sur la structure de répartition du travail. Les rôles peuvent être remplacés après l’acquisition d’une ressource ou après l’identification d’une ressource confirmée pour travailler sur la tâche. Cette flexibilité permet aux chefs de projet d’effectuer les tâches suivantes :

- Identifiez le nombre de ressources requises pour les lots de travail de la structure de répartition du travail.
- Estimez les coûts de projet.
- Déterminez un budget préliminaire.
- Estimez la durée de l’activité en fonction des rôles et des ressources.
- Développez des plans de gestion de projet, basés sur les informations disponibles sur le projet.

Des options supplémentaires ont été ajoutées dans la structure de répartition du travail pour mieux utiliser la fonctionnalité des ressources.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Attributions de ressources</td>
<td>Affichez les ressources affectées, les dates, le nombre d’heures et le type de réservation pour les tâches sur la structure de répartition du travail.</td>
</tr>
<tr class="even">
<td>Générer automatiquement l’équipe</td>
<td>Ajoutez automatiquement des ressources planifiées à l’aide de rôles associés à une tâche. Finance suggère automatiquement des ressources planifiées à l’aide d’une analyse de décision multicritères basée sur les rôles. Une fois que les rôles et l’effort (heures) ont été définis pour les tâches dans une structure de répartition du travail et une fois la structure validée, sélectionnez <strong>Générer automatiquement une équipe</strong>. Le nombre requis de ressources planifiées est ajouté à la structure de répartition du travail et à l’onglet <strong>Planification des projets et des équipes</strong>.</td>
</tr>
<tr class="odd">
<td>Ressource (liste déroulante)</td>
<td>Sur la page <strong>Lancer l’affectation des ressources</strong>, vous pouvez sélectionner des ressources pour réservation ferme ou provisoire, selon la durée spécifiée. Vous pouvez ajuster les paramètres d’affichage pour voir et définir la durée des activités de ressources. Vous pouvez sélectionner et affecter des ressources au niveau du lot de travail à l’aide des options suivantes :
<ul>
<li><strong>Accepter</strong> : confirmez les modifications apportées à la ressource affectée à une tâche.</li>
<li><strong>Annuler</strong> : annulez les modifications apportées à la ressource affectée à une tâche.</li>
<li><strong>Attribuer automatiquement</strong> : une ressource disponible ayant un rôle correspondant est automatiquement sélectionnée et affectée à la tâche sélectionnée.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Sur la page **Tous les projets**, sélectionnez le projet **Mise à niveau XYZ Phase 2**.
2. Sélectionnez **Plan** > **Activités** > **Structure de répartition du travail**.
3. Sélectionnez **Nouveau** pour ajouter les activités de niveau un suivantes à la structure de répartition du travail :

    - Initiation
    - Planification
    - Exécution en cours
    - Surveillance et contrôle
    - Fermer

4. Réglez les dates et les efforts (heures), comme indiqué dans l’illustration suivante.

    [![Définir les dates et les efforts.](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Sélectionnez la ligne de tâche **Initier**, puis, dans le champ **Rôle**, sélectionnez **Chef de projet senior**.
6. Cliquez sur **Publier**.
7. Sur la même ligne, dans le champ **Ressource**, sélectionnez **Daniel Goldschmidt**, puis **Accepter**.
8. Sélectionnez la ligne de tâche **Planification**, puis, dans le champ **Rôle**, sélectionnez **Analyste d’affaires**.
9. Sélectionnez **Publier**, puis **Générer automatiquement une équipe**.
10. Dans la zone de message qui s’affiche, sélectionnez **Oui**.
11. Dans le champ **Ressource**, vérifiez que la valeur est **Analyste d’affaires 1**.
12. Pour la ressource **Analyste d’affaires 1**, ouvrez la recherche et sélectionnez **Lancer les affectations de ressources**. Sélectionnez ensuite un employeur pour la tâche.
13. Sélectionnez **Affectation provisoire** &gt; **Capacité complète**.

    > [!NOTE] 
    > Vous ne recevez pas d’avertissement indiquant que la ressource spécifiée est désormais 2, car le nombre de ressources reste 1.

14. Sur la page **Structure de répartition du travail**, validez l’affectation de ressource sur la structure de répartition du travail, puis sélectionnez **Enregistrer**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]