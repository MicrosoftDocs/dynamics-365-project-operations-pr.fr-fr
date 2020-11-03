---
title: Configurer la comptabilité des projets internes
description: Cette rubrique offre des informations sur la configuration des pratiques comptables pour des projets internes dans Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075674"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="2f3d1-103">Configurer la comptabilité des projets internes</span><span class="sxs-lookup"><span data-stu-id="2f3d1-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="2f3d1-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="2f3d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2f3d1-105">Les projets internes permettent aux entreprises de suivre les coûts liés aux activités qui ne sont pas facturées à un client.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="2f3d1-106">Exemples de projets internes :</span><span class="sxs-lookup"><span data-stu-id="2f3d1-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="2f3d1-107">Développer un produit, comme une application mobile et suivre le coût associé au développement.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="2f3d1-108">Gérer le temps et les dépenses de prévente.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="2f3d1-109">Ce projet interne de prévente peut être converti ultérieurement en projet facturable si le devis est gagné.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="2f3d1-110">Tout projet non associé à un contrat dans Dynamics 365 Project Operations est traité comme interne.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="2f3d1-111">Les profils de coûts et de revenus du projet ne permettent pas de déterminer les règles comptables pour le projet.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="2f3d1-112">Le coût interne du projet est toujours comptabilisé selon les principes de résultat.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="2f3d1-113">Les comptes du grand livre pour les écritures sont définis sur la page **Configuration de la validation comptable**.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="2f3d1-114">Les transactions de temps sont validées en débitant le compte **Coût** et en créditant le compte **Répartition de la paie**.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="2f3d1-115">Les transactions de dépense sont validées en débitant le compte **Coût** et en créditant le **Compte de contrepartie des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>

<span data-ttu-id="2f3d1-116">Une fois les transactions enregistrées dans le projet, si le projet est associé à un contrat de projet, le système annule toutes les transactions accumulées et crée de nouvelles transactions facturables.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-116">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="2f3d1-117">Les transactions facturables suivent les règles comptables définies dans le profil de coût et de revenu du projet respectif.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-117">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>

