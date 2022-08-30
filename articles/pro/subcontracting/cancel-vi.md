---
title: Annuler une facture du fournisseur de projet
description: Cet article explique comment annuler une facture fournisseur de projet dans Microsoft Dynamics 365 Project Operations et l’impact financier de l’annulation d’une facture fournisseur de projet.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261087"
---
# <a name="cancel-a-project-vendor-invoice"></a>Annuler une facture du fournisseur de projet

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Une fois qu’une facture fournisseur est confirmée, elle ne peut plus être modifiée ni supprimée. Si une erreur s’est produite sur une facture fournisseur qui a été confirmée, vous pouvez utiliser l’action Annuler pour annuler l’impact de la facture fournisseur et créer une nouvelle facture fournisseur.

Lorsque vous sélectionnez **Annuler** sur une facture fournisseur, le comportement suivant se produit :

1. L’état de la facture fournisseur est mis à jour sur **Annulé**.
2. La facture fournisseur annulée et ses enregistrements associés passent en lecture seule et ne peuvent être ni modifiés ni supprimés.
3. Tous les chiffres réels du coût qui ont été créés sur la base des lignes de facture fournisseur dans le cadre de la confirmation de la facture fournisseur sont annulés.
4. Si des chiffres réels du coût étaient liés aux lignes de facture fournisseur dans le cadre du processus de rapprochement, la confirmation de facture fournisseur d’origine les annulait. Lors de l’annulation d’une facture fournisseur, ces chiffres réels du coût sont recréés. Les origines pointent vers les entrées de temps, de dépense ou d’utilisation de matériel.
5. Une fois la facture fournisseur annulée, vous pouvez à nouveau créer des journaux de correction, traiter les rappels de saisie de temps et annuler l’approbation des chiffres réels du temps, des dépenses ou du matériel d’origine.

> [!NOTE]
> Seules les factures fournisseur du projet confirmées peuvent être annulées. Les factures fournisseur dans d’autres états ne peuvent pas être annulées.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
