---
title: Fermer un devis – Simplifié
description: Cet article fournit des informations sur la clôture d’un devis dans Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e3a199843f379dc53d63372f91e8be2e1bcbf4e9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916929"
---
# <a name="close-a-quote---lite"></a>Fermer un devis – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Un devis de projet peut être fermé comme « conclu » ou » perdu ». Un projet de devis peut être fermé car les opérations d’activation et de révision sur les devis ne sont pas prises en charge dans Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Fermer un devis comme conclu

Lorsque vous fermez un devis de projet comme Gagné, le statut est défini sur Fermé et le raison du statut est Gagné. La fermeture du devis rend le devis du projet en lecture seule et crée un brouillon de contrat de projet contenant toutes les informations de devis. Comme un devis fermé ne peut pas être rouvert, une boîte de dialogue de confirmation confirmera vos modifications.

Si le devis est associé à une opportunité, tous les autres devis de projet sur l’opportunité sont automatiquement fermés comme perdus.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impact financier de la clôture d’un devis comme Conclu

S’il y a des chiffres réels pour le temps sur un projet alors qu’il est toujours joint à une ébauche de devis, seul le coût du temps ou des dépenses est enregistré. Une fois qu’un devis est clôturé comme Conclu, l’application refactorise les coûts en inversant les anciens chiffres réels de coûts et en recréant les chiffres réels de coûts. L’application traitera ces chiffres réels de coûts en fonction du mode de facturation de la ligne de contrat de projet associée. Si les coûts réels font référence à une ligne de contrat temps et matières, les chiffres réels de ventes non facturés correspondants sont créés pour la clôture du devis et la création du contrat de projet. Si les coûts réels font référence à une ligne de contrat à prix fixe, l’application arrête de retraiter les coûts réels basés sur les règles de facturation fractionnée pour les clients du contrat de projet.

## <a name="closing-a-quote-as-lost"></a>Fermeture d’un devis comme perdu :

Lorsque vous fermez un devis de projet comme Perdu, le statut est défini sur Fermé et le raison du statut est Perdu. La fermeture du devis rend le devis du projet en lecture seule. Étant donné qu’un devis fermé ne peut pas être rouvert et, avant de fermer un devis, une boîte de dialogue de confirmation confirmera vos modifications.

Si le devis de projet fermé comme Perdu fait référence à un projet sur l’une de ses lignes, ce projet est également marqué comme Fermé. Toutes les réservations de ressources à partir de ce jour sont annulées.

> [!NOTE]
> Dans Project Operations, la fermeture d’un devis comme conclu ou perdu n’aura aucune incidence sur ce statut de l’opportunité, qui restera ouverte jusqu’à ce qu’elle soit fermée manuellement.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]