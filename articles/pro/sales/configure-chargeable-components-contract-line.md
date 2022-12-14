---
title: Configurer les composants facturables d’une ligne de contrat de projet
description: Cet article fournit des informations sur la façon d’ajouter des composants facturables aux lignes de contrat dans Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 33296c93964cc88499e7a98d499b99463e59d62a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825561"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Configurer les composants facturables d’une ligne de contrat de projet

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_

Une ligne de contrat du projet a les composants *inclus* et *payant*.

Les composants inclus sont des composants soumis à :

  - Méthode de facturation et répartition des clients
  - Limites à ne pas dépasser 
  - Paramètres de fréquence de facturation définis sur la ligne de contrat basée sur le projet

Un sous-ensemble des composants inclus peut être marqué comme payant à l’aide du champ **Type de facturation**. Le champ **Type de facturation** est un ensemble d’options qui autorise les valeurs suivantes dans le contexte d’une ligne de contrat :

  - Facturable
  - Non facturable

Les composants payants peuvent être définis sur les tâches, les rôles et les catégories de transaction.

La tarification est définie sur les tâches pour une ligne de contrat de projet et s’applique à toutes les classes de transaction incluses sur la ligne. Si le champ **Inclure les tâches** sur une ligne de contrat est vide ou est défini sur **Projet entier**, l’onglet **Tâches payantes** n’est pas disponible.

La tarification est définie sur les rôles pour une ligne de contrat de projet s’applique uniquement à la classe de transaction **Temps**. Si le champ **Inclure le temps** sur une ligne de contrat est défini sur **Non**, l’onglet **Rôles facturables** ne sera pas disponible.

La tarification est définie sur les catégories de transaction pour une ligne de contrat de projet et s’applique uniquement à la classe de transaction **Dépense**. Si le champ **Inclure les dépenses** sur une ligne de contrat est défini sur **Non**, l’onglet **Catégories facturables** ne sera pas disponible.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Mettre à jour une tâche de projet pour qu’elle soit facturable ou non facturable

Une tâche de projet peut être facturable ou non sur une ligne de contrat spécifique, ce qui rend possible la configuration suivante :

Si une ligne de contrat basée sur un projet comprend **Temps** et une certaine tâche, **T1** y est associé comme payant. S’il y a une deuxième ligne de contrat qui inclut **Dépenses**, vous pouvez associer la tâche T1 sur la ligne de contrat comme non facturable. Le résultat est que tout le temps enregistré sur la tâche est facturable et toutes les dépenses sont non facturables.

Le type de facturation d’une tâche peut être configuré dans l’onglet **Tâches facturables** de la ligne de contrat en mettant à jour le champ **Type de facturation** dans la sous-grille des tâches de la ligne de contrat. Vous pouvez également mettre à jour le champ **Type de facturation** dans la sous-grille Configuration de la facturation de la tâche d’un projet qui affiche les lignes de contrat associées à une tâche.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Mettre à jour un rôle pour qu’il soit facturable ou non facturable

Un rôle peut être facturable ou non facturable sur une ligne de contrat spécifique.

Le type de facturation d’un rôle peut être configuré dans l’onglet **Rôles payants** d’une ligne de contrat. Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Rôles facturables**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Mettre à jour une catégorie de transaction comme facturable ou non facturable

Une catégorie de transaction peut être facturable ou non facturable sur une ligne de contrat spécifique.

Le type de facturation d’une transaction peut être configuré dans l’onglet **Catégories facturables** d’une ligne de contrat basée sur un projet. Pour ce faire, mettez à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**.

### <a name="resolve-chargeability"></a>Résoudre la chargeabilité

Une estimation ou un chiffre réel créé pour le temps n’est considéré comme facturable que si :

   - **Temps** est inclus dans la ligne de contrat.
   - **Rôle** est configuré comme facturable sur la ligne de contrat.
   - **Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de contrat.
 
 Si ces trois éléments sont vrais, la tâche est configurée comme facturable. 

Une estimation ou un chiffre réel créé pour une dépense n’est considéré comme facturable que si :

   - **Dépense** est inclus dans la ligne de contrat
   - **Catégorie de transaction** est configuré comme facturable sur la ligne de contrat
   - **Tâches incluses** est défini sur **Tâche sélectionnée** sur la ligne de contrat
  
 Si ces trois éléments sont vrais, la **Tâche** est configurée comme facturable. 

Une estimation ou un chiffre réel créé pour du matériel n’est considéré comme facturable que si :

   - **Matériel** est inclus dans la ligne de contrat
   - **Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de contrat

Si ces deux éléments sont vrais, la **Tâche** est configurée comme facturable. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Inclut le temps</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Inclut la dépense</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Inclut le matériel</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Tâches incluses</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Rôle</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Catégorie</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tâche</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Impact sur le fait que l’élément soit facturable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Projet entier </p>
            </td>
            <td width="65" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="70" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : <strong>Facturable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
            </td>
            <td width="65" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="70" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="65" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : <strong>Facturable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="65" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation sur les dépenses réelles : facturable </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : Facturable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
            </td>
            <td width="65" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="70" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : <strong>Non facturable</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Tâches sélectionnées uniquement </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : Facturable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Projet entier </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Facturable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </p>
                <p>
Type de facturation sur les dépenses réelles : facturable </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : Facturable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Projet entier </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Non disponible</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : Facturable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Projet entier </p>
            </td>
            <td width="65" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="70" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à l’heure actuelle : Facturable </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : Facturable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Oui </p>
            </td>
            <td width="75" valign="top">
                <p>
Projet entier </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Non disponible</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : Facturable </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Projet entier </p>
            </td>
            <td width="65" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="70" valign="top">
                <p>
Facturable </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à l’heure actuelle : Facturable </p>
                <p>
Type de facturation sur les dépenses réelles : facturable </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Oui </p>
            </td>
            <td width="78" valign="top">
                <p>
Oui </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Projet entier </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Impossible à définir </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à partir du chiffre réel de temps : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de dépenses : <strong>Non facturable</strong>
                </p>
                <p>
Type de facturation à partir du chiffre réel de matériel : <strong>Non disponible</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
