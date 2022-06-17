---
title: Nouveautés ou modifications de la mise à jour (version 27) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Project Service Automation version 27, V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912927"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Nouveautés ou modifications de la mise à jour (version 27) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour version 27 de Project Service Automation V3. Cette version a le numéro de build V3.10.45.98 et est généralement disponible par mise à jour automatique en janvier 2021.

## <a name="update-release-27"></a>Mise à jour (version 27)

### <a name="bug-fixes"></a>Corrections de bogues

**Général**

Les problèmes suivants ont été résolus :

- Les journaux générés par les plug-ins dans Project Service Automation n’ont pas été définis pour la suppression automatique.
- La mise à niveau automatique échoue car la solution Project Service Automation contient un élément NavBarArea et de titre null hérité.

**Temps et dépenses**

Les problèmes suivants ont été résolus :

- La grille **Saisie de l’heure** affiche des données incorrectes pour le comportement de date **Indépendant de TimeZone**.
- La grille **Saisie de l’heure** crée une heure incorrecte pour le comportement de date **Indépendant de TimeZone**.
- La recherche de tâches n’est pas limitée au projet sélectionné sur la page **Modifier l’entrée de temps**.
- L’approbation du temps pour les entrées de temps hors projet est bloquée car le système recherche un approbateur de projet.
- Les entrées correctes sur les statistiques affichent un message d’erreur incorrect.
- Lorsqu’une tâche contient une valeur nulle pour le coût réel et que les totaux du projet sont actualisés, l’erreur suivante se produit, "Clé donnée non présente dans le dictionnaire".
- Dans des cas spécifiques, les filtres **Par groupe** sur l’onglet **Estimation du projet** n’affiche pas les estimations de dépenses.
- L’intervalle **Heure d’été** n’est pas correct pour les entrées de temps.

**Gestion du projet**

Les problèmes suivants ont été résolus :

- Améliorations de la mise en cache, ce qui améliore les performances liées au chargement de la page **Projet**.
- Règle métier obsolète empêchant l’achèvement des tâches du projet.
- Les contours du complément Microsoft Project ne respectent pas le calendrier du complément, ce qui entraîne des besoins en ressources incorrects.
- La création de projets à partir de modèles définit de manière incorrecte les dates d’affectation et empêche la possibilité de générer des besoins en ressources.
- L’utilisateur ne peut pas accéder aux options **Catégorie**, **Description**, **Statut** à l’aide du clavier.
- Les valeurs de vente réelles du projet n’incluent pas les valeurs de vente des frais et des matériaux.
- L’agrégation des ventes réelles et du coût réel se produit avec différents taux de change.
- La description dans le **Modèle d’heure de travail par défaut** est trompeur.
- L’indentation d’une tâche ne supprime pas **Catégorie** dans l’interface utilisateur jusqu’à ce qu’il soit actualisé.
- Une validation manquante pour garantir le déplacement d’un projet au-delà de sa date de fin n’est pas autorisée.

**Ventes**

Les problèmes suivants ont été résolus :

- Une exception de référence nulle est générée sur une ligne de devis de projet car **Importer à partir de l’estimation de projet** est visible lorsqu’un projet n’a pas été sélectionné.
- L’erreur suivante, "Référence d’objet non définie sur une instance d’un objet" se produit lors de la fermeture d’un devis comme **Gagné**.
- Le statut d’ajustement n’est pas défini lors d’une annulation réelle lors de la dissociation d’un projet d’une ligne de contrat.
- Quand Dynamics 365 Field Service et Project Service Automation sont installés, les options **Tarification de verrouillage** et **Utiliser la tarification actuelle** ne sont pas affichées en même temps sur la page **Facture d’achat**.
- Pour le japonais, la traduction n’est pas cohérente avec les autres pages basées sur le calendrier.
- **Activer** et **Désactiver** ont été supprimés des entités **Association des tarifs** dans Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
