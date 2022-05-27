---
title: Valeurs par défaut d’une dimension financière
description: Cette rubrique fournit des informations sur la configuration des valeurs par défaut des dimensions financières.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9f43fed57a1411a55dcd7929f34e87aed136a6b5
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579487"
---
# <a name="financial-dimension-defaults"></a>Valeurs par défaut d’une dimension financière

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_



Dynamics 365 Project Operations utilise la structure [Dimensions financières](/dynamics365/finance/general-ledger/financial-dimensions) dans Dynamics 365 Finance pour fournir des informations supplémentaires sur les transactions de comptabilité auxiliaire de projet et de comptabilité.

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
3. Développez **Informations associées**, puis cliquez sur l’onglet **Sources de financement**.
4. Définissez les valeurs par défaut des dimensions financières. Notez que les dimensions financières par défaut proviennent du compte client.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Définir les dimensions financières d’une ligne de contrat de projet

1. Accédez à **Gestion du projet et comptabilité** > **Projets** > **Contrats de projet**.
2. Sélectionnez l’enregistrement que vous souhaitez mettre à jour et dans l’onglet **Contrat de projet**, sélectionnez **Afficher la comptabilité par défaut**.
3. Développez **Informations associées**, puis cliquez sur l’onglet **Lignes de contrat**.
4. Définissez les valeurs par défaut des dimensions financières. Les valeurs par défaut des dimensions financières sont applicables et ne peuvent être utilisées qu’avec des lignes de contrat à prix fixe (jalon).

Ces valeurs par défaut sont utilisées sur les transactions en compte de projet et les lignes de facture associées.

## <a name="define-default-financial-dimensions-for-projects"></a>Définir les dimensions financières par défaut pour des projets

Les projets sont créés et gérés dans CDS. Les attributs comptables des projets sont définis dans le module **Gestion du projet et comptabilité** dans Finance.

1. Accédez à **Gestion du projet et comptabilité** > **Projets** > **Tous les projets**.
2. Sélectionnez l’enregistrement que vous souhaitez mettre à jour et dans l’onglet **Projet**, sélectionnez **Afficher la comptabilité par défaut**.
3. Développez **Informations associées**, puis cliquez sur l’onglet **Configuration**.
4. Définissez les valeurs par défaut des dimensions financières. Notez que les dimensions financières proviennent par défaut du compte client. Si le projet est associé à une ligne de contrat avec plusieurs clients de contrat de projet, le client principal est utilisé pour les dimensions financières par défaut.

Les dimensions financières par défaut du projet permettent de définir les valeurs par défaut des lignes feuille pour les transactions de temps, de dépenses et de frais dans la **Feuille Intégration Project Operations** et sur les lignes de facture de projet associées.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
