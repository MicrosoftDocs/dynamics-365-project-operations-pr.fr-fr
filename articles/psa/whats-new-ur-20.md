---
title: Nouveautés ou modifications de la mise à jour (version 20) de Project Service Automation (correctif logiciel), V3
description: Cette rubrique répertorie les fonctionnalités et les correctifs disponibles dans la mise à jour (version 20) de Project Service Automation, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 12edae76dbc6de63d3e2d36058c4092f80ede77d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075689"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="e117d-103">Mise à jour (version 20) de Project Service Automation, V3</span><span class="sxs-lookup"><span data-stu-id="e117d-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="e117d-104">Nous sommes heureux d'annoncer la dernière mise à jour de l'application Project Service Automation pour Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e117d-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e117d-105">Cette version comprend des améliorations importantes de la qualité, des performances et de l'utilisation.</span><span class="sxs-lookup"><span data-stu-id="e117d-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e117d-106">Cette version est compatible avec Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="e117d-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e117d-107">Pour effectuer une mise à jour vers cette version, visitez la page des solutions du centre d'administration de Dynamics 365 online pour installer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="e117d-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e117d-108">Pour plus d'informations, voir [Installer, mettre à jour ou supprimer une solution par défaut](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e117d-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e117d-109">Cette rubrique répertorie les fonctionnalités et les correctifs nouveaux ou modifiés pour la mise à jour (version 20) de Project Service Automation V3.</span><span class="sxs-lookup"><span data-stu-id="e117d-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="e117d-110">Cette version a le numéro de build V 3.10.31.37 et est généralement disponible via une mise à jour automatique en juin 2020.</span><span class="sxs-lookup"><span data-stu-id="e117d-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="e117d-111">Mise à jour (version 20)</span><span class="sxs-lookup"><span data-stu-id="e117d-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e117d-112">Corrections de bogues</span><span class="sxs-lookup"><span data-stu-id="e117d-112">Bug fixes</span></span>

<span data-ttu-id="e117d-113">**Gestion du projet**</span><span class="sxs-lookup"><span data-stu-id="e117d-113">**Project Management**</span></span>

<span data-ttu-id="e117d-114">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="e117d-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e117d-115">L'importation des membres de l'équipe du projet avec une méthode d'allocation nécessitant des heures entraîne un message d'erreur peu explicite lorsque les heures spécifiées sont nulles.</span><span class="sxs-lookup"><span data-stu-id="e117d-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="e117d-116">Les utilisateurs reçoivent une erreur incorrecte lorsque le nombre maximal de caractères a été entré dans le champ **Description** pour une tâche de projet.</span><span class="sxs-lookup"><span data-stu-id="e117d-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="e117d-117">La page de **téléchargement du complément Microsoft Dynamics 365 Project Service Automation** redirige vers la page de téléchargement en anglais lorsque les paramètres de langue de l'utilisateur sont définis sur Japonais.</span><span class="sxs-lookup"><span data-stu-id="e117d-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="e117d-118">Lorsqu'une erreur de serveur se produit, l'étiquette de synchronisation dans l'onglet **Planifier** du formulaire **Projets** est parfois conservée.</span><span class="sxs-lookup"><span data-stu-id="e117d-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="e117d-119">Les mises à jour de tâche redondantes sont envoyées au serveur lorsqu'une tâche est modifiée.</span><span class="sxs-lookup"><span data-stu-id="e117d-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="e117d-120">**Ventes**</span><span class="sxs-lookup"><span data-stu-id="e117d-120">**Sales**</span></span>

<span data-ttu-id="e117d-121">Les problèmes suivants ont été résolus :</span><span class="sxs-lookup"><span data-stu-id="e117d-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="e117d-122">Sur le formulaire **Contrat** , un double-clic sur **Créer une facture** crée deux factures pour un seul enregistrement de chiffres réels.</span><span class="sxs-lookup"><span data-stu-id="e117d-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="e117d-123">Dans Internet Explorer 11, les utilisateurs ne peuvent pas créer d'entrées de dépenses.</span><span class="sxs-lookup"><span data-stu-id="e117d-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="e117d-124">La contrepassation du coût et la contrepassation des chiffres réels des ventes non facturées ne sont pas liées.</span><span class="sxs-lookup"><span data-stu-id="e117d-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="e117d-125">Le bouton **Actualiser les chiffres réels** du formulaire **Projet** n'actualise pas les **Heures réelles de la tâche**.</span><span class="sxs-lookup"><span data-stu-id="e117d-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="e117d-126">Le plug-in **PreValidateProjectTeamMemberCreate** peut créer des ressources réservables génériques en double lorsque l'attribut **msdyn_isgenericresourceprojectscoped** est défini sur **False**.</span><span class="sxs-lookup"><span data-stu-id="e117d-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="e117d-127">**Recalculer** efface les coûts facturables des détails de la ligne de devis basés sur le produit et des détails de la ligne de contrat.</span><span class="sxs-lookup"><span data-stu-id="e117d-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="e117d-128">Dans des scénarios spécifiques, le plug-in **PostEstimateLineUpdate** affiche une erreur d'exception de référence nulle.</span><span class="sxs-lookup"><span data-stu-id="e117d-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="e117d-129">La durée de la phase de temps sur le **Graphique d'analyse de la rentabilité** ne correspond pas à la durée des coûts dans les détails de la ligne de devis à prix fixe du devis.</span><span class="sxs-lookup"><span data-stu-id="e117d-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="e117d-130">Les valeurs d'unité et de groupe d'unités ne sont pas correctement définies par défaut pour les catégories de dépense sur les formulaires **Détails de la ligne de contrat** et **Détails de la ligne de devis**.</span><span class="sxs-lookup"><span data-stu-id="e117d-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="e117d-131">Les listes **Prix de revient de l'unité d'organisation** autorisent les chevauchements dans la plage de dates définie.</span><span class="sxs-lookup"><span data-stu-id="e117d-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="e117d-132">Les utilisateurs ne sont pas autorisés à modifier **OrgUnit** lorsque le type de commande n'est pas basé sur le travail, car cela va générer une erreur d'exception de référence nulle.</span><span class="sxs-lookup"><span data-stu-id="e117d-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="e117d-133">Lorsque vous tentez de passer du formulaire **Détails de la ligne de devis** à l'onglet **Devis** , le formulaire s'actualise et affiche l'onglet **Résumé**.</span><span class="sxs-lookup"><span data-stu-id="e117d-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
