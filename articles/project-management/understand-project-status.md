---
title: Comprendre le statut du projet
description: Cette rubrique fournit des informations sur le statut attribué aux projets dans Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965673"
---
# <a name="understand-project-status"></a><span data-ttu-id="8d84a-103">Comprendre le statut du projet</span><span class="sxs-lookup"><span data-stu-id="8d84a-103">Understand project status</span></span>

<span data-ttu-id="8d84a-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="8d84a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8d84a-105">La section **Statut** sur la page **Entité de projet** fournit un résumé de l’intégrité d’un projet en fonction du coût et des efforts.</span><span class="sxs-lookup"><span data-stu-id="8d84a-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="8d84a-106">Champs récapitulatifs du statut</span><span class="sxs-lookup"><span data-stu-id="8d84a-106">Status summary fields</span></span>

- <span data-ttu-id="8d84a-107">Le champ **Statut du projet global** est un champ modifiable qui affiche le statut du projet global.</span><span class="sxs-lookup"><span data-stu-id="8d84a-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="8d84a-108">Ce champ utilise le codage de couleurs, par exemple le vert, le jaune et le rouge pour indiquer un risque croissant.</span><span class="sxs-lookup"><span data-stu-id="8d84a-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="8d84a-109">Le champ **Commentaires** permet au chef de projet d’entrer des commentaires spécifiques relatifs au statut.</span><span class="sxs-lookup"><span data-stu-id="8d84a-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="8d84a-110">Le champ **Statut mis à jour le** n’est pas modifiable.</span><span class="sxs-lookup"><span data-stu-id="8d84a-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="8d84a-111">La valeur de ce champ est un horodatage qui indique la dernière mise à jour du statut.</span><span class="sxs-lookup"><span data-stu-id="8d84a-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="8d84a-112">Les champs **Performance de planification** et **Performances des coûts** sont définis à partir de la grille de suivi.</span><span class="sxs-lookup"><span data-stu-id="8d84a-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="8d84a-113">Lorsque l’écart de planification et des coûts du nœud racine dans la vue **Suivi des efforts** est positif, ces champs sont mis à jour sur **En avance**.</span><span class="sxs-lookup"><span data-stu-id="8d84a-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="8d84a-114">Lorsque l’écart de planification et des coûts du nœud racine est négatif, ces champs sont définis sur **En retard**.</span><span class="sxs-lookup"><span data-stu-id="8d84a-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
