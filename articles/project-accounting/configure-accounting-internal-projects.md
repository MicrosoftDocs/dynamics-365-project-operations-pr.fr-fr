---
title: Configurer la comptabilité des projets internes
description: Cette rubrique offre des informations sur la configuration des pratiques comptables pour des projets internes dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132375"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurer la comptabilité des projets internes

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les projets internes permettent aux entreprises de suivre les coûts liés aux activités qui ne sont pas facturées à un client. Exemples de projets internes :

- Développer un produit, comme une application mobile et suivre le coût associé au développement.
- Gérer le temps et les dépenses de prévente. Ce projet interne de prévente peut être converti ultérieurement en projet facturable si le devis est gagné.

Tout projet non associé à un contrat dans Dynamics 365 Project Operations est traité comme interne. Les profils de coûts et de revenus du projet ne permettent pas de déterminer les règles comptables pour le projet. Le coût interne du projet est toujours comptabilisé selon les principes de résultat. Les comptes du grand livre pour les écritures sont définis sur la page **Configuration de la validation comptable**.

- Les transactions de temps sont validées en débitant le compte **Coût** et en créditant le compte **Répartition de la paie**.
- Les transactions de dépense sont validées en débitant le compte **Coût** et en créditant le **Compte de contrepartie des dépenses**.

Une fois les transactions enregistrées dans le projet, si le projet est associé à un contrat de projet, le système annule toutes les transactions accumulées et crée de nouvelles transactions facturables. Les transactions facturables suivent les règles comptables définies dans le profil de coût et de revenu du projet respectif.


