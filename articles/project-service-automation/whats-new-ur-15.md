---
title: Nouveautés de la mise à jour (version 15) de Project Service Automation, V3
description: Cette rubrique donne des informations sur les nouveautés de la mise à jour (version 15) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168046"
---
# <a name="project-service-automation-v3-update-release-15"></a>Mise à jour (version 15) de Project Service Automation, V3

Nous sommes heureux d'annoncer la dernière mise à jour de l'application Dynamics 365 Project Service Automation (PSA). Cette version comprend des améliorations importantes de la qualité, des performances et de l'utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez le centre d'administration de Dynamics 365 Online et accédez à la page des solutions pour installer la mise à jour. Pour plus d'informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 15) de PSA V3. Cette version a le numéro de build V3.10.5.28 et est généralement disponible par mise à jour automatique en janvier 2020.

## <a name="update-release-15"></a>Mise à jour (version 15) 

### <a name="enhancements"></a>Améliorations

- Gestion du projet

### <a name="bug-fixes"></a>Correctifs de bogues

- Temps et dépenses

  - Correction : ajoutez la gestion des erreurs de chargement dans la vue Rapprochement.
  - Correction : centre des ressources du projet : renommez **Montant** pour réduire l'ambiguïté.
  - Correction : ajustez la vue **Copier les colonnes d'entrée de temps** pour inclure le type.
  - Correction : la modification de la durée de l'entrée de temps dans la vue grille à l'aide de nombres décimaux entraîne une erreur inconnue pour certains nombres.

- Gestion du projet

  - Correction : le menu déroulant pour **Utiliser en mode Suivi** se développe désormais en fonction de la largeur des options.
  - Correction : lors de la gestion de projets dans le fuseau horaire +13, les calculs des tâches peuvent afficher des résultats inexacts.
  - Correction : l'option **Heure de fin du membre de l'équipe** a été corrigée lors de l'utilisation d'un calendrier de 24 heures.
  - Correction : réactivez le **BPF** dans le formulaire principal **msdyn_project**.
  - Correction : le calcul des affectations n'ignore plus un jour.
  - Correction : une nouvelle bannière de notification a été ajoutée au formulaire de projet lorsque le fuseau horaire diffère entre l'utilisateur et le projet.

- Ventes

  - Correction : la recherche de catégorie d'estimation des dépenses peut être utilisée pour filtrer les doublons.
  - Correction : le code dans **PluginDomain.ExecuteInTryCatchBlock(..)** ne cache plus l'origine de l'exception.
  - Correction : un message d'erreur ne s'affiche plus dans **Recherche de projet** dans le formulaire **Ligne de devis** lorsqu'il y a plus de 1000 projets.
  - Correction : la grille **Estimations** pour les estimations de main-d'œuvre et les estimations de dépense affiche désormais le symbole de devise correct.
  - Correction : une fois qu'une organisation met à jour PSA de la version 14 vers la version 15, l'onglet **Planning** n'apparaît plus comme vide dans le formulaire **Projet**.
