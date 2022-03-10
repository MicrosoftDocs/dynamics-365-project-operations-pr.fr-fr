---
title: Configurer la création automatique de factures
description: Cette rubrique fournit des informations sur le paramétrage et la configuration de la création automatique de factures pro forma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1cce457fbc04ba9d3890d73439e6e7fd3db44d84a4498d5dc68ed82d362158b5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997513"
---
# <a name="set-up-automatic-invoice-creation"></a>Configurer la création automatique de factures 
 
_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_

Vous pouvez configurer la création automatique de factures dans Dynamics 365 Project Operations. Le système crée une facture pro forma provisoire selon le calendrier de facturation pour chaque contrat de projet et chaque ligne de contrat. Les calendriers de facturation sont configurés au niveau de la ligne de contrat. Chaque ligne d’un contrat peut présenter un calendrier de facturation distinct, ou le même calendrier de facturation peut être inclus sur toutes les lignes du contrat.

Lorsque vous créez une facture, le système crée toujours au moins une facture par contrat de projet. Dans certains cas, plusieurs factures peuvent être créées. Par exemple, si le contrat a plusieurs clients, le même nombre de factures que le nombre de clients qui ont des transactions facturables à facturer sera créé sur ce contrat de projet.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Comprendre comment les transactions sont incluses sur une facture 

Parfois, chaque ligne de contrat basée sur un projet spécifie une planification de facture distincte. Par exemple, les services de mise en œuvre pour le contrat Adatum ont les lignes de contrat suivantes :

- Travail prototype qui est un prix fixe avec deux jalons créés manuellement.
- Travail de mise en œuvre qui comprend le temps et sera facturé toutes les deux semaines le lundi.
- Les dépenses engagées qui doivent être facturées mensuellement le premier lundi de chaque mois.

Les planifications de facture définies sur chacun de ces deux éléments de ligne ressemblent au tableau suivant :

| Ligne de contrat | Date d’exécution de la facture | Date butoir de la transaction | Date du jalon | Montant du jalon |
| --- | --- | --- | --- | --- |
| Travail prototype | Lundi 5 octobre | - | Lundi 5 octobre | 5 000 USD |
| - | Mardi 3 novembre | - | Mardi 3 novembre | 12 000 USD |
| Travail d’implémentation | Lundi 5 octobre | Dimanche 4 octobre | - | - |
| - | Lundi 19 octobre | Dimanche 18 octobre | - | - |
| - | Lundi 2 novembre | Dimanche 1er novembre | - | - |
| - | Lundi 16 novembre | Dimanche 15 novembre | - | - |
| Dépenses engagées | Lundi 5 octobre | Dimanche 4 octobre | - | - |
| - | Lundi 2 novembre | Dimanche 1er novembre | - | - |

Dans cet exemple, lorsque la facturation automatique s’exécute sur :

- **4 octobre ou à toute date antérieure** : Aucune facture n’est générée pour ce contrat car la table **planification de facture** pour chacune de ces lignes de contrat n’indique pas le dimanche 4 octobre comme date d’exécution de la facture.
- **Lundi 5 octobre** : Une facture est générée pour :

    - Travail de prototype qui inclut le jalon, s’il est marqué comme **Prêt à facturer**.
    - Travail de mise en œuvre qui comprend toutes les transactions de temps créées avant la date limite de transaction du dimanche 4 octobre, avec le marquage **Prêt à facturer**.
    - Les dépenses engagées qui comprennent toutes les transactions de dépenses créées avant la date limite de transaction du dimanche 4 octobre, avec le marquage **Prêt à facturer**.
  
- **6 octobre ou à toute date antérieure au 19 octobre** : Aucune facture n’est générée pour ce contrat car la table **planification de facture** pour chacune de ces lignes de contrat n’indique pas le 6 octobre ou toute date antérieure au 19 octobre comme date d’exécution de la facture.
- **Lundi 19 octobre** : Une facture est générée pour le travail de mise en œuvre qui comprend toutes les transactions de temps créées avant la date limite de transaction du dimanche 18 octobre, avec le marquage  **Prêt à facturer**.
- **Lundi 2 novembre** : Une facture est générée pour :

    - Travail de mise en œuvre qui comprend toutes les transactions de temps créées avant la date limite de transaction du dimanche 1er novembre, avec le marquage **Prêt à facturer**.
    - Les dépenses engagées qui comprennent toutes les transactions de dépenses créées avant la date limite de transaction du dimanche 1er novembre, avec le marquage **Prêt à facturer**.

- **Mardi 3 novembre** : Une facture est générée pour le travail de prototype qui inclut le jalon pour 12 000 USD, s’il est marqué comme **Prêt à facturer**.

## <a name="configure-automatic-invoicing"></a>Configurer la facturation automatique

Procédez comme suit pour configurer l’exécution d’une facture automatique.

1. Dans **Project Operations**, accédez à **Paramètres** > **Configuration de facture périodique**.
2. Créez un traitement par lots, et nommez-le **Créer des factures dans Project Operations**. Le nom du traitement par lots doit inclure les mots « Créer des factures ».
3. Dans le champ **Type de tâche**, sélectionnez **Aucun**. Par défaut, les champs **Fréquence quotidienne** et **Est actif** sont définies sur **Oui**.
4. Cliquez sur **Exécuter le flux de travail**. Dans la boîte de dialogue **Rechercher un enregistrement**, trois flux de travail s’affichent :

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Sélectionnez **ProcessRunCaller**, puis cliquez sur **Ajouter**.
6. Dans la boîte de dialogue suivante, cliquez sur **OK**. Un flux de travail **Sleep** est suivi d’un flux de travail **Process**. 

> [!NOTE]
> Vous pouvez également sélectionner **ProcessRunner** à l’étape 5. Ensuite, lorsque vous sélectionnez **OK**, un workflow **Processus** est suivi d’un workflow **Veille**.

Les workflows **ProcessRunCaller** et **ProcessRunner** créent des factures. **ProcessRunCaller** appelle **ProcessRunner**. **ProcessRunner** est le workflow qui crée en fait les factures. Le workflow traverse toutes les lignes de contrat pour lesquelles des factures doivent être créées, et crée des factures pour ces lignes. Pour déterminer les lignes de contrat pour lesquelles des factures doivent être créées, la tâche recherche les dates d’exécution de factures des lignes de contrat. Si des lignes de contrat appartenant à un contrat sont associées à la même date d’exécution de la facture, les transactions sont combinées en une seule facture comportant deux lignes de facture. S’il n’existe pas de transaction pour créer des factures, la tâche ignore la création de facture.

Une fois que **ProcessRunner** a fini de s’exécuter, il appelle **ProcessRunCaller**, fournit l’heure de fin, et est fermé. **ProcessRunCaller** lance alors une minuterie qui s’exécute pendant 24 heures à partir de l’heure de fin spécifiée. À la fin de la minuterie, **ProcessRunCaller** est fermé.

Le processus de traitement par lots pour la création de factures est une tâche récurrente. Si ce traitement par lots est exécuté de nombreuses fois, plusieurs instances de la tâche sont créées et entraînent des erreurs. Par conséquent, vous devez démarrer le traitement par lots une seule fois, et redémarrer uniquement s’il cesse de s’exécuter.

> [!NOTE]
> La facturation par lots dans Project Operations ne s’exécute que pour les lignes de contrat de projet qui sont configurées par des planifications de facture. Une ligne de contrat avec une méthode de facturation à prix fixe doit avoir des jalons configurés. Une ligne de contrat de projet avec une méthode de facturation en régie nécessite la configuration d’un calendrier de facturation basé sur la date.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
