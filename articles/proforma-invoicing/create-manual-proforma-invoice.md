---
title: Factures pro forma
description: Cet article fournit des informations sur les factures proforma dans Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b56c3908cce3115d5c95a4b1b233db70fb6c149
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920563"
---
# <a name="proforma-invoices"></a>Factures pro forma

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

La facturation pro forma offre aux chefs de projet un deuxième niveau d’approbation avant de créer des factures pour les clients. Le premier niveau de l’approbation est terminé lorsque les entrées de temps, de dépenses et de matériel que les membres de l’équipe du projet envoient sont approuvées. Les factures pro forma confirmées sont disponibles dans le module Comptabilité de projet de Project Operations. Les comptables de projet peuvent effectuer des mises à jour supplémentaires telles que la taxe de vente, la comptabilité et la mise en page des factures.


## <a name="creating-project-invoices"></a>Création de factures de projet

Les factures de projet peuvent être créées une à la fois ou en bloc. Vous pouvez les créer manuellement ou les configurer de sorte qu’elles soient générées dans le cadre d’exécutions automatisées.

### <a name="manually-create-project-invoices"></a>Créer manuellement des factures de projet 

Dans la page de liste **Contrats de projets**, vous pouvez créer des factures de projet séparément pour chaque contrat de projet, ou vous pouvez créer des factures en bloc pour les contrats de plusieurs projets.

Pour créer une facture pour un contrat de projet spécifique, procédez comme suit :

- Sur la page de liste **Contrats de projet**, ouvrez un contrat de projet, puis cliquez sur **Créer une facture**.

    Une facture est générée pour toutes les transactions du contrat de projet sélectionné ayant le statut **Prêt pour la facturation**. Ces transactions comprennent le temps, les dépenses, les matériaux, les jalons et d’autres lignes de journal des ventes non facturées.

Suivez les étapes ci-dessous pour créer des factures en bloc.

1. Dans la page de liste **Contrats de projets**, sélectionnez un ou plusieurs contrats de projets pour lesquels créer une facture, puis sélectionnez **Créer des factures de projet**.

    Un message d’avertissement vous informe qu’un délai peut s’écouler avant la création des factures. Le processus est également affiché.

2. Cliquez sur **OK** pour fermer la zone de message.

    Une facture est générée pour toutes les transactions d’une ligne de contrat ayant le statut **Prêt pour la facturation**. Ces transactions comprennent le temps, les dépenses, les matériaux, les jalons et d’autres lignes de journal des ventes non facturées.

3. Pour afficher les factures qui sont générées, accédez à **Ventes** \> **Facturation** \> **Factures**. Vous verrez une facture pour chaque contrat de projet.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurer la création automatique de factures de projet 

Procédez comme suit pour configurer l’exécution d’une facture automatique.

1. Accédez à **Paramètres** \> **Traitements par lots**.
2. Créez un traitement par lots, et nommez-le **Créer des factures dans Project Operations**. Le nom du traitement par lots doit inclure le terme « Créer des factures ».
3. Dans le champ **Type de tâche**, sélectionnez **Aucun**. Par défaut, les options **Fréquence quotidienne** et **Est actif** sont définies sur **Oui**.
4. Cliquez sur **Exécuter le flux de travail**. Dans la boîte de dialogue **Rechercher un enregistrement**, les trois flux de travail suivants s’affichent :

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Sélectionnez **ProcessRunCaller**, puis cliquez sur **Ajouter**.
6. Dans la boîte de dialogue suivante, cliquez sur **OK**. Un flux de travail **Sleep** est suivi d’un flux de travail **Process**.

    Vous pouvez également sélectionner **ProcessRunner** à l’étape 5. Ensuite, lorsque vous sélectionnez **OK**, un workflow **Processus** est suivi d’un workflow **Veille**.

Les workflows **ProcessRunCaller** et **ProcessRunner** créent des factures. **ProcessRunCaller** appelle **ProcessRunner**. **ProcessRunner** est le workflow qui crée en fait les factures. Il traverse toutes les lignes de contrat pour lesquelles des factures doivent être créées, et crée des factures pour ces lignes. Pour déterminer les lignes de contrat pour lesquelles des factures doivent être créées, le traitement par lots examine les dates d’exécution des factures pour les lignes de contrat. Si des lignes de contrat appartenant à un contrat sont associées à la même date d’exécution de la facture, les transactions sont combinées en une seule facture comportant deux lignes de facture. Si aucune transaction ne nécessite la création d’une facture, le traitement par lots ne procède à aucune création.

Une fois **ProcessRunner** exécuté, il appelle **ProcessRunCaller**, fournit l’heure de fin, puis est fermé. **ProcessRunCaller** démarre alors un minuteur qui s’exécute pendant 24 heures à compter de l’heure de fin spécifiée. À la fin du minuteur, **ProcessRunCaller** est fermé.

Le processus de traitement par lots pour la création de factures est une tâche récurrente. Si ce processus de traitement par lots est exécuté plusieurs fois, plusieurs instances de la tâche sont créées et provoquent des erreurs. Par conséquent, vous devez démarrer le traitement par lots une seule fois, et vous devez le redémarrer uniquement s’il cesse de s’exécuter.

> [!NOTE]
> La facturation par lots ne s’exécute que pour les lignes de contrat de projet qui sont configurées par des calendriers de facturation. Une ligne de contrat avec une méthode de facturation à prix fixe doit avoir des jalons configurés. Une ligne de contrat de projet avec une méthode de facturation en régie nécessite la configuration d’un calendrier de facturation basé sur la date. Il en va de même pour une ligne de contrat basée sur un projet.      
 
### <a name="edit-a-draft-invoice"></a>Modifier un brouillon de facture

Lorsque vous créez un brouillon de facture de projet, toutes les transactions commerciales non facturées créées lors de l’approbation des entrées de temps, de dépenses et d’utilisation du matériel sont extraites sur la facture. Vous pouvez apporter les modifications suivantes lorsque la facture est toujours dans une phase de brouillon :

- Supprimer ou modifier les détails de la ligne de facture.
- Modifier et ajuster la quantité et le type de facturation.

Sélectionnez **Confirmer** pour confirmer une facture. L’action Confirmer est une action irréversible. Lorsque vous sélectionnez **Confirmer**, le système rend la facture en lecture seule et crée des chiffres réels de vente facturés à partir de chaque détail de ligne de facture pour chaque ligne de facture. Si le détail de ligne de facture fait référence à un chiffre réel de vente non facturé, le système contrepasse également le chiffre réel non facturé. (Tout détail de ligne de facture créé à partir d’une entrée de temps ou de dépenses fera référence à un chiffre réel de vente non facturé.) Les systèmes d’intégration comptables peuvent utiliser cette contrepassation pour contrepasser le travail en cours du projet à des fins comptables.

> [!NOTE]
> Les factures proforma confirmées et les enregistrements associés tels que les lignes de facture et les détails des lignes de facture ne peuvent pas être modifiés ou supprimés. 

### <a name="correct-a-confirmed-invoice"></a>Corriger une facture confirmée

Les factures confirmées peuvent être modifiées (corrigées). Lorsque vous corrigez une facture confirmée, un brouillon de la facture corrective est créé. Comme la supposition est que vous souhaitez contrepasser toutes les transactions et quantités de la facture d’origine, cette facture corrective inclut toutes les transactions de la facture d’origine, et toutes les quantités sont de 0 (zéro).

Si aucune transaction ne nécessite de correction, vous pouvez la supprimer du brouillon de facture corrective. Pour contrepasser ou ne retourner qu’une quantité partielle, vous pouvez modifier le champ **Quantité** sur le détail de la ligne. Si vous ouvrez le détail de ligne de facture, la quantité de la facture d’origine s’affiche. Vous pouvez ensuite modifier la quantité actuelle de la facture afin qu’elle soit inférieure ou supérieure à la quantité de la facture d’origine.

Lorsque vous confirmez une facture corrective, le chiffre réel facturé d’origine est contrepassé et un chiffre réel de ventes facturées est créé. Si la quantité a été réduite, la différence aura pour effet la création d’un chiffre réel de ventes non facturées. Par exemple, si la vente facturée d’origine était de huit heures, et que le détail de la ligne de facture corrective dispose d’une quantité réduite de six heures, la ligne de vente facturée d’origine est contrepassée et deux chiffres réels sont créés :

- Un chiffre réel de vente facturée de six heures.
- Un chiffre réel de ventes non facturées de deux heures restantes. Cette transaction peut être facturée ultérieurement ou marquée comme non facturable, selon les négociations avec le client.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
