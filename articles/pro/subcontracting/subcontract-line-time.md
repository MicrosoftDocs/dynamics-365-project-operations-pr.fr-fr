---
title: Lignes du contrat de sous-traitance pour le temps
description: Cette rubrique explique comment enregistrer des lignes du contrat de sous-traitance pour le temps et enregistrer l’achat de temps auprès des fournisseurs.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323863"
---
# <a name="subcontract-lines-for-time"></a>Lignes du contrat de sous-traitance pour le temps

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Un contrat de sous-traitance dans Dynamics 365 Project Operations peut avoir une ligne pour le temps. Les lignes du contrat de sous-traitance pour le temps permettent à un chef de projet d’acheter du temps pour une ressource fournisseur pour répondre aux besoins des tâches du projet et des ressources.

Dans Project Operations, pour créer une ligne pour le temps dans le contrat de sous-traitance, procédez comme suit :

1. Dans le volet de navigation, sélectionnez **Contrats de sous-traitance** et ouvrez un contrat de sous-traitance.
2. Sur l’onglet **Lignes du contrat de sous-traitance**, sélectionnez **Nouveau** pour créer une nouvelle ligne.
3. Sur la page **Création rapide**, dans le champ **Classe de transaction**, sélectionnez **Temps**.
4. Indiquez les informations obligatoires restantes, puis cliquez sur **Enregistrer**.

  Le tableau suivant fournit des informations sur les champs de la page **Ligne du contrat de sous-traitance** et de la page **Création rapide**.

| **Champ** | **Description** |
| --- | --- |
| Nom | Le nom de la ligne du contrat de sous-traitance. |
| Description | Une brève description des services qui sont achetés sur la ligne du contrat de sous-traitance. | 
| Type de ligne | Ce champ contient une valeur par défaut.  |
| Mode de facturation | Sélectionnez la méthode de facturation. En fonction du mode de facturation de la ligne du contrat de sous-traitance référencée, un échéancier de facturation basé sur des jalons est mis à disposition pour le mode de facturation à prix fixe. |
| Classe de transaction | Ce champ contient une valeur par défaut qui indique si la ligne du contrat de sous-traitance est utilisée pour enregistrer un achat de temps. |
| Rôle | Le rôle des ressources du contrat de sous-traitance dont le temps est acheté. Le rôle attribué aux ressources du contrat de sous-traitance détermine le coût de l’achat. |
| Début demandé | La date à laquelle les ressources du contrat de sous-traitance doivent commencer à travailler. Le démarrage demandé permet de choisir un tarif projet parmi ceux rattachés au contrat de sous-traitance. Le coût du rôle sur la ligne du contrat de sous-traitance est alors défini par défaut à partir de ce tarif. |
| Fin demandée | La date à laquelle l’affectation des ressources de sous-traitance se termine. Cette date est utilisée pour afficher des avertissements lorsqu’un chef de projet puise dans cette capacité pour les besoins en ressources survenant après cette date. |
| Quantité commandée | Le nombre d’heures de rôle achetées auprès du fournisseur. Cette valeur est utilisée pour afficher des avertissements lorsqu’un chef de projet puise dans cette capacité pour les besoins en ressources. |
| Groupe d’unités | La valeur de ce champ est définie par défaut sur le groupe d’unités Temps et ne peut pas être modifiée.  |
| Unité | Ce champ est défini par défaut sur l’unité de base des heures du groupe d’unités Temps. Vous pouvez modifier cette valeur pour acheter n’importe quelle unité du groupe d’unités Temps, comme le jour ou la semaine. La combinaison Rôle et Unité permet de calculer le prix unitaire de la ligne du contrat de sous-traitance. |
| Prix unitaire | Le prix unitaire provient par défaut de la combinaison Rôle et Unité des tarifs du projet qui s’applique à la date de début demandée de la ligne du contrat de sous-traitance. Lorsque les tarifs du projet applicables sont configurés dans une unité différente de celle sur la ligne du contrat de sous-traitance, le système utilise la conversion d’unité pour calculer le prix unitaire. |
| Sous-total | Il s’agit d’un champ en lecture seule qui est automatiquement calculé comme **Quantité x Prix unitaire** si les valeurs de quantité et de prix unitaire sont saisies. Si la quantité, le prix unitaire ou les deux sont vides, vous pouvez saisir une valeur dans le champ. |
| Taxe de ventes |  Entrez le montant de la taxe de ventes. |
| Montant total | Le montant total de la ligne de sous-traitance, taxes incluses. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
