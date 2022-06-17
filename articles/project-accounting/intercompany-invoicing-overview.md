---
title: Vue d’ensemble de la facturation intersociétés
description: Cet article offre des informations et des exemples sur la facturation intersociétés pour les projets.
author: sigitac
ms.date: 11/19/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fd17f6542558bae9d4b97d0a92aefae52571cfa8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913571"
---
# <a name="intercompany-invoicing-overview"></a>Vue d’ensemble de la facturation intersociétés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Votre organisation peut avoir plusieurs divisions, filiales et autres entités juridiques qui se transfèrent des produits et des services pour des projets. L’entité juridique qui fournit le service ou le produit est appelée *entité juridique prêteuse*. L’entité juridique qui reçoit le service ou le produit est appelée *entité juridique emprunteuse*.

L’illustration suivante montre un scénario typique dans lequel deux entités juridiques, Contoso Robotics USA (l’entité juridique emprunteuse) et Contoso Robotics UK (l’entité juridique prêteuse) partagent des ressources pour livrer un projet pour le client, Adventure works. Pour ce scénario, Contoso Robotics USA est chargé de livrer le travail à Adventure Works.

![Facturation intersociétés.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations utilise le flux suivant pour traiter les transactions intersociétés :

1. Les ressources de l’entité juridique prêteuse enregistrent les transactions de temps ou de dépenses intersociétés en comptabilisant le temps et les dépenses par rapport aux projets de l’entité juridique emprunteuse.
2. Les coûts de temps et de dépenses sont enregistrés dans la société prêteuse en utilisant la liste de prix de revient unitaire de la société emprunteuse.
3. Les transactions de vente non facturée intersociétés sont enregistrés dans la société prêteuse en utilisant la liste de prix de revient unitaire de la société emprunteuse.
4. Le revenu non facturé est enregistré dans la société emprunteuse à l’aide du tarif de vente du contrat de projet. Le client peut être facturé lors de l’enregistrement des revenus non facturés. Le client n’a pas à attendre la fin du traitement des factures intersociétés.
5. Les factures clients intersociétés sont créées périodiquement dans la société prêteuse. Les factures sont créées manuellement ou en utilisant un processus automatisé périodique. Une seule facture peut être créée pour chaque entité juridique emprunteuse ou des factures distinctes peuvent être créées par projet.
6. Lorsque la facture client intersociétés est validée dans l’entité juridique emprunteuse, la facture fournisseur en attente correspondante est créée dans l’entité juridique emprunteuse. Les coûts de la facture fournisseur en attente seront enregistrés dans le livre auxiliaire du projet lorsque la facture est validée.

Le diagramme suivant illustre la facturation intersociétés en ce qui concerne les événements comptables et les écritures attendues dans la comptabilité.

![Flux intersociétés.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Ressources supplémentaires

- [Configurer la facturation intersociétés](configure-intercompany-invoicing.md)
- [Enregistrer des transactions intersociétés](create-intercompany-transactions.md)
- [Créer des factures clients et fournisseurs intersociétés](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]