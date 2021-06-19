---
title: Workflow de gestion des dépenses
description: Cette rubrique explique comment utiliser le système de workflow dans Microsoft Dynamics 365 Finance, pour mettre en place un processus de révision des notes de frais dans la gestion des dépenses.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005203"
---
# <a name="expense-management-workflow"></a>Workflow de gestion des dépenses

Vous pouvez utiliser le système de workflow pour mettre en place un processus de révision des notes de frais dans la gestion des dépenses. Vous pouvez configurer un workflow qui utilise les critères suivants pour déterminer qui approuve les notes de frais :

- La hiérarchie de reporting des employés et les limites d’approbation prédéfinies
- Approbation à plusieurs niveaux qui prend en charge les approbateurs intermédiaires et un approbateur final
- Dimensions financières et responsabilité du projet
- Affectation à des utilisateurs ou groupes d’utilisateurs spécifiques

Les approbations de workflow peuvent être créées pour les notes de frais, les demandes de voyage, les avances de fonds et le recouvrement de la taxe sur la valeur ajoutée (TVA).

**Exemple**

Le processus suivant est un exemple de workflow de gestion des dépenses pour une note de frais.

1. Un employé crée et enregistre une note de frais.
2. L’employé envoit la note de frais pour approbation. L’approbateur est identifié en fonction des règles qui ont été définies lors de la configuration du workflow.
3. L’approbateur reçoit une notification indiquant qu’une note de frais est prête pour approbation. L’approbateur examine la note de frais et vérifie que les conditions suivantes sont remplies :

    - Les dépenses ne violent aucune politique de dépenses. Si une dépense enfreint une politique, l’approbateur vérifie que la note de frais comprend une justification commerciale valide.
    - Les reçus électroniques sont joints à la note de frais.

4. L’approbateur approuve la note de frais.
5. La note de frais est affectée au coordonnateur des comptes fournisseurs pour validation.
6. L’une des étapes suivantes se produit, selon que la comptabilisation automatique est configurée :

    - Si la validation automatique est configurée, la note de frais est traitée pour le paiement et le statut de la note de frais est mis à jour.
    - Si la validation automatique n’est pas configurée, le coordonnateur de la comptabilité fournisseur vérifie que tous les reçus originaux ont été soumis et que les reçus sont alignés avec les dépenses sur la note de frais. Tous les codes de taxe saisis dans la note de frais doivent également être vérifiés comme étant corrects.

Une fois ces exigences vérifiées, le rapport de dépenses est affiché.

Une fois la note de frais validée, le paiement est autorisé pour la note de frais et l’employé est remboursé.


[!INCLUDE[footer-include](../includes/footer-banner.md)]