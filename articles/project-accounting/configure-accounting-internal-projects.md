---
title: Configurer la comptabilité des projets internes
description: Cet article fournit des informations sur la configuration des pratiques comptables pour les projets internes dans Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7fc2b7247da699a194688b18aa0a695b06cc44c6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919459"
---
# <a name="configure-accounting-for-internal-projects"></a>Configurer la comptabilité des projets internes

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Les projets internes permettent aux entreprises de suivre les coûts liés aux activités qui ne sont pas facturées à un client. Exemples de projets internes :

- Développement d’un produit tel qu’une application mobile et suivi des coûts associés au développement.
- Gestion du temps et des dépenses avant-vente. Ce projet interne de prévente peut être converti ultérieurement en projet facturable si le devis est gagné.

Tout projet qui n’est pas associé à un contrat dans Dynamics 365 Project Operations est considéré comme interne. Les profils de coûts et de revenus du projet ne permettent pas de déterminer les règles comptables pour le projet. Le coût interne du projet est toujours validé à l’aide des principes de profits et pertes. Les comptes généraux imputables sont définis sur la page **Paramétrage de la validation dans la comptabilité**.

- Les transactions de temps sont validées en débitant le compte **Coût** et en créditant le compte **Affectation de la paie**.
- Les transactions de dépense sont validées en débitant le compte **Coût** et en créditant le **Compte de contrepartie des dépenses**.
- Les transactions d’article sont validées en débitant le compte **Coût** et en créditant le compte **Coût – Article**.

Une fois les transactions validées sur le projet, si le projet est associé à un contrat de projet, le système contrepasse toutes les transactions cumulées et crée des transactions facturables. Les transactions facturables suivent les règles comptables définies dans le profil Coût et produit du projet concerné.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
