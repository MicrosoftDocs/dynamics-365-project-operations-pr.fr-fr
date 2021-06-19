---
title: Unités d’organisation
description: Cette rubrique fournit des informations sur les unités d’organisation dans Dynamics 365 Project Service Automation.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/04/2019
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
ms.openlocfilehash: 3be18adfa1d346bdabae7e89375ca2c5a2dbda95
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009613"
---
# <a name="organizational-units"></a>Unités d’organisation 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Dynamics 365 Project Service Automation, une unité d’organisation est un groupe ou une division distincts dans une société de services professionnels qui utilise des ressources facturables avec des taux de coûts.

Pour les entreprises de services professionnels qui utilisent des ressources techniques dans différents domaines de pratiques ou branches d’activité, le coût pour remplir un rôle dans un domaine de pratique ou branche d’activité peut différer du coût pour remplir un rôle dans un autre domaine de pratique ou branche d’activité. Le concept d’unités d’organisation permet dans ce scénario de fournir un moyen de regrouper un ensemble de rôles facturables dans une division d’une société comportant une structure de coût distincte pour ces rôles.

## <a name="key-attributes-and-associations-of-organizational-units"></a>Attributs clés et associations d’unités d’organisation

Dans PSA, une unité d’organisation dans PSA a une devise spécifique et des listes de prix de revient spécifiques.

La devise d’une unité d’organisation est la devise principale qui sert à suivre les coûts.

Une ou plusieurs listes de prix de revient peuvent être liées à chaque unité d’organisation. PSA impose les restrictions suivantes aux tarifs qui peuvent être joints à une unité d’organisation :

- Les tarifs doivent figurer dans la devise de l’unité d’organisation
- Les tarifs doivent être des listes de prix de revient

En outre, il existe un attribut pour l’unité d’organisation sur l’entité Ressource. Chaque ressource peut être attribuée à une unité d’organisation.

## <a name="roles-of-organizational-units"></a>Rôles des unités d’organisation

L’unité d’organisation joue deux rôles dans PSA :

- **Unité contractuelle** – Unité d’organisation qui représente le groupe de sociétés ou la division principalement responsables de remporter la vente et de gérer la prestation du travail et des services au client. L’unité contractuelle est identifiée par le champ **Unité contractuelle** dans la section d’en-tête des pages **Opportunité**, **Devis**, **Contrat du projet** et **Projet**.
- **Unité d’allocation des ressources** – Unité d’organisation à laquelle une ressource appartient ou est attribuée. Cette unité d’organisation peut offrir ses ressources à certains rôles sur les énoncés des travaux et les projets qui appartiennent à l’unité contractuelle.

> ![Unités contractuelles et unités d’allocation des ressources](media/advanced-1.png)

## <a name="organizational-unit-faqs"></a>FAQ de l’unité d’organisation

Voici certaines des questions les plus fréquemment posées concernant les unités d’organisation.

### <a name="how-is-the-organizational-unit-entity-in-psa-related-to-the-organization-entity-that-already-exists-in-dynamics-365"></a>Comment l’entité Unité d’organisation dans PSA est-elle associée à l’entité Organisation qui existe déjà dans Dynamics 365 ?

L’entité Organisation dans Microsoft Dynamics 365 représente le nom d’une instance de Dynamics 365 globale. Ce nom est généralement celui de l’entreprise globale.

L’entité Unité d’organisation représente un groupe ou une division de l’entreprise globale. Ce groupe ou division possède un ensemble de rôles et une liste de prix de revient pour ces rôles, et ces rôles et tarifs diffèrent des rôles et tarifs d’autres groupes ou divisions de l’entreprise.

Lorsque PSA est installé, une unité d’organisation par défaut est créée selon l’organisation. Toutes les ressources existantes sont attribuées à l’unité d’organisation par défaut. Si des nouveaux utilisateurs ou ressources Active Directory sont importés dans Dynamics 365, le processus d’importation d’utilisateurs les affecte à l’unité d’organisation par défaut dans PSA.
 
### <a name="how-does-the-organizational-unit-entity-differ-from-the-business-unit-entity"></a>Comment l’entité de l’unité d’organisation diffère-t-elle de l’entité de division ?

Dans Dynamics 365, l’entité Division est un élément de sécurité. L’association d’un utilisateur avec une division détermine les entités et les enregistrements d’entité auxquels l’utilisateur a accès. Elle détermine également les autorisations (Créer, Lire, Écrire, Supprimer, Ajouter, Ajouter à, Attribuer ou Partager) que l’utilisateur prend pour ces enregistrements d’entités.

L’entité Unité d’organisation représente un groupe ou une division de société avec des taux de coût distincts pour les employés qui lui sont attribués. L’association d’une ressource à une unité d’organisation détermine le coût de la ressource dans un engagement dans un projet.

Lorsque vous implémentez Dynamics 365, optimisez l’autorisation de sécurité de la hiérarchie des divisions et l’attribution des utilisateurs à des divisions. Attribuez tous les utilisateurs qui doivent accéder généralement au même jeu d’enregistrement à la même division. L’unité d’organisation n’a aucun impact sur les autorisations ou l’accès de sécurité.

#### <a name="example-of-organizational-units-and-business-units"></a>Exemple d’unités d’organisation et de divisions

Contoso, Ltd a une pratique prospère en matière de technologie Microsoft. Jérôme et Bernadette sont tous les deux développeurs C\#, mais Bernadette est aux États-Unis, alors que Jérôme est en Inde. La plupart des engagements à un projet nécessitent des ressources Contoso Inde et Contoso US, et Jérôme et Bernadette ont besoin du même niveau d’accès de sécurité aux projets dans ce domaine de pratique. Toutefois, le coût des développeurs Contoso Inde diffère considérablement du coût des développeurs Contoso US.

Voici une manière optimale de concevoir ce scénario à l’aide de Dynamics 365 et PSA.

1. Créez les pratiques technologiques Microsoft en tant que division, puis associez-y Jérôme et Bernadette. De cette façon, vous garantissant que les deux employés aient le même niveau d’accès de sécurité à tous les projets dans ce domaine de pratique. Tous les deux pourront vérifier la progression et indiquer le temps passé, les dépenses et les mises à jour de tâche. 
2. Créez deux unités d’organisation afin de garantir que le coût du projet est correctement reflété. 
3. Associez Bernadette à Contoso US et associez Jérôme à Contoso Inde.
4. Attribuez les listes de prix de revient appropriées aux deux unités d’organisation. De cette façon, vous garantissez que les coûts enregistrés sur le projet pour Jérôme et Bernadette reflètent exactement la différence de coûts entre Contoso US et Contoso Inde.

### <a name="are-organizational-units-related-to-sales-territories-in-dynamics-365"></a>Les unités d’organisation sont-elles liées aux secteurs de vente dans Dynamics 365 ?

Il n’existe ni association, ni relation, entre les secteurs de vente et les unités d’organisation. Un secteur de vente est généralement une zone géographique où les ventes se produisent. Des tarifs de vente peuvent être associées à chaque secteur de vente.

Une unité d’organisation est un groupe ou une division interne à la société qui suit les coûts pour une série de rôles qu’ils vendent à d’autres divisions ou à des clients externes.

#### <a name="example-of-organizational-units-and-sales-territories"></a>Exemple d’unités d’organisation et de secteurs de vente

Contoso, Ltd. dispose de deux centres de développement : Contoso US et Contoso Inde. Les coûts des ressources diffèrent considérablement entre ces deux centres de développement.

Contoso vend ses services informatiques sur de nombreux marchés internationaux, par exemple en Amérique latine, en Amérique du Nord, en Asie Pacifique, en Europe de l’ouest et au Moyen-Orient. Les taux de factures pour les mêmes rôles de projet peuvent varier considérablement selon les marchés.

Contoso US et Contoso Inde doivent être configurés en tant qu’unités d’organisation, et chaque unité d’organisation doit avoir ses propres listes de prix de revient. L’Asie Pacifique, l’Amérique latine, l’Amérique du Nord, l’Europe de l’ouest et le Moyen-Orient doivent être configurés en tant que secteurs de vente, et chaque secteur de vente doit avoir ses propres tarifs de vente.

### <a name="why-is-there-a-restriction-on-the-association-of-price-lists-with-organizational-units"></a>Pourquoi existe-t-il une restriction sur l’association des tarifs aux unités d’organisation ? 

La tarification des ventes est généralement unique aux zones géographiques ou marchés où les services sont vendus. Les divisions internes d’une société n’ont généralement pas leur propre tarification des ventes pour le même type de services. Toutefois, les divisions internes ont un coût des marchandises vendues différent, selon les compétences de la personne qu’ils emploient et les conditions de travail de la région où elle travaille. Étant donné que les unités d’organisation sont modélisées en tant que divisions internes d’une société, elles peuvent avoir des listes de prix de revient uniques.

### <a name="why-cant-we-associate-sales-price-lists-to-organizational-units"></a>Pourquoi ne pouvons-nous pas associer des listes de prix de vente aux unités d’organisation ?

Dans PSA, les tarifs de ventes peuvent être associés à des clients et à des secteurs de vente. Les entités transactionnelles comme Opportunité, Devis, Contrat du projet et Projet utilisent des tarifs de entes joints au compte client ou au secteur de vente pour définir des taux de factures et des revenus potentiels sur l’engagement au projet.

Des listes de prix de revient sont associées aux unités d’organisation. Les entités transactionnelles comme Opportunité, Devis, Contrat du projet et Projet utilisent des listes de coûts de revient jointes à l’unité contractuelle pour déterminer les coûts d’un engagement à un projet.

### <a name="are-organizational-units-hierarchical-in-psa"></a>Les unités d’organisation sont-elles hiérarchiques dans PSA ?

Non. Dans la version actuelle de PSA, les unités d’organisation ne sont pas hiérarchiques. Cela signifie que vous ne pouvez pas :

- Configurer un modèle pour des prix de revient par défaut qui remontent dans la hiérarchie. 
- Générer de rapport sur les reports de produit ou de coût à différents niveaux de la hiérarchie de l’unité d’organisation.

### <a name="were-a-big-multinational-firm-with-a-complex-multilevel-hierarchy-of-cost-centers-divisions-and-billing-offices-how-can-we-make-the-best-use-of-the-organizational-unit-concept-in-this-version-of-the-project-service-app"></a>Nous sommes une grande multinationale avec une hiérarchie complexe de centres de coût, de divisions et de bureaux de facturation à plusieurs niveau. Comment optimiser l’utilisation du concept d’unité d’organisation dans cette version de l’application Project Service ?

Lorsque vous disposez d’une hiérarchie complexe de centres de coût, divisions, bureaux de facturation, etc., configurer les nœuds terminaux de cette hiérarchie en tant qu’unités d’organisation différentes.
L’exemple suivant affiche une hiérarchie typique :

**ContosoInde**

  - Pratique SAP 

    - Consultants techniques 
    - Consultants fonctionnels 
    
  - Pratique technologique Microsoft 

    - Consultants techniques
    - Consultants fonctionnels 
    
**Contoso US**

 - Pratique SAP 

    - Consultants techniques 
    - Consultants fonctionnels 
    
 - Pratique technologique Microsoft 

    - Consultants techniques 
    - Consultants opérationnels 
 
Si votre hiérarchie est similaire, vous devez la configurer en tant que liste plate, comme indiqué ci-dessous :
- Contoso Inde - Pratique SAP - Consultants techniques 
- Contoso Inde - Pratique SAP - Consultants opérationnels       
- Contoso Inde - Pratique Microsoft Technology - Consultants opérationnels 
- Contoso Inde - Pratique Microsoft Technology - Consultants opérationnels 
- Contoso US - Pratique SAP - Consultants techniques  
- Contoso US - Pratique SAP - Consultants opérationnels  
- Contoso US - Pratique Microsoft Technology - Consultants techniques 
- Contoso US - Pratique Microsoft Technology - Consultants opérationnels

### <a name="were-a-small-professional-services-company-that-operates-as-only-one-division-how-can-we-best-use-the-organizational-unit-concept-in-the-current-version-of-psa"></a>Nous sommes une petite entreprise de services professionnels qui fonctionne comme une seule division. Comment optimiser l’utilisation du concept de l’unité d’organisation dans la version actuelle de PSA ?

Si votre entreprise fonctionne comme une unité unique qui contient la liste des prix de revient, vous ne devez configurer aucune unité d’organisation. Pendant l’installation de PSA, Dynamics 365 crée une unité d’organisation par défaut ayant le même nom que l’organisation. Par défaut, tous les utilisateurs sont attribuées à cette unité d’organisation. Lorsque le système requiert qu’une unité d’organisation soit sélectionnée, cette unité d’organisation est activée par défaut.

### <a name="when-a-project-is-created-from-a-quote-or-project-contract-line-the-default-contracting-unit-comes-from-the-quote-or-project-contract-if-a-project-is-created-before-sales-entities-such-as-quote-or-project-contract-what-is-the-default-contracting-unit"></a>Lorsqu’un projet est créé à partir d’un devis ou d’une ligne de contrat du projet, l’unité contractuelle par défaut provient du devis ou du contrat du projet. Si un projet est créé avant les entités de vente, comme le devis ou le contrat du projet, quelle est l’unité contractuelle par défaut ?

Lorsqu’un projet est créé seul, l’unité contractuelle par défaut du projet dépend de l’utilisateur qui le crée. Cet utilisateur est également le responsable de projet par défaut. Si le projet est mappé à une entité de vente, par exemple un devis ou un contrat du projet, l’unité contractuelle du projet dépend plutôt de l’entité de vente. Dans ce cas, des estimations de projet peuvent être recalculées, car la liste de prix de revient est utilisée pour calculer les modifications d’estimation du coût si l’unité contractuelle est modifiée. La liste de prix de vente est utilisée pour calculer les estimations de ventes qui seront automatiquement modifiées pour qu’elles soient synchronisées sur les tarifs du projet sur le devis.

Les champs **Unité contractuelle** et **Devise** du projet sont verrouillés pour modification, car ils doivent être synchronisés sur les valeurs de l’entité commerciale (devis ou contrat du projet) auxquelles le projet est mappé.


[!INCLUDE[footer-include](../includes/footer-banner.md)]