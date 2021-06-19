---
title: Confirmer un contrat de projet
description: Cette rubrique fournit des informations sur le mode de confirmation d’un contrat dans Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003673"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="80e03-103">Confirmer un contrat de projet</span><span class="sxs-lookup"><span data-stu-id="80e03-103">Confirm a project contract</span></span>

<span data-ttu-id="80e03-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="80e03-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="80e03-105">Un contrat de projet dans Dynamics 365 Project Operations peut être actif avec la raison **Confirmé** ou fermé avec la raison **Perdu**.</span><span class="sxs-lookup"><span data-stu-id="80e03-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="80e03-106">Lorsque vous confirmez un contrat de projet, le statut est mis à jour en passant du statut de **Brouillon** au statut **Actif** et avec la raison de statut **Confirmé**.</span><span class="sxs-lookup"><span data-stu-id="80e03-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="80e03-107">Un contrat actif ou fermé ne peut pas être modifié ni rouvert.</span><span class="sxs-lookup"><span data-stu-id="80e03-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="80e03-108">Impact financier de la confirmation d’un contrat de projet</span><span class="sxs-lookup"><span data-stu-id="80e03-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="80e03-109">Après la confirmation d’un contrat de projet, l’application recalcule les coûts en contrepassant les anciens chiffres réels des coûts et en créant des chiffres réels des coûts.</span><span class="sxs-lookup"><span data-stu-id="80e03-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="80e03-110">Les nouveaux chiffres réels des coûts sont ensuite traités en fonction du mode de facturation de la ligne de contrat de projet associée.</span><span class="sxs-lookup"><span data-stu-id="80e03-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="80e03-111">Si les coûts réels font référence à une ligne de contrat Temps et matériel, l’application recrée automatiquement les chiffres réels des ventes non facturées correspondants.</span><span class="sxs-lookup"><span data-stu-id="80e03-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="80e03-112">Si les coûts réels font référence à une ligne de contrat à prix fixe, l’application arrête de retraiter les coûts réels.</span><span class="sxs-lookup"><span data-stu-id="80e03-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="80e03-113">Les limites à ne pas dépasser, la configuration de la chargeabilité, la tarification et le calcul des coûts réels sont évalués puis mis à jour dans le cadre du processus de confirmation.</span><span class="sxs-lookup"><span data-stu-id="80e03-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="80e03-114">Fermer un contrat de projet considéré Perdu</span><span class="sxs-lookup"><span data-stu-id="80e03-114">Close a project contract as lost</span></span>

<span data-ttu-id="80e03-115">Lorsque vous fermez un contrat de projet considéré perdu, le statut du contrat est mis à jour avec les statut **Fermé** et la raison du statut est **Perdu**.</span><span class="sxs-lookup"><span data-stu-id="80e03-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="80e03-116">Le contrat de projet passe en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="80e03-116">The project contract becomes read-only.</span></span> <span data-ttu-id="80e03-117">Une boîte de dialogue de confirmation est fournie avant la fin des modifications, car vous ne pouvez pas rouvrir un contrat de projet fermé.</span><span class="sxs-lookup"><span data-stu-id="80e03-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="80e03-118">Si le contrat de projet qui est fermé parce que considéré perdu fait référence à un projet sur ses lignes, ce projet est également marqué comme fermé.</span><span class="sxs-lookup"><span data-stu-id="80e03-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="80e03-119">Toutes les réservations de ressources à partir de ce jour sont annulées.</span><span class="sxs-lookup"><span data-stu-id="80e03-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="80e03-120">Les ventes réelles non facturées sur le contrat de projet qui ne figurent pas déjà sur une facture seront annulées.</span><span class="sxs-lookup"><span data-stu-id="80e03-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="80e03-121">Dans Dynamics 365 Project Operations, la fermeture d’un contrat de projet comme perdu n’affectera le statut de l’opportunité associée.</span><span class="sxs-lookup"><span data-stu-id="80e03-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="80e03-122">L’opportunité restera ouverte et doit être fermée manuellement.</span><span class="sxs-lookup"><span data-stu-id="80e03-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]