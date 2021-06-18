---
title: Copier les tarifs
description: Cette rubrique fournit des informations sur le mode de copie des tarifs dans Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e4f4eeda019f2af11a0d7a4469c41ee450eb03b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001423"
---
# <a name="copy-price-lists"></a>Copier les tarifs

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez créer des copies de tarifs dans Dynamics 365 Project Operations. Par exemple, vous pouvez créer des listes de prix pour l’année à venir à l’aide d’un tarif de l’année en cours.  Ou, vous pouvez copier un tarif pour les taux de facturation et les prix de vente à partir des listes de prix pour le coût. 

Pour faire une copie du tarif, procédez comme suit.

1. Ouvrez le tarif dont vous souhaitez faire une copie et sélectionnez **Copier**.
2. Saisissez toutes les informations nécessaires pour copier le tarif. Le tableau suivant présente les considérations à garder à l’esprit lors de la saisie d’informations.

| Champ | Description | Impact en aval |
| --- | --- | --- |
| Nom | Le nom du tarif source avec le **-copy** ajouté. | Le tarif inclut cette valeur sur toutes les pages de liste et options de liste déroulante. |
| Contexte | Saisissez le contexte souhaité pour le tarif indicatif. | Un tarif avec le contexte défini sur **Coût** est utilisé pour rechercher le prix des estimations de coûts et des chiffres réels des coûts. Un tarif avec le contexte défini sur **Ventes** est utilisé pour rechercher le prix des estimations de ventes et des chiffres réels de vente. Seuls les tarifs dont le contexte est défini sur **Ventes** peuvent être attachés à un tarif de projet pour un client, des devis ou un contrat. |
| Date de début | La date de début de la période au cours de laquelle le tarif est effectif. | Conjointement avec **Date de fin**, ce champ est utilisé pour déterminer quel tarif est applicable pour une certaine ligne d’estimation ou de chiffres réels. |
| Date de fin | La date de fin de la période au cours de laquelle le tarif est effectif. | Conjointement avec **Date de début**, ce champ est utilisé pour déterminer quel tarif est applicable pour une certaine ligne d’estimation ou de chiffres réels. |
| Devise | Devise du tarif source. Cela est configurable. | Lorsque cela est modifié, toutes les lignes de prix résultantes pour la main-d’œuvre, les dépenses et les articles du catalogue de produits sont converties dans la devise du tarif cible lors de la copie. |
| Unité de temps | Devise du tarif source. Cela est configurable. | Lorsque cela est modifié, toutes les lignes de prix résultantes pour la main-d’œuvre sont converties dans la devise du tarif unitaire cible lors de la copie. La conversion de la configuration de l’unité pour l’unité de temps du tarif source et l’unité de temps du tarif cible est utilisée. |
| Description | Une description du tarif source avec le **-copy** ajouté. Ce champ de texte vous permet de fournir une description sur plusieurs lignes du tarif. | Ce champ est affiché dans les vues **Associé(e)** sur le tarif dans diverses entités qui ont des tarifs associés. |

3. Enregistrez les tarifs. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Mettre à jour un tarif en appliquant une majoration à tous les prix

1. Sous les onglets **Rôle**, **Catégorie**, et **Élément tarifaire** d’un tarif, vous pouvez sélectionner **Mettre à jour les prix** pour appliquer une majoration pour tous les prix de la sous-grille. 
2. Sur la page de dialogue qui s’ouvre, entrez une majoration. Vous pouvez également saisir un pourcentage de majoration négatif pour réduire les prix d’un certain pourcentage. 
3. Sélectionnez **OK** dans la page de dialogue, puis vérifiez que les prix de la sous-grille reflètent les modifications que vous avez effectuées.


[!INCLUDE[footer-include](../includes/footer-banner.md)]