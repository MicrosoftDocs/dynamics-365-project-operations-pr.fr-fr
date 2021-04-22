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
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857975"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurer la comptabilité des projets internes

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les projets internes permettent aux entreprises de suivre les coûts liés aux activités qui ne sont pas facturées à un client. Exemples de projets internes :

- Développer un produit, comme une application mobile et suivre le coût associé au développement.
- Gérer le temps et les dépenses de prévente. Ce projet interne de prévente peut être converti ultérieurement en projet facturable si le devis est gagné.

Tout projet qui n’est pas associé à un contrat dans Dynamics 365 Project Operations est considéré comme interne. Les profils de coûts et de revenus du projet ne permettent pas de déterminer les règles comptables pour le projet. Le coût interne du projet est toujours comptabilisé selon les principes de résultat. Les comptes du grand livre pour les écritures sont définis sur la page **Configuration de la validation comptable**.

- Les transactions de temps sont validées en débitant le compte **Coût** et en créditant le compte **Répartition de la paie**.
- Les transactions de dépense sont validées en débitant le compte **Coût** et en créditant le **Compte de contrepartie des dépenses**.
- Les transactions d’article sont validées en débitant le compte **Coût** et en créditant le compte **Coût – Article**.

Une fois les transactions validées sur le projet, si le projet est associé à un contrat de projet, le système contrepasse toutes les transactions cumulées et crée des transactions facturables. Les transactions facturables suivent les règles comptables définies dans le profil de coût et de revenu du projet respectif.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
