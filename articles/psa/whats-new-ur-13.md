---
title: Nouveautés ou modifications de la mise à jour (version 13) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique donne des informations sur les nouveautés de la mise à jour (version 13) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: a4ebc2e6ca3f6be0a05a7240d762d7a8cf92d81b
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949451"
---
# <a name="project-service-automation-update-release-13-v3"></a>Mise à jour (version 13) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Dynamics 365 Project Service Automation (PSA). Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 Online et accédez à la page des solutions pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 13) de Project Service Automation V3. Cette version a le numéro de build V3.10.3.18 et est disponible selon le calendrier suivant :

- **Disponibilité générale (mise à jour automatique) :** novembre 2019
- **Mise à jour automatique :** décembre 2019


## <a name="update-release-13"></a>Mise à jour (version 13) 

### <a name="bug-fixes"></a>Correctifs de bogues

- Temps et dépenses

     - Correction : la fonctionnalité de recherche sur la page **Approbation des dépenses** ne fonctionne pas lorsque vous effectuez une recherche par objectif de dépense.

- Gestion des ressources

     - Correction : les nombres dans la vue Rapprochement ont été mis à jour pour être justifiés à droite.
     - Correction : les ressources nommées ne peuvent pas être affectées à des tâches via l’onglet **Planning**.

- Gestion du projet

     - Correction : exception de référence nulle lors de l’affectation d’un membre de l’équipe lorsque les informations de configuration de **TransactionType** sont manquantes pour **Unit** et **DefaultGroup**.

- Ventes

     - Correction : les enregistrements de type de transaction en double renvoient une erreur lors de la création des enregistrements de prix de rôle.
     - Résolu : des boutons supplémentaires pour **Nouvelle opportunité**, **Devis**, **Ligne de commande** et **Ajouter un produit** sont visibles dans les commandes pour les opportunités, les devis, les produits de la commande et la sous-grille Lignes basée sur un projet.




[!INCLUDE[footer-include](../includes/footer-banner.md)]