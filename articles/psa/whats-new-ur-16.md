---
title: Nouveautés ou modifications de la mise à jour (version 16) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 16) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 5651f8b3a2ddf406fcfd7a4e21901c53789fa4ed
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577371"
---
# <a name="project-service-automation-update-release-16-v3"></a>Mise à jour (version 16) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.  Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 (en ligne) et accédez à la page des solutions pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/dynamics365/project-service/upgrade-psa-home-page).
Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 16) de PSA V3. Cette version a le numéro de build V3.10.6.34 et est généralement disponible par mise à jour automatique en janvier 2020.


## <a name="update-release-16"></a>Mise à jour (version 16)

### <a name="bug-fixes"></a>Correctifs de bogues

-   Temps et dépenses

    -   Résolu : Les utilisateurs qui tentaient de soumettre des entrées de temps et de dépenses supprimées pour les approbations reçoivent désormais des messages d’erreur pertinents.

-   Gestion du projet

    -   Résolu : Les unités de ressources définies pour les membres de l’équipe dans les modèles sont respectées et les modèles sont appliqués à un nouveau projet.

    -   Résolu : Gestion améliorée de la réaffectation de la propriété d’enregistrement.

    -   Résolu : Les projets en cours de copie ne seront pas autorisés à être copiés tant que toutes les opérations de copie ne seront pas terminées.

-   Gestion des ressources

    -   Résolu : Les réservations prolongées gèrent désormais correctement les courtes durées et ne créent plus de zéro heure pour les réservations prolongées.

    -   Résolu : La vue de réconciliation s’affiche désormais lorsque le fuseau horaire du projet est +5 :30 GMT et que l’heure de l’utilisateur est différente.

-   Ventes

    -   Résolu : Lorsqu’un projet mappé sur une ligne de contrat est supprimé et qu’un nouveau projet est mappé, les enregistrements réels du nouveau projet ne sont pas réévalués en fonction des règles de facturation et de tarification définies sur la ligne de contrat. Cela a été corrigé dans cette version. Les prix et les enregistrements réels du projet nouvellement mappé seront inversés et recréés correctement en fonction des règles de tarification et de facturation de la ligne de contrat. Les enregistrements réels du projet non mappé seront également réévalués et recréés en conséquence.

    -   Résolu : Une validation supplémentaire a été ajoutée à un champ **Montant** d’une ligne d’estimation pour garantir que les valeurs nulles ne sont pas persistantes.

    -   Résolu : Lorsque les chiffres réels ont été mis à jour sur un projet, un bouton d’actualisation a été ajouté au formulaire principal du projet pour permettre aux utilisateurs de resynchroniser les chiffres réels.

    -   Résolu : Lorsque les utilisateurs passent de 2.X à 3.X, les projets avec une valeur NULL pour le nom du projet seront autorisés.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
