---
title: Nouveautés ou modifications dans Project Service Automation version 3
description: Cette rubrique donne des informations sur les nouveautés et les modifications dans Project Service Automation version 3.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: 6ce4c549b04716d466efa262dbc6a4abf28ea9eb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150665"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3"></a>Nouveautés ou modifications dans Project Service Automation version 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Cette rubrique donne des informations sur les modifications de l’interface utilisateur, des fonctionnalités et de la terminologie dans Project Service Automation entre la version 2 ou la version 1 et la version 3.

## <a name="project-scheduling"></a>Planification de projet
La planification de projet, qui était appelée Structure de répartition du travail (WBS) dans les versions précédentes, a été renommée Planification et est accessible en cliquant sur l’onglet **Planification**. 

![Planification de projet](media/psa-schedule-01.png)

Le planning a désormais une nouvelle surface d’interaction à la fois moderne et accessible. Cependant, le moteur de planification Project Service Automation sous-jacent n’a pas été modifié. Les boutons de commande du ruban de la grille de planification vous permettent d’interagir avec le planning comme dans la version précédente de Project Service Automation. Les modifications supplémentaires de la planification comprennent :

- **Diagramme de Gantt** - Le diagramme de Gantt n’est plus présent. Une nouvelle visualisation de Gannt sera disponible dans une prochaine mise à jour.
- **En-têtes de colonne** - Vous pouvez masquer les en-têtes de colonne dans la grille en cliquant sur l’indicateur vers le bas en regard de l’en-tête de colonne. 
- **Colonnes** - Vous pouvez afficher les colonnes masquées en cliquant sur **Ajouter une colonne**. 
- **Catégorie de transaction** - Un champ de recherche **Catégorie de transaction** a été ajoutée à la grille de planification et s’affiche par défaut. 
 
## <a name="project-templates"></a>Modèles de projet
Les modifications suivantes ont été apportées à la fonctionnalité Modèle de projet.

### <a name="create-a-project-template"></a>Créer un modèle de projet 
Vous pouvez créer un modèle de projet dans la version 3 comme dans les versions précédentes de Project Service Automation. Le modèle ne peut contenir qu’une planification et la planification peut inclure des affectations, mais elles ne sont pas obligatoires. Si la planification a des affectations, elles ne peuvent s’appliquer qu’aux ressources génériques. Vous pouvez générer des besoins en ressources pour les ressources génériques, mais la réservation ne peut pas être effectuée avec des ressources réelles du modèle. Vous ne pouvez pas réserver une ressource réelle à une équipe dans un modèle. 

### <a name="create-a-template-from-an-existing-template"></a>Créer un modèle à partir d’un modèle existant
Lorsque vous créez un modèle de projet à partir d’un modèle existant dans Project Service Automation version 3, les événements suivants se produisent : 

- La planification du projet source est copiée dans le modèle. 
- Les ressources génériques sont copiées dans l’équipe et les affectations de ressources génériques sont copiées. Les besoins pour les ressources génériques ne sont pas copiés. 

### <a name="create-a-template-from-an-existing-project"></a>Créer un modèle à partir d’un projet existant
Lorsque vous créez un modèle de projet à partir d’un projet existant, les événements suivants se produisent : 

- La planification du projet source est copiée dans le modèle. 
- Les ressources génériques sont copiées dans l’équipe et les affectations de ressources génériques sont conservées. Les besoins pour les ressources génériques ne sont pas copiés.    
- Les ressources nommées, à la fois attribuées ou non attribuées, sont supprimées de l’équipe et remplacées par des ressources génériques.
- Le cas échéant, les informations sur le client sont supprimées. 
- Le cas échéant, les références aux devis et contrats sont supprimées. 

### <a name="create-a-project-from-a-template"></a>Créer un projet à partir d’un modèle
Dans Project Service Automation version 3, lorsque vous créez un projet à partir d’un modèle, les événements suivants se produisent :

- La planification, l’équipe et les affectations sont copiées dans le nouveau projet.   
- La date de début est la date de copie ou la date sélectionnée par l’utilisateur.   
- Pour les membres de l’équipe générique avec des besoins en ressources dans le modèle, les besoins ne sont pas copiés ou générés automatiquement. Vous devez les générer. 

## <a name="copy-a-project"></a>Copier un projet
Dans Project Service Automation version 3, lorsque vous copiez un projet, les événements suivants se produisent : 

- La date de début estimée est copiée, mais peut être modifiée.  
- La planification et les tâches du projet sont copiées. 
- Les ressources génériques et leurs affectations sont copiées. Les besoins en ressources pour les ressources génériques ne sont pas copiés. Vous devez les régénérer. 
- Les ressources réelles et leurs affectations ne sont pas copiées. À la place, elles sont remplacées par des ressources génériques. 
- Les chiffres réels ne sont pas copiés dans le nouveau projet. 

## <a name="move-a-scheduled-project"></a>Déplacer un projet planifié
Lorsque vous avancez la planification d’un projet existant, les événements suivants se produisent : 

- Les dates des tâches sont automatiquement déplacées pour correspondre à la période de déplacement. 
- Les ressources génériques affectées restent affectées.   
- Si elles sont générées avant le déplacement du projet, les besoins pour la ressource générique restent inchangés et ne sont pas automatiquement régénérés. Vous devez les régénérer pour refléter les nouvelles affectations dues au déplacement des tâches. 
- Les affectations des ressources réelles sont modifiées pour correspondre au déplacement de la date des tâches. Les réservations de ressources réelles ne sont pas modifiées. Vous devez modifier les réservations à l’aide de la vue Rapprochement. 
- Les ressources de l’équipe avec des réservations mais sans affectations ne sont pas modifiées. 
- Les chiffres réels ne sont pas déplacés. 

## <a name="estimates"></a>Estimations
Les estimations ont été fractionnées en deux onglets, **Affectation de ressource** et **Estimations**. L’onglet **Affectation de ressource** contient les estimations de l’effort et affiche les affectations de ressource pour les tâches dans une vue par phases de temps. Vous pouvez modifier les estimations en fonction de ce que le moteur de planification a généré.

![Onglet Affectation de ressource affichant les estimations de l’effort et les affectations de ressource pour les tâches](media/resource-assignments-tab-02.png)

L’onglet **Estimations** affiche les montants du coût et des ventes pour les affectations de ressource. Les montants sont en lecture seule. L’évaluation des coûts et la tarification des ventes sont désormais déterminées par les affectations des membres de l’équipe sur la planification. Cela signifie que si vous avez une tâche sans affectation, celle-ci s’affiche sous l’emplacement non affecté. Cela signifie également que sans **rôle**, qui est une dimension de tarification par défaut, aucun coût ou aucune vente estimé n’est possible si un client ou un contrat/devis est associé au projet. 

![Onglet Estimations affichant les montants du coût et des ventes](media/estimates-tab-03.png)
  
La catégorie est également prise en charge sur les tâches dans la vue Planification. Le regroupement par catégorie dans la vue des estimations par phases de temps offre une meilleure expérience, surtout lorsque des estimations des dépenses sont également disponibles dans votre projet. Les estimations des dépenses sont entrées à l’aide d’une grille dans un onglet distinct. 

Les estimations des dépenses peuvent être entrées dans la grille de l’onglet **Estimations des dépenses**. 

![Onglet Estimations des dépenses affichant la grille des estimations des dépenses](media/expense-estimates-tab-04.png)

## <a name="resource-management"></a>Gestion des ressources
Dans Project Service Automation version 3, avec la nouvelle interface utilisateur de Unified Client et les modifications de la relation entre les réservations et les affectations, la dotation d’un projet en ressources génériques ou réelles a considérablement changé par rapport à la version 2 et la version 1. Toutefois, les concepts des ressources réservables, à la fois **réelles** et **génériques** restent inchangés, de même que les membres de l’équipe, les besoins, les affectations et les réservations.   

![Utilisation du sélecteur de ressources](media/resource-management-05.png)

### <a name="assign-a-real-bookable-resource"></a>Affecter une ressource réservable réelle 
Dans Project Service Automation version 3, les réservations et les affectations de tâches ne sont pas aussi étroitement liées que dans les versions précédentes de Project Service Automation. Vous pouvez utiliser la grille de l’équipe pour réserver un membre de l’équipe **réelle**, comme sur le marché.

À l’aide du sélecteur de ressources dans la planification, vous pouvez sélectionner le membre de l’équipe créé dans la vue de l’équipe et l’affecter à des tâches. Vous pouvez continuer à lui affecter des tâches, même après ses réservations. Utilisez l’onglet **Rapprochement** pour rapprocher les membres de l’équipe qui ont des différences de réservations et d’affectations.

Le sélecteur de ressources affiche les membres de l’équipe du projet. Vous pouvez également utiliser le sélecteur de ressources pour rechercher et afficher d’autres ressources réservables qui ne font pas partie de l’équipe du projet. Vous pouvez les affecter à une tâche afin qu’ils fassent partie de l’équipe du projet. Vous devez les réserver à l’aide de l’onglet **Tableau de planification** ou **Rapprochement**.

### <a name="assign-a-generic-bookable-resource-on-a-task-and-project-team-and-then-fulfill-with-a-real-resource-via-schedule-board"></a>Affecter une ressource réservable générique à une tâche et une équipe du projet et utiliser une ressource réelle via le tableau de planification 
Dans Project Service Automation version 3, la fonctionnalité Générer l’équipe n’est pas utilisée pour les ressources génériques. À la place, vous pouvez créer et affecter directement une ressource générique à partir de la planification en entrant le nom du poste de la ressource générique dans la cellule de ressource de la planification. Vous pouvez également sélectionner l’icône de ressource dans la cellule puis, à l’aide du sélecteur de ressources, entrer le nom de la ressource générique à créer. Un volet Création rapide s’ouvre pour vous permettre de définir le rôle et l’unité d’organisation du membre de l’équipe pour la ressource générique. Après avoir créé la ressource, celle-ci est affectée à la tâche et vous pouvez continuer à affecter cette ressource générique à d’autres tâches dans la planification.    
 
Lorsque vous avez affecté la ressource à toutes les tâches appropriées, vous pouvez générer un besoin en ressources et y répondre en effectuant une réservation directe avec le **Tableau de planification** ou en envoyant une demande de ressource. Vous pouvez également ajouter des ressources génériques directement dans la grille des membres de l’équipe. 

Les ressources génériques sont ajoutées à l’équipe du projet sans besoins en ressources et avec les dates de début/de fin du projet jusqu’à ce que le besoin en ressources soit généré. Pour générer un besoin, sélectionnez la ressource générique et cliquez sur **Générer**. Le lien du besoin s’affiche maintenant et les heures requises sont renseignées avec les heures affectées. Vous pouvez cliquer sur le lien pour ouvrir et mettre à jour le besoin.
  
Lorsque la réservation est terminée et complètement exécutée par une ressource nommée, la ressource générique est remplacée par la ressource nommée et l’affectation dans la planification est mise à jour avec la ressource nommée. 

Les ressources proposées pour les besoins sont mainteant stockées dans un onglet au lieu d’une section distincte.

### <a name="multiple-named-resources-fulfilling-a-generic-resource"></a>Plusieurs ressources nommées exécutant une ressource générique
Lorsqu’un besoin est satisfait avec plusieurs ressources, la ressource générique reste dans l’équipe et affectée à la tâche. Les membres de l’équipe nommée qui sont réservés ne sont pas affectés dans le cadre de leur poste. Le chef de projet peut affecter le travail si nécessaire aux ressources réelles.  La vue **Rapprochement** fournit une répartition des réservations sur plusieurs ressources pour plusieurs affectations de tâche. Cela n’est pas effectué automatiquement, car dans les scénarios plus compliqués, comme celui où un groupe de tâches composent le besoin, la façon dont le chef de projet souhaite les affecter, doit être prise en compte. Comme le système ne peut pas comprendre l’intention, les hypothèses seront probablement différentes de celles prévues et un résultat incorrect ou imprévisible se produira. Le résultat prévisible est que la ressource générique reste affectée jusqu’à ce que le chef de projet affecte délibérément des ressources à l’aide de la vue **Rapprochement**.

### <a name="reconciliation"></a>Rapprochement
L’onglet **Rapprochement** affiche les réservations et toutes les affectations pour chaque membre de l’équipe du projet. La vue affiche les heures dans les cellules qui peuvent représenter des périodes allant des mois jusqu’à des jours. Cette vue permet aux chefs de projet de rapprocher les réservations des membres de l’équipe et leurs affectations pour leur équipe de projet. Ceci est très utile, car les réservations et les affectations de tâche ne sont pas étroitement liées, ce qui offre plus de flexibilité lors de la planification d’un projet. 

![Onglet Rapprochement affichant les réservations et les affectations pour les membre de l’équipe du projet](media/resource-reconciliation-tab-06.png)

Pour chaque ressource, la vue calcule la différence entre les réservations d’un membre de l’équipe et un cumul de ses affectations de tâche et affiche les deux différences suivantes qui peuvent se produire avec les réservations et les affectations dans un projet : 

- **Pénurie de réservation** – Des pénuries de réservation se produisent lorsque la ressource a plus d’affectations que de réservations. Cette capacité n’ayant pas été réservée, un chef de projet peut corriger cette condition en étendant les réservations de la ressource pour compenser la pénurie. 
- **Réservations en trop** - Une réservation excessive se produit lorsque la ressource a été réservée pour le projet mais n’a pas été affectée à des tâches.  Cela peut être une occurrence acceptable, par exemple si la ressource a été réservée avant l’affectation des tâches. Toutefois dans d’autres cas, la ressource peut ne pas être planifiée pour une affectation, et le chef de projet doit envisager d’annuler les réservations de la ressource pour que la capacité soit utilisée pour un autre projet. 

Lorsque vous avez des affectations de tâche pour une ressource sans réservations (pénurie de réservation), vous pouvez sélectionner la pénurie de réservation globale et cliquer sur **Étendre la réservation**. Vous pouvez ensuite afficher la réservation nécessaire pour pallier à la pénurie de la ressource et sa disponibilité. 
 
## <a name="time-and-expense"></a>Temps et dépenses
Cette section donne des informations sur les modifications du temps, des dépenses et des approbations dans la version 3 de Project Service Automation. Dans le cadre de la solution Dynamics 365 Project Service Automation, la fonctionnalité **Entrée de temps** a été actualisée pour tirer parti de la structure Unified Interface. Cela permet de fournir une interface utilisateur cohérente et uniforme qui applique les principes de conception réactive pour une affichage optimal sur n’importe quelle taille d’écran ou n’importe quel appareil. 

### <a name="landing-page"></a>Page d’arrivée
L’expérience d’entrée de temps personnalisée et non extensible a été déconseillée dans la version 3. À la place, il existe maintenant une expérience de grille native extensible et accessible. Vous pouvez accéder à la fonctionnalité d’entrée de temps en utilisant le plan de site à gauche. Avec ce changement, vous ne pourrez plus entrer le temps pour une semaine à la fois. À la place, vous devez créer une entrée de temps pour chaque jour dans la grille. Après avoir créé quelques entrées de temps, les utilisateurs peuvent créer des entrées de temps en bloc avec la fonction **Copier** expliquée plus loin dans cette rubrique. 

![Page d’arrivée des entrées de temps](media/time-entry-landing-page-07.png)
 
### <a name="create-new-time-entries"></a>Créer des entrées de temps 
Cliquez sur **Nouveau** dans le ruban pour ouvrir une page de création rapide d’une entrée de temps où vous entrez la durée en minutes, heures ou jours. Pour ce faire, commencez par taper h, m ou j avec la quantité.  

![Création rapide d’une entrée de temps](media/quick-create-time-entry-08.png)

Les champs de recherche sont étayés par des vues système. Par exemple, une fois que vous avez entré les informations du projet, le champ **Tâche du projet** est défini par défaut sur la vue **Mes tâches du projet ouvertes**. Pour créer des entrées de temps pour les tâches qui ne sont pas affectées à l’utilisateur, cliquez sur **Modifier la vue** dans la boîte de dialogue de recherche et sélectionnez **Toutes les tâches du projet actives**. Une fois que l’entrée de temps a été créée et affichée dans la grille, vous pouvez modifier les valeurs de ligne directement dans la grille.  

### <a name="bulk-createcopy"></a>Création/copie en bloc 
Après avoir créé quelques entrées de temps, vous pouvez utiliser la fonctionnalité de copie pour créer des entrées de temps supplémentaires en bloc. Cliquez sur **Copier** pour ouvrir la boîte de dialogue **Copier**. Dans **À partir de la période : Date de début**, définissez la plage de dates à partir de laquelle les périodes doivent être copiées. Dans **Vers la période : Date de début**, entrez la date pour laquelle les entrées de temps doivent être créées. Cliquez sur **Copier** pour copier les entrées de temps dans le jour correspondant de la semaine indiquée dans **Vers la période**. Par exemple, l’entrée de temps du lundi de la semaine dernière est copiée dans le lundi de la semaine indiquée dans **Vers la période**. 

![Copier des entrées de temps en bloc](media/bulk-copy-time-entry-09.png)
 
### <a name="import-data"></a>Importer des données 
Les affectations et les échanges suivent le même modèle d’interface utilisateur, ce qui pemet à l’utilisateur de spécifier la plage de dates lorsque des réservations doivent être importées. Vous devez ensuite explicitement choisir les réservations qui doivent être copiées dans les entrées de temps **Brouillon**. Dans la version 3, vous ne pouvez plus afficher le modèle des entrées de temps **Suggérées** sur la grille et le calendrier.  

### <a name="change-in-calendar-control"></a>Modification du contrôle Calendrier
Dans la version 3, nous avons remplacé le contrôle Calendrier personnalisé et utilisons maintenant le calendrier UC pour afficher les entrées de temps de la semaine. Avec ce calendrier, vous pouvez afficher le jour, la semaine et le mois. 

> [!NOTE]
> Une limitation du calendrier est que ce contrôle ne prend pas en charge les actions sur des éléments de calendrier individuels. Par exemple, vous ne pourrez pas sélectionner un ou plusieurs éléments de calendrier et envoyer ou supprimer ces éléments. Cliquez sur un élément de calendrier pour ouvrir la page **Entité d’entrée de temps** pour des actions supplémentaires. 

### <a name="extensibility"></a>Extensibilité 
**Capturer des données dans les champs personnalisés des entités d’entrée de temps et de dépenses uniquement** - L’entrée de temps utilise une grille modifiable, une grille en lecture seule et des contrôles de calendrier à partir de la plateforme. Tous ces contrôles sont natifs et prennent donc en charge les personnalisations. Dans Project Service Automation version 3, vous pouvez ajouter des champs personnalisés supplémentaires, configurer des champs de recherche et les sauvegarder avec les vues personnalisées. Vous pouvez également définir une logique métier personnalisée basée sur les valeurs sélectionnées dans les champs personnalisés.  

**Capturer des données dans les champs personnalisés de l’entrée de temps et de dépenses et les propager via des entités prenant en charge le flux d’envoi et d’approbation** - Le traitement normal des entrées de temps est illustré dans le diagramme suivant.

![Traitement du flux d’une entrée de temps](media/process-time-entries-10.png)

Si les exigences de l’entreprise stipulent que les entités de temps et de dépenses doivent capturer des dimensions de tarification personnalisées et propager les valeurs définies par une ressource d’entrée de temps dans la dimension de tarification personnalisée par le biais de toutes les entités décrites dans le graphique précédent, consultez [Configurer des champs personnalisés comme dimensions de tarification](set-up-pricing-dimensions.md)

Pour répondre aux exigences de l’entreprise selon lesquelles les entités de temps et de dépenses doivent capturer des dimensions de tarification non personnalisées et propager les valeurs, vous pouvez utiliser le paramétrage des dimensions de tarification et exprimer les dimensions personnalisées en tant que dimensions de tarification sans taux de coût ou de facturation. Un autre scénario consisterait à ajouter un champ personnalisé à chacune des entités, en utilisant le même nom de champ dans toutes les entités. Des plug-ins personnalisés peuvent être créés pour associer les enregistrements des entités participant au flux d’envoi/d’approbation à l’aide des entités d’origine de transaction et de connexion de transaction.  

### <a name="delegate-time-and-expense-entry"></a>Déléguer une entrée de temps ou de dépenses
La plateforme Common Data Service ne prend pas en charge l’emprunt d’identité d’un autre utilisateur, ce qui signifie que la version 3 de Project Service Automation ne prend pas en charge l’entrée de temps et de dépenses déléguée. Toutefois, les partenaires et les clients ont trouvé une solution de contournement pour activer la prise en charge des expériences d’entrée de temps déléguées dans la version 3. Il s’agit uniquement d’une solution de contournement et non d’une solution complète. Il est donc important d’en connaître les limites et d’utiliser cette approche uniquement si les limites sont acceptables. 

> [!IMPORTANT]
> Ces informations doivent uniquement être considérées comme des conseils suggérés pour l’implémentation personnalisée par un partenaire/client. L’équipe du produit n’offre pas de support formel pour cette fonctionnalité par le biais de nos canaux de support.

### <a name="customization-details"></a>Détails de personnalisation 
La personnalisation vous permet d’ajouter une **Ressource réservable** aux expériences de création et de modification, qui permettent à un utilisateur d’agir en tant que délégué en remplaçant le champ **Ressource de réservation** par un autre utilisateur dont les entrées de temps et de dépenses doivent être enregistrées. Les étapes suivantes couvrent la délégation d’entrée de temps. Les mêmes informations s’appliquent à la délégation d’entrée de dépenses. 
 
1.  Assurez-vous que l’utilisateur a un accès de sécurité global sur les projets et les tâches du projet. 
1.  Comme le champ **Ressource réservable**, qui est un champ de l’entité **Entrée de temps**, n’est pas exposé dans la page **Création rapide**, vous devez l’ajouter.

    ou

    Créez une vue personnalisée, qui inclut la colonne **Ressource pouvant être réservée** pour afficher uniquement les entrées de temps créées pour la ressource. Publiez les personnalisations sur le concepteur de module d’application pour que cette vue s’affiche sous **Sélecteur de vues** dans la page **Entrées de temps**. Deux plug-ins gèrent la définition du responsable pour les entrées de temps hors projet :

    - PreValidateTimeEntryCreate
    - PreValidateTimeEntryUpdate
 
1. Créez un plug-in pour remplacer le champ **Responsable** par le responsable de l’utilisateur affecté dans le champ **Ressource réservable**. Utilisez la même **Phase d’exécution** que le plug-in hors bande (prévalidation) et utilisez un **Ordre d’exécution** plus élevé que les plug-ins OOB (supérieur à 1). Cela permet de s’assurer que le plug-in personnalisé est exécuté après les plug-ins OOB.  
 
### <a name="end-user-experience"></a>Expérience de l’utilisateur final
1.  Lorsque vous créez une entrée de temps dans la page de création rapide, entrez les détails du projet et des tâches du projet, puis choisissez l’utilisateur dans le champ **Ressource réservable** dont les entrées de temps devant être enregistrées. 
2.  Par défaut, ce champ affiche l’utilisateur connecté. Toutefois, comme l’utilisateur a remplacé ce champ, l’entrée de temps est maintenant créée pour la **Ressource réservable** choisie.
3.  Lorsque vous envoyez les entrées de temps que vous avez créées pour ces enregistrements, les entrées sont mises en file d’attente pour l’approbateur du projet comme prévu. 
4.  Lorsque vous rappelez les entrées de temps créées pour l’autre utilisateur, les entrées de temps sont retournées à l’état **Brouillon** avec le champ **Ressource réservable** défini sur l’autre utilisateur. 
5.  Éventuellement, vous pouvez basculer vers la vue personnalisée pour filtrer les entrées de temps créées pour l’autre utilisateur. 
 
### <a name="limitations"></a>Limitations
Les fonctionnalités **Copier** et **Importer** fonctionnent uniquement dans le contexte de l’utilisateur connecté. Cela signifie qu’il n’est pas possible de copier ou d’importer des entrées de temps créées pour l’utilisateur connecté en tant que ressource réservable.

Les entrées du temps qui ne s’appliquent pas à un projet sont acheminées pour approbation vers le responsable de la ressource réservable uniquement si l’étape 4 de la section **Détails de personnalisation** ci-dessus est terminée. Sinon, les entrées de temps hors projet pour l’autre utilisateur sont acheminées de manière incorrecte vers le responsable de l’utilisateur connecté. 

### <a name="other-changes"></a>Autres modifications 
La fonctionnalité **Réservations et tâches** a été supprimée. 

## <a name="multidimensional-pricing"></a>Tarification multidimensionnelle
Pour optimiser la flexibilité et répondre aux différents besoins de l’entreprise, la version 3 Project Service Automation prend en charge l’application discrète des ensembles de dimensions de tarification aux taux de coût et de facturation. Les valeurs de dimension peuvent être définies comme valeurs par défaut et propagées au processus d’évaluation des coûts et de tarification depuis le profilage des ressources aux entrées de temps en passant par les chiffres réels du projet. La configuration et la modification ou l’extension propres au client utilisent l’infrastructure d’adaptabilité standard.

Project Service Automation est fourni avec un ensemble par défaut de dimensions de tarification, de rôles et d’unités de ressource. Elle permet de configurer les prix et les coûts pour chaque combinaison de rôle et d’unité d’organisation.

Pour les clients de Project Service Automation qui souhaitent continuer à utiliser ces champs prédéfinis comme dimensions de tarification dans la version 3, aucune modification ne sera observable. Vous pouvez continuer à utiliser Project Service Automation comme d’habitude. Si, toutefois, vous devez évaluer le prix ou le coût de vos ressources avec d’autres attributs supplémentaires, la version 3 permet d’ajouter vos propres dimensions de tarification personnalisées dans Project Service Automation. L’extension des dimensions de tarification personnalisées est une expérience de configuration complexe. 

## <a name="quotes-and-contracts"></a>Devis et contrats
Dans la version 3 de Project Service Automation, les aspects de la configuration et de la gestion des devis et des contrats ont été modifiés. Les sections suivantes donnent des informations plus détaillées.

### <a name="set-up-chargeability-options"></a>Configurer les options d’exigibilité
Dans les versions 1 et 2, la configuration de l’exigibilité pour les rôles et les catégories pour des devis et des contrats spécifiques était effectuée à l’aide de la vue **Exigibilité** qui se trouvait dans la barre de navigation supérieure gauche d’une ligne de devis ou d’une ligne de contrat. C’était également à cet endroit que vous pouviez définir les prix pour ces rôles et catégories de dépenses.

À compter de la version 3, la configuration des options d’exigibilité par rôle et par catégorie de dépense est effectuée au niveau de la ligne de devis ou de contrat. La configuration de la tarification est séparée de la configuration de l’exigibilité. Vous trouverez les **Rôles facturables** et les **Catégories facturables** en tant qu’onglets dans les pages **Ligne de devis** et **Ligne de contrat** sans avoir à utiliser la barre de navigation supérieure.

![Rôles facturables](media/chargeable-12.png)
 
La configuration des rôles facturables et des catégories facturables utilise également le contrôle de grille modifiable prédéfini. Pour chaque rôle et catégorie, les options prises en charge pour le type de facturation pendant la phase Devis et contrat restent inchangées (**Facturable** et **Non facturable**) par rapport aux versions antérieures. **Gratuit** n’est pas un type pris en charge pendant la phase Devis ou Contrat. **Gratuit** est pris en charge uniquement lors de l’approbation du temps ou des dépenses.  
 
### <a name="create-and-edit-custom-pricing-for-a-project-service-automation-quote-and-project-contract"></a>Créer et modifier des tarifs personnalisés pour un devis et un contrat de projet Project Service Automation
Dans les versions 1 et 2, l’utilisation de tarifs personnalisés pour des devis et des contrats spécifiques était possible à l’aide de l’option **Modifier les prix** dans la vue **Exigibilité**. La vue **Exigibilité** se trouvait dans la barre de navigation supérieure gauche d’une ligne de devis ou d’une ligne de contrat. C’était également à cet endroit que vous pouviez définir les options d’exigibilité pour les rôles et les catégories de dépenses.

À compter de la version 3, la création et l’utilisation de tarifs de projet personnalisés pour un devis Project Service Automation et un contrat de projet Project Service Automation ont été séparées de la configuration de l’exigibilité. Le devis Project Service Automation et les contrats de projet Project Service Automation ont un nouvel onglet appelé **Tarifs du projet**. Cet onglet affiche une vue associée de tous les tarifs de projet qui sont joints au devis ou au contrat de projet Project Service Automation. Pour créer des tarifs personnalisés à partir de tarifs existants qui sont déjà associés au devis ou au contrat du projet, cliquez sur **Créer des tarifs personnalisés**. Une copie de tous les tarifs associés sera créée et jointe au devis ou au contrat. Vous pouvez maintenant ouvrir les tarifs et modifier le prix du rôle ou de la catégorie de dépenses afin que ces modifications de tarification s’appliquent uniquement à ce devis ou contrat. 
  
Le graphique suivant s’affiche avant la création des tarifs personnalisés.

![Avant les tarifs personnalisés](media/before-custom-price-lists-13.png)

Le graphique suivant s’affiche après la création des tarifs personnalisés.

![Après les tarifs personnalisés](media/after-custom-price-lists-14.png)

> [!NOTE]
> Un court décalage peut se produire entre le moment où vous cliquez sur **Créer des tarifs personnalisés** et le moment où les tarifs personnalisés sont créés. Nous vous recommandons d’actualiser la grille au lieu de cliquer à plusieures reprises. Les tarifs personnalisés ont été créés si le nom du devis ou le nom du contrat de projet est ajouté au nom des tarifs associés.
