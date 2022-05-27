---
title: Utiliser un champ existant dans Project Service comme dimension de tarification
description: Cette rubrique donne des informations sur l’utilisation de champs Project Service existants comme dimensions de tarification.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3d8251b4516b4598c9c92779c59b9609d8113ac9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580131"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>Utiliser un champ existant dans Project Service comme dimension de tarification

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) a plusieurs champs dans l’entité **Chiffres réels** qui peuvent être utilisés comme dimensions de tarification pour la tarification basée sur des ressources dans les organisations de projet. Par exemple, un champ courant est **Ressource réservable**. Les petites entreprises qui ont moins de 20 à 30 ressources facturables peuvent estimer qu’il est plus simple d’avoir des taux de facturation et de coût spécifiques à chaque ressource. Toutefois, avec l’augmentation de la main d’œuvre facturable, des taux spécifiques peut devenir irréaliste à maintenir car les taux de coût et de facturation des ressources commencent à varier à mesure que les ressources sont promues, ont plus d’expérience ou acquièrent des compétences différentes. Comme cette approche fonctionne toujours pour les entreprises d’une certaine taille, consultez [Utiliser une ressource réservable comme dimension de tarification](bookable-resource-pricing-dimension.md) pour comprendre comment un champ Project Service existant peut être utilisé comme dimension de tarification.

Un autre exemple est le champ Catégorie de transaction. Les clients et les responsables de l’implémentation utilisent la catégorie de transaction dans PSA pour classer le travail et utilisent le champ pour évaluer le prix et le coût selon la catégorie de travail. Pour plus d’informations, consultez [Utiliser une catégorie de transaction comme dimension de tarification](transaction-category-pricing-dimension.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
