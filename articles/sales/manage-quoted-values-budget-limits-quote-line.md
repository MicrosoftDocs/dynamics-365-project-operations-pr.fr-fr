---
title: Lignes du devis selon les projets
description: Cette rubrique fournit des informations sur l’utilisation des lignes de devis basées sur un projet pour le travail du projet.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075607"
---
# <a name="project-based-quote-lines"></a>Lignes du devis selon les projets

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les lignes de devis basées sur un projet sont conçues pour aider à estimer le travail du projet sur un engagement. La structure d’une ligne de devis basée sur un projet est étendue pour les devis du projet avec les concepts suivants :

- Mode de facturation
- Mappage de projet
- Classes de transaction incluses
- Limite à ne pas dépasser
- Configuration de l’exigibilité
- Estimation à l’aide des détails de la ligne de devis
- Clients de la ligne de devis

Le tableau suivant fournit des informations sur les champs de l’onglet **Général** de la ligne de devis basée sur le projet. Ces champs aident à jeter les bases d’une estimation détaillée et à la base du travail du projet.

| **Champ** | **Pertinence, objectif et conseils** | **Impact en aval** |
| --- | --- | --- |
| Nom | Nom de la ligne de devis qui devrait vous aider à identifier le composant discret du devis qui est estimé. | Copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Mode de facturation | Sur un devis créé à partir d’une opportunité, cette valeur est copiée à partir du champ correspondant sur la ligne d’opportunité. Ce champ comprend les deux principaux modèles de contrats pris en charge par Dynamics 365 Project Operations :</br>- Prix fixe</br>- Temps et matériel.| Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Project | Utilisez ce champ facultatif pour identifier le projet qui sera utilisé pour livrer le travail sur cet engagement. Lorsqu’un projet est mappé à une ligne de devis, cela aide à configurer des tâches facturables et également à intégrer une estimation basée sur le projet à la ligne de devis en tant que détails de la ligne de devis. Lorsqu’un projet n’est pas mappé à une ligne de devis basée sur un projet, l’estimation doit être créée manuellement en créant chaque détail de ligne de devis. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Inclure le temps | Un indicateur **Oui**/**Non** indique si les transactions de temps ou les coûts de main-d’œuvre sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis. Une valeur de **Non** indique que le coût des transactions de temps ou de coûts de main-d’œuvre ne seront pas inclus dans l’estimation sur cette ligne de devis. Une valeur de **Oui** indique que le coût des transactions de temps ou de coûts de main-d’œuvre seront inclus dans l’estimation sur cette ligne de devis. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Inclure la dépense | Un indicateur **Oui**/**Non** indique si les coûts de dépenses sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis. Une valeur de **Non** indique que le coût de dépenses ne seront pas inclus dans l’estimation sur cette ligne de devis. Une valeur de **Oui** indique que le coût de dépenses seront inclus dans l’estimation sur cette ligne de devis. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Inclure les frais | Un indicateur **Oui**/**Non** indique si les frais sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis. Une valeur de **Non** indique que les frais ne seront pas inclus dans l’estimation sur cette ligne de devis. Une valeur de **Oui** indique que les frais seront inclus dans l’estimation sur cette ligne de devis. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Montant du devis | Il s’agit du montant qui sera proposé au client pour tous les travaux prévus sur cette ligne de devis projet. Sur un devis créé à partir d’une opportunité, cette valeur est copiée à partir du champ **Budget client** sur la ligne d’opportunité. Lorsque la ligne de devis basée sur le projet comporte des détails de ligne, ce champ est verrouillé pour modification et est résumé à partir du montant sur les détails de la ligne de devis. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Estimation de taxe | Il s’agit d’un champ modifiable permettant à l’utilisateur d’ajouter le montant estimé de la taxe sur la ligne de devis. Lorsqu’une ligne de devis basée sur le projet comporte des détails de ligne, ce champ est verrouillé pour modification et est résumé à partir du montant de la taxe sur les détails de la ligne de devis. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Montant du devis après taxes | Ce champ est le montant de la ligne de devis après taxes et est en lecture seule. Le montant dans ce champ est calculé comme suit *Montant estimé + taxes*. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Limite à ne pas dépasser | Ce champ est modifiable et n’est disponible que sur les lignes de devis basées sur un projet qui ont une méthode de facturation **Temps et matériel**. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Budget client | Ce champ est modifiable et copié à partir du champ correspondant sur la ligne d’opportunité si le devis a été créé à partir d’une opportunité. | Ce champ est copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Règles de validation pour les champs de l’onglet Général des lignes de devis basées sur le projet

**Règle 1**  : Une certaine classe de transaction sur le projet sélectionné ne peut être incluse que sur une seule ligne de devis basée sur un projet d’un devis.

**Règle 2**  : Si une opportunité comporte plusieurs devis, il peut y avoir des lignes de devis de différents devis qui font toutes référence au même projet et incluent la même classe de transaction.

**Règle 3**  : Si les devis n’appartiennent pas à la même opportunité, ils ne peuvent pas inclure le même projet et la même classe de transaction.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Opportunité</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>devis</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Ligne de devis</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Inclure le temps</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Inclure la dépense</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Inclure</strong>
                </p>
                <p>
                    <strong>frais</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Valide/Non valide</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Motif</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violation de la règle n° 1. Le temps, les dépenses et les frais du projet P1 sont inclus dans les deux lignes de devis, QL1 et QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
T1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violation de la règle n° 1. Le temps et les frais du projet P1 sont inclus dans les deux lignes de devis, QL1 et QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Valide </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Le temps et les frais du projet P1 sont inclus sur QL1.
Les dépenses du projet P1 sont inclus sur QL2.
Il n’y a pas de chevauchement dans ce qui est inclus sur chaque ligne de devis, donc c’est valide.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Violation de la règle n° 1 ci-dessus </p>
                <p>
Q1 comprend le temps, les dépenses et les frais pour l’ensemble du projet P1.
                </p>
                <p>
QL2 comprend le temps, les dépenses et les frais pour l’ensemble du projet P1 et chevauche ce qui est inclus dans Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="54" valign="top">
                <p>
Valide </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Basé sur la règle n° 2, Q1 et Q2 sont deux citations sur la même opportunité, de sorte qu’ils peuvent tous les deux estimer pour les mêmes composants d’un projet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 sur Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="54" valign="top">
                <p>
Valide </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Basé sur la règle n° 3, Q1 et Q2 sont deux citations sur différentes opportunités, de sorte qu’ils peuvent tous les deux estimer pour les mêmes composants d’un même projet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
Q1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="48" valign="top">
                <p>
Oui </p>
            </td>
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="54" valign="top">
                <p>
Non valide </p>
            </td>
        </tr>
    </tbody>
</table>

