---
title: Créer et confirmer des journaux d’entrée
description: Cette rubrique offre des informations sur la création et la confirmation des journaux d’entrées dans Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 8cb768337bc197895a837670f93b99b132c97437
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584225"
---
# <a name="create-and-confirm-entry-journals"></a>Créer et confirmer des journaux d’entrée

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Vous utilisez des journaux d’entrée pour enregistrer les chiffres réels directement dans Microsoft Dynamics 365 Project Operations. Lorsque vous utilisez des journaux d’entrée, vous n’avez pas besoin de saisir les journaux de temps, de dépense et d’utilisation du matériel dans Project Operations.

Un seul journal d’entrée vous permet de créer plusieurs lignes de journal. Lorsque le journal est confirmé, une ligne de journal d’entrées enregistre le chiffre réel pour les détails suivants :

- Le coût ou le revenu, selon le type de transaction sélectionné.
- La classe sélectionnée de transaction. Les classes disponibles sont les suivantes : **Temps**, **Dépense**, **Matériel**, **Provision**, **Jalon** et **Taxe**.
- Le projet et/ou une tâche qui est sélectionné sur la ligne de journal.

Suivez ces étapes pour créer un journal d’entrées dans Project Operations.

1. Accédez à **Ventes** \> **Transactions** \> **Journaux**.
2. Sur la page de la liste **Journaux des entrées**, dans le volet Actions, sélectionnez **Nouveau** pour créer un journal.
3. Sur la page **Nouveau journal**, dans le champ **Description**, vous pouvez saisir une description du journal.
4. Veillez à ce que le champ **Type de journal** soit défini sur **Entrée**, puis sélectionnez **Enregistrer**. Une fois le nouveau journal des entrées enregistré, un onglet **Lignes du journal** devrait apparaître sur la page du journal.
5. Sur l’onglet **Lignes du journal**, dans la barre d’outils au-dessus de la grille, sélectionnez **Nouveau** pour créer une ligne du journal d’entrées.
6. Dans la boîte de dialogue **Création rapide** pour créer une ligne du journal des entrées, définissez les champs comme décrit dans la table suivante.

    | Champ | Description | Impact fonctionnel |
    | --- | --- | --- |
    | Classe de transaction | La ligne du journal peut être classée dans l’une des six classes de transaction : **Temps**, **Dépense**, **Matériel**, **Provision**, **Jalon** ou **Taxe**. | La classe de transaction **Taxe** est obsolète dans Project Operations. <br> Si vous créez une classe de transaction de type **Taxe**, elle ne sera pas traitée par la facturation ou dans les calculs de coûts ou de revenus. **Jalon** est une classe de transaction de revenus uniquement. <br>La classe de transaction **Provision** représente une avance qui a été reçue d’un client. Elle doit toujours être créée sous la forme d’une paire de lignes de journal des ventes facturées et des lignes de journal des ventes non facturées. |
    | Type de transaction | Les transactions de type **Coût**, **Ventes entre organisations** et **Coût unitaire d’allocation des ressources** doivent être utilisés pour enregistrer le coût.<br> Les transactions de type **Ventes non facturées** et **Ventes facturées** doivent être utilisées pour enregistrer les revenus. | La classe de transaction **Provision** ne fonctionne qu’avec les types de transaction **Ventes non facturées** et **Ventes facturées**.<br> La classe de transaction **Jalon** ne fonctionne qu’avec le type de transaction **Ventes facturées**. <br>Les transactions de type **Ventes entre organisations** et **Coût unitaire d’allocation des ressources** ne s’appliquent qu’à la classe de transaction **Temps** et celles-ci ne sont disponibles que sur les journaux des entrées dans le scénario de déploiement Lite et non lors du déploiement de Project Operations dans les scénarios basés sur les ressources/produits non stockés. |
    | Sélectionner un produit | Quand la classe de transaction **Matériel** est sélectionnée, ce champ vous permet de spécifier si la transaction du matériel pour laquelle vous créez la ligne du journal est un produit existant ou un produit en écriture. | Si vous sélectionnez **Produit hors catalogue**, vous pouvez entrer un nom pour le produit. |
    | Produit | Référence au produit du catalogue. | |
    | Description | Description de la ligne du journal pour faciliter son identification. | Pour les lignes du journal des ventes non facturées, la valeur sera utilisée comme description lors de la création des détails de la ligne de facture. |
    | Description externe | Description de la ligne de journal qui peut être utilisée pour le partage avec des parties prenantes externes. | Pour les lignes du journal des ventes non facturées, la valeur sera utilisée comme description externe lors de la création des détails de la ligne de facture. Elle peut également figurer sur la facture qui est envoyée au client. |
    | Type de facturation | Valeur qui indique si la ligne de journal sera comptée comme un composant facturable, gratuit ou non facturable sur le projet. | Dans un flux classique, le type de facturation est dérivé des conditions convenues qui sont configurées sur le contrat. Cependant, lorsque vous enregistrez une ligne de journal, vous pouvez entrer une valeur dans ce champ. |
    | Date du document | Utilisez une date à laquelle la transaction est survenue. | |
    | Date de début | Utilisez la date à laquelle la transaction est survenue. | Ce champ est utilisé pour la comparaison avec la date de création de la facture pour les transactions de type **Ventes non facturées**. Cette comparaison vous aidera à décider si la transaction est datée dans le futur ou dans le passé. Seules les transactions datées dans le passé seront ajoutées à la facture. |
    | Date de fin | Utilisez la date à laquelle la transaction est survenue. | |
    | Date comptable | Utilisez la date à laquelle l’impact comptable sera enregistré. | |
    | Client de la ligne de contrat | Par défaut, si la ligne de contrat n’a qu’un seul client, ce champ est défini sur le client sur la ligne de contrat lorsque la ligne de journal est enregistrée. Si la ligne de contrat a plusieurs clients, sélectionnez le bon client sur la ligne de contrat. | Si le système ne peut pas déterminer le client de la ligne de contrat sur la ligne de journal, et s’il est vide sur le chiffre réel de type **Ventes non facturées** créé à partir de la ligne de journal, le chiffre réel ne sera pas facturé. |
    | Project | Sélectionnez le projet sur lequel enregistrer le chiffre réel. | En fonction du projet, de la classe de transaction et de la tâche sélectionnés, le système tentera de déterminer le contrat, la ligne de contrat et le client de la ligne de contrat. |
    | Task | Sélectionnez la tâche sur laquelle enregistrer le chiffre réel. | Si vous avez associé des tâches à des lignes de contrat lors de la configuration du contrat, le système utilisera la tâche sélectionnée, ainsi qu’un projet et une classe de transaction, pour déterminer le contrat, la ligne de contrat et le client de la ligne de contrat. |
    | Catégorie de transaction | Sélectionnez la catégorie de transaction sur laquelle enregistrer le chiffre réel. | Pour les dépenses, la catégorie de transaction sélectionnée détermine le prix par défaut qui sera inscrit sur la ligne de journal lors de sa sauvegarde. |
    | Role | Ce champ est pertinent pour les lignes du journal de temps. Sélectionnez le rôle de la ressource qui a passé du temps sur le projet et/ou la tâche. | Pour les lignes de journal de temps, si vous utilisez la configuration prête à l’emploi pour la saisie des coûts de ressources et des taux de facturation par défaut, le rôle sélectionné est utilisé avec l’unité d’allocation des ressources pour déterminer le prix par défaut qui sera saisi sur la ligne de journal lors de sa sauvegarde. Si vous utilisez une configuration personnalisée pour la saisie des prix par défaut, vous devez revoir cette configuration pour déterminer si le champ **Rôle** est utilisé pour saisir les valeurs de prix par défaut. |
    | Sous-contrat | Si la ligne de journal représente une capacité sous-traitée, ou des dépenses ou des matériaux sous-traités, sélectionnez le sous-contrat approprié. | Lorsque les lignes du journal des coûts sont enregistrées, le sous-traitant sélectionné déterminera la liste de prix utilisée pour saisir le coût unitaire par défaut. |
    | Ligne de sous-traitance | Si la ligne de journal représente une capacité sous-traitée, ou des dépenses ou des matériaux sous-traités, sélectionnez la ligne de sous-contrat appropriée. | Lorsque les lignes de journal des coûts sont enregistrées, la ligne de sous-traitance sélectionnée garantira que les calculs de capacité disponible sur la ligne de sous-traitance sont correctement calculés. |
    | Méthode du montant | Par défaut, ce champ est défini sur **Multiplier la quantité par le prix**. Si ce mode est utilisé, le montant est calculé comme *Quantité* × *Prix*. L’autre mode pris en charge est **Prix fixe**. Lorsque ce mode est utilisé, le prix est défini sur le montant et la quantité n’est pas utilisée dans le calcul. | |
    | Planification d’unités et unité | Ensemble, la planification d’unités et l’unité identifient l’unité de la quantité. | La combinaison de l’unité et de la catégorie de transaction est utilisée pour saisir les prix par défaut des dépenses. Dans la configuration par défaut de Project Operations, la combinaison de l’unité, du rôle et de l’unité d’allocation des ressources est utilisée pour saisir les prix par défaut pour le temps. Si vous avez une configuration personnalisée pour la saisie des prix par défaut, elle est utilisée avec l’unité. La combinaison du produit et de l’unité est utilisée pour saisir les prix par défaut des matériaux. |
    | Quantité | Entrez la quantité. | |
    | Tarif | Si le prix est laissé vide lors de la création de la ligne de journal, les valeurs pertinentes seront utilisées pour saisir les prix par défaut, en fonction de la classe de transaction. Si un prix est entré lors de la création de la ligne de journal, ce prix est utilisé. | |
    | Taxes | Entrez n’importe quel montant de taxe. | En fonction du montant de taxe saisi, le montant étendu est calculé comme suit : *Montant* + *Taxe*. |

## <a name="confirm-an-entry-journal"></a>Confirmer un journal d’entrée

Après avoir saisi toutes les lignes de journal dans un journal de saisie, vous pouvez confirmer le journal. Ce processus enregistrera chaque ligne de journal en tant que chiffres réels sur les projets appropriés.

Une fois qu’un journal est confirmé, vous ne pouvez plus le modifier ni aucune de ses lignes.

## <a name="actuals-created-by-entry-journal-confirmation"></a>Chiffres réels créés par la confirmation du journal des entrées

Il existe quelques différences clés entre les chiffres réels créés par la confirmation du journal des entrées et les chiffres réels créés lors de l’approbation des journaux d’utilisation du temps, des dépenses et du matériel et de la confirmation des factures dans Project Operations :

- Les journaux d’entrées n’utilisent pas de connexions de transaction pour associer le chiffre réel du coût au chiffre réel des ventes non facturées. Les chiffres réels qui sont créés lorsque les journaux d’utilisation du temps, des dépenses et des matériaux sont approuvés utilisent toujours des connexions de transaction pour associer le coût aux chiffres réels des ventes non facturées.
- Les journaux d’entrées n’utilisent pas d’origines des transactions pour associer le chiffre réel du coût et le chiffre réel des ventes non facturées à tout enregistrement d’origine. Les chiffres réels qui sont créés lorsque les journaux d’utilisation du temps, des dépenses et des matériaux sont approuvés utilisent toujours des origines de transaction pour associer le coût et chiffres réels des ventes non facturées à l’entrée de temps d’origine.
- Lorsque les chiffres réels des ventes non facturées créées par la confirmation du journal des entrées sont facturées, les chiffres réels des ventes facturées créées lors de la confirmation de la facture sont associées aux chiffres réels de ventes non facturées, de la même manière que les chiffres réels de ventes non facturées créées lorsque les journaux d’utilisation du temps, des dépenses et des matériaux sont approuvés.
- Les lignes du journal des entrées créées pour le temps saisi par les ressources entre les organisations n’entraînent pas la création automatique des chiffres réels de types **Coût unitaire d’allocation des ressources** et **Ventes entre organisations**. Ces chiffres réels doivent être créés manuellement. Ce comportement diffère du comportement des entrées de temps qui sont enregistrées par des ressources entre organisations. Dans ce cas, lorsque le temps est approuvé, l’application crée automatiquement les chiffres réels de type **Coût** sur le projet et les chiffres réels de type **Coût unitaire d’allocation des ressources** et **Ventes entre organisations** sur la division propriétaire de l’employé. Puis elle utilise des connexions de transaction pour associer ces chiffres réels et des origines de transaction pour les associer à l’entrée de temps d’origine.
- Lorsque les journaux d’entrée sont confirmés, ils créent des chiffres réels. Toutefois, les journaux de correction ne peuvent pas être utilisés pour corriger ces chiffres réels. Ce comportement diffère du comportement des chiffres réels qui sont créés lorsque les journaux de temps, de dépense et d'utilisation de matériel sont approuvés. Dans ce cas, l’application vous permet d’utiliser les journaux de correction pour corriger les chiffres réels afin de corriger les éventuelles erreurs, à condition que ces chiffres réels n’aient pas encore été facturés. S’ils ont déjà été facturés, vous pouvez toujours corriger un chiffre réel si vous traitez un crédit complet de ce chiffre réel au client.

> [!NOTE]
> Les journaux d’entrée n’appliquent pas de règles strictes par défaut. Par conséquent, utilisez ces journaux d’entrées le moins possible et faites preuve de prudence pour vous assurer de ne pas créer de données financières corrompues dans votre système. Chaque fois que vous le pouvez, utilisez les journaux d’utilisation du temps, des dépenses et des matériaux, la configuration des jalons et des acomptes sur les contrats de projet et le processus de confirmation de facture de projet au lieu des journaux d’entrées pour créer des chiffres réels.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
