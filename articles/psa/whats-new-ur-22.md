---
title: Nouveautés ou modifications de la mise à jour (version 22) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 22) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: db4cbb9f9daadcb1911325f8bee987d5e480e1cf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150980"
---
# <a name="project-service-automation-update-release-22-v3"></a>Mise à jour (version 22) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 22) de Project Service Automation V3. Cette version a le numéro de build V 3.10.33.48 et est généralement disponible via une mise à jour automatique en juin 2020.

## <a name="update-release-22"></a>Mise à jour (version 22)

### <a name="bug-fixes"></a>Corrections de bogues



**Temps et dépenses**

Les problèmes suivants ont été résolus :

- Les **Entrées de temps** ne sont pas automatiquement ajoutées dans le calendrier des entrées de temps après l’importation.
- Le sélecteur de date de la grille **Entrée de temps** ne reconnaît pas les paramètres régionaux d’un utilisateur.

**Gestion des ressources**

Les problèmes suivants ont été résolus :

- En mode manuel, les modifications des contours **Attribution de ressource** ne sont pas reconnues lors de la génération des **Ressources requises**.
- Les **Demandes de ressources** ne prennent pas en charge les statuts de demande personnalisés.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- L’utilisation du double-clic sur EstimateGridControl n’analyse pas correctement les nombres au format néerlandais.
- Les heures affectées ne sont pas mises à jour correctement lorsque les affectations sont modifiées à l’aide du complément Microsoft Project pour ordinateur de bureau.
- Les grilles Suivi du projet et Estimations affichent un code devise de vente incorrect lorsque la devise du contrat est différente de la devise du client et l’organisation est configurée pour afficher des codes devise au lieu de symboles de devise.
- La date de fin d’un membre de l’équipe ajoute un jour si le calendrier des heures de travail est de 24 heures par jour.
- Dans le calendrier du projet, l’ajout d’une catégorie de transaction à une tâche ne déclenche pas l’enregistrement automatique.
- L’erreur suivante s’affiche lors de l’ajout d’un membre de l’équipe au modèle de projet : « Les ressources requises ne peuvent pas être associées aux modèles de projet ». 
- Le script de règle de ruban « msdyn.Approval.CanApproveOrReject » affiche une erreur d’expiration du délai.

**Ventes**

Les problèmes suivants ont été résolus :

- Un message d’erreur de validation ne s’affiche pas lorsqu’une liste de prix de revient est sélectionnée lors de la recherche de tarifs sur le formulaire/l’entité Nouveaux tarifs du projet de devis.
- La clôture du devis comme conclue ne permet pas d’accéder au contrat créé si un BPF joint au devis est en phase finale.
- La contrepassation des **Ventes non facturées** est liée au coût d’origine lorsqu’une entrée de temps est rappelée.
- Après avoir sélectionné le bouton **Confirmer**, le statut de la facture ne passe pas à **Confirmé** sauf si la facture est actualisée.
