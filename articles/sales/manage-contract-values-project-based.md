---
title: Utiliser des lignes de contrat basées sur un projet
description: Cette rubrique fournit des informations sur les lignes de contrat basées sur un projet.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c1c935a998cba8bd42ba2f11c8310d41e72de94adac7c2cb83f4c7224127b10b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6990043"
---
# <a name="work-with-projectbased-contract-lines"></a>Utiliser des lignes de contrat basées sur un projet

Les lignes de contrat basées sur un projet dans Dynamics 365 Project Operations ont pour vocation de contenir l’estimation et les accords de facturation des composants spécifiques du travail de projet dans un engagement. La structure d’une ligne de contrat basée sur un projet est étendue pour les estimations de projet et les scénarios de facturation avec les concepts suivants :

- Mode de facturation
- Mappage des projets et des tâches
- Classes de transaction incluses
- Limite à ne pas dépasser
- Configuration de l’exigibilité
- Estimations utilisant les détails de la ligne de contrat
- Client de la ligne de contrat

Les champs suivants se trouvent dans l’onglet **Général** des lignes de contrat basées sur un projet. Ces champs aident à configurer la base de départ d’une estimation détaillée et les modalités de facturation pour un travail basé sur un projet.

| Champ | Description | Impact en aval |
| --- | --- | --- |
| **Nom** | Le nom de la ligne de contrat qui identifie le composant discret du contrat estimé. Pour un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir d’une valeur correspondante de la ligne de devis basée sur le projet. | Cette valeur de champ est copiée dans la ligne de facture du projet créée à partir de cette ligne de contrat lorsque la facture est créée. |
| **Mode de facturation** | Dans un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir du champ correspondant dans la ligne de devis. Il s’agit d’un groupe d’options qui représente les deux principaux modèles de contrats pris en charge par Project Operations :</br>- **Prix fixe**</br>- **Temps et matériel** | En fonction du mode de facturation de la ligne de contrat référencée, la transaction réelle sera traitée. Si la ligne de contrat référencée par la transaction réelle a un mode de facturation pour le temps et le matériel, un enregistrement des coûts et un enregistrement réel des ventes non facturées sont créés. Si la ligne de contrat référencée par la transaction réelle a un mode de facturation à prix fixe, seul un coût réel est créé. |
| **Project** | Utilisez ce champ pour identifier le projet qui sera utilisé pour livrer le travail sur cet engagement. | La valeur de ce champ est utilisée conjointement avec les champs **Tâches incluses** et **Classes de transaction incluses** pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Inclure le temps** | Un marqueur indique si les transactions de temps ou les coûts de main-d’œuvre du projet sélectionné sont inclus sur cette ligne de contrat. La valeur **Non** indique que les transactions de temps ou les coûts de main-d’œuvre ne seront pas inclus dans cette ligne de contrat. La valeur **Oui** indique qu’ils le seront. | Cette valeur de champ est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Inclure la dépense** | Un marqueur indique si les dépenses du projet sélectionné seront incluses sur cette ligne de contrat. La valeur **Non** indique que les dépenses ne seront pas incluses dans cette ligne de contrat. La valeur **Oui** indique qu’elles le seront. | Cette valeur de champ est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Inclure les frais** | Un marqueur indique si les frais du projet sélectionné seront inclus sur cette ligne de contrat. La valeur **Non** indique que les frais ne seront pas inclus dans cette ligne de contrat. La valeur **Oui** indique qu’ils le seront. | Cette valeur de champ est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Montant contractuel** | Sur une ligne de contrat à prix fixe, il s’agit de la valeur convenue qui sera facturée au client pour tous les composants de travail associés à cette ligne de contrat. Sur une ligne de contrat de temps et de matériel, ce montant est une valeur estimée de ce qui sera facturé au client pour tous les composants de travail associés à cette ligne de contrat. Dans un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir du champ correspondant dans la ligne de devis. Lorsqu’une ligne de contrat basée sur un projet comporte des détails de ligne, ce champ est verrouillé pour modification et est synthétisé à partir du montant sur les détails de la ligne de contrat. | Lorsque la ligne de contrat comporte des détails de ligne, cette valeur peut être modifiée en changeant les montants des détails de ligne. Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer le montant avant taxes sur les jalons périodiques pour la facturation. |
| **Estimation de taxe** | L’utilisateur peut modifier ce champ pour saisir le montant estimé des taxes sur la ligne du contrat. Lorsqu’une ligne de contrat basée sur un projet comporte des détails de ligne, ce champ est verrouillé pour modification et est synthétisé à partir du montant des taxes sur les détails de la ligne de contrat. | Lorsque la ligne de contrat comporte des détails de ligne, cette valeur peut être modifiée en changeant les montants des taxes des détails de ligne. Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer la taxe sur les jalons périodiques pour la facturation. |
| **Montant contractuel après taxes** | Le montant de a ligne de contrat après taxes. Ce champ est en lecture seule et est calculé comme **Montant contractuel + taxes**. | Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer des jalons périodiques pour la facturation. |
| **Limite à ne pas dépasser** | L’utilisateur peut modifier ce champ et il n’est disponible que sur les lignes de contrat basées sur un projet qui ont un mode de facturation Temps et matériel. | Ce champ est modifiable par l’utilisateur. Lorsqu’un chiffre réel de temps ou de dépense fait référence à cette ligne de contrat pour le temps et le matériel, le montant réel est évalué par rapport à la limite à ne pas dépasser sur cette ligne de contrat après avoir comptabilisé les montants déjà dépensés et engagés. |
| **Budget client** | Ce champ est modifiable et est copié du champ correspondant sur la ligne de devis, si le contrat a été créé à partir d’un devis. | Ce champ n’est utilisé qu’à titre informatif et n’a aucune signification en aval. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Règle de validation pour les options de l’onglet Général des lignes de contrat basées sur un projet

Règle : un projet et une certaine classe de transaction ne peuvent être inclus que sur une seule ligne de contrat basée sur un projet dans un contrat.

| Contrat | Ligne de contrat | Project | Inclure le temps | Inclure les dépenses | Inclure les frais | Valide/Non valide | Motif                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Oui          | Oui             | Oui         | Non valide       | Viole la règle. Le temps, les dépenses et les frais du projet P1 sont inclus sur les deux lignes de contrat : CL1 et CL2.                                                                                       |
| C1       | CL2           | P1      | Oui          | Oui             | Oui         | Non valide       | Viole la règle. Le temps, les dépenses et les frais du projet P1 sont inclus sur les deux lignes de contrat : CL1 et CL2.                                                                                       |
| C1       | CL1           | P1      | Oui          | No              | Oui         | Non valide       | Viole la règle. Le temps et les frais du projet P1 sont inclus sur les deux lignes de contrat : CL1 et CL2.                                                                                                   |
| C1       | CL2           | P1      | Oui          | Oui             | Oui         | Non valide       | Viole la règle. Le temps et les frais du projet P1 sont inclus sur les deux lignes de contrat : CL1 et CL2.                                                                                                   |
| C1       | CL1           | P1      | Oui          | No              | Oui         | Valide           | Le temps et les frais du projet P1 sont inclus sur CL1. Les dépenses du projet P1 sont incluses sur CL2. </br>   Il n’y a pas de chevauchement dans ce qui est inclus sur chaque ligne de contrat et cela est donc valide.  |
| C1       | CL2           | P1      | No           | Oui             | No          | Valide           | Le temps et les frais du projet P1 sont inclus sur CL1. Les dépenses du projet P1 sont incluses sur CL2. </br>   Il n’y a pas de chevauchement dans ce qui est inclus sur chaque ligne de contrat et cela est donc valide.  |
| C1       | CL1           | P1      | Oui          | Oui             | Oui         | Non valide       | Viole la règle. Le temps, les dépenses et les frais du projet P1 sont inclus sur les lignes de deux contrats.                                                                                               |
| CL2      | CL2           | P1      | Oui          | Oui             | Oui         | Non valide       | Viole la règle. Le temps, les dépenses et les frais du projet P1 sont inclus sur les lignes de deux contrats.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]