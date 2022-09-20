---
title: Confirmer des factures fournisseurs du projet
description: Cet article explique comment confirmer une facture fournisseur de projet dans Microsoft Dynamics 365 Project Operations et décrit l’impact financier de la confirmation d’une facture fournisseur de projet.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475430"
---
# <a name="confirm-project-vendor-invoices"></a>Confirmer des factures fournisseurs du projet

**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés

Quand le paramètre **Une confirmation manuelle par PM est requise** est activé, les factures fournisseur créées dans Microsoft Dataverse ont un statut défini sur **Brouillon**. Les factures fournisseur créées de cette manière doivent être examinées et confirmées manuellement. Quand le paramètre **Une confirmation manuelle par PM est requise** est désactivé, les factures fournisseur créées dans Dataverse sont automatiquement confirmées. Aucune autre action n’est requise. 

Après avoir vérifié toutes les lignes d’une facture fournisseur dans Dynamics 365 Project Operations, sélectionnez **Confirmer** pour confirmer la facture fournisseur.

Lorsque vous sélectionnez **Confirmer** sur une facture fournisseur, le comportement suivant se produit :

1. Le statut de la facture fournisseur est mis à jour sur **Confirmé**.
1. La facture fournisseur confirmée et ses enregistrements associés passent en lecture seule et ne peuvent être ni modifiés ni supprimés.
1. Si des coûts réels font référence à la ligne de facture fournisseur dans le cadre du processus de rapprochement, tous les coûts réels associés à la ligne de facture fournisseur référencée sont annulés.
1. Des chiffres réels du coût sont créés à l’aide des informations de la ligne de facture fournisseur.
1. Vous ne pouvez plus créer des journaux de correction, traiter les rappels de saisie de temps et annuler l’approbation des chiffres réels du temps, des dépenses ou du matériel d’origine qui ont été annulés.
1. Dans Dynamics 365 Finance, la valeur **Coût du projet** est mise à jour à l’aide du journal d’intégration de projet et le compte d’intégration d’approvisionnement est *contrepassé* après la validation du journal d’intégration du projet.

> [!NOTE]
> Si une ligne d’une facture fournisseur a un statut de vérification autre que **Terminé**, la facture fournisseur ne peut pas être confirmée.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
