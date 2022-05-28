---
title: Confirmer une facture fournisseur de projet
description: Cette rubrique explique comment confirmer une facture fournisseur de projet dans Microsoft Dynamics 365 Project Operations et l’impact financier de la confirmation d’une facture fournisseur de projet.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595725"
---
# <a name="confirm-a-project-vendor-invoice"></a>Confirmer une facture fournisseur de projet

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Après avoir vérifié toutes les lignes d’une facture fournisseur dans Microsoft Dynamics 365 Project Operations, vous pouvez utiliser l’action Confirmer pour confirmer la facture fournisseur.

Lorsque vous sélectionnez **Confirmer** sur une facture fournisseur, le comportement suivant se produit :

1. L’état de la facture fournisseur est mis à jour sur **Confirmé**.
2. La facture fournisseur confirmée et ses enregistrements associés passent en lecture seule et ne peuvent être ni modifiés ni supprimés.
3. Si des coûts réels font référence à la ligne de facture fournisseur dans le cadre du processus de rapprochement, tous les coûts réels associés à la ligne de facture fournisseur référencée sont annulés.
4. Des chiffres réels du coût sont créés à l’aide des informations de la ligne de facture fournisseur.
5. Une fois la facture fournisseur confirmée, vous ne pouvez plus créer des journaux de correction, traiter les rappels de saisie de temps et annuler l’approbation des chiffres réels du temps, des dépenses ou du matériel d’origine qui ont été annulés.

> [!NOTE]
> Si une ligne d’une facture fournisseur a un statut de vérification autre que **Terminé**, la facture fournisseur ne peut pas être confirmée.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
