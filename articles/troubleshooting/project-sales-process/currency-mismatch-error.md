---
title: Erreur de non-concordance des devises
description: Cet article fournit des informations de résolution de problème au sujet d’une erreur de non-concordance de devise qui se produit lorsque vous enregistrez des types d’enregistrement spécifiques.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914721"
---
# <a name="currency-mismatch-error"></a>Erreur de non-concordance des devises 

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Lorsque vous enregistrez un projet, un contrat, un devis ou une ressource réservable, vous pouvez recevoir l’erreur **La devise de la société propriétaire ne correspond pas à celle de l’unité contractuelle. Choisissez une autre société propriétaire ou une autre unité contractuelle pour continuer**. Cela est dû au fait qu’il existe une discordance de devise entre la devise de l’unité contractante pour l’enregistrement et la devise de la société propriétaire.


## <a name="resolution"></a>Résolution

Pour résoudre ce problème, procédez comme suit :
- Vérifiez la devise de l’unité contractante pour cet enregistrement. Vous pouvez voir la devise en ouvrant l’enregistrement de l’unité d’organisation et en vérifiant la valeur sur l’onglet **Général** dans le champ **Devise**.
- Vérifiez la devise de la société propriétaire. Vous pouvez voir la devise en accédant à **Associé** > **Écritures comptables** dans l’enregistrement de l’entreprise. Double-cliquez sur l’enregistrement du grand livre associé à la société et vérifiez la valeur dans l’onglet **Général** du champ **Devise comptable**.

Si la devise définie dans l’unité contractante et l’enregistrement de la comptabilité ne correspondent pas, ajustez la configuration ou sélectionnez des valeurs différentes lorsque vous enregistrez l’enregistrement. Le système exige que ces enregistrements coïncident pour garantir des flux de facturation intersociétés corrects. Pour plus d’informations sur les configurations intersociétés, voir [Créer des transactions intersociétés](../../project-accounting/create-intercompany-transactions.md).

Si l’enregistrement de l’entreprise ne comporte pas d’enregistrement de comptabilité associé, cela indique qu’il manque un paramétrage dans la configuration de l’environnement. La configuration doit être corrigée par l’administrateur système. L’administrateur système doit accéder aux **Configurations de double écriture** et arrêter et redémarrer le **Mappage en double écriture des grands livres** avec la synchronisation initiale de ce mappage et ses conditions préalables. Pour plus d’informations, consultez [Versions du mappage à double écriture Project Operations](../../environment/resource-dual-write-maps.md).