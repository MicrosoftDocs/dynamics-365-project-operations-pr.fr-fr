---
title: Jalons de la ligne du contrat de sous-traitance
description: Cette rubrique explique comment créer et gérer un échéancier de facturation basé sur des jalons pour un contrat de sous-traitance avec un fournisseur.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3301e5a627e4842009fcd5e352f1b76fd3053ee3
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323773"
---
# <a name="subcontract-line-milestones"></a>Jalons de la ligne du contrat de sous-traitance

[!include [banner](../../includes/dataverse-preview.md)]

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Dans Dynamics 365 Project Operations, une ligne du contrat de sous-traitance avec une méthode de facturation à prix fixe peut spécifier un échéancier de facturation basé sur des jalons avec le fournisseur.

Les jalons pour la facturation fournisseur peuvent être générés automatiquement à une fréquence définie, ou vous pouvez les créer manuellement.

## <a name="automatically-create-a-milestone-based-invoice-schedule-for-a-subcontract-line"></a>Créer automatiquement un échéancier de facturation basé sur des jalons pour une ligne du contrat de sous-traitance

Procédez comme suit pour générer automatiquement un échéancier de facturation basé sur des jalons pour un ensemble fixe de jalons répartis de manière égale.

1. Allez dans **Paramètres** > **Fréquences de facturation** et paramétrez la fréquence de facturation des lignes du contrat de sous-traitance.
2. Ouvrez la page **Sous-traitance**, puis ouvrez le contrat de sous-traitance à utiliser, puis la ligne du contrat de sous-traitance à prix fixe pour laquelle vous allez créer un échéancier.
3. Sur l’onglet **Jalons de la ligne du contrat de sous-traitance**, sélectionnez **Générer des jalons périodiques**.
4. Dans la boîte de dialogue, saisissez ou sélectionnez une plage de dates, le nombre de jalons et la fréquence de facturation. Vous pouvez sélectionner une date de début, ou sélectionner le nombre de jalons et la fréquence de facturation ou la date de début, ou sélectionner la date de fin et la fréquence de facturation. Vous ne pouvez pas sélectionner la date de fin et le nombre de jalons.
À l’aide de ces informations, le système génère des jalons et des enregistrements qui sont affichés dans la grille **Jalons**.

   - **Nom du jalon** - Le nom du jalon est défini sur la date du jalon en fonction de la fréquence de facturation.
   - **Date du jalon** - La date est basée sur la fréquence de facturation.
   - **Montant du jalon** - Le montant est calculé en divisant le montant du sous-total sur la ligne de sous-traitance par le nombre de jalons.

Si la ligne de sous-traitance contient une valeur dans le champ **Montant de taxe estimé**, cette valeur est ajoutée à chaque jalon de manière égale lors de la génération de jalons périodiques.

La somme des montants des jalons de la ligne de contrat de sous-traitance doit être égale à la valeur de la ligne du contrat de sous-traitance. S’ils ne sont pas égaux, une erreur se produit. Vous pouvez corriger l’erreur et vérifier que le total du jalon est égal à la valeur de la ligne du contrat de sous-traitance en créant, modifiant ou supprimant des montants de jalon et de taxe. Une fois les modifications apportées, enregistrez et actualisez la page pour vous assurer qu’il n’y a plus d’erreurs.

## <a name="manually-create-subcontract-line-milestones"></a>Créer manuellement des jalons de la ligne du contrat de sous-traitance

Les jalons à prix fixe sur une ligne du contrat de sous-traitance peuvent être générés manuellement lorsqu’ils ne sont pas fractionnés périodiquement. Pour créer manuellement des jalons de la ligne du contrat de sous-traitance, procédez comme suit :

1. Sur le volet de navigation, sélectionnez **Contrats de sous-traitance** et ouvrez le contrat de sous-traitance que vous voulez utiliser.
2. Ouvrez la ligne de sous-traitance à prix fixe pour laquelle vous souhaitez créer un jalon.
3. Sur l’onglet **Jalons de la ligne du contrat de sous-traitance**, dans la sous-grille, sélectionnez **+ Nouveau jalon de la ligne du contrat de sous-traitance**.
4. Sur la page **Nouveau jalon de la ligne du contrat de sous-traitance**, saisissez les informations requises, basées sur le tableau suivant.

    | Champ | Description |
    | --- | --- |
    | Nom du jalon | Nom du jalon. |
    | Description | Une description du jalon.  |
    | Date du jalon | La date à laquelle le processus de création automatique de facture doit rechercher le statut de ce jalon afin de le prendre en compte pour la facturation. Cette valeur se trouve sur la ligne de facture fournisseur lors de la facturation de ce contrat de sous-traitance. |
    | Montant | Le montant ou la valeur du jalon qui sera facturé au client. Cette valeur se trouve sur la ligne de facture fournisseur lors de la facturation de ce contrat de sous-traitance. |
    | Taxes | Le montant de la taxe appliqué sur le jalon. Cette valeur se trouve sur la ligne de facture fournisseur lors de la facturation de ce contrat de sous-traitance. |
    | Montant après impôts | Ce champ en lecture seule est calculé comme suit : Montant + Taxe. Cette valeur se trouve sur la ligne de facture fournisseur lors de la facturation de ce contrat de sous-traitance. |
    | Statut de la facture | Lorsque le jalon est créé, ce statut est toujours défini sur **Non prêt pour la facturation**.  Lorsque le statut est **Prêt pour la facturation**, ce jalon est inclus sur la facture fournisseur. |

5. Sélectionnez **Enregistrer et fermer**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
