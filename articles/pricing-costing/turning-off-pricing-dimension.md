---
title: Désactiver une dimension de tarification
description: Cette rubrique donne des informations sur la désactivation des dimensions de tarification.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3d9f0cb2a054941b07809b61ca14a3145c6d6d06acd6ca40255d5ec9de92be22
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994498"
---
# <a name="turning-off-a-pricing-dimension"></a>Désactiver une dimension de tarification

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Vous devez peut-être vérifier et mettre à jour régulièrement votre stratégie de tarification. Les mises à jour que vous effectuez peuvent nécessiter de désactiver une dimension de tarification existante et d’en créer une nouvelle. Par exemple, vous avez peut-être précédemment fixé le prix par **Rôle**, mais maintenant vous avez décidé de fixer le prix par **Expérience professionnelle**. Cela peut nécessiter de désactiver la valeur **Rôle** comme dimension de tarification et de créer la valeur **Expérience professionnelle** comme nouvelle dimension de tarification. 

La désactivation d’une dimension de tarification, qu’elle soit prédéfinie ou personnalisée, peut être effectuée en définissant les champs **Applicable aux coûts** et **Applicable aux ventes** de la dimension de tarification sur **Non**.

Cependant, lorsque vous effectuez cette opération, il est possible que vous receviez ce message d’erreur, **La dimension de tarification ne peut pas être mise à jour ou supprimée s’il existe des enregistrements de prix associés.**

![Erreur de processus d’entreprise probablement lors de la désactivation d’une dimension de tarification.](media/Business-Process-Error.png)

Ce message d’erreur indique que des enregistrements de prix ont été précédemment configurés pour la dimension désactivée. Tous les enregistrements **Prix du rôle** et **Majoration du prix du rôle** qui font référence à une dimension doivent être supprimés avant que l’applicabilité de la dimension puisse être définie sur **Non**. Cette règle s’applique à la fois aux dimensions de tarification prédéfinies et aux dimensions de tarification personnalisées que vous avez peut-être créées. La raison de cette validation est que chaque enregistrement **Prix du rôle** doit avoir une combinaison unique de dimensions. Par exemple, sur une liste de prix appelée **Taux de coût US 2018**, les lignes **Prix du rôle** suivantes sont disponibles. 

| Titre standard         | Unité d’organisation    |Unité   |Prix  |Devise  |
| -----------------------|-------------|-------|-------|----------|
| Ingénieur système|Contoso US|heure| 100|USD|
| Ingénieur senior système|Contoso US|heure| 150| USD|


Lorsque vous désactivez la valeur **Titre standard** comme dimension de tarification et que le moteur de tarification recherche un prix, il utilise uniquement la valeur **Unité d’organisation** dans le contexte d’entrée. Si la valeur **Unité d’organisation** du contexte d’entrée est « Contoso US », le résultat n’est pas déterministe car les deux lignes correspondent. Pour éviter ce scénario, lorsque vous créez des enregistrements **Prix du rôle**, le système valide le fait que la combinaison de dimensions est unique. Si la dimension est désactivée après la création des enregistrements **Prix du rôle**, cette contrainte peut être enfreinte. Par conséquent, avant de désactiver une dimension, il est nécessaire de supprimer toutes les lignes **Prix du rôle** et **Majoration du prix du rôle** pour lesquelles cette valeur de dimension est renseignée.


[!INCLUDE[footer-include](../includes/footer-banner.md)]