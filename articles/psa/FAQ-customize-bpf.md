---
title: Comment personnaliser le flux des processus d’entreprise des phases du projet ?
description: Vue d’ensemble de la personnalisation du flux des processus d’entreprise des phases du projet.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149000"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Comment personnaliser le flux des processus d’entreprise des phases du projet ?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Il existe une limitation connue dans les précédentes versions de l’application Project Service que les noms des phases dans le flux des processus d’entreprise des phases du projet doivent correspondre exactement aux noms anglais attendus (**Quote**, **Plan**, **Close**). Sinon, la logique métier, qui repose sur les noms de la phase en anglais, ne fonctionne pas comme prévu. C’est la raison pour laquelle des actions familières comme **Changer de processus** ou **Modifier le processus** n’apparaissent pas comme disponibles dans le formulaire du projet, et que la personnalisation du flux des processus d’entreprise n’est pas encouragée. 

Cette limite a été traitée dans la version 2.4.5.48 et versions ultérieures. Cet article fournit des solutions suggérées pour les versions antérieures si vous devez personnaliser le flux des processus d’entreprise par défaut.  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>La logique métier nécessite un correspondance exacte avec des noms de phase en anglais

Le flux des processus d’entreprise des phases du projet inclut une logique métier qui pilote les comportements suivants dans l’application :
- Lorsque le projet est associé à un devis, le code définit le flux des processus d’entreprise sur la phase **Quote**.
- Lorsque le projet est associé à un contrat, le code définit le flux des processus d’entreprise sur la phase **Plan**.
- Lorsque le flux des processus d’entreprise est avancé à la phase **Close**, l’enregistrement du projet est désactivé. Lorsque le projet est désactivé, le formulaire et la structure de répartition du travail (WBS) du projet sont définis sur lecture seule, les réservations de ressources nommées sont libérées, et tous les tarifs associés sont désactivés.

Cette logique métier repose sur les noms en anglais des phases du projet. Cette dépendance aux noms de phase en anglais est la principale raison pour laquelle la personnalisation du flux des processus d’entreprise des phases du projet n’est pas encouragée, de même que les actions de flux des processus d’entreprise courantes comme **Changer de processus** ou **Modifier le processus** n’apparaissent pas sur l’entité du projet.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Que se passe -t-il si les noms de phase ne correspondent pas aux noms en anglais ?

Dans la version 1.x de l’application Project Service sur la plateforme 8.2, lorsque les noms de phase du flux des processus d’entreprise ne correspondent pas exactement aux noms de phase en anglais, la logique métier qui définit la phase appropriée pour les devis ou les contrats, ou qui ferme le projet, est ignorée. Aucun message d’erreur ne s’affiche. Par conséquent il semble que vous puissiez personnaliser le flux des processus d’entreprise de phases du projet. Toutefois, vous ne verrez aucun des processus automatiques travailler sur des devis, des contrats, et la fermeture de projet.

Dans la version 2.4.4.30 de l’application Project Service ou version antérieure sur la plateforme 9.0, une modification de l’architecture cruciale a été apportée aux flux des processus d’entreprise, qui nécessitait une réécriture de la logique métier de flux des processus d’entreprise. Par conséquent, si les noms de phase de processus ne correspondent pas aux noms en anglais attendus, vous recevez un message d’erreur. 

Si vous souhaitez personnaliser le flux des processus d’entreprise de phase du projet pour l’entité de projet, vous pouvez donc uniquement ajouter de toutes nouvelles étapes au flux des processus d’entreprise par défaut pour l’entité de projet, tout en conservant les phases **Quote**, **Plan**, and **Close** actuelles. Cette restriction garantit que vous ne receviez pas d’erreurs de la logique métier qui prévoit des noms de phase en anglais dans le flux des processus d’entreprise.

Dans la version 2.4.5.48 ou ultérieure, la logique métier décrite dans cet article a été supprimée du flux des processus d’entreprise par défaut pour l’entité de projet. La mise à niveau vers cette version ou une version ultérieure vous permettra personnaliser ou de remplacer le flux des processus d’entreprise par défaut par l’un des vôtres. 

## <a name="workarounds-for-earlier-versions"></a>Solutions pour les versions antérieures

Si la mise à niveau n’est pas une option, vous pouvez personnaliser le flux des processus d’entreprise des phases du projet pour l’entité de projet de l’une des deux manières suivantes :

1. Ajoutez des étapes supplémentaires à la configuration par défaut, tout en conservant les noms de phase en anglais pour **Quote**, **Plan**, and **Close**.


![Capture d’écran de l’ajout d’étapes à la configuration par défaut](media/FAQ-Customize-BPF-1.png)
 
2. Créez votre propre flux des processus d’entreprise et faites-en le flux des processus d’entreprise principal de l’entité de projet, ce qui vous permet d’avoir tous les noms de phase de votre choix. Toutefois, si vous souhaitez utiliser les mêmes étapes de projet standard **Quote**, **Plan**, and **Close**, vous devez effectuer certaines personnalisations qui sont exclues des noms de phase personnalisés. La logique la plus complexe consiste à fermer le projet, que vous pouvez toujours déclencher en désactivant simplement l’enregistrement de projet.

![Personnalisation de BPF](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Considérations supplémentaires pour la version 2.4.4.30 de l’application Project Service ou version antérieure sur la plateforme 9.0

Dans la version 2.4.4.30 de Project Service ou version antérieure sur la plateforme 9.0, avec un flux des processus d’entreprise personnalisé, le champ **Nom de la phase** sur l’entité de projet utilisée dans les vues de listes de graphique et de projet **Projet par phase** ne sera pas mis à jour, car il est couplé au flux des processus d’entreprise des étapes du projet par défaut. Vous pouvez gérer ce problème avec la procédure suivante :

- Ajoutez un champ personnalisé pour capturer l’étape actuelle du flux des processus d’entreprise qui est mise à jour à mesure que l’utilisateur avance dans le flux des processus d’entreprise personnalisé.

- Modifiez le graphique **Projet par phase** en fonction de votre champ personnalisé au lieu de la configuration par défaut.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Étapes pour créer votre propre flux des processus d’entreprise pour l’entité de projet

Pour créer votre propre flux des processus d’entreprise pour l’entité de projet, procédez comme suit :

1. Accédez à **Paramètres** > **Centre de traitement**. Ne copiez pas le flux des processus d’entreprise des phases du projet, car cela copie également la logique métier Project Service.

  ![Créer un processus](media/FAQ-Customize-BPF-3.png)

2. Utilisez le concepteur de processus pour créer les noms de phase de votre choix. Si vous souhaitez la même fonctionnalité que les phases par défaut pour **Quote**, **Plan**, and **Close**, vous devrez créer cela en fonction des noms de phase de votre flux des processus d’entreprise personnalisé.

   ![Capture d’écran du concepteur de processus utilisé pour personnaliser le flkux des processus d’entreprise](media/FAQ-Customize-BPF-4.png) 

3. Dans le concepteur de processus, cliquez sur **Ordre des flux des processus** pour faire du flux des processus d’entreprise personnalisé le flux des processus d’entreprise principal pour l’entité de projet en le plaçant au-dessus du flux des processus d’entreprise des phases du projet au haut de la liste.


   [Capture d’écran de l’utilisation du flux des processus de commande](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Les étapes suivantes s’appliquent à l’application 2.4.4.30 de Project Service ou version antérieure sur la plateforme 9.0

4. Ajoutez un nouveau champ personnalisé à l’entité de projet pour capturer les phases personnalisées de votre flux des processus d’entreprise personnalisé. Vous devez ajouter une logique métier (plug-in/workflow) pour mettre à jour ce champ lorsque la phase du flux des processus d’entreprise personnalisé est mise à jour.

   ![Capture d’écran de la personnalisation de l’entité de projet](media/FAQ-Customize-BPF-6-720.png)

5. Modifiez le graphique **Projet par phase** pour utiliser votre nouveau champ personnalisé pour les étapes.

   ![Capture d’écran de l’utilisation du graphique Projet par phase](media/FAQ-Customize-BPF-7-720.png)

6. Modifiez les vues de l’entité de projet pour inclure votre nouveau champ personnalisé pour les étapes.

   ![Capture d’écran de la modification des vues sur l’entité du projet](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]