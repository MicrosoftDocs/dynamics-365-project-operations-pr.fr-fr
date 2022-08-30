---
title: Configurer des sous-traitants en tant que ressources réservables
description: Cet article explique comment configurer et gérer les ressources de sous-traitant créées à partir d’utilisateurs et de contacts dans le système, afin qu’elles puissent être associées à des sous-contrats dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67df514cd1a0bd07d4ff2582e1a7738d913e0ac5
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261320"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>Configurer des sous-traitants en tant que ressources réservables

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Suivez ces étapes pour configurer des sous-traitants en tant que ressources réservables dans Microsoft Dynamics 365 Project Operations.

1. Accédez à **Projet** \> **Ressources**, puis sélectionnez **Nouveau**.
2. Sur la page **Nouvelle ressource réservable**, dans le champ **Type de ressource**, sélectionnez l′une des options suivantes :

    - **Utilisateur** : sélectionnez ce type de ressource si le sous-traitant doit accéder à Project Operations pour saisir le temps ou les dépenses. Si vous sélectionnez **Utilisateur**, le sous-traitant a besoin d′une licence valide pour accéder au système.
    - **Contact** ou **Compte** : sélectionnez l′un de ces types de ressources si le sous-traitant n′a pas besoin d′accéder à Project Operations, mais doit être disponible pour les affectations de tâches ou les réservations sur les projets. Aucun de ces types de ressources ne donne accès au système. Sélectionnez **Compte** pour représenter l′entreprise du fournisseur en tant que ressource réservable. Sélectionnez **Contact** pour représenter chaque employé du fournisseur.

3. Selon le type de ressource sélectionné, vous êtes invité à sélectionner l′utilisateur, le compte ou l′enregistrement de contact correspondant.
4. Dans le champ **Type de travailleur**, sélectionnez Sous-traitant pour configurer le sous-traitant en tant que ressource réservable.

    > [!NOTE]
    > Si vous laissez le champ **Type de travailleur** vide, la ressource réservable est considérée comme un employé.

5. Si vous avez sélectionné **Sous-traitant** comme type de travailleur, sélectionnez le fournisseur pour lequel travaille la ressource.
6. Sélectionnez le fuseau horaire de la ressource, puis cliquez sur **Enregistrer**. Pour attribuer un modèle d′heure de travail à la ressource réservable, vous pouvez sélectionner **Définir le calendrier** sur la page **Ressource réservable**.

Pour associer une ressource réservable à une ligne de contrat de sous-traitance, les conditions suivantes doivent être remplies :

- La ressource réservable doit être un sous-traitant.
- Une ressource réservable du type de ressource **Contact** doit être associée au compte fournisseur en tant que contact. Une ressource réservable du type de ressource **Utilisateur** ne doit pas être associée au compte fournisseur en tant que contact.
- La valeur du champ **Fournisseur** pour la ressource réservable doit correspondre à la valeur du champ **Fournisseur** pour le contrat de sous-traitance.

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>Mettre à jour le type de mappage de travailleur et de fournisseur pour les ressources réservables

Le champ **Type de travailleur** pour une ressource réservable détermine si la ressource réservable est un sous-traitant ou un employé. Le champ **Fournisseur** définit le compte fournisseur auquel la ressource réservable est associée. En associant une ressource réservable à un fournisseur en tant que contact, vous indiquez que le contact est un employé de la société du fournisseur.

Si les champs **Type de travailleur** et **Fournisseur** pour une ressource réservable sont modifiés, les modifications impactent toute validation future au niveau des nouveaux enregistrements que la ressource réservable crée, comme les entrées de temps. Cependant, les modifications n′invalident pas les enregistrements existants.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
