---
title: Journal d’intégration dans Project Operations
description: Cette rubrique fournit des informations sur l’utilisation du journal d’intégration dans Project Operations.
author: sigitac
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c5cc3254c52750b35be2c66137b6c57bbd9acbfbc89dedc6559059a89c8e2393
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987928"
---
# <a name="integration-journal-in-project-operations"></a>Journal d’intégration dans Project Operations

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les entrées de temps et de dépenses créent des transactions **Réelles** qui sont la vue opérationnelle du travail effectué par rapport à un projet. Dynamics 365 Project Operations fournit aux comptables un outil permettant d’examiner les transactions et d’ajuster les attributs comptables, le cas échéant. Une fois l’examen et les ajustements terminés, les transactions sont validées dans la comptabilité auxiliaire de projet et la comptabilité. Un comptable peut effectuer ces activités en utilisant le journal d’**intégration de Project Operations** (**Dynamics 365 Finance** > **Gestion de projet et comptabilité** > **Journaux** > **Journal d’intégration de ProjectOperations**).

![Flux du journal d’intégration.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Créer des enregistrement dans le journal d’intégration de Project Operations

Les enregistrements dans le journal d’intégration de Project Operations sont créés à l’aide d’un processus périodique, **Importer depuis la table intermédiaire**. Vous pouvez exécuter ce processus en accédant à **Dynamics 365 Finance** > **Gestion de projet et comptabilité** > **Périodique** > **Intégration dans Project Operations** > **Importer depuis la table intermédiaire**. Vous pouvez exécuter le processus de manière interactive ou configurer le processus pour qu’il s’exécute en arrière-plan si nécessaire.

Lorsque le processus périodique s’exécute, tous les chiffres réels qui ne sont pas encore ajoutés au journal d’intégration de Project Operations sont recherchés. Une ligne feuille est créée pour chaque transaction réelle.
Le système regroupe les lignes de journal en journaux distincts en fonction de la valeur sélectionnée dans le champ **Unité de période dans le journal d’intégration de Project Operations** (**Finance** > **Gestion et comptabilité de projets** > **Configurer** > **Paramètres de gestion et comptabilité de projets**, onglet **Project Operations dans Dynamics 365 Customer Engagement**). Voici les valeurs possibles pour ce champ :

  - **Jours** : les chiffres réels sont regroupés par date de transaction. Un journal distinct est créé pour chaque jour.
  - **Mois** : les chiffres réels sont regroupés par mois calendaire. Un journal distinct est créé pour chaque mois.
  - **Années** : les chiffres réels sont regroupés par année calendaire. Un journal distinct est créé pour chaque année.
  - **Tout** : toutes les transactions réelles sont incluses dans le même journal d’intégration. Si le journal n’est pas disponible lors de l’exécution du processus périodique, par exemple si le journal est en cours d’enregistrement des transactions, un nouveau journal est créé.

Les lignes de journal sont créées en fonction des chiffres réels du projet. La liste suivante comprend certaines des règles par défaut et de transformation les plus importantes :

  - Chaque transaction réelle de projet figure sur une ligne dans le journal d’intégration de Project Operations. Les transactions de coût et de vente non facturées pour le type de facturation Temps et matériel sont affichées sur des lignes séparées.
  - Le champ **Date** représente la date de la transaction. Le champ **Date comptable** représente la date à laquelle la transaction est enregistrée dans le registre. Si la date comptable est dans une [période comptable close](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), et que le paramètre **Définir automatiquement la date comptable pour ouvrir la période comptable** est défini sur l’onglet **Finance** de la page **Paratèmetres de gestion de projet et comptabilité**, le système ajustera la date comptable de la transaction à la première date de la prochaine période comptable ouverte.
  - Le champ **N° document** affiche le numéro de document de chaque transaction réelle. La séquence de numéros de document est définie sous l’onglet **Séquences de numéros**, dans la page **Paramètres de gestion de projet et comptabilité**. Un nouveau numéro est attribué à chaque ligne. Une fois le document publié, vous pouvez voir comment le coût et la transaction de vente non facturée sont associés en sélectionnant **Documents associés** sur la page **N° document de transaction**.
  - Le champ **Catégorie** représente une transaction de projet et les valeurs par défaut basées sur la catégorie de transaction pour le chiffre réel associé du projet.
    - Si **Catégorie de transaction** est défini dans le chiffre réel d’un projet et qu’une **Catégorie de projet** existe dans une entité juridique donnée, la catégorie par défaut est cette catégorie de projet.
    - Si **Catégorie de transaction** n’est pas défini dans le chiffre réel du projet, le système utilise la valeur du champ **Catégorie par défaut du projet** sous l’onglet **Project Operations dans Dynamics 365 Customer Engagement** sur la page **Paramètres de gestion de projet et comptabilité**.
  - Le champ **Ressource** représente la ressource de projet associée à cette transaction. La ressource est utilisée comme référence dans les propositions de facture de projet aux clients.
  - Le champ **Taux de change** prend la valeur par défaut du **Taux de change** configuré dans Dynamics 365 Finance. En l’absence de configuration du taux de change, le processus périodique **Importer depuis la table intermédiaire** n’ajoutera pas l’enregistrement à un journal et un message d’erreur sera ajouté au journal d’exécution de la tâche.
  - Le champ **Propriété de ligne** représente le type de facturation dans les chiffres réels du projet. Le mappage de la propriété de ligne et du type de facturation sont définis sous l’onglet **Project Operations dans Dynamics 365 Customer Engagement** sur la page **Paramètres de gestion de projet et comptabilité**.

Seuls les attributs comptables suivants peuvent être mis à jour dans les lignes de journal d’intégration de Project Operations :

- **Facturation du groupe de taxes de vente** et **Facturation du groupe de taxe de vente d’articles**
- **Dimensions financières** (en utilisant l’action **Répartir les montants**)

Les lignes de journal d’intégration peuvent être supprimées, mais toutes les lignes non publiées seront à nouveau insérées dans le journal une fois que vous aurez réexécuté le processus périodique **Importer depuis la table intermédiaire**.

Lorsque vous publiez le journal d’intégration, des transactions auxiliaires et de comptabilité sont créées. Ces dernières sont utilisées dans la facturation client en aval, la constatation du produit et les rapports financiers.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
