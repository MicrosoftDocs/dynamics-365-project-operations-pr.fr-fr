---
title: Vue d’ensemble de l’utilisation des ressources
description: Cette rubrique fournit des informations sur l’utilisation des ressources dans Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a683931bcd6a357c5feec9198b190b948ad17a40
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000793"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="dc75c-103">Vue d’ensemble de l’utilisation des ressources</span><span class="sxs-lookup"><span data-stu-id="dc75c-103">Resource utilization overview</span></span>

<span data-ttu-id="dc75c-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="dc75c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dc75c-105">Les ressources peuvent avoir une utilisation facturable cible.</span><span class="sxs-lookup"><span data-stu-id="dc75c-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="dc75c-106">Cette utilisation cible est définie soit comme un attribut dans le rôle par défaut d’une ressource, soit sur l’enregistrement de la ressource réservable individuelle.</span><span class="sxs-lookup"><span data-stu-id="dc75c-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="dc75c-107">Les calculs de l’utilisation sont basés sur les heures réelles déclarées par des ressources à l’aide d’entrées de temps approuvées.</span><span class="sxs-lookup"><span data-stu-id="dc75c-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="dc75c-108">Les formules suivantes sont utilisées pour calculer l’utilisation :</span><span class="sxs-lookup"><span data-stu-id="dc75c-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="dc75c-109">Utilisation facturable = Heures réelles facturables ÷ Capacité ressource</span><span class="sxs-lookup"><span data-stu-id="dc75c-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="dc75c-110">Utilisation non facturable = Temps réel avec ID du type de facturation = Non facturable, Gratuit ou Non disponible ÷ Capacité ressource</span><span class="sxs-lookup"><span data-stu-id="dc75c-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="dc75c-111">Interne = Temps réel sans contrat de vente ÷ Capacité ressource</span><span class="sxs-lookup"><span data-stu-id="dc75c-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="dc75c-112">Capacité ressource = Heures de travail de la ressource – Absence du bureau – Jours non ouvrables</span><span class="sxs-lookup"><span data-stu-id="dc75c-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="dc75c-113">Vous trouverez la vue **Utilisation des ressources** dans le volet **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="dc75c-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="dc75c-114">Chaque cellule dans la grille représente le pourcentage total d’utilisation de la ressource à une période, par exemple un jour, une semaine ou un mois.</span><span class="sxs-lookup"><span data-stu-id="dc75c-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="dc75c-115">Les formules suivantes sont utilisées pour colorer les cellules :</span><span class="sxs-lookup"><span data-stu-id="dc75c-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="dc75c-116">**Vert** : utilisation facturable >= utilisation cible de la ressource</span><span class="sxs-lookup"><span data-stu-id="dc75c-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="dc75c-117">**Jaune** : utilisation cible – 20 <= utilisation facturable <= utilisation cible</span><span class="sxs-lookup"><span data-stu-id="dc75c-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="dc75c-118">**Rouge** : utilisation facturable < utilisation cible - 20</span><span class="sxs-lookup"><span data-stu-id="dc75c-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="dc75c-119">Comme la vue **Utilisation des ressources** est basée sur le Tableau de planification, vous pouvez utiliser les fonctionnalités de filtrage du Tableau de planification pour filtrer vos résultats.</span><span class="sxs-lookup"><span data-stu-id="dc75c-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="dc75c-120">La grille nécessite que vous définissiez une utilisation cible du rôle ou de la ressource individuelle.</span><span class="sxs-lookup"><span data-stu-id="dc75c-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="dc75c-121">Pour effectuer cette configuration, accédez à **Ressources** > **Rôles des ressources**.</span><span class="sxs-lookup"><span data-stu-id="dc75c-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="dc75c-122">En outre, un rôle par défaut doit être affecté à chaque ressource réservable.</span><span class="sxs-lookup"><span data-stu-id="dc75c-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="dc75c-123">Accédez à **Ressources** > **Ressources**.</span><span class="sxs-lookup"><span data-stu-id="dc75c-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="dc75c-124">Dans l’onglet **Project Service**, vérifiez qu’un rôle de ressource est défini, et que le champ **Est la valeur par défaut** est défini sur **Oui**.</span><span class="sxs-lookup"><span data-stu-id="dc75c-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="dc75c-125">Vous pouvez ajouter des rôles supplémentaires où **Est la valeur par défaut** = **Non**.</span><span class="sxs-lookup"><span data-stu-id="dc75c-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="dc75c-126">Le rôle où **Est la valeur par défaut** = **Oui** est utilisé pour évaluer l’utilisation de la ressource par rapport à la cible de ce rôle.</span><span class="sxs-lookup"><span data-stu-id="dc75c-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="dc75c-127">Dans l’onglet **Project Service**, vous pouvez également définir une utilisation cible individuelle pour la ressource.</span><span class="sxs-lookup"><span data-stu-id="dc75c-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="dc75c-128">Le calcul de l’utilisation utilise ensuite cette utilisation cible pour évaluer la cible de la ressource au lieu de la cible du rôle par défaut de la ressource.</span><span class="sxs-lookup"><span data-stu-id="dc75c-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="dc75c-129">L’utilisation s’affiche uniquement pour une ressource si cette ressource est approuvée, temps facturable pendant la période affichée dans la grille.</span><span class="sxs-lookup"><span data-stu-id="dc75c-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]