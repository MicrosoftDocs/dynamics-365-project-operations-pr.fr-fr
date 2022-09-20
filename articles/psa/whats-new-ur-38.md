---
title: Nouveautés ou modifications de la mise à jour (version 38) de Project Service Automation (correctif logiciel), V3
description: Cet article répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour de Microsoft Dynamics 365 Project Service Automation version 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915182"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Nouveautés ou modifications de la mise à jour (version 38) de Project Service Automation (correctif logiciel), V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Microsoft Dynamics 365 Project Service Automation. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation. Elle est compatible avec Dynamics 365 9.x. Pour effectuer la mise à jour vers cette version, visitez la page des solutions en ligne du Centre d’administration pour Dynamics 365 et installez la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cet article répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour de Project Service Automation version 38, V3. Cette version a un numéro de build V3.10.59.117 et est généralement disponible via une mise à jour automatique en décembre 2021.

## <a name="update-release-38"></a>Mise à jour (version 38)

### <a name="bug-fixes"></a>Corrections de bogues

Les problèmes suivants ont été résolus.

**Temps et dépenses**

- Une exception se produit lorsque la longueur des journaux d’ensembles d’approbations dépasse 100 000 enregistrements.
- Les utilisateurs ne peuvent pas accéder à la grille **Entrée de temps** de la page principale **Entrée de temps**.
- La boîte de dialogue **Importation des entrées de temps** n’affiche aucun texte lorsqu’aucun élément n’est éligible pour l’importation.
- Les utilisateurs peuvent créer des ensembles d’approbations où le champ **Statut de destination** est défini sur **Inconnue**.

**Gestion du projet**

- Les contours ne s’affichent pas correctement dans les affectations de ressources pour UTC (+09:30) et UTC (+10:00) lorsque l’heure d’été commence.
- Le champ **Colonne supplémentaire** pour les structures de répartition du travail est masqué dans certains paramètres régionaux.
- Le sélecteur de date pour le contrôle du calendrier dans la grille **Tâche du projet** n’est pas correctement localisée pour le chinois.

**Vente**

- Les valeurs **Exécution du contrat** et **Coût réel du projet** ne correspondent pas lorsque les ressources réservables qui ont des unités contractantes et des devises différentes soumettent des entrées de temps.
- Un workflow personnalisé de vérification automatique des factures échoue lorsque les factures sont importées en tant que solution gérée. Le message suivant s’affiche : « Message Microsoft.Xrm.Sdk.InvalidPluginExecutionException : statut de la facture non valide. »
- Lorsque **Racine** est sélectionné comme option de résumé et que le projet comporte des estimations provenant d’un mélange de classes de transactions (par exemple, une combinaison d’estimations de temps, de dépenses et de matériel), le système récapitule toutes les classes de transactions sous la forme d’une seule ligne de frais.
- Dans les scénarios où une ligne de dépense est ajoutée avant qu’une ligne de contrat ne soit associée à un projet, la tarification correcte n’est pas entrée comme valeur par défaut dans le champ **Mettre à jour les prix**.
- Les montants de vente négatifs ne sont pas autorisés dans les entités **Projet** et **Tâche**.