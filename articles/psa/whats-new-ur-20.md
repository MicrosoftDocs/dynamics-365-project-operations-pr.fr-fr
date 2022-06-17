---
title: Nouveautés ou modifications de la mise à jour (version 20) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Project Service Automation version 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7265f4999ee9c584450efcf444621c00acd65920
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913059"
---
# <a name="project-service-automation-update-release-20-v3"></a>Mise à jour (version 20) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d’administration de Dynamics 365 online pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour version 20 de Project Service Automation V3. Cette version a le numéro de build V 3.10.31.37 et est généralement disponible via une mise à jour automatique en juin 2020.

## <a name="update-release-20"></a>Mise à jour (version 20)

### <a name="bug-fixes"></a>Corrections de bogues

**Gestion du projet**

Les problèmes suivants ont été résolus :

- L’importation des membres de l’équipe du projet avec une méthode d’allocation nécessitant des heures entraîne un message d’erreur peu explicite lorsque les heures spécifiées sont nulles.
- Les utilisateurs reçoivent une erreur incorrecte lorsque le nombre maximal de caractères a été entré dans le champ **Description** pour une tâche de projet.
- La **page de téléchargement du complément Microsoft Dynamics 365 Project Service Automation** redirige vers la page de téléchargement en anglais lorsque les paramètres de langue de l’utilisateur sont définis sur Japonais.
- Lorsqu’une erreur de serveur se produit, l’étiquette de synchronisation dans l’onglet **Planifier** du formulaire **Projets** est parfois conservée.
- Les mises à jour de tâche redondantes sont envoyées au serveur lorsqu’une tâche est modifiée.

**Ventes**

Les problèmes suivants ont été résolus :

- Sur le formulaire **Contrat**, un double-clic sur **Créer une facture** crée deux factures pour un seul enregistrement de chiffres réels.
- Dans Internet Explorer 11, les utilisateurs ne peuvent pas créer d’entrées de dépenses.
- La contrepassation du coût et la contrepassation des chiffres réels des ventes non facturées ne sont pas liées.
- Le bouton **Actualiser les chiffres réels** du formulaire **Projet** n’actualise pas les **Heures réelles de la tâche**.
- Le plug-in **PreValidateProjectTeamMemberCreate** peut créer des ressources réservables génériques en double lorsque l’attribut **msdyn_isgenericresourceprojectscoped** est défini sur **False**.
- **Recalculer** efface les coûts facturables des détails de la ligne de devis basés sur le produit et des détails de la ligne de contrat.
- Dans des scénarios spécifiques, le plug-in **PostEstimateLineUpdate** affiche une erreur d’exception de référence nulle.
- La durée de la phase de temps sur le **Graphique d’analyse de la rentabilité** ne correspond pas à la durée des coûts dans les détails de la ligne de devis à prix fixe du devis.
- Les valeurs d’unité et de groupe d’unités ne sont pas correctement définies par défaut pour les catégories de dépense sur les formulaires **Détails de la ligne de contrat** et **Détails de la ligne de devis**.
- Les listes **Prix de revient de l’unité d’organisation** autorisent les chevauchements dans la plage de dates définie.
- Les utilisateurs ne sont pas autorisés à modifier **OrgUnit** lorsque le type de commande n’est pas basé sur le travail, car cela va générer une erreur d’exception de référence nulle.
- Lorsque vous tentez de passer du formulaire **Détails de la ligne de devis** à l’onglet **Devis**, le formulaire s’actualise et affiche l’onglet **Résumé**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
