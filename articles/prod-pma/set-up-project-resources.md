---
title: Configurer les ressources de projet
description: Cette rubrique fournit des informations sur la configuration ou la demande de ressources de projet.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bf146c3bfb2fd558c471d8a9e980834cb1b87df
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288736"
---
# <a name="set-up-project-resources"></a>Configurer les ressources de projet

[!include [banner](../includes/banner.md)]

Vous devez configurer un calendrier et l’associer à un employé ou à un employé. Le calendrier permet de planifier le projet et le temps de travail des ressources réservées au projet. Lors de la configuration du calendrier, les chefs de projet peuvent effectuer un nivellement des ressources dans le cadre de l’optimisation des ressources. En fonction du calendrier du calendrier, des restrictions peuvent être appliquées aux ressources. Vous pouvez configurer un calendrier sur la page **Calendriers**.

Lorsque vous configurez un employé en tant que ressource de projet, vous pouvez choisir parmi les employés qui travaillent dans l’entreprise pour laquelle vous configurez des ressources. Vous pouvez également sélectionner des employés d’autres sociétés de votre organisation. Ces employés sont appelés ressources intersociétés.

Les procédures suivantes expliquent comment configurer un employé en tant que ressource de projet dans votre entreprise et comment configurer une ressource de projet intersociétés.

## <a name="set-up-a-worker-as-a-project-resource"></a>Configurer un employé en tant que ressource de projet

1. Sur la page **Employés**, dans la liste **Employés**, sélectionnez l’employé que vous ajoutez en tant que ressource de projet et ouvrez l’enregistrement de l’employé.
2. Dans le volet Actions, sélectionnez **Projet** &gt;**Configurer** &gt; **Configuration du projet**.
3. Sélectionnez un calendrier, puis fermez la page.

Vous pouvez également spécifier des projets par défaut pour une ressource en tant que type de pré-affectation. Les pré-affectations peuvent être utilisées lorsque le responsable de ressources ou le chef de projet sait à l’avance sur quels projets la ressource travaillera. Les pré-affectations peuvent être également basées sur la demande d’un commanditaire ou d’un client. Pour pré-attribuer un projet, sur la page **Attribuer des projets**, sur l’onglet **Projets**, dans la liste **Projets restants**, sélectionnez le projet approprié.

## <a name="set-up-an-intercompany-resource"></a>Configurer une ressource intersociétés

Lorsque vous configurez un employé en tant que ressource intersociétés, vous devez terminer la configuration à la fois dans la société prêteuse et dans la société emprunteuse.

### <a name="in-the-lending-company"></a>Dans la société de prêt

1. Dans Finance, vérifiez que la société de prêt est sélectionnée, puis suivez la procédure de la section précédente, « Configurer un employé en tant que ressource de projet ».
2. Sur la page **Comptabilité intersociétés**, sélectionnez **Nouveau**.
3. Dans le champ **ID d’entité juridique**, sélectionnez la société prêteuse. Complétez les champs restants, le cas échéant, puis cliquez sur **Enregistrer**.
4. Sur la page **Prix du transfert**, sélectionnez **Nouveau**.
5. Dans le champ **Entité juridique emprunteuse**, sélectionnez la société appropriée.
6. Pour prêter à la société emprunteuse uniquement la ressource que vous avez créée au début de cette section, dans le champ **Ressource**, sélectionnez le nom de la ressource que vous avez créée. Pour mettre toutes les ressources de la société prêteuse à disposition de la société emprunteuse, laissez le champ **Ressource** vide.
7. Sur la page **Gestion de projet et comptabilité**, sur l’onglet **Intersociétés**, définissez l’option **Activer la planification des ressources et les feuilles de temps intersociétés** sur **Oui**.

### <a name="in-the-borrowing-company"></a>Dans la société emprunteuse

- Sur la page **Liste des ressources**, dans le filtre de recherche, saisissez le nom de la ressource que vous avez créée pour la société prêteuse, afin de vérifier que le nom est inclus dans la liste des ressources de la société emprunteuse.

## <a name="request-project-resources"></a>Demander des ressources de projet
La fonctionnalité de planification des ressources de projet permet uniquement aux responsables des ressources de distribuer les ressources en personnel sur les engagements ou les projets. Pour activer cette fonctionnalité, effectuez les tâches suivantes ou vérifiez qu’elles ont été effectuées :

- Configurez des séquences de numéros.
- Configurer les workflows de gestion et de comptabilité des projets
- Activez les workflows de demande de ressources.

Une fois les tâches précédentes terminées, vous pouvez effectuer les tâches suivantes selon vos besoins :

- Créez une demande de ressource à partir d’une ressource à réservation souple.
- Surveillez les demandes de ressources.
- Répondez aux demandes de ressources.
- Demandez une ressource en personnel à une structure de répartition du travail.
- Réservez des ressources pour un projet sans avoir de demande de ressource en personnel.


[!INCLUDE[footer-include](../includes/footer-banner.md)]