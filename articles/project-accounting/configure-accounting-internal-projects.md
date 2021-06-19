---
title: Configurer la comptabilité des projets internes
description: Cette rubrique offre des informations sur la configuration des pratiques comptables pour des projets internes dans Project Operations.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad8b974ef75cb0a4e43af0aa254cec1bbcab154a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012853"
---
# <a name="configure-accounting-for-internal-projects"></a><span data-ttu-id="452cc-103">Configurer la comptabilité des projets internes</span><span class="sxs-lookup"><span data-stu-id="452cc-103">Configure accounting for internal projects</span></span>

<span data-ttu-id="452cc-104">_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_</span><span class="sxs-lookup"><span data-stu-id="452cc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="452cc-105">Les projets internes permettent aux entreprises de suivre les coûts liés aux activités qui ne sont pas facturées à un client.</span><span class="sxs-lookup"><span data-stu-id="452cc-105">Internal projects allow companies track cost related to activities that aren't being billed to a customer.</span></span> <span data-ttu-id="452cc-106">Exemples de projets internes :</span><span class="sxs-lookup"><span data-stu-id="452cc-106">Examples of internal projects include:</span></span>

- <span data-ttu-id="452cc-107">Développement d’un produit tel qu’une application mobile et suivi des coûts associés au développement.</span><span class="sxs-lookup"><span data-stu-id="452cc-107">Developing a product, such as a mobile app, and tracking the cost associated with the development.</span></span>
- <span data-ttu-id="452cc-108">Gestion du temps et des dépenses avant-vente.</span><span class="sxs-lookup"><span data-stu-id="452cc-108">Managing pre-sale time and expense.</span></span> <span data-ttu-id="452cc-109">Ce projet interne de prévente peut être converti ultérieurement en projet facturable si le devis est gagné.</span><span class="sxs-lookup"><span data-stu-id="452cc-109">This pre-sale internal project can be converted later to a billable project if quote is won.</span></span>

<span data-ttu-id="452cc-110">Tout projet qui n’est pas associé à un contrat dans Dynamics 365 Project Operations est considéré comme interne.</span><span class="sxs-lookup"><span data-stu-id="452cc-110">Any project not associated with a contract in Dynamics 365 Project Operations is treated as internal.</span></span> <span data-ttu-id="452cc-111">Les profils de coûts et de revenus du projet ne permettent pas de déterminer les règles comptables pour le projet.</span><span class="sxs-lookup"><span data-stu-id="452cc-111">Project cost and revenue profiles aren't used to determine accounting rules for the project.</span></span> <span data-ttu-id="452cc-112">Le coût interne du projet est toujours validé à l’aide des principes de profits et pertes.</span><span class="sxs-lookup"><span data-stu-id="452cc-112">Internal project cost is always posted using profit and loss principles.</span></span> <span data-ttu-id="452cc-113">Les comptes généraux imputables sont définis sur la page **Paramétrage de la validation dans la comptabilité**.</span><span class="sxs-lookup"><span data-stu-id="452cc-113">Ledger accounts for postings are defined on the **Ledger posting setup** page.</span></span>

- <span data-ttu-id="452cc-114">Les transactions de temps sont validées en débitant le compte **Coût** et en créditant le compte **Affectation de la paie**.</span><span class="sxs-lookup"><span data-stu-id="452cc-114">Time transactions are posted by debiting the **Cost** account and crediting the **Payroll allocation** account.</span></span>
- <span data-ttu-id="452cc-115">Les transactions de dépense sont validées en débitant le compte **Coût** et en créditant le **Compte de contrepartie des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="452cc-115">Expense transactions are posted by debiting the **Cost** account and crediting the **Offset account for expense**.</span></span>
- <span data-ttu-id="452cc-116">Les transactions d’article sont validées en débitant le compte **Coût** et en créditant le compte **Coût – Article**.</span><span class="sxs-lookup"><span data-stu-id="452cc-116">Item transactions are posted by debiting the **Cost** account and crediting the **Cost - Item** account.</span></span>

<span data-ttu-id="452cc-117">Une fois les transactions validées sur le projet, si le projet est associé à un contrat de projet, le système contrepasse toutes les transactions cumulées et crée des transactions facturables.</span><span class="sxs-lookup"><span data-stu-id="452cc-117">After transactions are posted to the project, if the project is associated with a project contract, the system reverses all accumulated transactions and creates new billable transactions.</span></span> <span data-ttu-id="452cc-118">Les transactions facturables suivent les règles comptables définies dans le profil Coût et produit du projet concerné.</span><span class="sxs-lookup"><span data-stu-id="452cc-118">The billable transactions follow the accounting rules defined in respective Project cost and revenue profile.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
