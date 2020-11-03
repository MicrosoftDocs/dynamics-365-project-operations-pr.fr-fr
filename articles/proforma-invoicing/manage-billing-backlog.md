---
title: Gérer la réplication de facturation
description: Cette rubrique fournit des informations sur la façon d'afficher et d'utiliser la réplication de facturation dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087903"
---
# <a name="manage-the-billing-backlog"></a>Gérer la réplication de facturation

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations dispose de deux vues dédiées pour vous aider à utiliser et gérer la réplication de facturation. Il s'agit de **Jalons de prix fixe** et **Réplication de facturation pour le temps et le matériel** Pour sélectionner une vue, dans la zone **Ventes** de Project Operations, sur la page de navigation de gauche, sélectionnez **Facturation**. Les liens de réplication de facturation y sont stockés.

## <a name="fixed-price-milestones"></a>Jalons de prix fixe

Cette vue répertorie tous les jalons de prix fixe sur toutes les lignes de contrat de projet du système. Un ou plusieurs jalons peuvent être marqués comme **Prêt pour la facturation** ou **Non prêt pour la facturation** dans cette vue. Lorsque vous marquez un jalon comme **Prêt pour la facturation** , le jalon devient disponible pour une facture provisoire.

Lorsque les lignes de contrat avec plusieurs clients ont une méthode de facturation à prix fixe, un jalon est créé pour chaque client de la ligne de contrat. L'utilisateur crée un jalon et ce jalon est fractionné en enregistrements de jalons spécifiques au client en interne, selon le pourcentage de facturation fractionné défini pour chaque client sur la ligne de contrat. Dans la vue **Jalons de prix fixes** , vous verrez des enregistrements de jalons spécifiques au client. Chacun de ces enregistrements de jalons peut être marqué comme **Prêt pour la facturation** séparément dans cette vue. Lorsqu'un ou plusieurs fractionnements de jalons associés sont marqués comme **Prêt pour la facturation** , l'en-tête passe de l'état **Non démarré** à **En cours**. Lorsque tous les fractionnements de jalons ont été facturés, le statut du jalon de l'en-tête devient **Terminé**.

Un jalon sur une facture provisoire est affiché dans cette vue avec le statut de facturation **Facture client créée**. Lorsque la facture provisoire est confirmée, le statut de facturation de cet enregistrement devient **Facture publiée**. Il n'est pas recommandé de mettre à jour cette valeur de statut à l'aide d'un code personnalisé. Project Operations ne fonctionnera pas correctement si ces valeurs de statut sont mises à jour avec un code personnalisé.

## <a name="time-and-material-billing-backlog"></a>Réplication de facturation pour le temps et le matériel

Cette vue répertorie toutes les ventes réelles non facturées qui n'ont pas été facturées pour l'ensemble des contrats de projet dans le système. Une ou plusieurs ventes réelles non facturées peuvent être marquées comme **Prêt pour la facturation** ou **Non prêt pour la facturation** dans cette vue. Marquer une vente réelle non facturée comme étant **Prêt pour la facturation** la rend disponible afin qu'elle figure sur une facture provisoire.

Les ventes réelles non facturées dont le statut **Ne pas dépasser** est **Échec** ne peuvent pas être marquées comme **Prêt pour la facturation**. Si ces ventes réelles doivent être marquées comme telles, réinitialisez le statut des autres ventes réelles de la ligne de contrat qui sont validées, puis évaluez le statut **Ne pas dépasser**.

Dans le cas de lignes de contrat avec plusieurs clients ayant une méthode de facturation du temps et du matériel, lorsque le temps et les dépenses sont approuvés, une vente réelle non facturée est créée pour chaque client sur la ligne de contrat, selon le pourcentage de facturation défini pour chaque client sur la ligne de contrat. Dans la vue **Réplication de facturation pour le temps et le matériel** , vous verrez ces ventes réelles non facturées spécifiques au client. Chacun de ces enregistrements de vente réelle non facturée peut être marqué comme **Prêt pour la facturation** séparément dans cette vue.

Une vente réelle non facturée sur une facture provisoire est affichée dans cette vue avec le **Statut de facturation** **Facture client créée**. Lorsque la facture provisoire est confirmée, le statut de facturation de cet enregistrement devient **Facture client publiée**. Lorsque ce statut est en vigueur, il n'est pas recommandé de mettre à jour cette valeur de statut à l'aide d'un code personnalisé. Project Operations ne fonctionnera pas correctement lorsque ces valeurs de statut sont mises à jour avec un code personnalisé.
