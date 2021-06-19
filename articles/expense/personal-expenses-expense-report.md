---
title: Utiliser les dépenses personnelles sur une note de frais
description: Cette rubrique fournit des informations sur la façon de gérer les dépenses personnelles engagées par les employés lors de leurs déplacements professionnels.
author: suvaidya
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: ae25eca08089d224f1e17e95eeb571054de8a5c0
ms.sourcegitcommit: fd6e9ff78392c7bac35591d9130c00d2750438ae
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "6025681"
---
# <a name="work-with-personal-expenses-on-an-expense-report"></a><span data-ttu-id="cafb3-103">Utiliser les dépenses personnelles sur une note de frais</span><span class="sxs-lookup"><span data-stu-id="cafb3-103">Work with personal expenses on an expense report</span></span>

<span data-ttu-id="cafb3-104">_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_</span><span class="sxs-lookup"><span data-stu-id="cafb3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cafb3-105">Lors de déplacements professionnels, un employé peut parfois débiter leur carte de crédit d’entreprise pour ses dépenses personnelles.</span><span class="sxs-lookup"><span data-stu-id="cafb3-105">During business travel, an employee might charge personal expenses to their corporate credit card.</span></span> <span data-ttu-id="cafb3-106">Si vous ne définissez pas de processus de gestion des dépenses personnelles lorsqu’un collaborateur soumet ses notes de frais détaillées, le processus d’approbation des notes de frais peut être perturbé.</span><span class="sxs-lookup"><span data-stu-id="cafb3-106">If a process hasn't been defined for handling personal expenses, the expense report approval process might be disrupted when an employee submits their itemized expense report.</span></span>

<span data-ttu-id="cafb3-107">Il existe deux méthodes que vous pouvez utiliser pour gérer les dépenses personnelles d’un employé :</span><span class="sxs-lookup"><span data-stu-id="cafb3-107">There are two methods you can use to work with an employee's personal expenses:</span></span>

  - <span data-ttu-id="cafb3-108">**Payé par l’employé** : Votre organisation ne paie pas les dépenses personnelles qui apparaissent sur la facture de la carte de crédit d’entreprise.</span><span class="sxs-lookup"><span data-stu-id="cafb3-108">**Paid by employee**: Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="cafb3-109">Au lieu de cela, l’employé paie directement le fournisseur de la carte de crédit pour les dépenses.</span><span class="sxs-lookup"><span data-stu-id="cafb3-109">Instead, the employee pays the credit card vendor directly for the expenses.</span></span> 
  - <span data-ttu-id="cafb3-110">**Payé par l’entreprise** : Votre organisation paie la totalité de la facture de la carte de crédit d’entreprise, puis débite le compte du travailleur pour les dépenses personnelles.</span><span class="sxs-lookup"><span data-stu-id="cafb3-110">**Paid by company**: Your organization pays the full bill for the corporate credit card, and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="cafb3-111">Vous pouvez sélectionner la méthode que votre organisation utilise sur la page **Paramètres de gestion des dépenses**.</span><span class="sxs-lookup"><span data-stu-id="cafb3-111">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>


## <a name="enable-split-expense-function-when-personal-amount-field-has-value-defined"></a><span data-ttu-id="cafb3-112">Activer la fonction de fractionnement des dépenses lorsque le champ de montant personnel a une valeur définie</span><span class="sxs-lookup"><span data-stu-id="cafb3-112">Enable split expense function when personal amount field has value defined</span></span>

<span data-ttu-id="cafb3-113">La fonctionnalité **Activer la fonction de fractionnement des dépenses lorsque le champ de montant personnel a une valeur définie** s’applique uniquement aux notes de frais approuvées à l’aide d’un workflow au niveau de la ligne.</span><span class="sxs-lookup"><span data-stu-id="cafb3-113">The feature, **Enable split expense function when personal amount field has value defined** only applies to expense reports that are approved using a line-level workflow.</span></span> <span data-ttu-id="cafb3-114">Les notes sont approuvées en accédant à **Traiter les notes de frais** > **Notes de frais qui me sont affectées** > **Ouvrir la note de frais**.</span><span class="sxs-lookup"><span data-stu-id="cafb3-114">Reports are approved by going to **Process expense reports** > **Expense reports assigned to me** > **Open expense report**.</span></span> 

<span data-ttu-id="cafb3-115">Pour activer cette fonctionnalité, accédez à **Espaces de travail** > **Gestion des fonctionnalités**, sélectionnez **Activer la fonction de fractionnement des dépenses lorsque le champ de montant personnel a une valeur définie**, puis sélectionnez **Activer maintenant**.</span><span class="sxs-lookup"><span data-stu-id="cafb3-115">To enable this feature, go to **Workspaces** > **Feature Management**, select **Enable split expense function when personal amount field has value defined**, and then select **Enable now**.</span></span> 

<span data-ttu-id="cafb3-116">Lorsque la fonctionnalité est activée, les lignes de dépenses qui utilisent cette fonctionnalité génèrent deux lignes lors de la soumission de la note.</span><span class="sxs-lookup"><span data-stu-id="cafb3-116">When the feature is enabled, expense lines that use this functionality generate two lines when the report is submitted.</span></span> <span data-ttu-id="cafb3-117">Deux lignes sont générées afin que l’approbateur puisse approuver chaque ligne séparément.</span><span class="sxs-lookup"><span data-stu-id="cafb3-117">Two lines are generated so that the approver can approve each line separately.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
