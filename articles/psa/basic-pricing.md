---
title: Tarification de projet
description: Cette rubrique fournit des informations sur le fonctionnement de la tarification dans Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
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
ms.openlocfilehash: dfbfb59547f295e5fb275264b9222bfa20517f6278144ca013e14a99454b6840
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000573"
---
# <a name="project-pricing"></a>Tarification de projet 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation étend l’entité Tarifs dans Dynamics 365 Sales. 

## <a name="key-entities"></a>Principales entités

Les tarifs inclut des informations fournies par quatre entités distinctes :

- **Tarifs** : Cette entité stocke des informations sur le contexte, la devise, la validité de la date, et l’unité de temps pour le temps de la tarification. Le contexte indique si les tarifs sont des taux de coût ou des taux de ventes. 
- **Devise** : Cette entité stocke la devise des prix sur les tarifs. 
- **Date** : Cette entité est utilisée lorsque le système essaie d’entrer un prix par défaut dans une transaction. La tarification PSA sélectionne les tarifs avec une validité de date qui inclut la date de la transaction. Si la tarification PSA trouve plusieurs tarifs effectifs à la date de transaction jointe au devis, contrat ou unité d’organisation associée, alors aucun prix n’a de valeur par défaut. 
- **Temps** : Cette entité stocke l’unité du temps dans laquelle les tarifs sont exprimés, comme les taux quotidiens ou horaires. 

L’entité Tarifs comporte trois tables associées qui stockent des prix :

  - **Prix du rôle** : Cette table stocke un taux pour une combinaison de valeurs de rôle et d’unité d’organisation et est utilisé pour définir des tarifs basés sur les rôles pour les ressources humaines.
  - **Prix de la catégorie de transaction** : Cette table stocke les prix par catégorie de transaction et est utilisée pour définir les prix des catégories de dépenses.
  - **Éléments tarifaires** : Cette table stocke les prix des produits du catalogue.

> ![Configuration des prix en utilisant des tarifs.](media/basic-guide-12.png)
 
Les tarifs sont une carte de tarifs. Une carte de tarifs est une combinaison de l’entité Tarifs et des lignes associées dans les tables Prix du rôle, Prix de la catégorie de la transaction et Éléments tarifaires.

## <a name="resource-roles"></a>Rôles des ressources

Le terme *rôle de la ressource* fait référence à un ensemble de compétences, de qualifications et de certifications qu’une personne doit avoir pour effectuer un ensemble spécifique de tâches sur un projet.

Le temps des ressources humaines est généralement estimé dans le devis selon le rôle qu’une ressource remplit sur un projet spécifique. Pour le temps de ressources humaines, PSA prend en charge les coûts et la facturation basés sur le rôle de la ressource. Le temps peut avoir le prix contenu dans n’importe quelle unité du groupe d’unités **Temps**.

Le groupe d’unités **Temps** est créé lorsque PSA est installé. Son unité par défaut est **Heure**. Vous ne pouvez pas supprimer, renommer, ou modifier les attributs du groupe d’unités **Temps** ou l’unité **Heure**. Cependant, vous pouvez ajouter d’autres unités au groupe d’unités **Temps**. Si vous essayez de supprimer le groupe d’unités **Temps** ou l’unité **Heure**, cela peut entraîner des défaillances dans la logique métier PSA.

> ![Configuration des prix par rôle.](media/basic-guide-13.png)
 
## <a name="transaction-categories-and-expense-categories"></a>Catégories de transactions et catégories de dépenses

Les voyages et autres dépenses encourus par les consultants de projet sont généralement facturés au client. PSA prend en charge la tarification des catégories de dépenses en utilisant des tarifs. Les billets d’avion, l’hôtel et la location de voiture sont des exemples de catégories de dépenses. Chaque ligne de tarif pour les dépenses spécifie la tarification d’une catégorie spécifique de dépenses. Pour la tarification des catégories de dépenses, PSA prend en charge les trois modes de tarification suivants :

- **À prix coûtant** : Le coût des dépenses est facturé au client, et aucune majoration n’est appliquée.
- **Pourcentage de majoration** : Le pourcentage sur le coût réel est facturé au client. 
- **Prix unitaire** : Le prix de facturation est défini par unité de la catégorie de dépenses. Le montant facturé au client est calculé selon le nombre d’unités de dépenses que le consultant signale. Le kilométrage utilise le mode de tarification de prix unitaire. Par exemple, la catégorie de dépenses de kilométrage peut être configurée pour 30 dollars américains (USD) par jour ou 2 USD par mile. Lorsqu’un consultant enregistre le kilométrage d’un projet, le montant à facturer est calculé selon le nombre de miles que le consultant a signalés.

> ![Configuration de la tarification pour les catégories de dépenses.](media/basic-guide-14.png)
 
## <a name="project-sales-pricing-and-overrides"></a>Tarification et remplacements de ventes du projet

Pour les devis et les contrats du projet, les tarifs du projet ont un autre modèle de remplacement de prix qu’une liste de prix de produits. Dans une ligne de devis basée sur un catalogue de produits, vous pouvez remplacer le prix des rôles et des catégories directement sur la ligne de devis, car chaque ligne de devis pointe exactement vers un article du catalogue. Toutefois, sur une ligne de devis basée sur un projet, vous ne pouvez pas remplacer le tarif des rôles et des catégories directement sur la ligne de devis. Pour prendre en charge les deux modèles distincts de remplacement, PSA a présenté une nouvelle association de tarifs, les tarifs de projet.

> [!NOTE]
> Il est recommandé d’avoir des tarifs distincts pour vos ressources de projet et vos articles de catalogue, en raison des différences de comportement entre les deux lors du remplacement de la tarification.

Chacune des entités suivantes peut contenir un ou plusieurs tarifs de ventes associés pour la tarification de projet :

- Client (compte) 
- Opportunité 
- Devis 
- Contrat du projet

L’association de ces entités avec des tarifs est indiquée par les tarifs du projet. Vous pouvez associer un ou plusieurs tarifs avec les entités de vente Client, Opportunité, Devis et Contrat du projet.

Des tarifs par défaut de projet ne sont pas automatiquement entrés sur un enregistrement client. Cependant, vous pouvez manuellement joindre des tarifs de projet à l’enregistrement de client. Toutefois, vous devez manuellement joindre des tarifs de projet uniquement si vous avez un contrat de tarification personnalisé avec le client. 

Lorsque des tarifs de projet sont attachés à une entité de ventes, PSA valide les informations suivantes :

- Les tarifs ont un contexte de **Ventes**. 
- La devise des tarifs correspond à la devise client. 

Sur un contrat de projet, PSA utilise l’ordre suivant de priorité pour définir automatiquement les tarifs associés de projet :

1. Devis
2. Opportunité
3. Client 
4. Paramètres globaux pour PSA

Lorsque des tarifs de projet sont entrés par défaut, PSA valide que la devise correspond à la devise client, et que les tarifs par défaut entrés ont un contexte de **Ventes**.

Vous pouvez associer plusieurs tarifs de projet aux entités Client, Opportunité, Devis et Contrat du projet. Cette fonctionnalité prend en charge les prix par défaut spécifiques à une date dans un contrat de projet à long terme, où vous pouvez nécessiter plusieurs tarifs pour tenir compte des mises à jour des prix qui se produisent en raison de l’inflation. Toutefois, si les tarifs que vous associez à l’entité Client, Opportunité, Devis ou Contrat du projet ont une validité de date se chevauchant, les prix par défaut peuvent être incorrects. Par conséquent, vous devez vous assurer que les tarifs de projet qui ont une validité de dates se chevauchant ne sont pas associés à ces entités.

### <a name="deal-specific-price-overrides"></a>Remplacements de prix spécifiques à une transaction

Dans PSA, vous pouvez créer des remplacements spécifiques aux transactions pour des prix sélectionnés dans les tarifs de projet entrés par défaut sur un devis ou un contrat du projet.

Par défaut, un contrat du projet est toujours une copie du tarif de ventes principal au lieu d’un lien direct vers celui-ci. Ce comportement aide à garantir que les accords tarifaires conclus avec un client dans un énoncé des travaux ne changent pas si le tarif principal est modifié.

Toutefois, dans un devis, vous pouvez utiliser un tarif principal. Par ailleurs, vous pouvez copier un tarif principal et le modifier pour créer un tarif personnalisé qui s’applique uniquement à ce devis. Pour créer un tarif spécifique à un devis, sur la page **Devis**, sélectionnez **Créer la tarification personnalisée**. Vous pouvez accéder au tarif du projet spécifique à la transaction uniquement à partir du devis. 

Lorsque vous créez un tarif personnalisé de projet, seuls les composants de projet des tarifs sont copiés. En d’autres termes, des tarifs créés comme copie du tarif existant de projet attaché au devis, et ce nouveau tarif est associé uniquement aux prix des rôles et aux prix des catégories de transactions.

> ![Affichage et configuration de la tarification personnalisée d’un contrat de projet.](media/basic-guide-15.png)
  
## <a name="tracking-costs"></a>Suivi des coûts

PSA effectue le suivi des coûts pour utiliser le temps des ressources humaines sur des projets. Il effectue également le suivi des coûts pour d’autres dépenses qui surviennent pendant le projet, tels que les dépenses en voyages.

Comme les taux de factures, les taux de coûts pour les ressources humaines sont également configurés à l’aide de tarifs. Voici les principales différences entre le comportement de la liste de prix de revient et du tarif de vente :

- Le taux de coût d’une ressource ne peut pas être remplacé sur un projet, un contrat ou un devis spécifiques. Toutefois, les taux de factures peuvent être remplacés à chaque transaction si des modifications spécifiques à la nature de la transaction sont apportées. 

- L’ordre suivant permet de résoudre une liste de prix de revient :

    1. La liste de prix de revient qui est jointe à l’unité d’organisation.
    2. La liste de prix de revient qui est jointe aux paramètres Project Service. Étant donné que les listes de prix de revient dans de nombreux différentes devises peuvent être attachées aux paramètres Project Service, PSA crée une correspondance de devise entre la devise de l’unité d’organisation contractuelle du projet, du contrat ou du devis, et la devise de la liste de prix de revient.
    3. Pour les dépenses, les modes de tarification À prix coûtant et Majoration du coût ne s’appliquent pas aux listes de prix de revient. Même si ces modes de tarification sont utilisés sur la liste de prix de revient pour configurer les coûts des catégories de transactions, le système les ignore, et aucun prix de revient par défaut n′est entré.


[!INCLUDE[footer-include](../includes/footer-banner.md)]