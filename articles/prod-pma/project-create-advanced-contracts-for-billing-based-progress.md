---
title: Créer des contrats avancés pour la facturation selon la progression
description: Cet article explique comment créer des contrats de projet afin de pouvoir générer des factures pour les clients, en fonction d’un pourcentage de travail terminé.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 26fe072b8241c7fdc96629f534e33a8fe53d3164
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913663"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Créer des contrats avancés pour la facturation selon la progression
[!include [banner](../includes/banner.md)]

Cet article explique comment créer des contrats de projet afin de pouvoir créer des factures pour les clients, en fonction d’un pourcentage de travail terminé. Les montants des factures sont automatiquement calculés pour les catégories de budget de travail que vous définissez pour un projet. Le délai de facturation est défini lorsque vous négociez le contrat de projet avec le client.

Utilisez les procédures de cet article pour définir un contrat, un projet associé et les règles de facturation qui calculent les montants de la facture pour les catégories de travail budgétisées définies pour le projet.

Une fois que vous avez créé le contrat et le projet, vous pouvez configurer les détails du projet. Par exemple, vous pouvez définir des activités et affecter des collaborateurs au projet.

## <a name="example"></a>Exemple

Votre organisation est une entreprise de développement de logiciels. Vous acceptez de développer un progiciel de comptabilité de paie pour un client pour un montant total de 20 000 dollars américains (USD). Votre organisation accepte de facturer le client lorsque vous atteignez des pourcentages spécifiques du projet. Vous configurez les catégories de projet suivantes pour le travail, afin de pouvoir les utiliser dans le processus de facturation :

- Consultance
- Conception
- Installation

Vous configurez également des règles de facturation qui calculent automatiquement les montants de facture pour le pourcentage de travail achevé pour chaque catégorie.

Le responsable du budget crée un budget pour les catégories de projet. La quantité de travail achevé est automatiquement calculée en pourcentage du travail réel par rapport aux montants budgétés.

## <a name="prerequisites"></a>Conditions préalables

Avant de créer un projet qui utilise des règles de facturation, vous devez configurer les séquences de numéros pour les règles de facturation et un journal des frais qui est utilisé pour valider les facturations en fonction de la progression.

1. Accédez à **Gestion et comptabilité des projets** \> **Configuration** \> **Paramètres de gestion et comptabilité des projets**.
2. Sur la page **Paramètres de gestion et comptabilité des projets**, dans l’onglet **Séquences de numéros**, définissez la séquence de numéros à utiliser lors de la création des règles de facturation.
3. Accédez à **Gestion de projet et comptabilité** \> **Journaux** \> **Frais**.
4. Sur la page **Journal des frais**, sélectionnez **Nouveau** et entrez le nom du journal.

## <a name="create-a-contract-for-progress-billings"></a>Créer un contrat pour la facturation en fonction de la progression

Utilisez cette procédure pour créer un contrat de projet pour un projet à prix fixe. Vous créez une facture de projet lorsque le travail terminé sur le projet atteint un pourcentage spécifié.

1. Accédez à **Gestion de projet et comptabilité** \> **Projets** \> **Contrats de projet**.
2. Sur la page **Contrats de projet**, sélectionnez **Nouveau**.
3. Dans la boîte de dialogue **Nouveau contrat de projet**, définissez les champs suivants :

    - **Nom**
    - **Type de financement**
    - **Source de financement**
    - **Devise de vente** - Par défaut, cette devise est utilisée pour les factures des clients associées au contrat de projet. Cependant, vous pouvez modifier la devise de vente sur une facture client spécifique.

4. Cliquez sur **OK**. Les informations sont copiées dans l’en-tête de la page **Contrats de projet**.
5. Sur la page **Contrats de projet**, remplissez le reste des informations requises pour le projet.

## <a name="create-a-project-for-progress-billings"></a>Créer un projet pour la facturation en fonction de la progression

Suivez ces étapes pour créer un projet et tous les sous-projets associés à un contrat de projet.

1. Accédez à **Gestion de projets et comptabilité** \> **Projets** \> **Tous les projets**.
2. Sur la page **Tous les projets**, sélectionnez **Nouveau**.
3. Dans la boîte de dialogue **Nouveau projet**, dans le champ **Type de projet**, sélectionnez **Temps et matériel**.
4. Sélectionnez un groupe de projets. Un groupe de projets définit les informations de validation pour les projets affectés au groupe.
5. Sélectionnez **Créer un projet**.
6. Une fois le projet créé, définissez l’étape du projet sur **En cours**.

## <a name="create-a-budget-for-a-project"></a>Créer un budget pour un projet

Les catégories de budget sont utilisées pour calculer automatiquement les montants de factures pour le pourcentage de travail achevé pour chaque catégorie. Suivez ces étapes pour créer des catégories de budget pour les coûts estimés.

1. Accédez à **Gestion de projets et comptabilité** \> **Projets** \> **Tous les projets**.
2. Sur la page **Tous les projets**, sélectionnez et ouvrez le projet souhaité.
3. Sur la page **Projets**, dans le volet Actions, dans l’onglet **Planifier**, dans le groupe **Budget**, sélectionnez **Budget du projet**.
4. Sur la page **Budget du projet**, entrez un coût estimé pour chaque catégorie du projet.

## <a name="create-billing-rules-for-progress-billings"></a>Créer des règles de facturation pour la facturation en fonction de la progression

1. Accédez à **Gestion de projet et comptabilité** \> **Projets** \> **Contrats de projet**.
2. Dans la page de liste **Contrats de projets**, sélectionnez et ouvrez un contrat de projet.
3. Sur la page du contrat de projet, sur le raccourci **Règles de facturation**, sélectionnez **Ajouter**.
4. Sur la page **Règle de facturation**, dans le champ **Type de ligne**, sélectionnez **Progression**.
5. Sur le raccourci **Détails de la ligne de règle de facturation**, dans le champ **Valeur du contrat**, saisissez la valeur totale du contrat.
6. Dans le champ **Catégorie**, sélectionnez la catégorie dans laquelle publier la transaction de frais.
7. Dans le champ **Projet**, sélectionnez le projet qui utilise cette règle de facturation.
8. Facultatif : affectez la règle de facturation à des projets supplémentaires. Sur le raccourci **Projet**, dans la section **Projets disponibles**, sélectionnez un projet, puis sélectionnez le bouton flèche droite pour ajouter le projet à la section **Projets sélectionnés**.
9. Facultatif : calculez le pourcentage que le client retient des paiements sur une facture. Sur le raccourci **Conditions de rétention des paiements**, sélectionnez la source de financement, puis, dans le champ **Pourcentage de rétention**, entrez le pourcentage de rétention.
10. Répétez ces étapes pour créer des règles de facturation supplémentaires pour le contrat de projet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]