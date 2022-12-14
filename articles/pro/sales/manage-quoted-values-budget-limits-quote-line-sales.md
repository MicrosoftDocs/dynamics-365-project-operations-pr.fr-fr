---
title: Présentation de lignes du devis de projet
description: Cet article fournit des informations sur l’utilisation de lignes de devis basées sur un projet pour le travail d’un projet.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e6a67b5c37508085c9ec3d8385eaa6828536de00
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825655"
---
# <a name="project-quote-lines-overview"></a>Présentation de lignes du devis de projet 

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_

Les lignes de devis basées sur un projet sont conçues pour aider à estimer le travail du projet sur un engagement. La structure d’une ligne de devis basée sur un projet est étendue pour les devis du projet avec les concepts suivants :

- Mode de facturation
- Mappage des tâches et projets
- Classes de transaction incluses
- Limite à ne pas dépasser
- Configuration de l’exigibilité
- Estimation à l’aide des détails de la ligne de devis
- Clients de la ligne de devis

Le tableau suivant fournit des informations sur les champs de l’onglet **Général** de la ligne de devis basée sur le projet. Ces champs aident à jeter les bases d’une estimation détaillée et à la base du travail du projet.

| **Champ** | **Description** | **Impact en aval** |
| --- | --- | --- |
| Nom | Le nom de la ligne de devis qui vous aide à identifier le composant discret du devis qui est estimé. | Copié dans la ligne de contrat de projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Mode de facturation | Sur un devis créé à partir d’une opportunité, cette valeur est copiée à partir du champ correspondant sur la ligne d’opportunité. Ce champ comprend les deux principaux modèles de contrats pris en charge par Dynamics 365 Project Operations :</br>- Prix fixe</br>- Temps et matériel.| Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Project | Utilisez ce champ facultatif pour identifier le projet qui sera utilisé pour livrer le travail sur cet engagement. Lorsqu’un projet est mappé à une ligne de devis, cela aide à configurer des tâches facturables et également à intégrer une estimation basée sur le projet à la ligne de devis en tant que détails de la ligne de devis. Lorsqu’un projet n’est pas mappé à une ligne de devis basée sur un projet, l’estimation doit être créée manuellement en créant chaque détail de ligne de devis. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu.|
| Tâches incluses | Indique si cette ligne de devis est utilisée pour tout ou partie des tâches du projet pour le projet sélectionné. Ce champ contient les valeurs possibles suivantes :</br>- Toutes les tâches du projet</br>- Tâches du projet sélectionnées uniquement</br>Une valeur vide dans ce champ équivaut à l’option **Toutes les tâches du projet**. | Lorsque **Tâches du projet sélectionnées uniquement** est sélectionné sur la page du projet, l’onglet **Configuration de la facturation de la tâche** vous permet de sélectionner des tâches spécifiques pour les associer à cette ligne de devis. Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Inclure le temps | Une valeur **Oui**/**Non** indique si les transactions de temps ou les coûts de main-d’œuvre sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis. Une valeur de **Non** indique que le coût des transactions de temps ou de coûts de main-d’œuvre ne seront pas inclus dans l’estimation sur cette ligne de devis. Une valeur de **Oui** indique que le coût des transactions de temps ou de coûts de main-d’œuvre seront inclus dans l’estimation sur cette ligne de devis. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Inclure la dépense | Une valeur **Oui**/**Non** indique si les coûts de dépense sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis. Une valeur de **Non** indique que le coût de dépenses ne seront pas inclus dans l’estimation sur cette ligne de devis. Une valeur de **Oui** indique que le coût de dépenses seront inclus dans l’estimation sur cette ligne de devis. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Inclure le matériel | Une valeur **Oui**/**Non** indique si les coûts de matériel sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis. Une valeur **Non** indique que les coûts de matériel ne seront pas inclus dans l’estimation sur cette ligne de devis. Une valeur **Oui** indique que les coûts de matériel seront inclus dans l’estimation sur cette ligne de devis. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Inclure les frais | Une valeur **Oui**/**Non** indique si les frais sur le projet sélectionné seront inclus dans l’estimation sur cette ligne de devis. Une valeur **Non** indique que les frais ne seront pas inclus dans l’estimation sur cette ligne de devis. Une valeur **Oui** indique que les frais seront inclus dans l’estimation sur cette ligne de devis. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Montant du devis | Il s’agit du montant qui sera proposé au client pour tous les travaux prévus sur cette ligne de devis basée sur le projet. Sur un devis créé à partir d’une opportunité, cette valeur est copiée à partir du champ **Budget client** sur la ligne d’opportunité. Lorsque la ligne de devis basée sur le projet comporte des détails de ligne, ce champ est verrouillé pour modification et est résumé à partir du montant sur les détails de la ligne de devis. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Estimation de taxe | Il s’agit d’un champ modifiable permettant à l’utilisateur d’ajouter le montant estimé de la taxe sur la ligne de devis. Lorsqu’une ligne de devis basée sur le projet comporte des détails de ligne, ce champ est verrouillé pour modification et est résumé à partir du montant de la taxe sur les détails de la ligne de devis. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Montant du devis après taxes | Ce champ est le montant de la ligne de devis après taxes et est en lecture seule. Le montant dans ce champ est calculé comme suit *Montant estimé + taxes*. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Limite à ne pas dépasser | Ce champ est modifiable et n’est disponible que sur les lignes de devis basées sur un projet qui ont une méthode de facturation **Temps et matériel**. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |
| Budget client | Ce champ est modifiable et copié à partir du champ correspondant sur la ligne d’opportunité si le devis a été créé à partir d’une opportunité. | Cette valeur est copiée dans la ligne de contrat du projet créée à partir de cette ligne de devis lorsque le devis est conclu. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Règles de validation pour les champs de l’onglet Général des lignes de devis basées sur le projet

**Règle 1** : Si le champ **Tâches incluses** est vide ou s’il est défini sur **Toutes les tâches du projet**, un projet est inclus dans la ligne de devis.

**Règle 2** : Si le champ **Tâches incluses** est vide ou s’il est défini sur **Toutes les tâches du projet**, un projet et une certaine classe de transaction ne peuvent être inclus que sur une seule ligne de devis basée sur un projet d’un devis.

**Règle 3** : Si le champ **Tâches incluses** est défini sur **Tâches du projet sélectionnées uniquement**, un projet et une certaine classe de transaction ne peuvent être inclus que sur plusieurs lignes de devis basées sur un projet d’un devis.

**Règle 4** : Si une opportunité comporte plusieurs devis, il peut y avoir des lignes de devis de différents devis qui font toutes référence au même projet et incluent la même classe de transaction.

**Règle 5** : Si les devis n’appartiennent pas à la même opportunité, ils ne peuvent pas inclure le même projet et la même classe de transaction.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Opportunité</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>devis</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Ligne de devis</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Tâches incluses</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Inclure le temps</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Inclure la dépense</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Inclure le matériel</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Inclure </strong>
                </p>
                <p>
                    <strong>Frais</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Valide/Non valide</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Motif</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vide </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violation de la règle n° 2. Le temps, les dépenses et les frais du projet P1 sont inclus dans les lignes de devis, QL1 et QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vide </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vide </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violation de la règle n° 2. Le temps, le matériel et les frais du projet P1 sont inclus dans les lignes de devis, QL1 et QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vide </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vide </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valide </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Le temps, le matériel et les frais du projet P1 sont inclus dans QL1 <br>
Les dépenses du projet P1 sont inclus sur QL2 <br>
Il n’y a aucun chevauchement concernant ce qui est inclus sur chaque ligne de devis et donc valide.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vide </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Violation de la règle n° 2 </p>
                <p>
Q1 inclut le temps, le matériel, les dépenses et les frais sur un sous-ensemble de tâches du projet P1 </p>
                <p>
QL2 comprend le temps, les dépenses et les frais pour l’ensemble du projet P1 et il y a donc chevauchement avec ce qui est inclus sur Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Vide </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valide </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Selon la règle n° 3, </p>
                <p>
Q1 inclut le temps, le matériel, les dépenses et les frais sur un sous-ensemble de tâches du projet P1.
                </p>
                <p>
QL2 inclut le temps, le matériel, les dépenses et les frais pour un sous-ensemble de tâches du projet P1.
                </p>
                <p>
La seule validation supplémentaire concerne le sous-ensemble de tâches sur QL1 qui est différent du sous-ensemble de tâches sur QL2 pour s’assurer qu’il n’y a pas de chevauchement. Ceci est fait par le système lorsque des tâches sont associées.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Toutes les tâches du projet ou vides </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valide </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Selon la règle n° 5, Q1 et Q2 sont deux devis sur la même opportunité. Ils peuvent ainsi tous les deux faire une estimation pour les mêmes composants d’un projet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Toutes les tâches du projet ou vides </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Toutes les tâches du projet ou vides </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Non valide </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Selon la règle n° 4, Q1 et Q2 sont deux devis sur différentes opportunités. Ils ne peuvent ainsi par faire d’estimation pour les mêmes composants d’un même projet.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
T1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Toutes les tâches du projet ou vides </p>
            </td>
            <td width="45" valign="top">
                <p>
Oui </p>
            </td>
            <td width="46" valign="top">
                <p>
Oui </p>
            </td>
            <td width="43" valign="top">
                <p>
Oui </p>
            </td>
            <td width="41" valign="top">
                <p>
Oui </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
