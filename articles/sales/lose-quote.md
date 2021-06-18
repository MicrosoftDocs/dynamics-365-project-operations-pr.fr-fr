---
title: Copier les devis selon les projets
description: Cette rubrique offre des informations sur la copie des devis selon les projets dans Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e9009391d33c5dd5988ae65e13ca1ca1ec398bc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999083"
---
# <a name="copy-project-based-quotes"></a>Copier les devis selon les projets

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez facilement créer un devis de projet en copiant un existant. 

- Pour copier un devis de projet, sur la page de liste **Devis de projets** ou la page des détails **Devis de projet**, sélectionnez le devis de projet à copier, puis sélectionnez **Copier**.

Cela ouvrira une page de dialogue où vous pourrez entrer les paramètres de la copie. Le tableau suivant répertorie les champs inclus dans la page de dialogue : Selon les valeurs que vous sélectionnez, le processus de copie peut changer.

| **Champ** | **Description** | **Impact en aval** |
| --- | --- | --- |
| Rubrique | Saisissez la rubrique, ou le nom, du devis cible. Lorsque la boîte de dialogue s’ouvre, le système le définira sur la rubrique du devis source avec **-copie** comme suffixe. | |
| Prospect | Référence à la société ou à l’enregistrement de compte du client. Lorsque la boîte de dialogue s’ouvre, le système le définira sur le compte du devis source. | Ce champ est le client principal du devis. |
| Unité contractuelle | Unité organisationnelle responsable de la livraison du ou des projets associés à cette transaction.
Lorsque la boîte de dialogue s’ouvre, le système le définira sur l’unité contractuelle du devis source. | L’unité contractuelle est la division de l’entreprise qui exécutera les projets après la conclusion de la transaction. Chaque unité contractuelle dispose d’une devise. La devise est utilisée pour déclarer les coûts estimés et réels engagés pendant l’exécution du projet. |
| Devise | Il s’agit de la devise dans laquelle la transaction est réalisée. Lorsque la boîte de dialogue s’ouvre, le système le définira sur la devise du devis source. Cela peut être modifié et si c’est le cas, le champ **Copier le prix** est toujours défini sur **Non**. En effet, les tarifs sur le devis source ne sont plus pertinentes. | La devise est utilisée par défaut pour un tarif, pour générer une estimation financière sur le devis et finalement pour facturer le client lorsque la transaction est gagnée. |
| Date de livraison demandée | Il s’agit de la date de livraison demandée par le client. | Elle est utilisée comme date de fin lors de la création de dates de facturation selon une fréquence spécifique. |
| Copier la tarification | Une valeur Oui/Non indique si la tarification du devis doit être copiée à partir du devis source. | Si **Oui** est sélectionné, le tarif du projet et les références du tarif du produit sont copiés du devis source vers le devis cible. Si **Non** est sélectionné, les tarifs sont rétablis par défaut en fonction des derniers tarifs qui ont été configurés sur les paramètres du compte ou du projet. |

Lorsque vous sélectionnez **OK** sur la page de dialogue, le système crée une copie du devis de projet en fonction des paramètres sélectionnés dans la boîte de dialogue. Le nouveau devis de projet s’ouvre. 

> [!NOTE]
> Les informations suivantes ne sont pas copiées de la source vers le devis cible :
>
> - Planifications de facture
> - Devis et clients de la ligne de devis
> - Référence du projet sur le projet – lignes de devis basées sur les informations budgétaires client
>
>Étant donné que ces informations sont très spécifiques à chaque devis, ces champs et enregistrements ne sont pas copiés. Les lignes de devis pour les projets et les produits, les estimations sur les détails de la ligne de devis et les valeurs à ne pas dépasser au niveau du devis sont copiées. Les valeurs par défaut de prix et de taux de coût dépendent de l’option **Copier la tarification** sélectionnée sur la page de dialogue **Copier les paramètres**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]