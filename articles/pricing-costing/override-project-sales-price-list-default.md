---
title: Remplacer les tarifs de vente des projets
description: Cet article fournit des informations sur la création de tarifs de vente personnalisés.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8d0a769f415679b08f3228fcb14fbbbd37533ebc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911915"
---
# <a name="override-project-sales-price-lists"></a>Remplacer les tarifs de vente des projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

## <a name="customer-specific-project-price-lists"></a>Tarifs de projet spécifique pour un client

Dans Dynamics 365 Project Operations, les accords de prix spécifiques à un client peuvent être configurés sous la forme de tarifs de projet sur un enregistrement de compte.

Pour configurer un tarif de projet spécifique pour un client, dans la zone **Ventes**, accédez à l’enregistrement de compte.

1. Ouvrer la page de liste **Comptes**.
2. Recherchez et double-cliquez sur un enregistrement de client pour ouvrir la page de détails **Compte**.
3. Sur l’onglet **Tarifs de projet**, sélectionnez **+ Nouveau tarif de projet**.
4. Dans la page **Nouveau tarif de projet**, sélectionnez un tarif dans la liste déroulante. Seuls les tarifs dont le contexte est défini sur **Ventes** et dont la devise correspond à la devise du compte sont inclus.
5. Nommez l’association et sélectionnez **Enregistrer**. Un tarif de projet spécifique pour un client est créé. Ce tarif sera utilisé pour créer les prix de projet par défaut sur les devis de projet ou les contrats créés pour ce client, si la date de création du devis ou du contrat de projet est conforme à la date d’entrée en vigueur du tarif.

## <a name="custom-pricing-on-project-quotes"></a>Tarification personnalisée sur les devis de projet

Sur les devis de projet, vous pouvez avoir une tarification de projet qui commence par un tarif standard par défaut qui est défini par défaut selon le client ou selon les paramètres du projet.

Lorsque vous avez besoin d’une tarification personnalisée pour un travail lié à un projet sur un devis particulier, vous pouvez l’obtenir à partir de l’entité associée des tarifs du projet.

Effectuez les étapes suivantes pour configurer une tarification de projet spécifique à un devis.

1. Ouvrez le devis du projet et sélectionnez l’onglet **Tarifs du projet**.
2. Dans la sous-grille, sélectionnez **Créer une tarification personnalisée**.

Tous les tarifs du projet joints au devis sont copiés dans les nouveaux tarifs. Les noms des nouveaux tarifs reflètent le nom du devis avec un horodatage pour la création de ces tarifs.

Vous pouvez utiliser chacun de ces tarifs et faire des mises à jour des prix de la main-d’œuvre (prix du rôle) et des dépenses (prix de la catégorie). Ces prix s’appliqueront uniquement à ce devis de projet.

## <a name="price-lists-on-a-project-contract"></a>Tarifs sur un contrat de projet

Dans un contrat de projet, la tarification du projet est toujours définie par défaut comme un tarif personnalisé avec le nom du contrat et la date et l’heure de création ajoutées au nom. Cela est vrai, que le contrat ait été créé lorsque le devis a été remporté ou que le contrat ait été créé à partir de zéro. Si nécessaire, vous pouvez supprimer cette association au tarif personnalisé et associer un tarif standard au contrat de projet à la place.

Lorsque vous associez un tarif standard à des tarifs du projet sur un devis ou un contrat, toute modification apportée aux prix dans le tarif aura un impact sur tous les devis et contrats qui utilisent le tarif.


[!INCLUDE[footer-include](../includes/footer-banner.md)]