---
title: Nouveautés ou modifications de la mise à jour (version 13) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique donne des informations sur les nouveautés de la mise à jour (version 13) de Project Service Automation, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075700"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="11979-103">Mise à jour (version 13) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="11979-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="11979-104">Nous sommes heureux d'annoncer la dernière mise à jour de l'application Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="11979-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="11979-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="11979-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="11979-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="11979-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="11979-107">Pour effectuer une mise à jour vers cette version, visitez le centre d'administration de Dynamics 365 Online et accédez à la page des solutions pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="11979-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="11979-108">Pour plus d'informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="11979-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="11979-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 13) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="11979-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="11979-110">Cette version a le numéro de build V3.10.3.18 et est disponible selon le calendrier suivant :</span><span class="sxs-lookup"><span data-stu-id="11979-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="11979-111">**Disponibilité générale (mise à jour automatique) :** novembre 2019</span><span class="sxs-lookup"><span data-stu-id="11979-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="11979-112">**Mise à jour automatique :** décembre 2019</span><span class="sxs-lookup"><span data-stu-id="11979-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="11979-113">Mise à jour (version 13)</span><span class="sxs-lookup"><span data-stu-id="11979-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="11979-114">Correctifs de bogues</span><span class="sxs-lookup"><span data-stu-id="11979-114">Bug fixes</span></span>

- <span data-ttu-id="11979-115">Temps et dépenses</span><span class="sxs-lookup"><span data-stu-id="11979-115">Time and Expense</span></span>

     - <span data-ttu-id="11979-116">Correction : la fonctionnalité de recherche sur la page **Approbation des dépenses** ne fonctionne pas lorsque vous effectuez une recherche par objectif de dépense.</span><span class="sxs-lookup"><span data-stu-id="11979-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="11979-117">Gestion des ressources</span><span class="sxs-lookup"><span data-stu-id="11979-117">Resource Management</span></span>

     - <span data-ttu-id="11979-118">Correction : les nombres dans la vue Rapprochement ont été mis à jour pour être justifiés à droite.</span><span class="sxs-lookup"><span data-stu-id="11979-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="11979-119">Correction : les ressources nommées ne peuvent pas être affectées à des tâches via l'onglet **Planning**.</span><span class="sxs-lookup"><span data-stu-id="11979-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="11979-120">Gestion du projet</span><span class="sxs-lookup"><span data-stu-id="11979-120">Project Management</span></span>

     - <span data-ttu-id="11979-121">Correction : exception de référence nulle lors de l'affectation d'un membre de l'équipe lorsque les informations de configuration de **TransactionType** sont manquantes pour **Unit** et **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="11979-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="11979-122">Ventes</span><span class="sxs-lookup"><span data-stu-id="11979-122">Sales</span></span>

     - <span data-ttu-id="11979-123">Correction : les enregistrements de type de transaction en double renvoient une erreur lors de la création des enregistrements de prix de rôle.</span><span class="sxs-lookup"><span data-stu-id="11979-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="11979-124">Correction : les boutons supplémentaires pour **Nouvelle opportunité** , **Devis** , **Ligne de commande** et **Ajouter un produit** sont visibles dans les commandes pour les opportunités, les devis, les produits de commande et la sous-grille Lignes basées sur le projet.</span><span class="sxs-lookup"><span data-stu-id="11979-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


