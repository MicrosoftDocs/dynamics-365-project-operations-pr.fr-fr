---
title: Ressources de la ligne du contrat de sous-traitance
description: Cette rubrique explique comment spécifier les ressources dédiées, fournies par le fournisseur pour une ligne du contrat de sous-traitance spécifique pour le temps.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48440f82170bde7f0a0a45f8f9849d688b232949
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323368"
---
# <a name="subcontract-line-resources"></a>Ressources de la ligne du contrat de sous-traitance

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, un fournisseur peut spécifier des ressources qui seront utilisées pour fournir la capacité de ressources achetée sur la ligne du contrat de sous-traitance pour le temps.

## <a name="create-subcontract-line-resources"></a>Créer des ressources pour la ligne du contrat de sous-traitance

Pour créer des ressources pour la ligne du contrat de sous-traitance, procédez comme suit :

1. Sur le volet de navigation, sélectionnez **Contrats de sous-traitance** et ouvrez le contrat de sous-traitance que vous voulez utiliser.
2. Ouvrez la ligne du contrat de sous-traitance pour le temps pour lequel vous souhaitez spécifier des ressources fournisseur.
3. Sur l’onglet **Ressources de la ligne du contrat de sous-traitance**, dans la sous-grille, sélectionnez **+ Nouvelle ressource de ligne du contrat de sous-traitance**.
4. Sur la page **Nouveau jalon de la ligne du contrat de sous-traitance**, saisissez les informations requises, puis cliquez sur **Enregistrer et fermer**.

Le tableau suivant explique les champs de la ressource de la ligne du contrat de sous-traitance.

| Champ |  Description |
| ----- | ------------ |
| Ressource réservable | Sélectionnez une ressource réservable de type « Sous-traitant » que vous souhaitez utiliser comme ressource sur la ligne du contrat de sous-traitance. Si vous n’avez pas encore créé de ressource réservable pour le sous-traitant, laissez ce champ vide. Une ressource réservable est créée lorsque vous enregistrez l’enregistrement.  |
| Contact | Si le champ **Ressource réservable** est vide, vous pouvez créer une ressource de la ligne du contrat de sous-traitance à partir d’un contact existant. Utilisez la recherche pour afficher la liste des contacts actifs dans le système. Sélectionnez un contact pour le fournisseur de ce contrat de sous-traitance. Le contact que vous sélectionnez est validé lorsque vous enregistrez la fiche. Si le contact que vous avez sélectionné n’est pas un contact valide, votre enregistrement ne sera pas enregistré. S’il n’y a pas de ressource réservable pour le contact sélectionné, le système crée une ressource réservable pour le contact sélectionné avant de créer la ressource de la ligne du contrat de sous-traitance. |
| Utilisateur | Si le champ **Ressource réservable** est vide, vous pouvez créer une ressource de la ligne du contrat de sous-traitance en sélectionnant un utilisateur actif. Utilisez la recherche pour afficher la liste des utilisateurs actifs dans le système. S’il n’y a pas de ressource réservable pour l’utilisateur sélectionné, le système crée une ressource réservable pour l’utilisateur sélectionné avant de créer la ressource de la ligne du contrat de sous-traitance. |
| Date de début | La date de début de l’affectation du sous-traitant. Si cette ressource est réservée pour une période antérieure à cette plage de dates, un avertissement s’affiche. |
| Date de fin | La date à laquelle l’affectation du sous-traitant se termine. Si cette ressource est réservée pour une période postérieure à cette plage de dates, un avertissement s’affiche. |
| Effort | Le nombre total d’heures d’effort que le sous-traitant passera sur cette ligne de sous-traitance. Si cette ressource est réservée au-delà de l’effort allouée sur ce sous-contrat, un avertissement s’affiche. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
