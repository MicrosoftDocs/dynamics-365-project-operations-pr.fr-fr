---
title: Valeurs par défaut d’une dimension financière
description: Cette rubrique fournit des informations sur la configuration des valeurs par défaut des dimensions financières.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 03b9a9028c1610b191db9c1bfb0163adc88bdf3e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642360"
---
# <a name="financial-dimension-defaults"></a>Valeurs par défaut d’une dimension financière

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations utilise la structure [Dimensions financières](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) dans Dynamics 365 Finance pour fournir des informations supplémentaires sur les transactions comptables et auxiliaires.

Les dimensions financières par défaut peuvent être définies selon un client, une source de financement de projet, un jalon, une ligne de contrat de projet ou un projet.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Définir les dimensions financières par défaut pour un client

Les valeurs par défaut des dimensions client sont spécifiées dans Finance. Effectuez les étapes suivantes pour définir les valeurs par défaut des dimensions.

1. Accédez à **Comptabilité client** > **Clients** > **Tous les clients**.
2. Sur la page **Clients**, dans l’onglet **Dimensions financières**, définissez les valeurs de dimensions financières pour un client spécifique.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Définir les dimensions financières par défaut pour des contrats de projet

Les contrats de projet sont créés et gérés dans Common Data Service (CDS). Les attributs comptables des contrats de projet sont définis dans le module **Gestion du projet et comptabilité** dans Finance.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Définir les dimensions financières d’une source de financement de projet

1. Accédez à **Gestion du projet et comptabilité** > **Projets** > **Contrats de projet**.
2. Sélectionnez l’enregistrement que vous souhaitez mettre à jour et dans l’onglet **Contrat de projet**, sélectionnez **Afficher la comptabilité par défaut**.
3. Développez **Informations connexes** et sélectionnez l’onglet **Sources de financement**.
4. Définissez les valeurs par défaut d’une dimension financière. Notez que les dimensions financières par défaut proviennent du compte client.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Définir les dimensions financières d’une ligne de contrat de projet

1. Accédez à **Gestion du projet et comptabilité** > **Projets** > **Contrats de projet**.
2. Sélectionnez l’enregistrement que vous souhaitez mettre à jour et dans l’onglet **Contrat de projet**, sélectionnez **Afficher la comptabilité par défaut**.
3. Développez **Informations connexes** et sélectionnez l’onglet **Lignes de contrat**.
4. Définissez les valeurs par défaut d’une dimension financière. Les valeurs par défaut des dimensions financières sont applicables et ne peuvent être utilisées qu’avec des lignes de contrat à prix fixe (jalon).

Ces valeurs par défaut sont utilisées pour les transactions de compte de projet et les lignes de facture connexes.

## <a name="define-default-financial-dimensions-for-projects"></a>Définir les dimensions financières par défaut pour des projets

Les projets sont créés et gérés dans CDS. Les attributs comptables des projets sont définis dans le module **Gestion du projet et comptabilité** dans Finance.

1. Accédez à **Gestion du projet et comptabilité** > **Projets** > **Tous les projets**.
2. Sélectionnez l’enregistrement que vous souhaitez mettre à jour et dans l’onglet **Projet**, sélectionnez **Afficher la comptabilité par défaut**.
3. Développez **Informations connexes** et sélectionnez l’onglet **Configurer**.
4. Définissez les valeurs par défaut d’une dimension financière. Notez que ces dimensions financières par défaut proviennent du compte client. Si le projet est associé à une ligne de contrat ayant plusieurs clients de contrat de projet, le client principal est utilisé pour définir les valeurs par défaut des dimensions financières.

Les dimensions financières par défaut du projet sont utilisées pour définir les valeurs par défaut de la ligne de journal des transactions de temps, de dépenses et de frais dans le **Journal d’intégration de Project Operations** et les lignes de facture de projets connexes.
