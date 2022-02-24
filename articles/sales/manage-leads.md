---
title: Gérer les prospects
description: Cette rubrique fournit des informations sur la gestion des prospects selon le projet.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 31613936d48f785eeba4ec7c066761c8f69924cf
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947876"
---
# <a name="manage-leads"></a>Gérer les prospects

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les prospects selon le projet peuvent être gérés et qualifiés dans Project Operations. Le processus de gestion des prospects comprend la création de prospects basés sur le travail et la qualification de ces prospects. 

## <a name="project-sales-leads"></a>Prospects selon le projet

Dans la section **Ventes**, dans le volet de navigation de gauche, ouvrez la page de liste **Prospects** pour afficher une liste de tous les enregistrements de prospects dans le système. La liste des prospects affichée est basée sur le travail et d’autres types de prospects qui peuvent être créés si vous disposez également de Dynamics 365 Sales ou des applications Dynamics 365 Field Service.

Vous pouvez créer un vue filtrée pour afficher uniquement les prospects selon un projet en créant un filtre sur la valeur **Type**. Par exemple, vous pouvez choisir d’afficher uniquement les prospects selon le travail.

## <a name="create-a-new-lead-for-a-project-based-deal"></a>Créer un prospect pour une transaction basée sur un projet

Lorsqu’un prospect selon un projet est qualifié, une opportunité et un compte sont créés. Une opportunité selon un projet est le point de départ des activités de poursuite des ventes dans la phase Opportunité. Les opportunités basées sur des projets possèdent des fonctionnalités uniques nécessaires pour vendre le travail de projet. Ces capacités incluent :

- Modes de facturation pour le temps et les matières et à prix fixes
- Tarifs en vigueur à plusieurs dates pour les ressources humaines, les dépenses et le matériel engagés sur les projets

Pour qu’un prospect qualifié crée automatiquement une opportunité, définissez l’attribut **Type** sur **Basé sur le travail** lorsque vous créez le prospect. Si vous choisissez un type différent, le prospect ne créera pas d’opportunité selon un projet lorsqu’il sera qualifié. Si l’opportunité selon le projet n’est pas créée, les fonctionnalités spécifiques au projet ne seront pas disponibles dans les processus de vente en aval.

Le tableau suivant comprend des informations de champ importantes pour un prospect et les implications en aval de ces champs.
 
| **Champ** | **Emplacement** | **Description** | **Impact en aval** |
| --- | --- | --- | --- |
| Rubrique | Onglet Général | Ce champ de texte doit contenir une brève description de la transaction. | Le sujet du prospect sera par défaut le sujet de l’opportunité et le nom du devis et du contrat de projet. |
| Type | Onglet Général | Ce champ de groupe d’options comporte les options suivantes :</br>- Basé sur le travail (disponible uniquement lorsque Project Operations est installé)</br>- Basé sur l’article (disponible uniquement lorsque Project Operations et Sales sont installés)</br>- Service basé sur la maintenance (disponible lorsque Field Service est installé) | Lorsque la valeur de ce champ est définie sur **Basé sur le travail** sur le prospect, celui-ci est qualifié pour créer une opportunité basée sur un projet. Une opportunité basée sur un projet est requise pour activer toutes les extensions et fonctionnalités spécifiques au projet dans le processus de vente en aval pour cette transaction. |
| Prénom | Onglet Général | Prénom du contact du prospect | Lorsque le prospect est qualifié, un compte, un contact et une opportunité sont créés. Le prénom du contact est la valeur définie ici. |
| Nom de famille | Onglet Général | Nom du contact du prospect | Lorsque le prospect est qualifié, un compte, un contact et une opportunité sont créés. Le nom du contact est la valeur définie ici. |
| Société | Onglet Général | Nom de la société du client prospect | Lorsque le prospect est qualifié, un compte, un contact et une opportunité sont créés. Le nom du compte créé est la valeur définie ici. |
| Devise | Onglet Détails | Devise du client prospect | Lorsque le prospect est qualifié, un compte, un contact et une opportunité sont créés. La devise du compte créé est la valeur définie ici. |

## <a name="qualify-a-new-project-based-lead"></a>Qualifier un nouveau prospect selon un projet

Les prospects qui ont la valeur **Type** définie sur **Basé sur le travail** sont appelés prospects selon des projets. Lorsqu’un prospect basé sur un projet est qualifié, les éléments suivants sont créés :

- Un compte qui utilise le champ **Société** du prospect.
- Un enregistrement de contact associé au compte en fonction des valeurs des champs **Prénom** et **Nom** sur le prospect.
- Une opportunité basée sur un projet qui a le champ **Type** défini sur **Basé sur le travail**.

Pour plus d’informations sur la qualification des prospects, voir [Qualifier ou convertir des prospects](/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="lead-qualification-and-legal-entity-information"></a>Qualification du prospect et informations sur l’entité légale 

Lorsque vous exécutez Project Operations en utilisant le mode de déploiement, Project Operations pour les scénarios basés sur les ressources/non stockés, chaque client et opportunité devra disposer d’un champ **Entreprise propriétaire** défini. La société propriétaire est une entité juridique de votre organisation qui est propriétaire de la livraison du projet. Chaque client, ou compte avec le type de relation de client, doit avoir la valeur de champ **Entreprise propriétaire** définie sur l’entité juridique qui conclut un contrat et négocie avec ce client. Un client ne peut se trouver que dans une seule entité juridique.

Lorsqu’un prospect est qualifié, les enregistrements de client et d’opportunité créés ont le champ **Entreprise propriétaire** défini sur la société de l’enregistrement de ressource réservable de l’utilisateur actuel.

Si l’enregistrement de ressources réservables de l’utilisateur actuel est vide, la valeur du champ **Entreprise propriétaire** sur l’enregistrement utilisateur est utilisée par défaut sur le client et les enregistrements d’opportunité.

## <a name="business-process-flow-for-project-based-deals"></a>Flux des processus d’entreprise pour les offres basées sur des projets

Les flux des processus d’entreprise suivants sont pris en charge pour les transactions basées sur des projets dans Project Operations :

- Processus d’entreprise prospect-opportunité
- Processus de vente Opportunité

Le processus d’entreprise prospect-opportunité prend en charge les phases suivantes :

| Nom de la phase | Entité mappée | Fonctionnalité |
| --- | --- | --- |
| Qualifier | Prospect | Qualifiez le prospect pour créer un compte, un contact et une opportunité. |
| Développer | Opportunité | Développer l’opportunité pour ajouter plus d’informations concernant le travail impliqué, les principales parties prenantes et la concurrence. |
| Proposer | Opportunité | Développez la proposition et obtenez l’approbation de l’équipe de vérification interne. |
| Fermer | Opportunité | Concluez l’opportunité pour fermer la transaction. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]