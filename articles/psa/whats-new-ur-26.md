---
title: Nouveautés ou modifications de la mise à jour (version 26) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 26) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948821"
---
# <a name="project-service-automation-update-release-26-v3"></a>Mise à jour (version 26) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 26), V3 de Project Service Automation. Cette version a un numéro de build V3.10.44.59 et est généralement disponible via une mise à jour automatique en décembre 2020.

## <a name="update-release-26"></a>Mise à jour (version 26)

### <a name="bug-fixes"></a>Corrections de bogues

**Temps et dépenses**

Les problèmes suivants ont été résolus :

- Les utilisateurs peuvent modifier la tâche sur une entrée de temps qui a été approuvée/soumise.
- Erreur « Référence d'objet non définie » lors de l'enregistrement d'une entrée de temps.
- L'importation des entrées de temps à partir des affectations de ressources crée des entrées de temps avec des valeurs DateHeure incorrectes.
- Lorsque Project Service Automation et l'application Field Service sont toutes deux installés, le bouton **Nouveau** s'affiche deux fois sur la barre de commandes pour les entrées de temps dans l'application Field Service.
- Les mises à jour des cellules **Autoriser unité** et **Groupe d’unités** fonctionnent désormais dans la grille **Estimations des dépenses**.
- Le formulaire **Mettre à jour l'entrée de temps Modifier** comprend **Chronologie**.
- L'approbation du temps pour les entrées de temps hors projet bloque le système lors de la recherche d'un rôle d'approbateur de projet.

**Gestion des ressources**

Les problèmes suivants ont été résolus :

- Ajout de validation dans le plug-in **PostProjectCreate** pour vérifier une exigence principale avant d'en créer.
- Le formulaire de création rapide **Membre de l'équipe de projet** lève une exception de référence nulle si des champs sont supprimés du formulaire.
- La génération d'exigences pendant 12 heures sur 1 an échouera.
- Exception de référence nulle de message d'erreur améliorée lors de la création des besoins en ressources.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- Amélioration de la validation pour traiter l'exception de référence nulle générée dans le plug-in **PreProjectUpdate**.
- Les projets publiés par le complément de bureau Microsoft Project suppriment les affectations non attribuées.
- Ajout d'une nouvelle validation lorsque la référence de projet d'une tâche n'est pas valide en raison d'une exception de référence nulle dans le plug-in **PreValidateProjectTaskUpdate**.
- La grille Membre d'équipe n'affiche pas les affectations distinctes sur l'enregistrement des membres de l'équipe.
- Ajout de nouveaux messages de validation et d'erreur en raison d'une exception de référence nulle dans le plug-in **PreProjectTaskDelete**.

**Ventes**

Les problèmes suivants ont été résolus :

- Lors de la sélection d'une ligne basée sur un projet dans un devis ou un contrat, le bouton **Suggestion** ne doit être visible que lors de la sélection d'une ligne basée sur un produit associée à un produit existant.
- Split du privilège **Create_Product** à partir du privilège **Create_ProjectContract**.
- La suppression d'une ligne de facture entraîne un échec de référence nul sur **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]