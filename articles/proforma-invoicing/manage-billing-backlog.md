---
title: Gérer la réplication de facturation
description: Cette rubrique fournit des informations sur la façon d’afficher et d’utiliser la réplication de facturation dans Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9837af0d3c0b2476edab35a53092cf95a44e5244
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599981"
---
# <a name="manage-billing-backlog"></a>Gérer la réplication de facturation

**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés

Dynamics 365 Project Operations offre des vues dédiées permettant de gérer le backlog de facturation. Pour gérer la réplication de facturation, sélectionnez les liens dans la zone **Ventes**, sous **Facturation**. 

Les vues suivantes sont disponibles :

- Provisions et avances
- Provisions et avances disponibles
- Jalons de prix fixe
- Réplication de facturation pour le temps et le matériel

## <a name="retainers-and-advances"></a>Provisions et avances

La vue **Provisions et avances** répertorie toutes les provisions et avances sur l’ensemble des contrats de projet. Après la facturation d’une provision ou d’une avance, le montant de l’avance devient utilisable.

## <a name="available-retainers-and-advances"></a>Provisions et avances disponibles

La vue **Provisions et avances disponibles** répertorie toutes les provisions et avances disponibles sur l’ensemble des contrats de projet. Après la facturation d’une provision ou d’une avance, le montant de l’avance devient utilisable et est ajouté à la liste. Une fois le montant de la provision ou de l’avance complètement utilisé, il est supprimé de la liste.

## <a name="fixed-price-milestones"></a>Jalons de prix fixe

La vue **Jalons à prix fixe** répertorie tous les jalons à prix fixe sur l’ensemble des lignes de contrat de projet. À partir de cette vue, le statut **Prêt pour la facturation** ou **Non prêt pour la facturation** peut être affecté à un ou plusieurs jalons. L’affectation du statut **Prêt pour la facturation** à un jalon le met à disposition pour figurer sur une facture provisoire.

Lorsque les lignes de contrat multi-clients ont une méthode de facturation à prix fixe, un jalon est créé pour chaque client sur la ligne de contrat. Un jalon peut être créé, puis fractionné en enregistrements de jalons individuels spécifiques au client. Cet fractionnement est interne et conforme au pourcentage de fractionnement de facturation défini pour chaque client sur la ligne de contrat. Dans la vue **Jalons à prix fixe**, vous verrez les enregistrements de jalons spécifiques au client. Chacun de ces enregistrements de jalons peut être marqué comme **Prêt pour la facturation** séparément dans cette vue. Lorsqu’un ou plusieurs des fractionnements de jalons associés sont marqués comme **Prêt à facturer**, l’état de l’en-tête passe de **En cours** à **Non commencé**. Lorsque tous les fractionnements de jalons sont facturés, le statut du jalon d’en-tête devient **Terminé**.

Un jalon sur une facture provisoire est affiché dans cette vue avec le statut de facturation **Facture client créée**. Lorsque la facture en mode brouillon est confirmée, le statut de facturation de l’enregistrement est mis à jour sur **Facture client publiée**. 

> [!NOTE] 
> Ne mettez pas à jour la valeur d’état à l’aide de code personnalisé. Project Operations ne fonctionne pas correctement lorsque ces valeurs de statut sont mises à jour avec un code personnalisé.

## <a name="time-and-material-billing-backlog"></a>Réplication de facturation pour le temps et le matériel

La vue **Réplication de facturation pour le temps et le matériel** répertorie tous les chiffres réels des ventes non facturées dans tous les contrats de projet du système qui n’ont pas été facturés. Une ou plusieurs ventes réelles non facturées peuvent être marquées comme **Prêt pour la facturation** ou **Non prêt pour la facturation** dans cette vue. Marquer une vente réelle non facturée comme étant **Prêt pour la facturation** la rend disponible afin qu’elle figure sur une facture provisoire.

Les chiffres réels de ventes non facturées avec un statut **Ne pas dépasser** **Échoué** ne peuvent pas être marqués comme **Prêt pour la facturation**. Si les chiffres réels doivent être marqués comme **Prêt à facturer**, réinitialisez le statut des autres chiffres réels sur la ligne de contrat qui sont validés, puis réévaluez le statut **Ne pas dépasser**.

Si les lignes de contrat multi-clients ont une méthode de facturation du temps et des matériels, une fois le temps et les dépenses approuvés, un chiffre réel de ventes non facturé est créé pour chaque client sur la ligne de contrat selon le pourcentage de fractionnement de facturation défini pour chacun des clients. Dans la vue **Réplication de facturation pour le temps et le matériel**, vous verrez ces chiffres réels de ventes non facturés spécifiques au client individuel. Chacun de ces enregistrements de vente réelle non facturée peut être marqué comme **Prêt pour la facturation** séparément dans cette vue.

Un chiffre réel de ventes non facturées figurant sur une facture provisoire s’affiche sur cette vue avec le statut de facturation **Facture client créée**. Lorsque la facture provisoire est confirmée, le statut de facturation de cet enregistrement devient **Facture client validée**. 

> [!NOTE] 
> Ne mettez pas à jour la valeur d’état à l’aide de code personnalisé. Project Operations ne fonctionne pas correctement lorsque ces valeurs de statut sont mises à jour avec un code personnalisé.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
