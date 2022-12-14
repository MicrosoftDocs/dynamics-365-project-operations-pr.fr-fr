---
title: Fermer les devis basés sur les projets
description: Cet article fournit des informations sur la clôture de devis dans Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b35417d4258a1e837fdf7a61bbcc303ec04a900
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824213"
---
# <a name="close-project-based-quotes"></a>Fermer les devis basés sur les projets

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Un devis de projet peut être fermé comme **conclu** ou **perdu**. 

## <a name="close-a-quote-as-won"></a>Fermer un devis comme conclu

La clôture d’un devis de projet comme conclu définira le statut du devis sur **Fermé** et la raison du statut sur **Conclu**. La fermeture des devis les rend en lecture seule et crée un brouillon de contrat de projet avec toutes les informations de devis. Étant donné qu’un devis fermé ne peut pas être rouvert, avant de fermer un devis, une boîte de dialogue de confirmation confirmera vos modifications.

Le contrat de projet créé à partir d’un devis de projet est également mis à disposition dans le module Gestion de projet et comptabilité de Project Operations. Si un contrat de projet n’est mappé à un projet sur aucune de ses lignes, ce contrat de projet est mis à disposition en tant que contrat de projet inactif et devient actif dès qu’un projet est mappé à au moins une de ses lignes de contrat.

Si le devis est associé à une opportunité, tous les autres devis de projet sur l’opportunité sont automatiquement fermés comme perdus.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impact financier de la clôture d’un devis comme Conclu

S’il y a eu des chiffres réels pour le temps enregistré sur un projet alors qu’il est encore joint à un projet de devis, seul le coût du temps ou de la dépense est enregistré. Une fois qu’un devis est clôturé comme Conclu, l’application refactorise les coûts en inversant les anciens chiffres réels de coûts et en recréant les chiffres réels de coûts. L’application traitera ces chiffres réels de coûts en fonction du mode de facturation de la ligne de contrat de projet associée. Si les chiffres réels de coûts font référence à une ligne de contrat de temps et d’article, le système créera automatiquement les chiffres réels des ventes non facturés correspondants lorsque le devis est clôturé et que le contrat de projet est créé. Si les chiffres réels de coûts font référence à une ligne de contrat à prix fixe, l’application arrête de retraiter les chiffres réels de coûts en fonction des règles de facturation fractionnée pour les clients du contrat de projet.

Tous les chiffres réels retraités sont disponibles dans le module Gestion de projet et comptabilité pour que le comptable du projet puisse les vérifier, les mettre à jour et les enregistrer dans la comptabilité. 

## <a name="close-a-quote-as-lost"></a>Fermer un devis comme Perdu

La clôture d’un devis de projet comme Perdu définira le statut sur **Fermé** et la raison du statut sur **Perdu**. La fermeture du devis le rend en lecture seule. Étant donné qu’un devis fermé ne peut pas être rouvert et, avant de fermer un devis, une boîte de dialogue de confirmation confirmera vos modifications.

Si le devis de projet qui est fermé comme perdu a un projet référencé sur l’une de ses lignes, ce projet est également marqué comme fermé et toutes les réservations de ressources à partir de ce jour sont annulées.

> [!NOTE]
> Dans Project Operations, la fermeture d’un devis comme conclu ou perdu n’aura aucune incidence sur ce statut de l’opportunité, qui restera ouverte jusqu’à ce qu’elle soit fermée manuellement.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
