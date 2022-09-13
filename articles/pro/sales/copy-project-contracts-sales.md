---
title: Copier les contrats de projets
description: Cet article fournit des informations sur la copie de contrat de projet dans Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8fa17bbd5738e4bc6330c728a3418a2be6828eef
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410025"
---
# <a name="copy-project-contracts"></a>Copier les contrats de projets

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Vous pouvez facilement créer de nouveaux contrats de projet en faisant des copies de contrats existants de l'une des deux manières suivantes : 

  - Dans la page de liste **Contrats de projets**, sélectionnez un contrat de projet, puis sélectionnez **Copier**.
  - Sur la page de détails **Contrat de projet**, sélectionnez **Copier**.

Une page de dialogue s’ouvre où vous pourrez sélectionner les paramètres du contrat copié. Les champs suivants sont inclus dans la page de dialogue. Selon les valeurs que vous sélectionnez dans cette page de dialogue, le processus de copie peut changer.

| **Champ** | **Description** | **Impact en aval** |
| --- | --- | --- |
| Rubrique | Entrez la rubrique du contrat cible. Lorsque la page de dialogue s’ouvre, le système définira ce champ avec le nom du contrat source et **-copy** comme suffixe. | Il n’y a pas d’impact en aval pour ce champ. |
| Client | Référence à la société ou à l’enregistrement de compte du client. Lorsque la boîte de dialogue s’ouvre, le système définira ce champ sur le compte du contrat source. | Ce champ est le client principal du contrat. |
| Unité contractuelle | Unité organisationnelle responsable de la livraison du ou des projets associés à cette transaction. Lorsque la page de dialogue s’ouvre, le système le définira sur l’unité contractuelle du contrat source. | L’unité contractuelle est la division de l’entreprise qui exécutera les projets après la conclusion de la transaction. Chaque unité contractuelle dispose d’une devise. Cette devise est utilisée pour déclarer les coûts estimés et réels engagés pendant le projet. |
| Devise | Devise dans laquelle la transaction est réalisée. Lorsque la page de dialogue s’ouvre, le système définira le champ sur la devise du contrat source. La devise peut être modifiée. Si c’est le cas, le champ **Copier la tarification** est toujours défini sur **Non**, car les tarifs sur le contrat source ne sont plus pertinents. | La devise est utilisée par défaut pour des tarifs, pour générer des estimations financières sur le contrat et pour facturer le client lorsque la transaction est gagnée. |
| Date de livraison demandée | Date de livraison demandée par le client. | Cette date est utilisée comme date de fin lors de la création de dates de facturation selon une fréquence spécifique. |
| Copier la tarification | Indique si la tarification du contrat doit être copiée à partir du contrat source. | Si le champ est défini sur **Oui**, les références des listes de prix des projets et des produits sont copiées à partir de la source vers le contrat cible. Si **Non** est sélectionné, les tarifs sont définis par défaut en fonction des derniers tarifs sur les paramètres du compte ou du projet. |

Lorsque vous sélectionnez **OK** sur la page de dialogue, le système crée une copie du contrat en fonction des paramètres sélectionnés. Le nouveau contrat s’ouvrira.

Les informations suivantes ne sont pas copiées de la **Source** vers le **Contrat cible** :

  - Planifications de facture
  - Clients du contrat et de la ligne de contrat
  - Référence de projet sur les lignes de contrat par projet
  - Informations sur le budget client

Étant donné que ces informations sont spécifiques à chaque contrat, ces champs et enregistrements ne sont pas copiés. Les lignes de contrat pour les projets et les produits, les estimations sur les détails de la ligne de contrats et les valeurs à ne pas dépasser au niveau du contrat sont copiées. Les valeurs par défaut de prix et de taux de coût dépendent de la sélection du champ **Copier la tarification** sur la page de dialogue **Copier les paramètres**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
