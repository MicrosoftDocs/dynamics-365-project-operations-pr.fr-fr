---
title: Processus de vente
description: Cette rubrique fournit des informations sur les processus de vente de base.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2561a54af6bdb9764a318f012fdc53f7b3298893
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145175"
---
# <a name="sales-processes"></a>Processus de vente

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Les processus de vente utilisés dans une organisation basée sur un projet diffèrent des processus de vente utilisés dans une organisation basée sur un produit. Cette différence se produit parce que plusieurs cycles de vente pour les organisations basées sur un projet sont longs et requièrent des techniques personnalisées d’estimation pour analyser et créer des devis pour chaque transaction. Dynamics 365 Project Service Automation utilise une partie de la même fonctionnalité qui est utilisée dans le processus de vente pour Dynamics 365 Sales. Voici quelques exemples :

- Une entité Prospect permet de suivre le processus de vente.
- Les prospects en cours de qualification sont suivis en tant qu’opportunités. Le processus de vente peut également commencer par l’opportunité.
- Il est possible d’accéder à tous les artefacts associés à une opportunité. Ces artefacts comprennent l’équipe des ventes, les parties prenantes, la probabilité, l’évaluation, les phases de vente et les processus d’entreprise.
- Plusieurs devis sont créés pour une opportunité.
- Un devis est marqué comme **Fermée et conclue** pour créer une commande client. Dans PSA, la commande client est personnalisée et est appelée un contrat de projet.

L’illustration suivante montre un processus de vente habituel dans une organisation basée sur un projet.

> ![Processus de vente dans une organisation basée sur un projet](media/basic-guide-1.png)

## <a name="estimating-a-sale"></a>Estimation d’une vente
La valeur d’une vente peut être estimée sur la base de projets précédemment livrés et la complexité des projets. Pour les projets impliquant des extensions de projets précédents, ou des projets où l’expertise du fournisseur est élevée et des modèles de travail réputés sont utilisés, vous pouvez utiliser un processus plus simple d’estimation. Les projets plus complexes ont généralement un processus d’achat plus long. Par conséquent, il existe plus de phases dans le processus d’évaluation de ventes. Au début du processus, l’équipe de vente utilise l’entrée des responsables de compte et d’experts spécialisés pour commencer à créer une estimation générale de chaque composant distinct de travail qui est cité. Ces composants de travail sont représentés par des lignes de devis. 

Vous pouvez créer une estimation générale de devis. À la fin, cette évaluation générale sera remplacée par une estimation plus détaillée basée sur un plan du projet créé en utilisant des modèles de projets normalisés. Ces modèles permettent d’établir une planification et de déterminer des valeurs monétaires sur le devis et ses composants (lignes de devis). 

Vous pouvez créer plusieurs devis pour un projet et les regrouper sous un type d’entité unique d’opportunité. À la fin, l’un de ces devis est marqué comme **Fermé et conclu**, et un contrat de projet ou un énoncé des travaux est créé. Un contrat de projet contient la valeur contractuelle de chaque composant (ligne de contrat) qui est acceptée par le client pour la livraison. Un énoncé des travaux est généralement créé en tant que document Microsoft Word. Toutes les factures envoyées au client pendant la durée de la livraison du projet fait référence au contrat du projet ou à l’énoncé des travaux.

Vous pouvez également créer des devis alternatifs sous un type d’entité Opportunité ou configurer le système pour qu’un contrat de projet soit créé lorsqu’un devis est conclu. Dans ce cas, vous pouvez joindre un document Word qui représente l’énoncé des travaux à l’enregistrement de contrat du projet.

![Fermeture d’un devis pour créer un contrat de projet](media/basic-guide-2.png)

## <a name="configuring-the-sales-process"></a>Configuration du processus de vente
Vous pouvez utiliser des flux des processus d’entreprise dans Microsoft Dynamics 365 pour configurer votre processus de vente. Les flux des processus d’entreprise donnent à votre force de vente une interface visuelle guidée qu’ils peuvent utiliser pour transférer la transaction dans les différentes phases courantes dans votre entreprise.

Par exemple, votre société peut comporter les six étapes suivantes dans le processus de vente :

1. Inclure
2. Estimation
3. Révision interne
4. Contrat
5. Livrer
6. Fermer

Ces six étapes sont représentés par des chevrons (\>) que vous sélectionnez pour les développer dans chaque type d’entité Opportunité que vous créez.

![Configuration du processus d’entreprise dans Dynamics 365](media/basic-guide-3.png)
 
Votre organisation peut utiliser différentes entités pour représenter la même transaction à mesure qu’elle évolue. Au début du processus de vente, une transaction est représentée par l’entité Opportunité. Au fil du temps et à mesure que des informations émergent, vous pouvez utiliser des estimations générales pour créer un ou plusieurs devis. Si l’un de ces devis est examiné par les parties prenantes internes et du client, l’entité Devis représente la transaction. Une fois que le client accepte le devis, un contrat du projet ou un énoncé des travaux représente la transaction. Pour soutenir ce comportement, des flux des processus d’entreprise sont structurés afin que chaque phase du processus soit liée à une table de base de données différente.

La phase **Inclure** dans le processus de vente peut être soutenue par une entité Opportunité. Les phases **Estimation** et **Révision interne** ne sont soutenus par une entité Devis. Les phases **Contrat**, **Livraison** et **Fermer** peuvent être soutenues par une entité Contrat du projet.

Lorsque vous déplacez les transactions via les phases, vous êtes invité à créer l’enregistrement d’entité approprié pour vous aider et vous guider dans le processus. Les phases peuvent être conditionnelles. Par exemple, si vous avez besoin d’une révision interne d’un devis uniquement si le devis utilise des tarifs personnalisés, vous pouvez configurer cette condition à la phase appropriée du processus d’entreprise. La phase **Révision interne** est affichée alors uniquement pour les devis qui utilisent des tarifs personnalisés. Pour toutes les autres transactions et devis, la phase **Estimation** est suivie de la phase **Contrat**.

> [!NOTE]
> PSA contient des pages spécifiques pour les entités Opportunité, Devis, Commande, et Facture. Vous devez créer des opportunités, des devis, des commandes et des factures de service de projet à l’aide des pages d’informations de projet de celles-ci. Si vous utilisez une autre page pour créer un enregistrement, vous ne pourrez pas ouvrir l’enregistrement à partir de la page **Informations sur le projet**. Si vous souhaitez ouvrir un enregistrement à partir de la page **Informations sur le projet**, vous devez supprimer l’enregistrement et le recréer à l’aide de la page **Informations sur le projet**. Sur la page **Informations sur le projet**, une logique métier pour chacun de ces types d’entités garantit que le champ **Type** de l’enregistrement est correctement défini, et que tous les concepts obligatoires sont correctement initialisés.

> ![Informations sur le projet pour une nouvelle commande](media/basic-guide-4.png)
 
## <a name="differences-between-project-service-automation-and-sales"></a>Différences entre Project Service Automation et Sales
Bien que le processus de vente dans PSA utilise les fonctionnalités de base du processus de vente de Sales, il présente des différences clés en raison des variations dans les pratiques commerciales des organisations basées sur un projet. Voici quelques exemples :

- **Devis de projet** : Dans Project Service Automation, un devis est fermé une fois qu’un contrat de projet est créé à partir d’un devis. Dans Sales, vous pouvez conserver un devis ouvert après l’avoir remporté. La raison pour cette différence est que la correspondance entre un devis et un contrat de projet est meilleure pour les organisations basées sur un projet. 
- **Activation et révisions** : Dans PSA, l’activation et les révisions ne sont pas prises en charge pour les devis de projet. Dans Sales, un devis peut être verrouillé pour empêcher toute modification supplémentaire.
- **Fermeture d’un devis comme perdue ou conclu** : Dans PSA, lorsqu’un devis de projet est fermé comme conclu ou perdu, l’opportunité reste ouverte. Tous les autres devis de l’opportunité sont fermés comme étant perdus. Dans Sales, lorsqu’un devis est fermé comme conclu ou perdu, l’utilisateur est invité à exécuter des actions sur l’opportunité. Selon l’entrée de l’utilisateur, l’opportunité sous-jacente peut être fermée ou laissée être ouverte.

## <a name="tracking-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Suivi des révisions des devis et des plans de projet dans le cycle de vente
Dans PSA, vous ne pouvez pas suivre les modifications apportées à un devis. À la place, vous devez marquer le devis existant comme **Fermé comme perdu** puis créer un devis. Vous pouvez copier un devis ou cloner un devis basé sur un projet à l’aide de PSA.

## <a name="tracking-comments-and-approvals-of-quotes-and-project-contracts"></a>Suivi des commentaires et des approbations de devis et de contrats de projet
Vous pouvez gérer la révision et l’approbation des devis et des contrats de projet à l’aide du mur d’enregistrement et des publications. Votre organisation peut créer des workflows et des plug-ins personnalisés pour attribuer, rediriger, réaffecter et gérer les notifications de révision et d’approbation des éléments de travail.
