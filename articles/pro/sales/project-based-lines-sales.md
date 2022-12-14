---
title: Lignes de l’opportunité du projet
description: Cet article fournit des informations sur les lignes d’opportunité basées sur un projet. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e4f67bd9b7d51559e2942e9005b8f5f9187b1f78
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824952"
---
# <a name="project-opportunity-lines"></a>Lignes de l’opportunité du projet 

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Les lignes d’opportunités de projet ne sont disponibles que dans les opportunités selon les projets. Les enregistrements d’opportunités selon les projets ont la valeur de champ **Type** définie sur **Basé sur le travail**.

Les lignes d’opportunités de projet sont les éléments de ligne qui seront fournis au client à l’aide d’un projet. Cependant, un projet ne peut pas être lié à une lignes d’opportunités selon les projets. Les projets peuvent être liés à des éléments de ligne à partir de la phase **Devis** et ensuite, car l’opportunité est à une phase précoce du cycle de vie d’une transaction. La détermination du nombre de projets qui seront utilisés pour livrer le travail au client est une décision qui est prise plus tard dans la phase de vente. Vous pouvez utiliser la phase d’opportunité pour identifier les composants de livraison discrète pour le client. Les décisions concernant le nombre réel de projets utilisés pour fournir ces composants peuvent être repoussées jusqu’à ce que plus d’informations soient connues sur le travail lui-même.

Vous trouverez ci-dessous les champs d’une ligne d’opportunité de projet :

| **Champ** | **Location** | **Description** | **Impact en aval** |
| --- | --- | --- | --- |
| Type de produit | Onglet Général (masqué) | Vous pouvez sélectionner une des options suivantes :</br>- Service basé sur un projet (disponible uniquement lorsque Dynamics 365 Project Operations est installé)</br>- Produit (disponible uniquement lorsque Project Operations et Dynamics 365 Sales sont installés) | La valeur de ce champ est définie sur **Service basé sur des projets** lorsque vous créez la ligne d’opportunité selon un projet à partir de la grille de lignes basée sur le projet sur l’opportunité. <br> Si vous modifiez ou remplacez cette valeur, la fonctionnalité de projet ne sera pas activée sur vos éléments de ligne basés sur le projet. |
| Opportunité | Onglet Général | Ce champ est en lecture seule et fait référence à l’enregistrement d’opportunité parent auquel cet élément de ligne appartient. | Il n’y a pas d’impact en aval à partir de ce champ. |
| Nom | Onglet Général | Ce champ de texte modifiable qui peut être utilisé pour donner une courte identité à l’élément de ligne. | Cette valeur est reportée sur la ligne de devis lorsque vous créez un devis à partir de cette opportunité. |
| Budget client | Onglet Général | Ce champ de devise modifiable peut être utilisé pour suivre le montant que le client est prêt à dépenser pour cet élément de ligne. | Cette valeur est reportée sur le champ correspondant de la ligne de devis lorsque vous créez un devis à partir de cette opportunité. |
| Mode de facturation | Onglet Général | Ce champ modifiable contient les valeurs suivantes :</br>- Temps et matériel</br>- Prix fixe | Cette valeur est reportée sur le champ correspondant de la ligne de devis lorsque vous créez un devis à partir de cette opportunité. Une fois la ligne de devis créée, le champ est verrouillé et ne peut pas être modifié. Attribuez cette valeur de champ aussi précisément que possible. Si vous devez modifier la valeur de ce champ sur la ligne de devis, supprimez et recréez la ligne de devis. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
