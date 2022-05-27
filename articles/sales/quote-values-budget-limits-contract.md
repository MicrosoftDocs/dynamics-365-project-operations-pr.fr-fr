---
title: Paramètres de devis de projet
description: Cette rubrique fournit des renseignements sur les informations et les paramètres qui s’appliquent aux devis de projet et qui ont un impact.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c5870c75d5337b951a453000369baf9f6e81a1da
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8575163"
---
# <a name="header-details-for-project-based-quotes"></a>Détails d’en-tête pour les devis basés sur des projets

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_


Cet article explique les informations qui s’appliquent à un devis de projet. Cela inclut les paramètres qui affectent toutes les lignes de devis et les informations sur le devis qui sont résumées sur tous les éléments de ligne pour piloter les indicateurs de performance clés du devis de projet.

Le tableau suivant répertorie les champs d’informations récapitulatives d’un devis de projet qui sont propres à Dynamics 365 Project Operations ou qui ont des changements importants dans le comportement des devis de Dynamics 365 Sales.

| **Champ** | **Emplacement** | **Description** | **Impact en aval** |
| --- | --- | --- | --- |
| Type | Onglet Résumé (masqué) | Ce champ de groupe d’options comporte les options suivantes :</br>- Basé sur le travail (disponible uniquement lorsque Project Operations est installé)</br>- Basé sur l’article (disponible uniquement lorsque Project Operations et Sales sont installés)</br>- Service basé sur la maintenance (disponible lorsque Dynamics 365 Field Service est installé) | Lorsque vous utilisez l’application Project Operations, la valeur de ce champ est automatiquement définie sur **Basé sur le travail**. Cela classe le devis comme un devis basé sur un projet. Un devis doit être basé sur un projet pour activer toutes les extensions et fonctionnalités spécifiques au projet. |
| Société propriétaire | Synthèse | L’entité juridique qui comptabilisera les coûts et les revenus générés par ce projet ou les projets associés à ce devis. Lorsqu’un devis est créé à partir d’une Opportunité, ce champ est copié à partir du champ correspondant sur l’Opportunité. | La société propriétaire équivaut au concept d’entité juridique dans le module **Gestion de projet et comptabilité** de Project Operations. Tous les coûts et revenus accumulés par ce projet seront comptabilisés dans la comptabilité de la société propriétaire. |
| Prospect | Onglet Résumé | Référence à la société ou à l’enregistrement de compte du client. Un client valide à référencer sur le devis du projet doit être configuré en tant que client dans la société propriétaire du devis. La société propriétaire affiche la liste des entités juridiques qui sont configurées dans le module **Gestion de projet et comptabilité** de Project Operations. Lorsqu’un devis est créé à partir d’une opportunité, ce champ est copié à partir du champ correspondant sur l’opportunité. | La devise du devis de projet est définie par défaut en fonction de la devise du client. Elle ne peut toutefois pas être modifiée avant le devis enregistré. |
| Gestionnaire de comptes | Onglet Résumé | Nom du Gestionnaire de compte de cette transaction. Lorsqu’un devis est créé à partir d’une opportunité, ce champ est copié à partir du champ correspondant sur l’opportunité. | Le gestionnaire de compte est responsable de la gestion de la relation avec le client jusqu’à la réalisation de ce projet. En fonction de l’enregistrement de ressource réservable lié au gestionnaire du compte, l’unité contractuelle utilise par défaut le devis du projet.|
| Unité contractuelle | Onglet Résumé | Unité organisationnelle responsable de la livraison du ou des projets associés à ce devis. Lorsqu’un devis est créé à partir d’une opportunité, ce champ est copié à partir du champ correspondant sur l’opportunité. | L’unité contractuelle est la division de l’entreprise qui exécutera les projets après la conclusion de la transaction. Chaque unité contractuelle dispose d’une devise, et cette devise est utilisée pour déclarer les coûts estimés et réels engagés pendant l’exécution du projet. |
| Tarif du produit | Onglet Résumé | Il s’agit du tarif utilisé pour les prix par défaut sur les lignes de devis basées sur le produit. La liste des options de ce champ affiche une liste de tarifs où la devise du tarif correspond à la devise du devis. Lorsqu’un devis est créé à partir d’une opportunité, ce champ est copié à partir du champ correspondant sur l’opportunité. Ce champ sur l’opportunité est défini par défaut à partir de l’enregistrement de compte mais peut être modifié. | Lorsqu’un devis est conclu, la valeur du champ est copiée dans le contrat de projet créé. |
| Devise | Onglet Résumé | Cela indique la devise qui sera utilisée pour déclarer la valeur de cette transaction. C’est également la devise dans laquelle le client sera facturé si la transaction est conclue. Lorsqu’un devis est créé à partir d’une opportunité, ce champ est copié à partir du champ correspondant sur l’opportunité. Ce champ sur l’opportunité est défini par défaut à partir de l’enregistrement de compte mais peut être modifié par l’utilisateur.  | Une fois un devis enregistré, ce champ n’est plus modifiable. Ceci est utilisé pour attribuer des tarifs de produits et de projets par défaut sur le devis. La devise présente sur le devis est utilisée pour correspondre à la devise du tarif. |
| Limite à ne pas dépasser | Onglet Résumé | Cela indique le plafond négocié sur la valeur finale que le client accepte pour cette transaction. | Ce plafond est évalué lors de l’exécution et s’applique à tous les éléments de ligne et projets associés à cet accord. |
| Date de livraison demandée | Onglet Résumé | Lorsqu’un devis est créé à partir d’une opportunité, ce champ est copié à partir du champ correspondant sur l’opportunité. | Cette date est utilisée comme date de fin pour la génération des planifications de facture. |

Vous trouverez ci-dessous les onglets et les indicateurs de performance clés disponibles sur un devis de projet qui sont propres à Project Operations ou qui présentent des changements de comportement importants à partir des devis de vente :

| **Champ** | **Emplacement** | **Description** |
| --- | --- | --- |
| Analyse de la rentabilité | Onglet sur le devis | L’onglet montre les métriques suivantes :</br>- Coût facturable total</br></br>- Coût non facturable total</br>- Revenu total</br>- Revenu total (de base)</br>- Marge brute</br>- Marge brute ajustée|
| Comparaison aux exigences client | Onglet sur le devis | Cet onglet montre les métriques suivantes :</br>- Estimation de l’achèvement</br>- Fin demandée</br>- Budget client</br>- Valeur du devis |
| Analyse du devis | Onglet sur le devis | Cet onglet résume les principaux indicateurs de performance clés suivants pour un devis de projet</br>- Comparaison avec les attentes des clients en matière de budget et de planification</br>- Marge brute</br>- Marge brute ajustée |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
