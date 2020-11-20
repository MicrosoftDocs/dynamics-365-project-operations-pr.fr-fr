---
title: Gérer la réplication de facturation – Simplifié
description: Cette rubrique fournit des informations sur les différentes vues disponibles à utiliser lors de la gestion de la réplication de facturation.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e3ca167fa53a6923727eff3e7c34c8706dc7455
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176968"
---
# <a name="manage-the-billing-backlog---lite"></a>Gérer la réplication de facturation – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations dispose de vues dédiées pour aider à la gestion de la réplication de facturation. Pour gérer la réplication de facturation, sélectionnez les liens dans la zone **Ventes**, sous **Facturation**. 

Les vues suivantes sont disponibles :

- Provisions et avances
- Provisions et avances disponibles
- Jalons de prix fixe
- Réplication de facturation pour les produits
- Réplication de facturation pour le temps et le matériel

## <a name="retainers-and-advances"></a>Provisions et avances

La vue **Provisions et avances** répertorie toutes les provisions et les avances de tous les contrats de projet dans le système. Après la facturation d’une provision ou d’une avance, le montant de l’avance devient utilisable.

## <a name="available-retainers-and-advances"></a>Provisions et avances disponibles

La vue **Provisions et avances disponibles** répertorie toutes les provisions et les avances disponibles de tous les contrats de projet dans le système. Après la facturation d’une provision ou d’une avance, le montant de l’avance devient utilisable et est ajouté à la liste. Une fois que le montant de la provision ou de l’avance est complètement utilisé, il est supprimé de la liste.

## <a name="fixed-price-milestones"></a>Jalons de prix fixe

La vue **Jalons de prix fixes** répertorie tous les jalons à prix fixe de toutes les lignes de contrat de projet du système. Un ou plusieurs jalons peuvent être marqués comme **Prêt pour la facturation** ou **Non prêt pour la facturation** dans cette vue. Le fait de marquer un jalon comme **Prêt pour la facturation** le rend disponible pour pouvoir figurer sur une facture en mode brouillon.

Lorsque les lignes de contrat multi-clients ont une méthode de facturation à prix fixe, un jalon est créé pour chaque client sur la ligne de contrat. Un jalon peut être créé, puis fractionné en enregistrements de jalons individuels spécifiques au client. Cet fractionnement est interne et conforme au pourcentage de fractionnement de facturation défini pour chaque client sur la ligne de contrat. Dans la vue **Jalons à prix fixe**, vous verrez les enregistrements de jalons spécifiques au client. Chacun de ces enregistrements de jalons peut être marqué comme **Prêt pour la facturation** séparément dans cette vue. Lorsqu’un ou plusieurs fractionnements de jalon connexes sont marquées comme **Prêt pour la facturation**, le statut de l’en-tête est mis à jour, passant ainsi de **En cours** à **Pas démarré**. Lorsque tous les fractionnements de jalon sont facturés, le statut du jalon de l’en-tête est mis à jour sur **Terminé**.

Un jalon sur une facture provisoire est affiché dans cette vue avec le statut de facturation **Facture client créée**. Lorsque la facture en mode brouillon est confirmée, le statut de facturation de l’enregistrement est mis à jour sur **Facture client publiée**. Ne mettez pas à jour cette valeur de statut à l’aide d’un code personnalisé. Project Operations ne fonctionne pas correctement lorsque ces valeurs de statut sont mises à jour avec un code personnalisé.

## <a name="product-billing-backlog"></a>Réplication de facturation pour les produits

La vue **Réplication de facturation pour les produits** répertorie toutes les lignes de contrat basées sur les produits dans tous les contrats de projet du système. Une ou plusieurs lignes de contrat basées sur les produits peuvent être marqués comme **Prêt pour la facturation** ou **Non prêt pour la facturation** dans cette vue. Le fait de marquer une ligne de contrat basée sur les produits comme **Prêt pour la facturation** le rend disponible pour pouvoir figurer sur une facture en mode brouillon.

Une ligne de contrat basée sur les produits qui se trouve sur une facture en mode brouillon est affichée dans cette vue avec le statut de facturation **Facture client créée**. Lorsque la facture provisoire est confirmée, le statut de facturation de cet enregistrement devient **Facture client publiée**. Ne mettez pas à jour cette valeur de statut à l’aide d’un code personnalisé. Project Operations ne fonctionne pas correctement lorsque ces valeurs de statut sont mises à jour avec un code personnalisé.

## <a name="time-and-material-billing-backlog"></a>Réplication de facturation pour le temps et le matériel

La vue **Réplication de facturation pour le temps et le matériel** répertorie tous les chiffres réels des ventes non facturées dans tous les contrats de projet du système qui n’ont pas été facturés. Une ou plusieurs ventes réelles non facturées peuvent être marquées comme **Prêt pour la facturation** ou **Non prêt pour la facturation** dans cette vue. Marquer une vente réelle non facturée comme étant **Prêt pour la facturation** la rend disponible afin qu’elle figure sur une facture provisoire.

Les chiffres réels de ventes non facturées avec un statut **Ne pas dépasser** **Échoué** ne peuvent pas être marqués comme **Prêt pour la facturation**. Si les chiffres réels doivent être marqués comme **Prêt pour la facturation**, réinitialisez le statut des autres chiffres réels sur la ligne de contrat qui sont validés. Puis, réévaluez le statut **Ne pas dépasser**.

Si les lignes de contrat multi-clients ont une méthode de facturation du temps et des matériels, une fois le temps et les dépenses approuvés, un chiffre réel de ventes non facturé est créé pour chaque client sur la ligne de contrat selon le pourcentage de fractionnement de facturation défini pour chacun des clients. Dans la vue **Réplication de facturation pour le temps et le matériel**, vous verrez ces chiffres réels de ventes non facturés spécifiques au client individuel. Chacun de ces enregistrements de vente réelle non facturée peut être marqué comme **Prêt pour la facturation** séparément dans cette vue.

Un chiffre réel de ventes non facturé qui se trouve sur une facture en mode brouillon est affiché dans cette vue avec le statut de facturation **Facture client créée**. Lorsque la facture provisoire est confirmée, le statut de facturation de cet enregistrement devient **Facture client publiée**. Ne mettez pas à jour cette valeur de statut à l’aide d’un code personnalisé. Project Operations ne fonctionne pas correctement lorsque ces valeurs de statut sont mises à jour avec un code personnalisé.
