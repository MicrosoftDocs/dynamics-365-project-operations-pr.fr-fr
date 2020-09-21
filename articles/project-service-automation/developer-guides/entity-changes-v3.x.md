---
title: Modifications d'entité, de contrôle et d'interface utilisateur (Project Service Automation 3.x)
description: Cette rubrique décrit les modifications de solution pour Microsoft Dynamics Project Service Automation 3.x.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9f8828c6-541c-4945-8c99-5785118e191d
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 56aa0bb8272b886bcd15dadd0f74fff3bc43e26b
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2020
ms.locfileid: "3168081"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Modifications d'entité, de contrôle et d'interface utilisateur (Project Service Automation 3.x)
Avec la version Microsoft Dynamics Project Service Automation (PSA) 3.x, de nombreuses modifications ont été apportées aux entités, aux contrôles, aux vues et à l'interface utilisateur. Cette rubrique fournit des informations sur ces modifications importantes.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Relations parent-enfant pour les entités document vente, ligne de document vente, détails de la ligne de document de vente
Dans les versions de Dynamics 365 Project Service Automation (PSA) publiées avant la version 3.0, certaines relations entre les entités de documents vente, lignes de document de vente, et détails de la ligne de document vente ont été mises en œuvre via les champs de type chaîne qui maintiendraient une représentation de chaîne du GUID de l'entité associée. C'était en raison des limitations de la plateforme qui nécessitaient un code personnalisé important côté serveur et client de la solution pour que ces relations fonctionnement similairement aux relations d'entités Dynamics CRM standard et faire agir les champs de la chaîne comme des champs de recherche.

PSA 3.0 a été mise à jour pour tirer parti des nouvelles relations d'entités entre les entités document vente et ligne de document de vente.

Étant donné que les champs de recherche peuvent à présent être utilisés pour désigner des références aux entités, les champs contenant la valeur de chaîne du GUID de l'entité associée dans les versions précédentes ne sont plus nécessaires et par conséquent ont été rendus obsolètes. Le code personnalisé côté client et serveur qui gère les relations définies par des champs de chaîne hérités a été également rendu obsolète.

### <a name="entity-schema-changes"></a>Modifications du schéma d'entité
Le tableau suivant présente une liste un à un des champs de chaîne obsolètes et des nouveaux champs de recherche pour les entités. 

 Entité |   Champ obsolète (Chaîne) | Nouveau champ (Recherche)
--- | --- | ---
invoicedetail (Ligne de facture) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (Chiffres réels) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (Planification de facture de la ligne de contrat de projet) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (Jalon de la ligne de contrat du projet) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (Fait) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (Détails de la ligne de facture) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (Ligne de journal) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (Catégorie de ressource de la ligne de contrat du projet) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (Détails de la ligne de contrat du projet) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (Catégorie de transaction de la ligne de contrat) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (Classification de transactions de la ligne de contrat du projet) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (Planification de facture de la ligne de devis) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (Catégorie de ressource de ligne de devis) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (Jalon de la ligne de devis) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (Détails de la ligne de devis) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (Catégorie de transaction de la ligne de devis) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (Classification de la transaction de ligne de devis) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (Ligne de commande) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Vues et contrôles personnalisés obsolètes
Les vues et contrôles personnalisés suivants, et leurs artefacts associés, ont été rendus obsolètes.

- Vue Exigibilité.
- Contrôles de grille personnalisés pour afficher les détails de la ligne de devis sur la page **Informations sur le projet** pour la ligne de devis.
- Contrôles de grille personnalisés pour afficher les détails de la ligne de contrat du projet sur la page **Informations sur le projet** pour la ligne de commande client.

> [!NOTE]
> Pour obtenir la liste complète des ressources déconseillées, consultez [Ressources web déconseillées dans Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Module d'application d'interface client unifiée
Avec le lancement des modules d'applications d'interface client unifiée (ICU), les entrées du plan de site PSA ont été supprimées du système.  
La fonctionnalité associée au basculement entre les formulaires pour Opportunité, Devis, Commande, Facture a été rendue obsolète, car elle n'est plus nécessaire car le module des applications de l'ICU inclut uniquement des versions PSA des formulaires.  

Les ressources web suivantes ont été rendues obsolètes :

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Pour obtenir la liste complète des ressources obsolètes, consultez [Ressources web obsolètes dans Project Service Automation v3.x](../developer-guides/web-resources-deprecated-v3.x.md).


