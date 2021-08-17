---
title: Configurer les composants facturables d’une ligne de devis
description: Cette rubrique fournit des informations sur la configuration de composants payants et non facturables sur une ligne de devis basée sur un projet.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec8a999142fd9960c79ef981e499ae840642e57b269c83d201d2db006179de09
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995983"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Configurer les composants facturables d’une ligne de devis 

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma, Project Operations pour les scénarios basés sur les ressources/produits non stockés_

Une ligne de devis basée sur un projet a le concept des composants *inclus* et *payant*.

Les composants inclus sont soumis à :

  - Méthode de facturation et répartition des clients
  - Limites à ne pas dépasser 
  - Paramètres de fréquence de facturation définis sur la ligne de devis basée sur le projet

Un sous-ensemble des composants inclus peut être marqué comme payant à l’aide du champ **Type de facturation**. Le champ **Type de facturation** est un ensemble d’options qui autorise les valeurs suivantes dans le contexte d’une ligne de devis :

  - Facturable
  - Non facturable

Les composants payants peuvent être définis sur les tâches, les rôles et les catégories de transaction.

La tarification est définie sur les tâches pour une ligne de devis et s’applique à toutes les classes de transaction incluses sur cette ligne. Si le champ **Inclure les tâches** est défini sur **Projet entier** ou laissé vide, l’onglet **Tâches payantes** n’est pas disponible.

La tarification est définie sur les rôles pour une ligne de devis et s’applique uniquement à la classe de transaction **Temps**. Si le champ **Inclure le temps** est défini sur **Non** dans une ligne de devis de projet, l’onglet **Rôles facturables** n’est pas disponible.

La tarification est définie sur les catégories de transaction pour une ligne de devis et s’applique uniquement à la classe de transaction **Dépense**. Si le champ **Inclure les dépenses** est défini sur **Non** dans une ligne de devis de projet, l’onglet **Catégories facturables** n’est pas disponible.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Mettre à jour une tâche de projet pour qu’elle soit facturable ou non facturable

Une tâche de projet peut être facturable ou non dans le contexte d’une ligne de devis basée sur un projet spécifique, ce qui rend possible la configuration suivante.

Si une ligne de devis basée sur un projet comprend **Temps** et la tâche **T1**, la tâche est associée à la ligne de devis comme facturable. S’il y a une deuxième ligne de devis qui inclut **Dépenses**, vous pouvez associer la tâche **T1** sur la ligne de devis comme non facturable. Le résultat est que tout le temps enregistré sur la tâche est facturable et toutes les dépenses enregistrées sur la tâche sont non facturables.

Le type de facturation d’une tâche peut être configuré dans l’onglet **Tâches facturables** de la ligne de devis basée sur un projet en mettant à jour le champ **Type de facturation** dans la sous-grille **Tâches de la ligne de contrat**. Vous pouvez également mettre à jour le type de facturation d’une tâche de projet dans le champ **Type de facturation** dans la sous-grille dans la configuration de la facturation de la tâche d’un projet qui affiche les lignes de devis associées à une tâche.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Mettre à jour un rôle pour qu’il soit facturable ou non facturable

Un rôle peut être payant ou non dans le contexte d’une ligne de devis spécifique à un projet.

Le type de facturation d’un rôle peut être configuré dans l’onglet **Rôles facturables** de la ligne de devis en mettant à jour le champ **Type de facturation** dans la sous-grille **Rôles facturables**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Mettre à jour une catégorie de transaction comme facturable ou non facturable

Une catégorie de transaction peut être facturable ou non facturable sur une ligne de devis spécifique.

Le type de facturation d’une transaction peut être configuré dans l’onglet **Catégories facturables** de la ligne de devis en mettant à jour le champ **Type de facturation** dans la sous-grille **Catégories facturables**.

### <a name="resolve-chargeability"></a>Résoudre la chargeabilité
Une estimation ou un chiffre réel créé pour le temps ne sera considéré comme facturable que si :

   - **Temps** est inclus dans la ligne de devis.
   - **Rôle** est configuré comme facturable sur la ligne de devis.
   - **Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis. 

Si ces trois éléments sont vrais, la **Tâche** est également configurée comme facturable. 

Une estimation ou un chiffre réel créé pour une dépense n’est considéré comme facturable que si : 

   - **Dépense** est inclus dans la ligne de devis.
   - **Catégorie de transaction** est configuré comme facturable sur la ligne de devis.
   - **Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis.

Si ces trois éléments sont vrais, la **Tâche** est également configurée comme facturable. 

Une estimation ou un chiffre réel créé pour du matériel ne sera considéré comme facturable que si :

   - **Matériel** est inclus dans la ligne de devis.
   - **Tâches incluses** est défini sur **Tâches sélectionnées** sur la ligne de devis.

Si ces deux éléments sont vrais, la **Tâche** doit également être configurée comme facturable. 


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
Ne peut pas être défini </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à l’heure actuelle : Facturable </p>
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
Facturable </p>
            </td>
            <td width="350" valign="top">
                <p>
Facturation à l’heure actuelle : Facturable </p>
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
Ne peut pas être défini </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Facturable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ne peut pas être défini </p>
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
Ne peut pas être défini </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Non facturable</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Ne peut pas être défini </p>
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
Ne peut pas être défini </p>
            </td>
            <td width="65" valign="top">
                <p>
Ne peut pas être défini </p>
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
Ne peut pas être défini </p>
            </td>
            <td width="65" valign="top">
                <p>
Ne peut pas être défini </p>
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
Ne peut pas être défini </p>
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
Ne peut pas être défini </p>
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
