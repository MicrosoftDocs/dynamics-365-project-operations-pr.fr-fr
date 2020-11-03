---
title: Désactiver une dimension de tarification
description: Cette rubrique indique comment configurer des dimensions de tarification dans la solution Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "4075825"
---
# <a name="turn-off-a-pricing-dimension"></a>Désactiver une dimension de tarification

Vous devez peut-être vérifier et mettre à jour régulièrement votre stratégie de tarification. Les mises à jour que vous effectuez peuvent nécessiter de désactiver une dimension de tarification existante et d'en créer une nouvelle. Par exemple, vous avez peut-être précédemment fixé le prix par **Rôle** , mais maintenant vous avez décidé de fixer le prix par **Expérience professionnelle**. Cela peut nécessiter de désactiver la valeur **Rôle** comme dimension de tarification et de créer la valeur **Expérience professionnelle** comme nouvelle dimension de tarification. 

La désactivation d'une dimension de tarification, qu'elle soit prédéfinie ou personnalisée, peut être effectuée en définissant les champs **Applicable aux coûts** et **Applicable aux ventes** de la dimension de tarification sur **Non**.

Toutefois, lorsque vous effectuez cette action, vous pouvez recevoir le message d'erreur suivant.

![Erreur de processus d'entreprise probablement lors de la désactivation d'une dimension de tarification](media/Business-Process-Error.png)


Ce message d'erreur indique que des enregistrements de prix ont été précédemment configurés pour la dimension désactivée. Tous les enregistrements **Prix du rôle** et **Majoration du prix du rôle** qui font référence à une dimension doivent être supprimés avant que l'applicabilité de la dimension puisse être définie sur **Non**. Cette règle s'applique à la fois aux dimensions de tarification prédéfinies et aux dimensions de tarification personnalisées que vous avez peut-être créées. La raison de cette validation est que Project Service a la contrainte que chaque enregistrement **Prix du rôle** doit avoir une combinaison unique de dimensions. Par exemple, sur une liste de prix appelée **Taux de coût US 2018** , les lignes **Prix du rôle** suivantes sont disponibles. 

| Titre standard         | Unité d'organisation    |Unité   |Prix  |Devise  |
| -----------------------|-------------|-------|-------|----------|
| Ingénieur système|Contoso US|Hour| 100|USD|
| Ingénieur senior système|Contoso US|Hour| 150| USD|


Lorsque vous désactivez la valeur **Titre standard** comme dimension de tarification et que le moteur de tarification de Project Service recherche un prix, il utilise uniquement la valeur **Unité d'organisation** dans le contexte d'entrée. Si la valeur **Unité d'organisation** du contexte d'entrée est « Contoso US », le résultat n'est pas déterministe car les deux lignes correspondent. Pour éviter ce scénario, lorsque vous créez des enregistrements **Prix du rôle** , Project Service valide que la combinaison de dimensions est unique. Si la dimension est désactivée après la création des enregistrements **Prix du rôle** , cette contrainte peut être enfreinte. Par conséquent, avant de désactiver une dimension, il est nécessaire de supprimer toutes les lignes **Prix du rôle** et **Majoration du prix du rôle** pour lesquelles cette valeur de dimension est renseignée.

