---
title: Vue d’ensemble du processus de vente
description: Cette rubrique fournit des informations sur les processus de vente de base.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a03cb4949cafdf0754a89435542f616c41d65a5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996024"
---
# <a name="sales-process-overview"></a>Vue d’ensemble du processus de vente

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Les processus de vente utilisés dans une organisation basée sur un projet diffèrent des processus de vente utilisés dans une organisation basée sur un produit. En effet, plusieurs cycles de vente pour les organisations basées sur un projet sont longs et requièrent des techniques personnalisées d’estimation pour analyser et créer des devis pour chaque transaction. Dynamics 365 Project Operations utilise certaines des fonctionnalités suivantes qui sont utilisées dans un processus de vente :

- Un enregistrement de prospect permet de suivre le processus de vente.
- Les prospects en cours de qualification sont suivis en tant qu’opportunités.
- Tous les artefacts associés à une opportunité sont accessibles. Ces artefacts incluent l’équipe de vente, les parties prenantes, la probabilité, l’évaluation, les phases de vente et les processus d’entreprise.
- Plusieurs devis sont créés pour une opportunité.
- Un devis a le statut **Fermé et conclu** pour créer une commande client. Dans Project Operations, la commande client est personnalisée et est appelée un contrat de projet.

## <a name="estimate-a-sale"></a>Estimer une vente
La valeur d’une vente peut être estimée sur la base de projets précédemment livrés et la complexité des projets. Pour les projets impliquant des extensions de projets précédents, ou des projets où l’expertise du fournisseur est élevée et des modèles de travail réputés sont utilisés, vous pouvez utiliser un processus plus simple d’estimation. Les projets plus complexes ont généralement un processus d’achat plus long. Par conséquent, il existe plus de phases dans le processus d’évaluation de ventes. Au début du processus, l’équipe de vente utilise l’entrée des responsables de compte et d’experts spécialisés pour commencer à créer une estimation générale de chaque composant distinct de travail qui est cité. Ces composants de travail sont représentés par des lignes de devis. 

Vous pouvez créer une estimation générale de devis. À la fin, cette évaluation générale sera remplacée par une estimation plus détaillée basée sur un plan du projet créé en utilisant des modèles de projets normalisés. Ces modèles permettent d’établir une planification et de déterminer des valeurs monétaires sur le devis et ses composants (lignes de devis). 

Vous pouvez créer plusieurs devis pour un projet et les regrouper sous un enregistrement d’opportunité unique. À la fin, l’un de ces devis est marqué comme **Fermé et conclu**, et un contrat de projet ou un énoncé des travaux est créé. Un contrat de projet contient la valeur contractuelle de chaque composant (ligne de contrat) qui est acceptée par le client pour la livraison. Un énoncé des travaux est généralement créé en tant que document Microsoft Word. Toutes les factures envoyées au client pendant la durée de la livraison du projet fait référence au contrat du projet ou à l’énoncé des travaux.

Vous pouvez également créer des devis alternatifs sous un enregistrement d’opportunité ou configurer le système pour qu’un contrat de projet soit créé lorsqu’un devis est conclu. Dans ce cas, vous pouvez joindre un document Word qui représente l’énoncé des travaux à l’enregistrement de contrat du projet.

## <a name="configure-the-sales-process"></a>Configurer le processus de vente
Vous pouvez utiliser des flux des processus d’entreprise pour configurer votre processus de vente. Ces flux fournissent une interface visuelle guidée pour faire avancer les transactions à travers les étapes du processus de vente.

Par exemple, votre société peut comporter les six étapes suivantes dans le processus de vente :

1. Qualifier
2. Estimation
3. Révision interne
4. Contrat
5. Livrer
6. Fermer
 
Votre organisation peut utiliser différentes entités pour représenter la même transaction à mesure qu’elle évolue. Au début du processus de vente, une transaction est représentée par l’entité Opportunité. Au fil du temps et à mesure que des informations émergent, vous pouvez utiliser des estimations générales pour créer un ou plusieurs devis. Si l’un de ces devis est examiné par les parties prenantes internes et du client, l’entité Devis représente la transaction. Une fois que le client accepte le devis, un contrat du projet ou un énoncé des travaux représente la transaction. Pour soutenir ce comportement, des flux des processus d’entreprise sont structurés afin que chaque phase du processus soit liée à une table de base de données différente.

La phase **Inclure** dans le processus de vente peut être soutenue par une entité Opportunité. Les phases **Estimation** et **Révision interne** ne sont soutenus par une entité Devis. Les phases **Contrat**, **Livraison** et **Fermer** peuvent être soutenues par une entité Contrat du projet.

Lorsque vous déplacez les transactions via les phases, vous êtes invité à créer l’enregistrement d’entité approprié pour vous aider et vous guider dans le processus. Les phases peuvent être conditionnelles. Par exemple, si vous avez besoin d’une révision interne d’un devis uniquement si le devis utilise des tarifs personnalisés, vous pouvez configurer cette condition à la phase appropriée du processus d’entreprise. La phase **Révision interne** est affichée alors uniquement pour les devis qui utilisent des tarifs personnalisés. Pour toutes les autres transactions et devis, la phase **Estimation** est suivie de la phase **Contrat**.

> [!NOTE]
> Project Operations a des pages spécifiques pour les enregistrements d’entité Opportunité, Devis, Commande et Facture. Vous devez créer ces enregistrements à l’aide des pages d’informations sur le projet de ces entités. Sinon, vous ne pourrez pas ouvrir les enregistrements à partir de la page **Informations de projet**. Si vous souhaitez ouvrir un enregistrement à partir de la page **Informations de projet**, vous devez supprimer l’enregistrement et le recréer à l’aide de la page **Informations de projet** où la logique métier de chacun de ces types d’entités garantit que le champ **Type** de l’enregistrement est correctement défini et que tous les concepts obligatoires sont correctement initialisés.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Suivre des révisions des devis et des plans de projet dans le cycle de vente
Dans Project Operations, vous ne pouvez pas suivre les modifications apportées à un devis. À la place, vous devez marquer le devis existant comme **Fermé comme perdu** puis créer un devis. Vous pouvez copier un devis ou cloner un devis basé sur un projet.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Suivre des commentaires et des approbations de devis et de contrats de projet
Vous pouvez gérer la révision et l’approbation des devis et des contrats de projet à l’aide du mur d’enregistrement et des publications. Votre organisation peut créer des workflows et des plug-ins personnalisés pour attribuer, rediriger, réaffecter et gérer les notifications de révision et d’approbation des éléments de travail.


[!INCLUDE[footer-include](../includes/footer-banner.md)]