---
title: Fermer un devis – Simplifié
description: Cette rubrique offre des informations sur la conclusion un devis dans Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ad206232d616cdbdc83e2a17b9177cfb98ffda9
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175708"
---
# <a name="close-a-quote---lite"></a>Fermer un devis – Simplifié

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Un devis de projet peut être fermé comme « conclu » ou » perdu ». Les opérations Activer et Réviser sur les devis ne sont pas prises en charge dans Microsoft Dynamics 365 Project Operations, vous pouvez donc fermer un brouillon de devis.

## <a name="close-a-quote-as-won"></a>Fermer un devis comme conclu

La clôture d’un devis de projet comme conclu fermera le statut du devis comme Fermé et la raison du statut comme Conclu. La fermeture du devis rend le devis du projet en lecture seule et crée un brouillon de contrat de projet contenant toutes les informations de devis. Puisqu’un devis fermé ne peut pas être rouvert, une boîte de dialogue de confirmation de confirmation s’ouvre avant que les modifications ne soient effectuées, car un devis fermé ne peut pas être rouvert et les modifications sont irréversibles.

Si le devis est associé à une opportunité, tous les autres devis de projet sur l’opportunité sont automatiquement fermés comme perdus.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Impact financier de la clôture d’un devis comme Conclu

S’il y a eu des chiffres réels pour le temps enregistré sur un projet alors qu’il est encore joint à un projet de devis, seul le coût du temps ou de la dépense est enregistré. Une fois qu’un devis est clôturé comme Conclu, l’application refactorise les coûts en inversant les anciens chiffres réels de coûts et en recréant les chiffres réels de coûts. L’application traitera ces chiffres réels de coûts en fonction du mode de facturation de la ligne de contrat de projet associée. Si les chiffres réels de coûts font référence à une ligne de contrat de temps et d’article, le système créera automatiquement les chiffres réels des ventes non facturés correspondants lorsque le devis est clôturé et que le contrat de projet est créé. Si les chiffres réels de coûts font référence à une ligne de contrat à prix fixe, l’application arrête de retraiter les chiffres réels de coûts en fonction des règles de facturation fractionnée pour les clients du contrat de projet.

## <a name="closing-a-quote-as-lost"></a>Fermeture d’un devis comme perdu :

La clôture d’un devis de projet comme Perdu définira le statut sur Fermé et la raison du statut sur Perdu. La fermeture du devis rend le devis du projet en lecture seule. Étant donné qu’un devis fermé ne peut pas être rouvert et, avant de fermer un devis, une boîte de dialogue de confirmation confirmera vos modifications.

Si le devis de projet qui est fermé comme perdu a un projet référencé sur l’une de ses lignes, ce projet est également marqué comme fermé et toutes les réservations de ressources à partir de ce jour sont annulées.

> [!NOTE]
> Dans Project Operations, la fermeture d’un devis comme conclu ou perdu n’aura aucune incidence sur ce statut de l’opportunité, qui restera ouverte jusqu’à ce qu’elle soit fermée manuellement.
