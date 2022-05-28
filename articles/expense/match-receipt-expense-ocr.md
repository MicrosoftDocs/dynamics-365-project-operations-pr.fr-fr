---
title: Capturer un reçu à l’aide d’OCR
description: Cette rubrique fournit des informations sur le traitement de la reconnaissance optique de caractères (OCR) pour les reçus.
author: suvaidya
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d4c2cce88514e7822515fc407fc7cf31cb34924
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596277"
---
# <a name="capture-a-receipt-using-ocr"></a>Capturer un reçu à l’aide d’OCR

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

La saisie des dépenses a été améliorée grâce à l’introduction du traitement de reconnaissance optique de caractères (OCR) pour les reçus. Cette fonctionnalité est conçue pour améliorer l’expérience utilisateur lors de la création de notes de frais.

## <a name="key-features"></a>Fonctionnalités clés

- Le système extrait le nom du prestataire, la date et le montant total des reçus.
- Le système essaiera de faire correspondre les reçus non joints aux transactions de dépenses non jointes.
- Vous pouvez créer des transactions de dépenses saisies manuellement à partir des reçus.

## <a name="attach-receipts-to-an-expense-report"></a>Joindre des reçus à une note de frais

Pour joindre automatiquement des reçus qui incluent des transactions par carte de crédit lors de la création d’une note de frais, procédez comme suit.

  1. Ouvrez l’espace de travail **Gestion des dépenses**.
  2. Vérifiez que l’onglet **Reçus** contient bien des reçus non joints. Vous pouvez également télécharger des reçus sur l’onglet **Reçus**.
  3. Vérifiez que l’onglet **Dépenses** contient bien des dépenses non jointes. En règle générale, l’administrateur des dépenses importe ces dépenses à partir d’un fournisseur de cartes de crédit.
  4. Sélectionnez **Nouvelle note de frais**. Notez que vous pouvez désormais inclure les dépenses et les reçus également lorsque vous créez une note de frais. Si vous ajoutez à la fois des dépenses et des reçus, un rapprochement automatique des reçus et des dépenses est déclenché.

## <a name="create-or-match-receipts-to-an-expense-report"></a>Créer ou faire correspondre des reçus à une note de frais
Pour créer une dépense ou faire correspondre une dépense à partir d’un reçu, procédez comme suit.

  1. Sur une note de frais, sur l’onglet **Reçus**, joignez un reçu en sélectionnant **Ajouter des reçus**.
  2. Sous l’image téléchargée du reçu, notez les options **Créer** et **Faire correspondre**.

      - Sélectionnez **Créer** pour créer une transaction de dépense saisie manuellement et remplir les valeurs extraites du reçu.
      - Si vous sélectionnez **Faire correspondre**, le système essaie de faire correspondre une dépense existante au reçu.

## <a name="installation"></a>Installation

Pour utiliser ces capacités de dépenses avancées, installez le complément Expense Management Service pour Microsoft Microsoft Dynamics 365 Finance et activez les fonctionnalités dans votre instance. Vous pouvez accéder au complément depuis votre projet dans Microsoft Dynamics Lifecycle Services (LCS).

1. Connectez-vous à LCS et ouvrez l’environnement souhaité.
2. Accédez à **Télécharger avec informations détaillées**.
3. Sélectionnez **Maintenir à jour**, ou faites défiler vers le bas jusqu’au raccourci **Compléments d’environnement**.
4. Sélectionnez **Installez un nouveau complément**.
5. Sélectionnez **Service de gestion des dépenses**.
6. Suivez le guide d’installation et acceptez les termes et conditions.
7. Sélectionnez **Installer**.

Dans l’espace de travail **Gestion des fonctionnalités**, activez les fonctionnalités suivantes :

- Notes de frais réinventées
- Correspondance automatique et création de dépenses à partir d’un reçu

Lorsque vous activez ces fonctionnalités, les actions suivantes se produisent :

- L’espace de travail **Gestion des dépenses** existant est remplacé par le nouvel espace de travail.
- Un nouvel élément de menu pour la visibilité des champs de dépenses est ajouté.
- Vous pouvez toujours ouvrir l’ancienne page **Notes de frais** en allant dans **Gestion des dépenses> Mes dépenses> Notes de frais**.
- Les workflows et toutes les approbations vous dirigent toujours vers la page des notes de frais existantes.
- Les reçus seront traités via Microsoft Azure Cognitive Services et les métadonnées seront extraites et ajoutées.
- Une option est ajoutée, elle vous permet de créer une note de frais qui comprend des reçus non joints mis en correspondance.
- Une option ajoutée aux notes de frais vous permet de créer une ligne de dépenses à partir d’un reçu ou de tenter de faire correspondre un reçu existant à une ligne de dépenses existante.

## <a name="frequently-asked-questions"></a>Forums aux questions

**Microsoft utilise-t-il mes données pour ses modèles ?**

Non, Microsoft a créé un modèle général de Machine Learning pour son service de traitement des reçus. Ce modèle n’est pas basé sur les reçus que vous téléchargez.

**Où cette fonctionnalité est-elle disponible et traitée ?**

La disponibilité de cette fonctionnalité dans différentes régions est répertoriée dans le tableau suivant. Si votre région n’est pas actuellement prise en charge, soumettez une demande pour faire passer en priorité la disponibilité du service OCR dans votre région. 

| Région | Prise en charge                         |
|--------|-----------------------------------|
| USA    | Oui                               |
| CAN    | Oui                               |
| Royaume-Uni     | Oui                               |
| AUS    | Oui                               |
| UE     | Partiellement. Reçus en anglais seulement. |
| Asie   | No                                |
| Japon  | No                                |
| Afrique | No                                |

**Où vont mes reçus ?**

Finance contactera Cognitive Services pour extraire des données du champ. Cognitive Services conservera une copie de votre reçu pendant 24 heures maximum pendant le traitement. Une fois le traitement terminé, Cognitive Services supprimera le reçu. Les reçus sont toujours stockés dans Finance.

Pour plus d’informations, consultez [Activer la compréhension des reçus avec la nouvelle fonctionnalité de Form Recognizer](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
