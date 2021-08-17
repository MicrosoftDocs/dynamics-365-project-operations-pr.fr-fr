---
title: Gérer des propositions de facture pour un projet
description: Cette rubrique fournit des détails sur le traitement des factures client avec Project Operations pour les scénarios basés sur les ressources/non stockés.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 61b43e05eb179e2b00189076290433dd72f89a6bc7ef72140fc1efd752149d43
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989908"
---
# <a name="manage-project-invoice-proposals"></a>Gérer des propositions de facture pour un projet

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les propositions de facture de projet peuvent être traitées par votre service de facturation lorsque les deux conditions suivantes sont remplies :

  - Le chef de projet confirme la facture pro forma dans Microsoft Dataverse.
  - Toutes les transactions de vente non facturées de temps et de matières qui sont incluses dans la facture pro forma sont validées à l’aide de la feuille **Intégration de Project Operations** de Dynamics 365.

Suivez les étapes suivantes pour terminer une proposition de facture de projet dans Dynamics 365 Finance.

1. Consultez les informations de facturation pour les transactions de temps et de matières et enregistrez la feuille **Intégration Project Operations**.
2. Consultez les informations de facturation pour les jalons de facturation à prix fixe.
3. Vérifiez et mettez en forme la proposition de facture de projet.
4. Validez et imprimez les factures du projet.

## <a name="manage-billing-information-in-the-project-operations-integration-journal"></a>Gérez les informations de facturation dans le journal d’intégration de Project Operations

Les projets réels créés dans Dataverse sont examinés et publiés dans Finance par le comptable du projet. Pour plus d’informations sur l’utilisation du journal d’intégration, voir [Journal d’intégration de Project Operations](../project-accounting/project-operations-integration-journal.md).

Les coûts réels et les ventes réelles non facturées sont ajoutés au journal d’intégration en tant que lignes distinctes :

  - Le prix de revient unitaire et le montant du coût sur le coût réel par défaut de la transaction de coût réel du projet dans Dataverse.
  - Le prix de vente unitaire et le montant des ventes sur la transaction de vente non facturée sont par défaut de la transaction de vente réelle non facturée du projet dans Dataverse.

### <a name="billing-sales-tax"></a>Facturation de la taxe

Le calcul de la taxe pour la facturation est déterminé par la combinaison de champs **Groupe de taxes de facturation** et **Groupe de taxes des éléments de facturation** sur un enregistrement de vente non facturé sur la ligne de journal **Intégration de Project Operations**. Le système définit par défaut ces valeurs de champ en fonction des paramètres de l’onglet **Finances** sur la page **Gestion de projet et paramètres comptables**.

- **Méthode de groupe de taxes** détermine la logique de facturation par défaut du groupe de taxes :
  
  - **Projet** : Définit toujours par défaut le groupe de taxes de facturation du projet. Vous pouvez consulter ou modifier le groupe de taxes de facturation par défaut sur un projet en sélectionnant **Afficher la comptabilité par défaut** sur la page **Tous les projets**.
  - **Contrat du projet** : Définit toujours par défaut le groupe de taxes de facturation du contrat du projet. Vous pouvez consulter ou modifier le groupe de taxes par défaut sur un contrat de projet en sélectionnant **Afficher la comptabilité par défaut** sur la page **Contrats de projets**.
  - **Client** : Définit toujours par défaut le groupe de taxes de facturation du client.
  - **Recherche** : Recherchera dans toutes les entités ci-dessus et sélectionnera la première valeur disponible. La recherche commence par l’entité **Projet**, puis l’entité **Contrat de projet** et enfin l’entité **Client**.

- **Méthode de groupe de taxes d’article** détermine la logique de facturation par défaut du groupe de taxes d’article :
  
  - Pour les types de transactions de temps, de dépenses et de frais, le groupe de taxes de l’article de facturation sera toujours par défaut l’entité **Catégorie de projet**.
  - Pour les types de mouvement matières, le groupe de taxes d’article de facturation est défini par défaut en fonction du paramètre **Méthode de groupe de taxes d’article** dans **Gestion de projet et paramètres comptables**. Le numéro d’article définit par défaut le groupe de taxes d’article de l’entité **Produit sorti**. La catégorie définit par défaut le groupe de taxes d’article de l’entité **Catégorie de projet**.

### <a name="financial-dimensions"></a>Dimensions financières

Les dimensions financières des enregistrements de ventes non facturées dans le journal **Intégration de Project Operations** par défaut dans l’entité **Projet**. Les dimensions financières peuvent être examinées et ajustées en sélectionnant **Ventiler les montants**. Si vous devez modifier les dimensions financières de l’enregistrement des ventes non facturées après la validation du journal d’intégration mais avant la confirmation de la facture pro forma, accédez à **Tous les projets** > **Gestion** > **Transactions validées**, sélectionnez la transaction, puis sélectionnez **Traiter** > **Ajuster la comptabilité**.

### <a name="exchange-rates"></a>Taux de change

La devise de la transaction non facturée en Dataverse est utilisée comme devise de transaction dans Finance et convertie dans la devise comptable de la société en utilisant les taux de change définis dans Finance.


## <a name="manage-the-financial-attributes-of-billing-milestones"></a>Gérer les attributs financiers des jalons de facturation 

Les lignes de contrat de projet utilisant la méthode de facturation à prix fixe sont facturées via les [Jalons de prix fixe](../sales/invoice-schedules-contract-line.md#create-a-fixed-price-invoice-schedule-for-a-contract-line). Le comptable du projet peut consulter les étapes de facturation dans Finance en accédant à **Gestion de projet et comptabilité** > **Tous les projets** > **Gestion** > **Transactions en compte**.

### <a name="billing-sales-tax"></a>Facturation de la taxe

Les valeurs **Groupe de taxes** et **Groupe de taxes d’article** par défaut des paramètres lorsqu’un nouveau jalon de facturation est créé dans Dataverse. Le système définit par défaut les valeurs de ces champs en fonction des paramètres de l’onglet **Finance** sur la page **Gestion de projet et paramètres comptables**.

- La **Méthode de groupe de taxes** détermine la logique de valeur par défaut de la **Facturation du groupe de taxes** :

    - **Projet** définit toujours par défaut le groupe de taxes de facturation du projet. Vous pouvez consulter ou modifier le groupe de taxes par défaut sur un projet en sélectionnant **Afficher la comptabilité par défaut** sur la page **Tous les projets**.
    - **Contrat du projet** définit toujours par défaut le groupe de taxes de facturation du contrat du projet. Vous pouvez consulter ou modifier le groupe de taxes par défaut sur un contrat de projet en sélectionnant **Afficher la comptabilité par défaut** sur la page **Contrats de projets**.
    - **Client** définit toujours par défaut le groupe de taxes de facturation du client.
    - **Recherche** recherchera dans toutes les entités de cette liste et sélectionnera la première valeur disponible. La recherche commence par l’entité **Projet**, puis l’entité **Contrat de projet**, puis l’entité **Client**.

- **Groupe de taxe d’article de jalon à prix fixe** est utilisé comme valeur par défaut dans le champ **Groupe de taxe d’article** pour le jalon de facturation. Le comptable peut vérifier et modifier cette valeur sur la page **Transactions en compte**. Le système utilise la valeur de la transaction en compte lors de la création d’une ligne de proposition de facture de projet.
 

### <a name="financial-dimensions"></a>Dimensions financières

Les dimensions financières par défaut pour le jalon de facturation à prix fixe sont définies sur les lignes de contrat de projet. Accédez à **Contrats de projet** > **Afficher la comptabilité par défaut** et sur l’onglet **Lignes de contrat**, sélectionnez **Ligne de contrat de prix**, puis définissez les valeurs de dimension financière que vous souhaitez utiliser par défaut.

Le comptable du projet peut modifier les informations sur la taxe et les dimensions financières sur les jalons de la facture jusqu’à ce que la proposition de facture du projet soit créée.


## <a name="create-project-invoice-proposals"></a>Créer des propositions de facture pour un projet

Les propositions de facture de projet peuvent être consultées dans le module **Gestion de projet et comptabilité** en accédant à **Factures de projet** > **Propositions de facture de projet**.

L’en-tête de proposition de facture de projet est créé dans Finance lorsque la facture pro forma est confirmée dans Dataverse. Pour un rapprochement plus facile, le système définit le numéro de proposition de facture projet dans Finance sur le même numéro que l’ID de facture pro forma dans Dataverse. Étant donné que les factures pro forma ne sont pas nécessairement confirmées dans le même ordre dans lequel elles ont été créées, la souches de numéros de proposition de facture de projet dans Finance doit permettre des modifications de nombres de plus en plus élevés. Configurez les souches de numéros en suivant les étapes suivantes :

1. Dans Finance, accédez à **Administration d’organisation** > **Souches de numéros** > **Souches de numéros**.
2. Dans le filtre **Domaine**, sélectionnez **Projets**.
3. Dans le filtre **Référence**, sélectionnez **Proposition de facture**.
4. Utilisez le champ **Entreprise** pour filtrer chaque entité juridique avec l’intégration Project Operations Dataverse activée.
5. Ouvrez **Détails de la souches de numéros** et sur l’onglet **Général** définissez :

    - **Autoriser les modifications utilisateur : vers un nombre inférieur** = **Oui**
    - **Autoriser les modifications utilisateur : vers un nombre supérieur** = **Oui**

Les lignes de proposition de facture de projet sont ajoutées par le système à l’aide du processus périodique **Importer depuis la table de préparation** (**Gestion de projet et comptabilité** > **Périodique** > **Intégration de Project Operations** > **Importer depuis la table de préparation**). Ce processus peut être exécuté manuellement ou en utilisant une planification périodique. Le système n’ajoutera pas de lignes au document de proposition de facture tant que toutes les lignes ne seront pas prêtes à être facturées. Les transactions de temps et de matières ne sont prêtes à être facturées que lorsqu’elles sont validées à l’aide du journal **Intégration de Project Operations**.

## <a name="format-and-print-invoice-proposals"></a>Mettre en forme et imprimer les propositions de facture

Le comptable de projet peut personnaliser une impression de facture de projet en utilisant la page **Mettre en forme la proposition de facture** et les capacités de gestion des impressions.

### <a name="format-invoice-proposals"></a>Mettre en forme les propositions de facture

La page **Mettre en forme les propositions de facture** permet d’afficher les transactions de regroupement personnalisées dans la facture du projet client.

1. Sur la page **Proposition de facture de projet**, sélectionnez **Imprimer** > **Mettre en forme la proposition de facture**.
2. Sélectionnez **Nouveau** pour créer un regroupement pour l’impression de la facture du projet.
3. Dans le champ **Détail/Résumé**, sélectionnez les options de ce regroupement :

    - Sélectionnez **Détail** pour imprimer les détails de la transaction de la facture client.
    - Sélectionnez **Synthèse** pour imprimer la synthèse de la transaction de la facture client.

> [!NOTE]
> La sélection dans le champ **Détail/Résumé** sur la page **Mettre en forme la proposition de facture** remplace l’option sélectionnée dans le champ **Format de facture** sur la page **Propositions de factures** pour imprimer une facture détaillée ou une facture récapitulative.

- Sélectionnez les lignes de transaction à inclure dans cette section sur l’onglet **Transactions disponibles** et sélectionnez **Inclure les transactions** pour les déplacer vers l’onglet **Opérations sélectionnées**.
- Sélectionnez **Déplacer vers le haut** et **Descendre** pour changer l’ordre des sections.
- Sélectionnez **Aperçu avant impression** pour prévisualiser la facture formatée.

### <a name="print-management"></a>Gestion d’impression

La gestion de l’impression utilise différents fichiers de rapport pour imprimer, spécifier les destinations et personnaliser le texte du pied de page de la facture. La gestion de l’impression peut être configurée au niveau du module, mais ces paramètres peuvent être remplacés pour un client, un contrat ou une proposition de facture spécifique. Pour accéder à cette fonction sur la page **Proposition de facture de projet**, sélectionnez **Imprimer** > **Gestion d’impression**.

La configuration de la gestion de l’impression est affichée sous la forme d’une arborescence, où chaque niveau de nœud affiche les documents disponibles à ajuster. Vous pouvez affecter des impressions personnalisées au niveau du module, du client, du contrat ou du document de proposition de facture. Pour modifier l’impression du document d’origine, développez le nœud souhaité et sélectionnez **Article d’origine**. Dans le champ **Format de rapport**, sélectionnez le format de rapport à utiliser pour l’impression. Vous pouvez utiliser des formats de rapport personnalisés en utilisant [Cadre de gestion des documents commerciaux](/dynamics365/fin-ops-core/dev-itpro/analytics/er-business-document-management).

## <a name="post-invoice-proposals"></a>Valider les propositions de facture

Une fois que la facture a été examinée et modifiée et que les lignes de proposition de facture sont satisfaisantes, vérifiez les totaux de la facture et la taxe. Dans le groupe **Détails**, sélectionnez **Totaux** puis sélectionnez **Valider** pour valider la facture.

Pour afficher la facture avant la validation, décochez **Validation**. **Pro forma** sera imprimé sur la facture pour indiquer qu’il s’agit d’un exemple de facture. Pour imprimer la facture, cochez **Imprimer la facture**.

En plus de la page **Proposition de facture**, les propositions de facture peuvent également être publiées en exécutant le travail périodique, **Valider les propositions de facture**. Pour trouver cette tâche, accédez à **Gestion de projet et comptabilité** > **Périodique** > **Factures de projet** > **Publier des propositions de facture**.

Cette page affiche toutes les propositions de facture prêtes à être validées. Vous pouvez planifier la validation des propositions de facture en sélectionnant **Lot**. Définissez **Paramètre de traitement par lots** sur **Oui** et définissez la récurrence du traitement par lots en sélectionnant **Récurrence**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
