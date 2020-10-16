---
title: Fermer des devis
description: Cette rubrique offre des informations sur la conclusion un devis dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896188"
---
# <a name="close-quotes"></a><span data-ttu-id="473ea-103">Fermer des devis</span><span class="sxs-lookup"><span data-stu-id="473ea-103">Close quotes</span></span> 

<span data-ttu-id="473ea-104">_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="473ea-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="473ea-105">Un devis de projet peut être fermé comme « conclu » ou » perdu ».</span><span class="sxs-lookup"><span data-stu-id="473ea-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="473ea-106">Les opérations Activer et Réviser sur les devis ne sont pas prises en charge dans Microsoft Dynamics 365 Project Operations, vous pouvez donc fermer un brouillon de devis.</span><span class="sxs-lookup"><span data-stu-id="473ea-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="473ea-107">Fermer un devis comme conclu</span><span class="sxs-lookup"><span data-stu-id="473ea-107">Close a quote as Won</span></span>

<span data-ttu-id="473ea-108">La clôture d’un devis de projet comme conclu fermera le statut du devis comme Fermé et la raison du statut comme Conclu.</span><span class="sxs-lookup"><span data-stu-id="473ea-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="473ea-109">La fermeture du devis rend le devis du projet en lecture seule et crée un brouillon de contrat de projet contenant toutes les informations de devis.</span><span class="sxs-lookup"><span data-stu-id="473ea-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="473ea-110">Puisqu’un devis fermé ne peut pas être rouvert, une boîte de dialogue de confirmation de confirmation s’ouvre avant que les modifications ne soient effectuées, car un devis fermé ne peut pas être rouvert et les modifications sont irréversibles.</span><span class="sxs-lookup"><span data-stu-id="473ea-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="473ea-111">Si le devis est associé à une opportunité, tous les autres devis de projet sur l’opportunité sont automatiquement fermés comme perdus.</span><span class="sxs-lookup"><span data-stu-id="473ea-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="473ea-112">Impact financier de la clôture d’un devis comme Conclu</span><span class="sxs-lookup"><span data-stu-id="473ea-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="473ea-113">S’il y a eu des chiffres réels pour le temps enregistré sur un projet alors qu’il est encore joint à un projet de devis, seul le coût du temps ou de la dépense est enregistré.</span><span class="sxs-lookup"><span data-stu-id="473ea-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="473ea-114">Une fois qu’un devis est clôturé comme Conclu, l’application refactorise les coûts en inversant les anciens chiffres réels de coûts et en recréant les chiffres réels de coûts.</span><span class="sxs-lookup"><span data-stu-id="473ea-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="473ea-115">L’application traitera ces chiffres réels de coûts en fonction du mode de facturation de la ligne de contrat de projet associée.</span><span class="sxs-lookup"><span data-stu-id="473ea-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="473ea-116">Si les chiffres réels de coûts font référence à une ligne de contrat de temps et d’article, le système créera automatiquement les chiffres réels des ventes non facturés correspondants lorsque le devis est clôturé et que le contrat de projet est créé.</span><span class="sxs-lookup"><span data-stu-id="473ea-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="473ea-117">Si les chiffres réels de coûts font référence à une ligne de contrat à prix fixe, l’application arrête de retraiter les chiffres réels de coûts en fonction des règles de facturation fractionnée pour les clients du contrat de projet.</span><span class="sxs-lookup"><span data-stu-id="473ea-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="473ea-118">Fermeture d’un devis comme perdu :</span><span class="sxs-lookup"><span data-stu-id="473ea-118">Closing a quote as lost:</span></span>

<span data-ttu-id="473ea-119">La clôture d’un devis de projet comme Perdu définira le statut sur Fermé et la raison du statut sur Perdu.</span><span class="sxs-lookup"><span data-stu-id="473ea-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="473ea-120">La fermeture du devis rend le devis du projet en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="473ea-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="473ea-121">Étant donné qu’un devis fermé ne peut pas être rouvert et, avant de fermer un devis, une boîte de dialogue de confirmation confirmera vos modifications.</span><span class="sxs-lookup"><span data-stu-id="473ea-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="473ea-122">Si le devis de projet qui est fermé comme perdu a un projet référencé sur l’une de ses lignes, ce projet est également marqué comme fermé et toutes les réservations de ressources à partir de ce jour sont annulées.</span><span class="sxs-lookup"><span data-stu-id="473ea-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="473ea-123">Dans Project Operations, la fermeture d’un devis comme conclu ou perdu n’aura aucune incidence sur ce statut de l’opportunité, qui restera ouverte jusqu’à ce qu’elle soit fermée manuellement.</span><span class="sxs-lookup"><span data-stu-id="473ea-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
