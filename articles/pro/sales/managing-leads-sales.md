---
title: Gérer les prospects– Simplifié
description: Cette rubrique fournit des informations sur la gestion des prospects selon le projet (pro).
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e789295d4b1f5a53fcf179a2998f60d35f48f99
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513786"
---
# <a name="manage-leads---lite"></a>Gérer les prospects– Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Les prospects selon le projet peuvent être gérés et qualifiés dans Project Operations. Le processus de gestion des prospects comprend la création de prospects basés sur le travail et la qualification de ces prospects. 

## <a name="list-of-project-sales-leads"></a>Liste des prospects selon le projet

Dans la section **Ventes**, dans le volet de navigation de gauche, ouvrez la page de liste **Prospects** pour afficher une liste de tous les enregistrements de prospects dans le système. Les prospects de la liste sont basés sur le travail et d'autres types de prospects qui peuvent être créés si vous disposez également des applications Dynamics 365 Sales ou Dynamics 365 Field Service.

Vous pouvez créer un vue filtrée pour afficher uniquement les prospects selon un projet en créant un filtre sur la valeur **Type**. Par exemple, vous pouvez choisir d’afficher uniquement les prospects selon le travail.

## <a name="creating-a-new-lead-for-a-project-based-deal"></a>Création d’un prospect pour une transaction basée sur un projet

Lorsqu’un prospect selon un projet est qualifié, une opportunité et un compte sont créés. Une opportunité selon un projet est le point de départ des activités de poursuite des ventes dans la phase Opportunité. Les opportunités selon les projets ont des capacités uniques qui sont nécessaires pour vendre le travail de projet. Ces capacités incluent :

- Modes de facturation pour le temps et les matières et à prix fixes
- Tarifs en vigueur à plusieurs dates pour les ressources humaines, les dépenses et le matériel engagés sur les projets.

Pour qu’un prospect qualifié crée automatiquement une opportunité, définissez l’attribut **Type** sur **Basé sur le travail** lorsque vous créez le prospect. Si vous choisissez un type différent, le prospect ne créera pas d’opportunité selon un projet lorsqu’il sera qualifié. Si l’opportunité selon le projet n’est pas créée, les fonctionnalités spécifiques au projet ne seront pas disponibles dans les processus de vente en aval.

Le tableau suivant comprend des informations de champ importantes pour un prospect et les implications en aval de ces champs.

| **Champ** | **Emplacement** | **Description** | **Impact en aval** |
| --- | --- | --- | --- |
| Rubrique | Onglet Général | Ce champ de texte doit contenir une brève description de la transaction. | Le sujet du prospect sera par défaut le sujet de l’Opportunité et le nom du Devis et du Contrat de projet. |
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

Pour plus d’informations sur la qualification des prospects, voir [Qualifier ou convertir des prospects](https://docs.microsoft.com/dynamics365/sales-enterprise/qualify-lead-convert-opportunity-sales).

## <a name="business-process-flow-for-project-based-deals"></a>Flux des processus d’entreprise pour les offres basées sur des projets

Les flux des processus d’entreprise suivants sont pris en charge pour les transactions basées sur des projets dans Project Operations :

- Processus d’entreprise prospect-opportunité
- Processus de vente Opportunité

Le processus d’entreprise prospect-opportunité prend en charge les phases suivantes :

| Nom de la phase | Entité mappée | Fonctionnalité |
| --- | --- | --- |
| Qualifier | Prospect | Qualifiez le prospect pour créer un compte, un contact et une opportunité. |
| Développer | Opportunité | Développez l’opportunité pour ajouter plus d’informations sur le travail impliqué, les principales parties prenantes et la concurrence. |
| Proposer | Opportunité | Développez la proposition et obtenez l’approbation de l’équipe de vérification interne. |
| Fermer | Opportunité | Concluez l’opportunité pour fermer la transaction. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]