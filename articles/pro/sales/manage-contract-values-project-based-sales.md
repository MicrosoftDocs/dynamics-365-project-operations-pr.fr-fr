---
title: Vue d’ensemble des lignes de contrat de projet
description: Cet article fournit des informations sur l’utilisation des lignes de contrat de projet dans Project Operations.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5a529233692a39b0674417cd4ea225e40243086
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824623"
---
# <a name="project-contract-lines-overview"></a>Vue d’ensemble des lignes de contrat de projet

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Les lignes de contrat basées sur un projet dans Dynamics 365 Project Operations ont pour vocation de contenir l’estimation et les accords de facturation des composants spécifiques du travail de projet dans un engagement. La structure d’une ligne de contrat basée sur un projet est étendue pour les estimations de projet et les scénarios de facturation avec les concepts suivants :

- Mode de facturation
- Mappage des projets et des tâches
- Classes de transaction incluses
- Limite à ne pas dépasser
- Configuration de l’exigibilité
- Estimations utilisant les détails de la ligne de contrat
- Client de la ligne de contrat

Le tableau suivant comprend les champs présents sous l’onglet **Général** des lignes de contrat basées sur un projet qui aident à configurer la base de départ d’une estimation détaillée et les modalités de facturation pour un travail basé sur un projet.

| Champ | Description | Impact en aval |
| --- | --- | --- |
| **Nom** | Nom de la ligne de contrat. Il identifie le composant discret du contrat estimé. Pour un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir d’une valeur correspondante de la ligne de devis basée sur le projet. | Le nom copié dans la ligne de facture du projet créée à partir de cette ligne de contrat lorsque la facture est créée. |
| **Mode de facturation** | Dans un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir du champ correspondant dans la ligne de devis. Il s’agit d’un groupe d’options qui représente les deux principaux modèles de contrats pris en charge par Project Operations :</br>- **Prix fixe**</br>- **Temps et matériel** | En fonction du mode de facturation de la ligne de contrat référencée, la transaction réelle sera traitée. Si la ligne de contrat référencée par la transaction réelle a un mode de facturation pour le temps et le matériel, des enregistrements réels des coûts et des ventes non facturées sont créés. Si la ligne de contrat référencée par la transaction réelle a un mode de facturation à prix fixe, seul un coût réel est créé. |
| **Project** | Utilisez ce champ pour identifier le projet qui sera utilisé pour livrer le travail sur cet engagement. | Cette valeur sera utilisée en conjonction avec **Tâches incluses** et **Classes de transaction incluses** pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Tâches incluses** | Indique si cette ligne de contrat comprend toutes les tâches du projet pour le projet sélectionné ou seulement un sous-ensemble de tâches. Il s’agit d’un groupe d’options avec les valeurs possibles suivantes :</br>- **Toutes les tâches du projet**</br>- **Tâches du projet sélectionnées uniquement**. Une valeur vide dans ce champ équivaut à sélectionner **Toutes les tâches du projet**. | Si **Tâches sélectionnées uniquement** est sélectionné, vous pouvez sélectionner des tâches spécifiques et les associer à cette ligne de contrat dans l’onglet **Configuration de la facturation de la tâche** sur la page **Projet**. La valeur sera utilisée conjointement avec les classes **Projet** et **Transaction incluses** pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Inclure le temps** | Une valeur **Oui**/**Non** indique si les transactions de temps ou les coûts de main-d’œuvre sur le projet sélectionné seront inclus dans cette ligne de contrat. La valeur **Non** indique que les transactions de temps ou le coût de main-d’œuvre ne seront pas inclus dans cette ligne de contrat. La valeur **Oui** indique qu’ils le seront. | Cette valeur est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Inclure la dépense** | Une valeur **Oui**/**Non** indique si les coûts de dépense sur le projet sélectionné seront inclus dans cette ligne de contrat. La valeur **Non** indique que les dépenses ne seront pas incluses dans cette ligne de contrat. La valeur **Oui** indique qu’elles le seront. | Cette valeur est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Inclure le matériel** | Une valeur **Oui**/**Non** indique si les coûts de matériel sur le projet sélectionné seront inclus dans cette ligne de contrat. Une valeur **Non** indique que les coûts de matériel ne seront pas inclus dans cette ligne de contrat. La valeur **Oui** indique qu’elles le seront. | Cette valeur est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Inclure les frais** | Une valeur **Oui**/**Non** indique si les frais sur le projet sélectionné seront inclus dans cette ligne de contrat. La valeur **Non** indique que les frais ne seront pas inclus dans cette ligne de contrat. La valeur **Oui** indique qu’ils le seront. | Cette valeur est utilisée conjointement avec le projet pour résoudre la référence de ligne de contrat sur un enregistrement de ligne réel ou estimé. |
| **Montant contractuel** | Sur une ligne de contrat à prix fixe, ce montant est la valeur convenue qui sera facturée au client pour tous les composants de travail associés à cette ligne de contrat. Sur une ligne de contrat de temps et de matériel, ce montant est une valeur estimée de ce qui sera facturé au client pour tous les composants de travail associés à cette ligne de contrat. Dans un contrat de projet créé à partir d’un devis, cette valeur est copiée à partir du champ correspondant dans la ligne de devis. Lorsqu’une ligne de contrat basée sur un projet comporte des détails de ligne, ce champ est verrouillé pour modification et est synthétisé à partir du montant sur les détails de la ligne de contrat. | Lorsque la ligne de contrat comporte des détails de ligne, cette valeur peut être modifiée en changeant les montants des détails de ligne. Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer le montant avant taxes sur les jalons périodiques pour la facturation. |
| **Estimation de taxe** | L’utilisateur peut modifier ce champ pour saisir le montant estimé des taxes sur la ligne du contrat. Lorsqu’une ligne de contrat basée sur un projet comporte des détails de ligne, ce champ est verrouillé pour modification et est synthétisé à partir du montant des taxes sur les détails de la ligne de contrat. | Lorsque la ligne de contrat comporte des détails de ligne, cette valeur peut être modifiée en changeant les montants des taxes des détails de ligne. Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer les taxes sur les jalons périodiques pour la facturation. |
| **Montant contractuel après taxes** | Le montant de a ligne de contrat après taxes. Ce champ est en lecture seule et est calculé comme **Montant contractuel + taxes**. | Sur une ligne de contrat à prix fixe, cette valeur est utilisée pour générer des jalons périodiques pour la facturation. |
| **Limite à ne pas dépasser** | L’utilisateur peut modifier ce champ et il n’est disponible que sur les lignes de contrat basées sur un projet qui ont un mode de facturation défini sur le temps et le matériel. | Ce champ est modifiable par l’utilisateur. Lorsqu’un chiffre réel de temps et de matériel fait référence à cette ligne de contrat pour le temps et le matériel, le montant réel est évalué par rapport à la limite à ne pas dépasser sur la ligne de contrat. Cette évaluation est finalisée après la comptabilisation des montants déjà dépensés et engagés. |
| **Budget client** | Ce champ est modifiable et est copié du champ correspondant sur la ligne de devis si le contrat a été créé à partir d’un devis. | Ce champ n’est utilisé qu’à titre informatif et n’a aucune signification en aval. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Règles de validation pour les options de l’onglet Général des lignes de contrat basées sur un projet

Règle 1 : si le champ **Tâches incluses** est vide ou défini sur **Toutes les tâches du projet**, toutes les tâches du projet sont incluses dans la ligne du contrat.

Règle 2 : lorsque le champ **Tâches incluses** est vide ou défini explicitement sur **Toutes les tâches du projet**, un projet et une certaine classe de transactions ne peuvent être inclus que sur une seule ligne de contrat de projet d’un contrat.

Règle 3 : lorsque le champ **Tâches incluses** est défini sur **Tâches du projet sélectionnées uniquement**, un projet et une certaine classe de transactions peuvent être inclus que sur plusieurs lignes de contrat de projet d’un contrat.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Contrat</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Ligne de contrat</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Tâches incluses</strong>
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
                    <strong>Inclure le matériel</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Inclure </strong>
                </p>
                <p>
                    <strong>Frais</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>Valide/Non valide</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Motif</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vide </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violation de la règle n° 2. Le temps, les dépenses, le matériel et les frais du projet P1 sont inclus dans les lignes de contrat CL1 et CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vide </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vide </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violation de la règle n° 2. Le temps, le matériel et les frais du projet P1 sont inclus dans les lignes de contrat CL1 et CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vide </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vide </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valide </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Le temps, le matériel et les frais du projet P1 sont inclus dans CL1.
                </p>
                <ul>
                    <li>
Les dépenses du projet P1 sont inclus sur CL2.
                    </li>
                </ul>
                <p>
Il n’y a aucun chevauchement concernant ce qui est inclus sur chaque ligne de contrat et donc valide.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vide </p>
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Violation de la règle n° 2 </p>
                <p>
C1 inclut le temps, le matériel, les dépenses et les frais sur un sous-ensemble de tâches du projet P1.
                </p>
                <p>
CL2 comprend le temps, le matériel, les dépenses et les frais pour l’ensemble du projet P1 et chevauche donc ce qui est inclus dans C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Vide </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valide </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Selon la règle n° 3 </p>
                <p>
C1 inclut le temps, les dépenses, le matériel et les frais sur un sous-ensemble de tâches du projet P1.
                </p>
                <p>
CL2 inclut le temps, les dépenses, le matériel et les frais pour un sous-ensemble de tâches du projet P1.
                </p>
                <p>
La seule validation supplémentaire concerne le sous-ensemble de tâches sur CL1 qui est différent du sous-ensemble de tâches sur CL2 pour s’assurer qu’il n’y a pas de chevauchements. Ceci est fait par le système lorsque des tâches sont associées.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
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
            <td width="42" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
