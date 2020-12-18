---
title: Créer des factures clients et fournisseurs intersociétés
description: Cette rubrique fournit des informations sur la manière de créer des factures clients et fournisseurs intersociétés.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: f1560469d2bdbb8e81dc26c16b272c44446ab20a
ms.sourcegitcommit: addbe0647619413e85e7cde80f6a21db95ab623e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2020
ms.locfileid: "4595464"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a>Créer des factures clients et fournisseurs intersociétés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Un comptable de projet dans une entité juridique prêteuse crée une facture client intersociétés pour les coûts de projet qui sont transférés à l'entité emprunteuse. Une fois la facture client intersociétés approuvée et validée, l'entité juridique prêteuse envoie la facture intersociétés à l'entité juridique emprunteuse.

Le comptable de projet de l'entité juridique prêteuse peut configurer un traitement par lots pour générer des factures intersociétés de manière récurrente. Le comptable de projet spécifie les critères, tels que des projets spécifiques, pour créer des factures intersociétés dans un lot.

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a>Créer manuellement une facture client intersociétés pour les transactions de projet 

Utilisez cette procédure pour créer manuellement une facture client intersociétés pour les transactions de projet. Recherchez les heures qui ont été validées par des collaborateurs sur des projets dans les entités juridiques emprunteuses et les dépenses engagées par votre entité juridique pour le compte d'entités juridiques emprunteuses. Vous pouvez effectuer une recherche par nom d'entité juridique, numéro de contrat de projet, numéro de projet, plage de dates ou toute combinaison de ces options. Dans les résultats de la recherche, sélectionnez les transactions à ajouter à une facture intersociétés.

1. Dans Dynamics 365 Finance, accédez à **Gestion et comptabilité des projets** > **Factures de projet** > **Factures clients intersociétés**. Sur la page de liste **Factures clients intersociétés**, dans le volet Actions, sélectionnez **Nouveau.**
2. Sur la page **Créer une facture intersociétés**, dans le champs **Entité juridique**, sélectionnez une entité juridique emprunteuse.
3. Facultatif : saisissez un contrat de projet spécifique et un numéro de projet.
4. Affinez la recherche en sélectionnant une plage de dates. Saisissez des dates spécifiques dans les champs **Date de début** et **Date de fin**. Seules les transactions intersociétés validées dans cette plage de dates sont affichées dans les résultats de la recherche.
5. Définissez **Paramètre de ligne de journal avancé du projet** sur **Oui** et sélectionnez **Rechercher**.
6. Dans les résultats de la recherche, sélectionnez les transactions à inclure dans la proposition de facture intersociétés, puis sélectionnez **OK**.
7. Sur la page **Facture client intersociétés**, les transactions de projet intersociétés que vous avez sélectionnées dans les résultats de la recherche s'affichent. Pour modifier les transactions avant d'envoyer la facture à l'entité juridique emprunteuse, procédez comme suit :
  
    1. Ouvrez la page **Créer une proposition de facture**. Sélectionnez des transactions intersociétés supplémentaires pour la facture actuelle, puis sélectionnez **Ajouter une ligne**.
    2. Pour supprimer une ligne, sélectionnez-la, puis cliquez sur **Supprimer**.
    3. Afficher des commentaires, des raisons, des dimensions financières et d'autres informations au sujet d'une ligne sélectionnée sur le raccourci **Lignes de facture**.
    
8. Pour valider la facture client intersociétés, sélectionnez **Valider** dans le volet Actions.

> [!NOTE]
> Si votre organisation exige que les factures intersociétés soient examinées avant leur validation, un administrateur système peut configurer un flux de travail pour les factures intersociétés. Si aucun flux de travail n'est configuré pour les factures intersociétés, vous pouvez valider la facture intersociétés.

## <a name="create-a-batch-job-for-intercompany-invoices"></a>Créer un traitement par lots pour les factures intersociétés

Vous pouvez créer plusieurs factures intersociétés en même temps pour toutes les entités juridiques emprunteuses. À l'aide de la fonctionnalité de recherche, vous pouvez par exemple rechercher toutes les transactions qui sont validées par les collaborateurs empruntés et liées à des projets gérés par d'autres entités juridiques. Ensuite, pour chaque entité juridique emprunteuse, vous pouvez créer une facture intersociétés pour les transactions fournies dans les résultats de la recherche.

1. Accédez à **Gestion et comptabilité des projets** > **Périodique** > **Factures de projet** > **Créer des factures clients intersociétés**.
2. Sur la page **Créer des factures clients et fournisseurs intersociétés**, dans le champs **Société**, sélectionnez une entité juridique à facturer. Si vous ne sélectionnez pas de société, toutes les transactions qui répondent aux critères de recherche sont affichées pour toutes les entités juridiques emprunteuses.
3. Dans **Créer une facture par**, indiquez si vous souhaitez créer une facture pour les transactions intersociétés basées sur un projet ou sur une entité juridique emprunteuse.
4. Facultatif : pour sélectionner un projet et un contrat de projet spécifiques pour lesquels créer des factures intersociétés, cliquez sur **Sélectionner**. Sur la page **Demande**, dans le champ **Critères**, sélectionnez le contrat de projet, le numéro de projet ou les deux, puis sélectionnez **OK**.
5. Sur l'onglet **Lot**, configurez un traitement par lots pour créer des factures intersociétés de manière récurrente. Pour plus d'informations, voir [Soumettre une tâche de traitement par lots à partir d'un formulaire](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).
6. Pour valider les factures client intersociétés, sélectionnez **Valider** dans le volet Actions.

> [!NOTE]
> Si votre organisation exige que les factures intersociétés soient examinées avant leur validation, un administrateur système peut configurer un flux de travail pour les factures intersociétés. Si aucun flux de travail n'est configuré pour les factures intersociétés, vous pouvez valider les factures intersociétés.

## <a name="post-the-intercompany-vendor-invoice"></a>Valider la facture fournisseur intersociétés

Un comptable de projet de l'entité juridique emprunteuse peut consulter les factures fournisseur intersociétés en attente lorsque la facture client intersociétés correspondante est validée. Dans Finance, dans l'entité juridique emprunteuse, accédez à **Comptabilité fournisseur** > **Factures** > **Facture fournisseur en attente**. Le numéro de facture en attente correspondra au numéro de facture client intersociétés. Vérifiez que la facture est correcte, puis validez la facture. La validation d'une facture fournisseur intersociétés crée des transactions comptables et auxiliaires qui reflètent les coûts de transaction dans l'entité juridique emprunteuse.
