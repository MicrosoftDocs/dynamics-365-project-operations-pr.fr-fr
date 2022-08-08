---
title: Journal d’intégration dans Project Operations
description: Cet article fournit des informations sur l’utilisation du journal d’intégration dans Project Operations.
author: sigitac
ms.date: 06/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d6f1709c4bf44cfd45516d9ac74b30d4817bb653
ms.sourcegitcommit: a5a1d81d2fe0a6f684e79859fcddf45e913d76bc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2022
ms.locfileid: "9106272"
---
# <a name="integration-journal-in-project-operations"></a>Journal d’intégration dans Project Operations

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Entrées de temps, de dépenses et de matériel créent des transactions **Réelles** représentant la vue opérationnelle du travail effectué par rapport à un projet. Dynamics 365 Project Operations fournit aux comptables un outil permettant d’examiner les transactions et d’ajuster les attributs comptables, le cas échéant. Une fois l’examen et les ajustements terminés, les transactions sont validées dans la comptabilité auxiliaire de projet et la comptabilité. Un comptable peut effectuer ces activités à l’aide de la feuille **Intégration Project Operations** (**Dynamics 365 Finance** > **Gestion et comptabilité de projet** > **Feuilles** > Feuille **Intégration Project Operations**.

![Flux du journal d’intégration.](./media/IntegrationJournal.png)

### <a name="create-records-in-the-project-operations-integration-journal"></a>Créer des enregistrements dans le journal d’intégration de Project Operations

Les enregistrements dans le journal d’intégration de Project Operations sont créés à l’aide d’un processus périodique, **Importer depuis la table intermédiaire**. Vous pouvez exécuter ce processus en accédant à **Dynamics 365 Finance** > **Gestion et comptabilité de projet** > **Périodique** > **Intégration Project Operations** > **Importer depuis la table intermédiaire**. Vous pouvez exécuter le processus de manière interactive ou configurer le processus pour qu’il s’exécute en arrière-plan si nécessaire.

Lorsque le processus périodique s’exécute, tous les chiffres réels qui ne sont pas encore ajoutés au journal d’intégration de Project Operations sont recherchés. Une ligne feuille est créée pour chaque transaction réelle.
Le système regroupe les lignes feuille dans des feuilles distinctes en fonction de la valeur sélectionnée dans le champ **Unité de période dans la feuille Intégration Project Operations** (**Finance** > **Gestion et comptabilité de projet** > **Configuration** > **Paramètres de gestion et comptabilité de projet**, onglet **Project Operations sur Dynamics 365 Customer Engagement**). Voici les valeurs possibles pour ce champ :

  - **Jours** : les chiffres réels sont regroupés par date de transaction. Un journal distinct est créé pour chaque jour.
  - **Mois** : les chiffres réels sont regroupés par mois calendaire. Un journal distinct est créé pour chaque mois.
  - **Années** : les chiffres réels sont regroupés par année calendaire. Un journal distinct est créé pour chaque année.
  - **Tout** : toutes les transactions réelles sont incluses dans le même journal d’intégration. Si le journal n’est pas disponible lors de l’exécution du processus périodique, par exemple si le journal est en cours d’enregistrement des transactions, un nouveau journal est créé.

Les lignes de journal sont créées en fonction des chiffres réels du projet. La liste suivante comprend certaines des règles par défaut et de transformation les plus importantes :

  - Chaque transaction réelle de projet figure sur une ligne dans le journal d’intégration de Project Operations. Les transactions de coût et de vente non facturées pour le type de facturation Temps et matériel sont affichées sur des lignes séparées.
  - Le champ **Date** représente la date de la transaction. Le champ **Date comptable** représente la date à laquelle la transaction est enregistrée dans le registre. Si la date comptable est dans une [période comptable close](/dynamics365/finance/general-ledger/close-general-ledger-at-period-end), et que le paramètre **Définir automatiquement la date comptable pour ouvrir la période comptable** est défini sur l’onglet **Finance** de la page **Paramètres de gestion de projet et comptabilité**, le système ajustera la date comptable de la transaction à la première date de la prochaine période comptable ouverte.
  - Le champ **N° document** affiche le numéro de document de chaque transaction réelle. La séquence de numéros de document est définie sous l’onglet **Séquences de numéros**, dans la page **Paramètres de gestion de projet et comptabilité**. Un nouveau numéro est attribué à chaque ligne. Une fois le document publié, vous pouvez voir comment le coût et la transaction de vente non facturée sont associés en sélectionnant **Documents associés** sur la page **N° document de transaction**.
  - Le champ **Catégorie** représente une transaction de projet et les valeurs par défaut basées sur la catégorie de transaction pour le chiffre réel associé du projet.
    - Si **Catégorie de transaction** est défini dans le chiffre réel d’un projet et qu’une **Catégorie de projet** existe dans une entité juridique donnée, la catégorie par défaut est cette catégorie de projet.
    - Si une **catégorie d’approvisionnement** n’est pas définie dans le chiffre réel Projet, le système utilisera la valeur définie dans le champ **Valeurs par défaut de la catégorie de projet** sur l’onglet **Project Operations sur Dynamics 365 Customer Engagement** de la page **Paramètres de gestion et comptabilité des projets**.
  - Le champ **Ressource** représente la ressource de projet associée à cette transaction. La ressource est utilisée comme référence dans les propositions de facture de projet aux clients.
  - Par défaut, le champ **Taux de change** est défini sur **Taux de change de la devise** dans Dynamics 365 Finance. En l’absence de configuration du taux de change, le processus périodique **Importer depuis la table intermédiaire** n’ajoutera pas l’enregistrement à un journal et un message d’erreur sera ajouté au journal d’exécution de la tâche.
  - Le champ **Propriété de ligne** représente le type de facturation dans les chiffres réels du projet. La propriété de la ligne et le mappage du type de facturation sont définis sur l’onglet **Project Operations sur Dynamics 365 Customer Engagement** sur la page **Paramètres de gestion et comptabilité des projets**.

Seuls les attributs comptables suivants peuvent être mis à jour dans les lignes de journal d’intégration de Project Operations :

- **Facturation du groupe de taxes de vente** et **Facturation du groupe de taxe de vente d’articles**
- **Dimensions financières** (en utilisant l’action **Répartir les montants**)

Les lignes de journal d’intégration peuvent être supprimées. Toutefois, toutes les lignes non publiées seront à nouveau insérées dans le journal une fois que vous aurez réexécuté le processus périodique **Importer depuis la table intermédiaire**.

### <a name="post-the-project-operations-integration-journal"></a>Publier le journal d’intégration Project Operations

Lorsque vous publiez le journal d’intégration, des transactions auxiliaires et de comptabilité sont créées. Ces dernières sont utilisées dans la facturation client en aval, la constatation du produit et les rapports financiers.

Le journal d'intégration Project Operations sélectionné peut être publié à l'aide de l'option **Publication** sur la page du journal d'intégration Project Operations. Tous les journaux peuvent être publiés automatiquement en exécutant un processus dans **Périodiques** > **Intégration Project Operations** > **Journal d’intégration Project Operations**.

La publication peut être effectuée de manière interactive ou par lots. Notez que tous les journaux qui ont plus de 100 lignes seront automatiquement reportés dans un lot. Pour de meilleures performances lorsque des journaux comportant de nombreuses lignes sont validés dans un lot, activez la fonctionnalité **Publier le journal d'intégration Project Operations à l'aide de plusieurs tâches par lots** dans l'espace de travail **Gestion des fonctionnalités**. 

#### <a name="transfer-all-lines-that-have-posting-errors-to-a-new-journal"></a>Transférer toutes les lignes comportant des erreurs de validation vers un nouveau journal

> [!NOTE]
> Pour utiliser cette fonctionnalité, activez la fonctionnalité **Transférer toutes les lignes avec des erreurs de validation vers un nouveau journal d'intégration Project Operations** dans l'espace de travail **Gestion des fonctionnalités**.

Lors de la validation dans le journal d'intégration Project Operations, le système valide chaque ligne du journal. Le système comptabilise toutes les lignes sans erreur et crée un nouveau journal pour toutes les lignes comportant des erreurs de comptabilisation. Pour consulter les journaux qui comportent des lignes d'erreur de validation, accédez à **Gestion et comptabilité des projets** > **Journaux** > **Journal d'intégration Project Operations**, et filtrez les journaux à l'aide du champ **Journal d’origine**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
