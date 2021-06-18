---
title: Subventions de projet
description: Cette rubrique explique comment créer ou modifier une subvention.
author: RadhikaRS
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 8e875ec086ee4c5e2ed3b16adcc6048ac8351ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999578"
---
# <a name="project-grants"></a>Subventions de projet

[!include [banner](../includes/banner.md)]

Une subvention est un don financier pour un objectif ou un projet spécifique. Généralement, des restrictions s’appliquent sur la façon dont une subvention peut être dépensée. Dans Gestion de projet et comptabilité, vous pouvez saisir et suivre les subventions, et définir leur relations avec les projets et contrats de projet. Par exemple, vous pouvez effectuer les tâches suivantes :

- Associer des subventions à des projets et des sources de financement grâce à des liens vers les pages **Projet** et **Détails du contrat de projet**.
- Saisissez et suivez les modifications apportées à une subvention à mesure qu’elle passe d’un statut à un autre.
- Saisissez et suivez les coûts, les montants demandés et les montants attribués.
- Créez des subventions principales et associez-leur des sous-subventions.

Vous pouvez créer une subvention en saisissant tous les détails dans un nouvel enregistrement, ou vous pouvez copier les détails d’une subvention existante et les mettre à jour.

## <a name="create-a-new-grant"></a>Créer une subvention

1. Accédez à **Gestion de projet et comptabilité** \> **Subventions** \> **Subventions**.
2. Sélectionnez **Nouveau** \> **Subvention**.
3. Sur la page des détails de la subvention, sur le raccourci **Général**, dans le champ **ID de subvention**, saisissez un identifiant alphanumérique pour la subvention.
4. Dans le champ **Nom de la subvention**, entrez un nom pour la subvention.
5. Dans le champ **Description**, ajoutez des détails sur la nouvelle subvention.

    La plupart des autres champs de la page sont facultatifs et vous pouvez entrer la quantité d’informations que vous souhaitez.

    La liste suivante décrit les informations spécifiées sur chaque raccourci de la page des détails de la subvention :

    - **Général** – Saisissez le nom, le statut, la description, le but et le montant de la subvention.
    - **Informations de contact** – Entrez les détails sur les membres du personnel, le service qui gère la subvention et le client de la subvention ou la source d’organisation de la subvention. Vous pouvez également indiquer si votre organisation est une entité intermédiaire qui reçoit la subvention et la transmet ensuite à un autre destinataire. Sélectionnez **Ajouter** pour ajouter des informations de contact, par exemple les numéros de téléphone et les adresses e-mail de l’organisation qui accorde la subvention.
    - **Dates et délais** – Saisissez les dates liées à la subvention et à la demande de subvention. Il peut s’agir de la date d’échéance de la demande, la date de soumission et la date à laquelle la subvention est approuvée ou rejetée.
    - **Projets associés et contrats de projet** – Vous ne pouvez saisir des informations sur ce raccourci que si le champ **Statut de la subvention** sur le raccourci **Général** est défini sur **Actif** ou **Attribué**. Sélectionnez l’une des options suivantes pour terminer la tâche associée :

        - **Ajouter une source de financement** – Ajoutez une nouvelle source de financement pour la subvention. Vous pouvez saisir tous les détails maintenant, ou vous pouvez utiliser les informations par défaut et les mettre à jour ultérieurement.
        - **Ajouter un contrat de projet** – Ajoutez ou mettez à jour les informations du contrat de projet.
        - **Ajouter un projet** – Ajoutez ou mettez à jour les détails du projet.

    - **Configurer** – Entrez les détails relatifs aux correspondants, si ces informations sont requises. De nombreuses organisations qui octroient des subventions exigent que les bénéficiaires dépensent un montant spécifique de leur propre argent ou de leurs propres ressources, afin de correspondre au montant accordé dans la subvention. Dans le champ **Projet local ou ID de suivi**, vous pouvez saisir un identifiant différent de l’identifiant du projet.

        > [!NOTE]
        > Si une partie de la subvention est attribuée à une autre organisation, définissez l’option **Sous-donateur** sur **Oui**. Pour les subventions accordées aux États-Unis, vous pouvez spécifier si une subvention sera accordée dans le cadre d’un mandat d’État ou d’un mandat fédéral.

    - **Détails du tirage** – Ajoutez ou mettez à jour des informations sur la fréquence à laquelle les fonds de subvention peuvent être retirés, facturés ou dépensés.

## <a name="create-a-new-grant-from-a-copy"></a>Créer une nouvelle subvention à partir d’une copie

1. Accédez à **Gestion de projet et comptabilité** \> **Subventions** \> **Subventions**.
2. Sélectionnez **Nouveau** \> **Copier à partir de la subvention**.
3. Entrez un identifiant alphanumérique et un nom pour la nouvelle subvention, puis sélectionnez **OK**.
4. Sur la page des détails de la subvention, examinez les détails de la subvention copiée et apportez les modifications nécessaires. La plupart des champs de la page sont facultatifs.

## <a name="view-or-modify-grant-details"></a>Afficher ou modifier les détails de la subvention

1. Accédez à **Gestion de projet et comptabilité** \> **Subventions** \> **Subventions**.
2. Sélectionnez la subvention à modifier.
3. Dans l’onglet **Subvention** du volet Actions, cliquez sur **Modifier** dans le groupe **Mettre à jour**.
4. Vérifiez les détails de la subvention et apportez les modifications nécessaires.


[!INCLUDE[footer-include](../includes/footer-banner.md)]