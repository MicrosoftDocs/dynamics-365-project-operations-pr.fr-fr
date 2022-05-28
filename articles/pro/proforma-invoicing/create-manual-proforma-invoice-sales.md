---
title: Factures de projet pro forma
description: Cette rubrique fournit des informations sur les factures de projet pro forma dans Project Operations.
author: rumant
ms.date: 04/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f2ce672a412f7ad73b072854590cd423a3499fc1
ms.sourcegitcommit: 650a84add65588defdd2ac2c4524806baab070e0
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2022
ms.locfileid: "8628851"
---
# <a name="proforma-project-invoices"></a>Factures de projet pro forma

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

La facturation de projet pro forma offre aux chefs de projet un deuxième niveau d’approbation avant de créer des factures pour les clients. Le premier niveau de l’approbation est terminé lorsque les entrées de temps, de dépenses et de matériel que les membres de l’équipe du projet envoient sont approuvées.

Le déploiement simplifié de Dynamics 365 Project Operations n’est pas conçu pour générer des factures destinées aux clients. La liste suivante montre pourquoi les factures ne peuvent pas être générées :

- Ne contiennent pas d’informations sur les taxes.
- Impossible de convertir d’autres devises dans la devise de facturation.
- Impossible de mettre en page correctement les factures pour l’impression.

Par contre, vous pouvez utiliser un système financier ou de comptabilité pour créer des factures destinées aux clients qui utilisent les informations de propositions de facture générées.

## <a name="creating-project-invoices"></a>Création de factures de projet

Les factures de projet peuvent être créées une à la fois ou en bloc. Vous pouvez les créer manuellement, ou elles peuvent être configurées pour qu’elles soient générées lors d’exécutions automatisées.

### <a name="manually-create-project-invoices"></a>Créer manuellement des factures de projet 

Dans la page de liste **Contrats de projets**, vous pouvez créer des factures de projet séparément pour chaque contrat de projet, ou vous pouvez créer des factures en bloc pour les contrats de plusieurs projets.

   - Pour créer une facture pour un contrat de projet spécifique, dans la page de liste **Contrats de projets**, ouvrez un contrat de projet, puis sélectionnez **Créer une facture**.

   Une facture est générée pour toutes les transactions du contrat de projet sélectionné ayant le statut **Prêt pour la facturation**. Ces transactions comprennent le temps, les dépenses, les matériels, les jalons, les lignes de contrat basées sur les produits et d’autres lignes de journal de ventes non facturées qui peuvent avoir été confirmées.

Pour créer des factures en bloc :

1. Dans la page de liste **Contrats de projets**, sélectionnez un ou plusieurs contrats de projets pour lesquels créer une facture, puis sélectionnez **Créer des factures de projet**.
2. Un message d’avertissement vous informe qu’un délai peut s’écouler avant la création des factures. Le processus est également affiché. Cliquez sur **OK** pour fermer la zone de message.

   Une facture est générée pour toutes les transactions d’une ligne de contrat ayant le statut **Prêt pour la facturation**. Ces transactions comprennent le temps, les dépenses, les matériels, les jalons, les lignes de contrat basées sur les produits et d’autres lignes de journal de ventes non facturées qui peuvent avoir été confirmées.

3. Pour afficher les factures qui sont générées, accédez à **Ventes** \> **Facturation** \> **Factures**. Vous verrez une facture pour chaque contrat de projet.

### <a name="set-up-automated-creation-of-project-invoices"></a>Configurer la création automatique de factures de projet 

Procédez comme suit pour configurer l’exécution d’une facture automatique.

1. Accédez à **Paramètres** \> **Traitements par lots**.
2. Créez un traitement par lots, et nommez-le **Créer des factures dans Project Operations**. Le nom du traitement par lots doit inclure le terme « Créer des factures ».
3. Dans le champ **Type de tâche**, sélectionnez **Aucun**. Par défaut, les options **Fréquence quotidienne** et **Est actif** sont définies sur **Oui**.
4. Cliquez sur **Exécuter le flux de travail**. Dans la boîte de dialogue **Rechercher un enregistrement**, les workflows suivants s’affichent :

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. Sélectionnez **ProcessRunCaller**, puis cliquez sur **Ajouter**.
6. Dans la boîte de dialogue suivante, cliquez sur **OK**. Un flux de travail **Sleep** est suivi d’un flux de travail **Process**.

    Vous pouvez également sélectionner **ProcessRunner** à l’étape 5. Ensuite, lorsque vous sélectionnez **OK**, un workflow **Processus** est suivi d’un workflow **Veille**.

Les workflows **ProcessRunCaller** et **ProcessRunner** créent des factures. **ProcessRunCaller** appelle **ProcessRunner**. **ProcessRunner** est le workflow qui crée les factures. Ce workflow traverse toutes les lignes de contrat pour lesquelles des factures doivent être créées, et crée les factures. Pour déterminer les lignes de contrat pour lesquelles des factures doivent être créées, le workflow recherche les dates d’exécution de factures des lignes de contrat. Si des lignes de contrat qui appartiennent à un contrat disposent de la même date d’exécution de factures, les transactions sont combinées en une seule facture avec deux lignes de facture. S’il n’existe pas de transaction pour lesquelles créer des factures, aucune facture n’est créée.

Une fois que **ProcessRunner** a fini de s’exécuter, il appelle **ProcessRunCaller**, fournit l’heure de fin, et est fermé. **ProcessRunCaller** démarre alors un minuteur qui s’exécute pendant 24 heures à compter de l’heure de fin spécifiée. À la fin du minuteur, **ProcessRunCaller** est fermé.

Le processus de traitement par lots pour la création de factures est une tâche récurrente. Si ce traitement par lots est exécuté de nombreuses fois, plusieurs instances de la tâche sont créées et peuvent entraînent des erreurs. Pour contourner ce problème, démarrez le traitement par lots une seule fois, et redémarrez-le uniquement s’il cesse de s’exécuter.

> [!NOTE]
> La facturation par lots ne s’exécute que pour les lignes de contrat de projet qui sont configurées par des calendriers de facturation. Une ligne de contrat avec une méthode de facturation à prix fixe doit avoir des jalons configurés. Une ligne de contrat de projet avec une méthode de facturation en régie nécessite la configuration d’un calendrier de facturation basé sur la date. Il en va de même pour une ligne de contrat basée sur un projet.      
 
### <a name="edit-a-draft-invoice"></a>Modifier un brouillon de facture

Lorsque vous créez un brouillon de facture de projet, toutes les transactions commerciales non facturées créées lors de l’approbation des entrées de temps et de dépenses sont extraites sur la facture. Vous pouvez apporter les modifications suivantes lorsque la facture est toujours dans une phase de brouillon :

- Supprimer ou modifier les détails de la ligne de facture.
- Modifier et ajuster la quantité et le type de facturation.
- Ajouter directement le temps, les dépenses, le matériel et les frais comme transactions sur la facture. Vous pouvez utiliser cette fonctionnalité si la ligne de facture est mappée à une ligne de contrat qui permet ces classes de transactions.

Sélectionnez **Confirmer** pour confirmer une facture. Cette action est irréversible. Lorsque vous sélectionnez **Confirmer**, la facture devient en lecture seule et crée des chiffres réels de vente facturés à partir de chaque détail de ligne de facture pour chaque ligne de facture. Si le détail de ligne de facture fait référence à un chiffre réel de vente non facturé, le chiffre réel non facturé est contrepassé. Tout détail de ligne de facture créé à partir d’une entrée de temps, de dépense ou d’utilisation de matériel fera référence à un chiffre d’affaires réel non facturé. Les systèmes d’intégration comptables peuvent utiliser cette contrepassation pour contrepasser le travail en cours du projet à des fins comptables.

### <a name="correct-a-confirmed-invoice"></a>Corriger une facture confirmée

Les factures confirmées peuvent être modifiées. Lorsque vous corrigez une facture confirmée, un brouillon de la facture corrective est créé. Comme la supposition est que vous souhaitez contrepasser toutes les transactions et quantités de la facture d’origine, cette facture corrective inclut toutes les transactions de la facture d’origine, et toutes les quantités sont de zéro.

Si certaines transactions ne nécessitent pas de correction, vous pouvez les supprimer du brouillon de facture corrective. Pour contrepasser ou ne retourner qu’une quantité partielle, vous pouvez modifier le champ **Quantité** sur le détail de la ligne. Si vous ouvrez le détail de ligne de facture, la quantité de la facture d’origine s’affiche. Vous pouvez ensuite modifier la quantité actuelle de la facture afin qu’elle soit inférieure ou supérieure à la quantité de la facture d’origine.

Lorsque vous confirmez une facture corrective, le chiffre réel facturé d’origine est contrepassé et un chiffre réel de ventes facturées est créé. Si la quantité a été réduite, la différence aura pour effet la création d’un chiffre réel de ventes non facturées. Par exemple, si la vente facturée d’origine était de huit heures, et que le détail de la ligne de facture corrective dispose d’une quantité réduite de six heures, la ligne de vente facturée d’origine est contrepassée et deux chiffres réels sont créés :

- Un chiffre réel de vente facturée de six heures.
- Un chiffre réel de ventes non facturées de deux heures restantes. Cette transaction peut être facturée ultérieurement ou marquée comme non facturable, selon ce qui a été négocié avec le client.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
