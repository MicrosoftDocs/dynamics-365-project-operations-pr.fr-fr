---
title: Nouveautés ou modifications de la mise à jour (version 36) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Microsoft Dynamics 365 Project Service Automation version 36, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/06/2021
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: a8942713109075da2503c9d22d40b6ac95ae00be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924979"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-36-v3"></a>Nouveautés ou modifications de la mise à jour (version 36) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour de Project Service Automation version 36, V3. Cette version a le numéro de build V3.10.57.152 et est généralement disponible par mise à jour automatique en octobre 2021.

## <a name="update-release-36"></a>Mise à jour (version 36)

### <a name="bug-fixes"></a>Correctifs de bogues

Les problèmes suivants ont été résolus.

**GÉNÉRAL**
- Le nom du champ **Modèle d’heure de travail par défaut** est mal traduit dans la page **Paramètres du projet**.
- Les plug-ins asynchrones ne gèrent pas correctement les exceptions liées à **SharedVariableService**.

**Temps et dépenses**
- Lorsque des lignes de journal sont manquantes ou que l’utilisateur ne dispose pas des privilèges appropriés pour lire les lignes de journal, une erreur incorrecte se produit lors de l’annulation des approbations du projet.
- Les utilisateurs ne peuvent pas annuler une approbation si une entrée de dépense ou une entrée de temps est associée à plusieurs approbations du projet.
- Les champs **Absence** et **Congés** sont incorrectement traduits en chinois lors d’une recherche dans la page de création rapide **Entrée de temps**.

**Gestion des ressources**
- L’utilisateur ne peut pas rechercher des ressources dans l’**Assistant de planification** si le mode d’affichage est défini sur **Jour**, **Semaine** ou **Mois**.
- Les ressources génériques sont autorisées à tort à avoir des noms de position vides. 
- La clôture d’un contrat comme perdu n’annule pas les réservations futures.

**Vente**
- Si un environnement contient un grand volume de produits, les performances se dégradent dans la grille **Estimation des matériaux**.
- Lors de la création d’un projet à partir d’un modèle, la devise du projet n’affiche pas par défaut l’unité contractuelle du chef de projet respectif.
- Les montants réels ne correspondent pas toujours à ce qui est reflété sur le projet dû ou les montants deviennent négatifs dans des scénarios de rappel spécifiques.
- Une erreur se produit si vous associez un projet créé à partir d’un modèle de projet à une ligne de contrat.
- Les utilisateurs peuvent supprimer une ligne de contrat avec les jalons : **Prêt(e) pour la facturation** et **Facture créée**. Cela ne devrait pas être autorisé.
- Lorsque des estimations sont importées à partir d’un projet, l’exigibilité des détails de la ligne du devis est définie de manière incorrecte lorsque la facturation basée sur les tâches est activée pour la ligne de devis.
- Si vous ajoutez un jalon de facturation à prix fixe, il n’apparaît dans la sous-grille des jalons qu’après actualisation de la page.
- Une exception de référence nulle est générée si vous créez un contrat de projet avec un nom de devis nul.
- Les tâches en mode manuel pour lesquelles la devise du projet est différente de la devise de la ressource donnent des estimations de prix incorrectes.
- Les utilisateurs ne peuvent pas rappeler une transaction corrigée avec succès par une facture corrective.
- Les catégories de transactions désactivées apparaissent dans la grille **Estimations des dépenses**.



