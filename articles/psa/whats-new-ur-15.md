---
title: Nouveautés ou modifications de la mise à jour (version 15) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique donne des informations sur les nouveautés de la mise à jour (version 15) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: d052dd670ac31fae57a71cb71682da86a237b3487482a9548f3fb9e52516c407
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004443"
---
# <a name="project-service-automation-update-release-15-v3"></a>Mise à jour (version 15) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Dynamics 365 Project Service Automation (PSA). Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 Online et accédez à la page des solutions pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 15) de PSA V3. Cette version a le numéro de build V3.10.5.28 et est généralement disponible par mise à jour automatique en janvier 2020.

## <a name="update-release-15"></a>Mise à jour (version 15) 

### <a name="enhancements"></a>Améliorations

- Gestion du projet

### <a name="bug-fixes"></a>Correctifs de bogues

- Temps et dépenses

  - Correction : ajoutez la gestion des erreurs de chargement dans la vue Rapprochement.
  - Correction : centre des ressources du projet : renommez **Montant** pour réduire l’ambiguïté.
  - Correction : ajustez la vue **Copier les colonnes d’entrée de temps** pour inclure le type.
  - Correction : la modification de la durée de l’entrée de temps dans la vue grille à l’aide de nombres décimaux entraîne une erreur inconnue pour certains nombres.

- Gestion du projet

  - Correction : le menu déroulant pour **Utiliser en mode Suivi** se développe désormais en fonction de la largeur des options.
  - Correction : lors de la gestion de projets dans le fuseau horaire +13, les calculs des tâches peuvent afficher des résultats inexacts.
  - Correction : l’option **Heure de fin du membre de l’équipe** a été corrigée lors de l’utilisation d’un calendrier de 24 heures.
  - Correction : réactivez le **BPF** dans le formulaire principal **msdyn_project**.
  - Correction : le calcul des affectations n’ignore plus un jour.
  - Correction : une nouvelle bannière de notification a été ajoutée au formulaire de projet lorsque le fuseau horaire diffère entre l’utilisateur et le projet.

- Ventes

  - Correction : la recherche de catégorie d’estimation des dépenses peut être utilisée pour filtrer les doublons.
  - Correction : le code dans **PluginDomain.ExecuteInTryCatchBlock(..)** ne cache plus l’origine de l’exception.
  - Correction : un message d’erreur ne s’affiche plus dans **Recherche de projet** dans le formulaire **Ligne de devis** lorsqu’il y a plus de 1000 projets.
  - Correction : la grille **Estimations** pour les estimations de main-d’œuvre et les estimations de dépense affiche désormais le symbole de devise correct.
  - Correction : une fois qu’une organisation met à jour PSA de la version 14 vers la version 15, l’onglet **Planning** n’apparaît plus comme vide dans le formulaire **Projet**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]