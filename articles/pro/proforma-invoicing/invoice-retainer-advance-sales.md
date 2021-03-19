---
title: Facturer une provision ou une avance
description: Cette rubrique fournit des informations sur la facturation d’une provision ou d’une avance dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c53e39a8c6fb27deff5e7a05d5cca3a4215466
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274140"
---
# <a name="invoice-a-retainer-or-an-advance"></a>Facturer une provision ou une avance

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations prend en charge les contrats basés sur un acompte et paiements anticipés ponctuels. Sur un contrat de projet, vous pouvez enregistrer un échéancier des provisions ou une avance ponctuelle. Cependant, l’enregistrement au niveau du contrat de projet ne rend pas immédiatement une provision ou une avance disponible pour utilisation. Pour utiliser une provision ou une avance sur une facture facturant réellement le client, la provision ou l’avance doit être facturée en premier.

Suivez les étapes suivantes pour facturer une provision ou une avance.

1. Sélectionnez **Ventes** > **Facturation** > **Provisions et avances**. 
2. Sur la page **Avances et provisions**, utilisez le filtre pour sélectionner la provision ou l’avance spécifique à facturer et marquez-la comme étant **Prête à facturer**.
3. Créez une facture manuellement à partir de la page de liste ou de détails **Contrat de projet**. La provision ou l’avance est indiquée sur le projet de facture dans la section **Avances et provisions** sur la page **Facture**.
4. Confirmez la facture. Cela rendra la provision ou l’avance disponible pour utilisation. Vous pouvez vérifier la facture sur la page de liste **Provisions et avances**. Pour une avance ou une provision facturée, le montant disponible est indiqué dans la grille.

## <a name="create-a-retainer-or-advance-from-the-invoice-grid"></a>Créer une provision ou une avance à partir de la grille de facturation

Vous pouvez créer une provision ou une avance directement sur une facture.

1. Sur un projet de facture, sur la sous-grille **Avances et provisions**, sélectionnez **Nouveau** pour créer une nouvelle provision ou une nouvelle avance. 
2. Sur la page **Création rapide**, ajoutez les informations nécessaires, puis sélectionnez **Enregistrer**. La provision ou l’avance est créée sur le contrat de projet lié à la facture. La provision ou l’avance est automatiquement marquée comme étant **Prête à facturer**, puis ajoutée à la sous-grille **Avances et provisions** sur la page **Facture**.

## <a name="reconcile-an-invoiced-retainer-or-advance"></a>Rapprocher une provision ou une avance facturée

Une fois qu’une provision ou une avance est facturée, ils peuvent être utilisés ou rapprochés sur une facture avec le temps, les dépenses, les jalons ou d’autres frais liés au projet. Le client verra le montant de sa facture réduit du montant de la provision ou de l’avance utilisée sur cette facture.

Sur chaque facture générée pour un contrat de projet qui a facturé des provisions ou des avances, Project Operation applique automatiquement la provision ou l’avance à la facture.

Cela peut être vu dans la grille **Provisions et avances appliquées** sur la page **Facture**. Le tableau suivant fournit des informations sur les champs de la grille **Provisions et avances appliquées** de la page **Facture de projet**.

| Champ | Emplacement | Description | Impact en aval |
| --- | --- | --- | --- |
| Description | La grille **Provisions et avances appliquées** sur la page **Facture de projet**. |Ce champ en lecture seule fournit une description de la provision ou de l’avance utilisée sur cette facture. Cette valeur ne peut pas être modifiée sur la facture. Cette valeur peut être mise à jour sur la sous-grille de la page **Contrat du projet**. | Ce champ peut être affiché au client sur la facture imprimée pour indiquer quelle provision ou avance est appliquée sur la facture. |
| Date de livraison | La grille **Provisions et avances appliquées** sur la page **Facture de projet**.  | Ce champ en lecture seule fournit la date de la facture de la provision ou de l’avance utilisée sur cette facture. Cette valeur ne peut pas être modifiée sur la facture. Cette valeur peut être mise à jour sur la sous-grille de la page **Contrat du projet**. | Ce champ peut être affiché au client sur la facture imprimée pour indiquer la date à laquelle la provision ou l’avance a été facturée pour la première fois au client. |
| Montant | La grille **Provisions et avances appliquées** sur la page **Facture de projet**.  | Ce champ en lecture seule fournit le montant de la provision ou de l’avance utilisée sur cette facture. Cette valeur ne peut pas être modifiée sur la facture. Cette valeur peut être mise à jour sur la sous-grille de la page **Contrat du projet**. | Ce champ peut être affiché au client sur la facture imprimée pour indiquer le montant d’origine de la provision ou de l’avance ayant été versée par le client. |
| Montant utilisé | La grille **Provisions et avances appliquées** sur la page **Facture de projet**.  | Ce champ en lecture seule fournit la valeur calculée qui récapitule la quantité de provision ou d’avance qui a été utilisée. | Ce champ peut être affiché au client sur la facture imprimée pour indiquer le montant de la provision ou de l’avance ayant déjà été utilisée. |
| Total final | La grille **Provisions et avances appliquées** sur la page **Facture de projet**.  | Ce champ modifiable fournit le montant de la provision ou de l’avance en cours d’utilisation sur cette facture de projet. Ce montant ne peut pas être supérieur à ce qui est disponible sur l’avance. Le système calcule automatiquement cela comme la différence entre les champs **Montant** et **Montant utilisé** sur la grille. Vous pouvez diminuer ce montant pour utiliser moins que ce qui est disponible, mais vous ne pouvez pas augmenter le montant pour utiliser plus que ce qui est disponible. | Ce champ peut être affiché au client sur la facture imprimée pour indiquer le montant de la provision ou de l’avance en cours d’utilisation sur la facture. |
| Montant du solde de la provision. | La grille **Provisions et avances appliquées** sur la page **Facture de projet**.  | Ce champ en lecture seule indique la valeur du montant de la provision ou de l’avance qui restera après la confirmation de la facture. | Ce champ peut être affiché au client sur la facture imprimée pour indiquer le montant qui restera de cette provision ou avance une fois la facture confirmée et payée. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]