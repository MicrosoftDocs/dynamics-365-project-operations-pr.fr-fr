---
title: Créer un modèle d’heures de travail
description: Cette rubrique décrit la procédure de création d’un modèle d’heures de travail dans Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981252"
---
# <a name="create-a-work-hours-template-project-service"></a>Créer un modèle d’heures de travail (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Pour créer et gérer un projet, vous devez appliquer un modèle de calendrier au projet. Le modèle de calendrier définit les attributs de projet suivants :

- Heures de travail, y compris l’heure de début et l’heure de fin
- Jours de travail
- Exceptions de calendrier, par exemple les jours non ouvrés

Le modèle de calendrier appliqué à un projet est une copie du modèle de calendrier défini dans les paramètres de votre organisation.

> [!NOTE]
> Si vous modifiez le modèle de calendrier, ces modifications ne se propagent pas aux heures de travail du projet. Pour modifier les heures de travail du projet, un nouveau modèle doit être appliqué.

Pour créer un modèle de calendrier pour votre organisation, il existe deux exigences clés :

- Définissez les heures de travail souhaitées du modèle à l’aide d’une ressource réservable nouvelle ou existante.
- Créez un nouveau modèle de calendrier et associez le modèle à la ressource réservable.

**Définir les heures de travail du modèle**

1. Accédez à **Ressources** \> **Ressources**.
2. Créez une nouvelle ressource à référencer dans le modèle de calendrier ou sélectionnez une ressource existante.
3. Sélectionnez l’onglet **Heures de travail** de la ressource et suivez les instructions dans [Définition des heures de travail pour une ressource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) pour configurer les règles du calendrier.

**Créer un modèle de calendrier**

1. Accédez à **Paramètres** \> **Modèle de calendrier**.
2. Sélectionnez **Nouveau** et entrez un nom, une description et une ressource de modèle.


> [!NOTE]
> Lorsqu’une ressource est référencée dans un modèle de calendrier, une copie du calendrier de la ressource est associée au modèle de calendrier. Si vous modifiez les heures de travail du modèle de calendrier, ces modifications ne se propagent pas au modèle de calendrier.


### <a name="see-also"></a>Voir aussi  
 [Configurer des ressources](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
