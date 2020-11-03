---
title: Demandes de déplacement
description: Cette rubrique fournit des informations sur les demandes de déplacement.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075609"
---
# <a name="travel-requisitions"></a>Demandes de déplacement

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Une demande de déplacement énumère les dépenses qui seront engagées aux fins du déplacement. Une demande de déplacement est soumise pour examen et peut être utilisée pour autoriser des dépenses.

Vous devrez peut-être soumettre une demande de déplacement avant d’engager toute dépense facturée à l’organisation. Cette exigence s’applique, que vous facturiez des dépenses sur une carte de crédit d’entreprise, que vous dépensiez de l’argent que vous avez reçu d’une avance de fonds ou que vous engagiez des dépenses personnelles qui seront remboursées par l’organisation.

Les demandes de déplacement et les politiques peuvent être utilisées pour aider à gérer les dépenses de l’organisation. Par exemple, si votre organisation travaille sur un projet à prix fixe qui nécessite des déplacements, les frais de déplacement des membres de l’équipe du projet doivent s’inscrire dans le budget du projet. En exigeant que les frais de déplacement soient approuvés avant qu’ils ne soient engagés, l’organisation peut aider à s’assurer que le projet respecte le budget.

## <a name="configuration"></a>configuration 

Les demandes de déplacement peuvent être configurées comme « obligatoires » en activant le paramètre « Préautorisation de déplacement obligatoire » dans les paramètres de Gestion des dépenses. 

## <a name="create-and-submit-a-travel-requisition"></a>Créer et soumettre une demande de déplacement

1. Accédez à **Mes dépenses : Demande de déplacement** et sélectionnez **Nouvelle demande de déplacement**.
2. Saisissez un objet et une destination pour la demande.
3. Dans le champ **Description du déplacement** , entrez toute information supplémentaire. 
4. Pour chacune des dépenses attendues, telles que le vol, les repas ou la location de voiture, créez une ligne de dépenses. Incluez la date estimée, le montant estimé et la devise de chaque dépense. 
5. Lorsque vous avez terminé d’ajouter les dépenses prévues, sélectionnez **Enregistrer**.
6. Lorsque vous êtes prêt à soumettre la demande de déplacement, sélectionnez **Workflow** > **Envoyer**.

Vous pouvez consulter vos demandes de déplacement approuvées sous **Mes dépenses : demande de déplacement**. 

## <a name="view-available-travel-requisitions"></a>Afficher les demandes de déplacement disponibles

Vous pouvez consulter toutes vos demandes de déplacement approuvées sous **Mes dépenses : Demandes de déplacement**.

## <a name="approve-travel-requisitions"></a>Approuver des demandes de déplacement

Sélectionnez la demande de déplacement que vous souhaitez approuver, puis sélectionnez **Workflow** > **Approuver**.  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a>Soumettre une note de frais en utilisant votre demande de déplacement approuvée

1. Créez une note de frais et dans l’en-tête de note de frais, et dans la liste des demandes de déplacement approuvées, sélectionnez **Mapper à la demande de déplacement**.
2. Le champ **Montant de la demande de déplacement** est automatiquement mis à jour dans l’en-tête de la note de frais.
3. Ajoutez chaque dépense engagée pour le déplacement. Si le champ **Préautorisé** est activé, le montant rapproché et le montant autorisé pour la catégorie de dépenses spécifique seront mis à jour.

> [!NOTE]
> Lorsque vous mappez une note de frais à une demande de déplacement approuvée, le montant de la transaction ne peut pas être supérieur au montant autorisé. 
