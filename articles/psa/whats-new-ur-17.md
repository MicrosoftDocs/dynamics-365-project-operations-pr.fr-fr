---
title: Nouveautés ou modifications de la mise à jour (version 17) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles pour la mise à jour (version 17) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 12df166e1bd1b5f0e11d79dc24122fb1ed7e6e6c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280800"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="5ddab-103">Mise à jour (version 17) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="5ddab-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5ddab-104">Nous sommes heureux d’annoncer la dernière mise à jour de l’application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5ddab-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="5ddab-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5ddab-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="5ddab-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5ddab-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5ddab-107">Pour effectuer une mise à jour vers cette version, visitez le centre d’administration de Dynamics 365 (en ligne) et accédez à la page des solutions pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5ddab-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="5ddab-108">Pour plus d’informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5ddab-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5ddab-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 17) de PSA V3.</span><span class="sxs-lookup"><span data-stu-id="5ddab-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="5ddab-110">Cette version a le numéro de build V3.10.6.34 et sera disponible partout par mise à jour automatique en mars 2020.</span><span class="sxs-lookup"><span data-stu-id="5ddab-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="5ddab-111">Mise à jour (version 17)</span><span class="sxs-lookup"><span data-stu-id="5ddab-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5ddab-112">Correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="5ddab-112">Bug fixes</span></span>

<span data-ttu-id="5ddab-113">**Général**</span><span class="sxs-lookup"><span data-stu-id="5ddab-113">**General**</span></span>

- <span data-ttu-id="5ddab-114">Résolu : Mise à jour de Project Service Automation pour appliquer des licences Team Member (Project Resource Hub comprendra les métadonnées 3.x du plan relatif à Team Member)</span><span class="sxs-lookup"><span data-stu-id="5ddab-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="5ddab-115">**Temps et dépenses**</span><span class="sxs-lookup"><span data-stu-id="5ddab-115">**Time and Expense**</span></span>

- <span data-ttu-id="5ddab-116">Résolu : Il n’est pas possible de remplacer une estimation de dépenses d’un prix non nul par zéro (0).</span><span class="sxs-lookup"><span data-stu-id="5ddab-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="5ddab-117">La modification est ignorée.</span><span class="sxs-lookup"><span data-stu-id="5ddab-117">The change is ignored.</span></span>

<span data-ttu-id="5ddab-118">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="5ddab-118">**Project Management**</span></span>

- <span data-ttu-id="5ddab-119">Résolu : Une vérification des valeurs nulles a été ajoutée sur le nom du poste d’un membre de l’équipe.</span><span class="sxs-lookup"><span data-stu-id="5ddab-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="5ddab-120">Résolu : Le champ **msdyn_userresourceid** de l’entité **msdyn_resourceassignment** est devenue obsolète.</span><span class="sxs-lookup"><span data-stu-id="5ddab-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="5ddab-121">Résolu : La mise à niveau de 2.x à 3.x gère désormais les cadres de travail vides sur les affectations de tâches.</span><span class="sxs-lookup"><span data-stu-id="5ddab-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="5ddab-122">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="5ddab-122">**Sales**</span></span>

- <span data-ttu-id="5ddab-123">Résolu : **Invoice.PreValidateInvoiceUpdate** gère désormais correctement le scénario de réaffectation des propriétaires d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="5ddab-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="5ddab-124">Résolu : Lorsque la classe de transaction est **Temps**, **UnitGroup** n’est pas modifiable pour toutes les entités, y compris **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** et **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="5ddab-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="5ddab-125">Cependant, **Unité** est non modifiable uniquement pour **JournalLine** et **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="5ddab-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]