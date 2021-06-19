---
title: Nouveautés ou modifications de la mise à jour (version 17) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 17) de Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: 364a64e0ea501ac5b7faaf254c7af3648cfe1f9b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006688"
---
# <a name="project-service-automation-update-release-17-v3"></a>Mise à jour (version 17) de Project Service Automation, V3

[!include [banner](../includes/psa-now-project-operations.md)]

Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365. Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.  Cette version est compatible avec Dynamics 365 9.x. Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 (en ligne) et accédez à la page des solutions pour installer la mise à jour. Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](/power-platform/admin/install-remove-preferred-solution).

Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 17) de PSA V3. Cette version a le numéro de build V3.10.6.34 et sera disponible partout par mise à jour automatique en mars 2020.


## <a name="update-release-17"></a>Mise à jour (version 17)

### <a name="bug-fixes"></a>Correctifs de bogues

**Général**

- Résolu : Mise à jour de Project Service Automation pour appliquer des licences Team Member (Project Resource Hub comprendra les métadonnées 3.x du plan relatif à Team Member)
 
**Temps et dépenses**

- Résolu : Il n’est pas possible de remplacer une estimation de dépenses d’un prix non nul par zéro (0). La modification est ignorée.

**Gestion du projet**

- Résolu : Une vérification des valeurs nulles a été ajoutée sur le nom du poste d’un membre de l’équipe.
- Résolu : Le champ **msdyn_userresourceid** de l’entité **msdyn_resourceassignment** est devenue obsolète.
- Résolu : La mise à niveau de 2.x à 3.x gère désormais les cadres de travail vides sur les affectations de tâches.

**Ventes**

- Résolu : **Invoice.PreValidateInvoiceUpdate** gère désormais correctement le scénario de réaffectation des propriétaires d’enregistrements.
- Résolu : Lorsque la classe de transaction est **Temps**, **UnitGroup** n’est pas modifiable pour toutes les entités, y compris **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** et **ContractLineDetails**. Cependant, **Unité** est non modifiable uniquement pour **JournalLine** et **InvoiceLineDetails**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]