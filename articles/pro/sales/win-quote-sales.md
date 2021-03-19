---
title: Fermer un devis – Simplifié
description: Cette rubrique offre des informations sur la conclusion un devis dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6214e1b5bec5c9173a6b6e69578de14654da633e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272270"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="9ec89-103">Fermer un devis – Simplifié</span><span class="sxs-lookup"><span data-stu-id="9ec89-103">Close a quote - lite</span></span>

<span data-ttu-id="9ec89-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="9ec89-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9ec89-105">Un devis de projet peut être fermé comme « conclu » ou » perdu ».</span><span class="sxs-lookup"><span data-stu-id="9ec89-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="9ec89-106">Un projet de devis peut être fermé car les opérations d'activation et de révision sur les devis ne sont pas prises en charge dans Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="9ec89-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="9ec89-107">Fermer un devis comme conclu</span><span class="sxs-lookup"><span data-stu-id="9ec89-107">Close a quote as Won</span></span>

<span data-ttu-id="9ec89-108">Lorsque vous fermez un devis de projet comme Gagné, le statut est défini sur Fermé et le raison du statut est Gagné.</span><span class="sxs-lookup"><span data-stu-id="9ec89-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="9ec89-109">La fermeture du devis rend le devis du projet en lecture seule et crée un brouillon de contrat de projet contenant toutes les informations de devis.</span><span class="sxs-lookup"><span data-stu-id="9ec89-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="9ec89-110">Comme un devis fermé ne peut pas être rouvert, une boîte de dialogue de confirmation confirmera vos modifications.</span><span class="sxs-lookup"><span data-stu-id="9ec89-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="9ec89-111">Si le devis est associé à une opportunité, tous les autres devis de projet sur l’opportunité sont automatiquement fermés comme perdus.</span><span class="sxs-lookup"><span data-stu-id="9ec89-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="9ec89-112">Impact financier de la clôture d’un devis comme Conclu</span><span class="sxs-lookup"><span data-stu-id="9ec89-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="9ec89-113">S'il y a des chiffres réels pour le temps sur un projet alors qu'il est toujours joint à une ébauche de devis, seul le coût du temps ou des dépenses est enregistré.</span><span class="sxs-lookup"><span data-stu-id="9ec89-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="9ec89-114">Une fois qu’un devis est clôturé comme Conclu, l’application refactorise les coûts en inversant les anciens chiffres réels de coûts et en recréant les chiffres réels de coûts.</span><span class="sxs-lookup"><span data-stu-id="9ec89-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="9ec89-115">L’application traitera ces chiffres réels de coûts en fonction du mode de facturation de la ligne de contrat de projet associée.</span><span class="sxs-lookup"><span data-stu-id="9ec89-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="9ec89-116">Si les coûts réels font référence à une ligne de contrat temps et matières, les chiffres réels de ventes non facturés correspondants sont créés pour la clôture du devis et la création du contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="9ec89-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="9ec89-117">Si les coûts réels font référence à une ligne de contrat à prix fixe, l'application arrête de retraiter les coûts réels basés sur les règles de facturation fractionnée pour les clients du contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="9ec89-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="9ec89-118">Fermeture d’un devis comme perdu :</span><span class="sxs-lookup"><span data-stu-id="9ec89-118">Closing a quote as lost:</span></span>

<span data-ttu-id="9ec89-119">Lorsque vous fermez un devis de projet comme Perdu, le statut est défini sur Fermé et le raison du statut est Perdu.</span><span class="sxs-lookup"><span data-stu-id="9ec89-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="9ec89-120">La fermeture du devis rend le devis du projet en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="9ec89-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="9ec89-121">Étant donné qu’un devis fermé ne peut pas être rouvert et, avant de fermer un devis, une boîte de dialogue de confirmation confirmera vos modifications.</span><span class="sxs-lookup"><span data-stu-id="9ec89-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="9ec89-122">Si le devis de projet fermé comme Perdu fait référence à un projet sur l'une de ses lignes, ce projet est également marqué comme Fermé.</span><span class="sxs-lookup"><span data-stu-id="9ec89-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="9ec89-123">Toutes les réservations de ressources à partir de ce jour sont annulées.</span><span class="sxs-lookup"><span data-stu-id="9ec89-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="9ec89-124">Dans Project Operations, la fermeture d’un devis comme conclu ou perdu n’aura aucune incidence sur ce statut de l’opportunité, qui restera ouverte jusqu’à ce qu’elle soit fermée manuellement.</span><span class="sxs-lookup"><span data-stu-id="9ec89-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]