---
title: Vue d’ensemble des structures de répartition du travail
description: Une structure de répartition du travail est une description du travail qui sera effectué pour un projet. Il s’agit d’une hiérarchie des tâches qui représente la compréhension par l’équipe projet de la composition du travail, de son étendue, du coût et de la durée de chaque composant ou tâche.
author: Yowelle
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWorkBreakdownStructure
audience: Application User
ms.reviewer: johnmichalak
ms.assetid: 241a0464-0056-4a69-b468-0afbe2d5f3ae
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f1e69d7cc97e3a7a59bdba387282fe19d12f5780
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683397"
---
# <a name="work-breakdown-structures-overview"></a>Vue d’ensemble des structures de répartition du travail

[!include [banner](../includes/banner.md)]

Une structure de répartition du travail est une description du travail qui sera effectué pour un projet. Il s’agit d’une hiérarchie des tâches qui représente la compréhension par l’équipe projet de la composition du travail, de son étendue, du coût et de la durée de chaque composant ou tâche. Une WBS a trois objectifs principaux :

-   Décrire la répartition ou décomposition du travail en tâches.
-   Planifier le travail à effectuer pour le projet.
-   Estimer le coût de chaque tâche.

Le degré des détails dans une structure de répartition du travail dépend du niveau de précision requis dans les estimations et le niveau de suivi requis par rapport à ces estimations. Les projets qui ont une tolérance très basse aux écarts de durée ou de coût nécessitent généralement une structure de répartition du travail plus détaillée, et un suivi diligent de la progression et du coût des travaux par rapport à la structure de répartition du travail. Ce type de projet est courant dans les secteurs de la construction et de l’ingénierie. 

En revanche, les projets dans des secteurs tels que les médias et la publicité, les logiciels et l’infrastructure informatique ont tendance à être uniques en leur genre, et la productivité dépend de l’expérience et de la qualification de la personne qui exécute la tâche. Par conséquent, ces industries utilisent une structure de répartition du travail pour obtenir une approximation de la taille d’un projet, et non pour suivre l’avancement de ce projet en détail. 

La création d’une WBS est un processus intensif qui se déroule généralement sur une longue période et qui nécessite la collaboration et les informations d’une grande variété de personnes. Cette rubrique décrit la manière dont vous pouvez utiliser les améliorations de la WBS pour répondre à vos besoins en matière d’estimations et de suivi.

## <a name="prerequisites-for-creating-a-wbs"></a>Conditions préalables à la création d’une WBS
Pour créer une WBS, vous devez être en mesure de créer un calendrier de travail et d’estimer le coût du travail.

### <a name="prerequisites-for-creating-a-work-schedule"></a>Conditions préalables pour créer une planification des tâches

Pour utiliser les capacités complètes de planification des fonctionnalités de la WBS, procédez comme suit :

1.  Configurez un calendrier par défaut et un calendrier de projet :
    1.  Cliquez sur **Gestion de projets et comptabilité** &gt; **Paramétrage** &gt; **Paramètres de gestion de projets et de comptabilité** &gt; **Planification**. Dans le champ **Calendrier de travail par défaut**, spécifiez un calendrier par défaut. Ce sera le calendrier de travail par défaut pour tout nouveau projet créé.
    2.  Vous pouvez modifier le calendrier par défaut pour un projet spécifique. Cliquez sur la page de détails du projet, puis sur le raccourci **Équipe de projet et planification**, mettez à jour le champ **Calendrier de planification** en sélectionnant un autre calendrier.

2.  Mettez en place des jours et des heures de travail standard. Le calendrier que vous définissez comme calendrier de travail pour votre projet sera utilisé dans la WBS pour déterminer les informations suivantes :

-   Jours ouvrables et congés
-   Nombre d’heures de travail dans une journée

Pour paramétrer les jours ouvrables et les heures de travail d’un calendrier, ou pour créer un nouveau calendrier, cliquez sur **Administration de l’organisation** &gt; **Éléments communs** &gt; **Calendriers**.

### <a name="prerequisites-for-estimating-the-cost-of-work"></a>Condition requise pour estimer le coût des travaux

Pour utiliser toutes les fonctionnalités d’estimation des coûts de la WBS, vous devez configurer les coûts et les prix de vente pour les travailleurs, les catégories de main-d’œuvre, les dépenses et les honoraires, et les articles.

-   Pour configurer le coût et le prix de vente des catégories de main-d’œuvre, de dépenses et de frais, cliquez sur **Gestion de projet et comptabilité** &gt; **Paramétrage** &gt; **Prix**.
-   Pour configurer le coût et le prix de vente des articles, utilisez la page **Accords commerciaux** pour chaque élément de la liste **Produits lancés** dans la gestion des informations sur le produit.

## <a name="creating-a-wbs"></a>Création d’un adaptateur WBS
La création d’une WBS implique trois activités :

1.  **Décomposition du travail** : créez une répartition du travail en morceaux ou tâches gérables.
2.  **Planning de travail** : estimez le temps nécessaire pour terminer une tâche, définissez les interdépendances des tâches et sélectionnez les dates de début et de fin des tâches.
3.  **Estimation de coût** : estimez les coûts pour chaque tâche.

Les sections suivantes expliquent comment les fonctionnalités WBS peuvent vous aider dans chacune de ces activités.

### <a name="work-decomposition"></a>Décomposition du travail

La création d’une ventilation ou d’une décomposition du travail est généralement la première étape du processus de création d’une WBS. La fonctionnalité WBS prend en charge les constructions de base suivantes pour la répartition ou la décomposition du travail. 

**Tâche racine du projet** La tâche racine du projet est la tâche récapitulative de niveau supérieur d’un projet. Toutes les autres tâches du projet sont créées en dessous. La tâche du nœud racine est toujours définie sur le nom du projet. L’effort, les dates et la durée du nœud racine résument les valeurs des tâches sous la tâche racine. Vous ne pouvez pas modifier les propriétés de nœud racine ou supprimer le nœud racine.

**Tâches récapitulatives ou de conteneur** Une tâche récapitulative est une tâche qui comporte des sous-tâches ou des tâches constitutives en dessous d’elle. Une tâche récapitulative n’a pas d’efforts ou coûts de travail qui lui sont propres. Au lieu de cela, l’effort de travail et le coût d’une tâche récapitulative sont la somme de l’effort de travail et du coût de ses tâches constitutives. La date de début des tâches constitutives est utilisée en tant que date de début de la tâche récapitulative, et la date de fin des tâches constitutives est utilisée en tant que date de fin. Vous pouvez modifier le nom d’une tâche récapitulative, mais vous ne pouvez pas modifier les propriétés de planification pour effort, dates et durée. Si vous supprimez une tâche récapitulative, vous supprimez également toutes ses tâches constitutives. 

**Tâches de nœud terminal** Une tâche de nœud terminal représente le lot de travail le plus granulaire du projet. Un nœud terminal possède un effort estimé, un nombre de ressources planifiées, des dates de début et de fin planifiées, et une durée. 

Vous pouvez effectuer les opérations de hiérarchie suivantes pour activer la création d’une hiérarchie de travail ou d’une décomposition pour un projet. 

**Nouvelle tâche** Toute nouvelle tâche que vous créez est automatiquement ajoutée sous le nœud racine et un numéro de WBS est automatiquement attribué à la tâche. Le numéro de la WBS représente le niveau de la tâche dans la hiérarchie. Pour les tâches du premier niveau sous la tâche racine du projet, un schéma de numérotation de 1, 2, 3, etc., est utilisé. Pour les tâches sous le premier niveau, un schéma de numérotation de 1.1, 1.2, 1.3, etc., est utilisé. Pour chaque niveau ajouté sous un niveau précédent, une nouvelle série de nombres en pointillés est ajoutée. 

Actuellement, vous ne pouvez pas personnaliser la numérotation WBS. 

**Mettre une tâche en retrait** Lorsque vous mettez en retrait une tâche, elle devient un enfant de la tâche qui la précède. Le numéro WBS de la nouvelle tâche enfant est automatiquement recalculé en fonction du numéro WBS de son nouveau parent. La tâche parent est désormais une tâche récapitulative ou conteneur, et devient donc un cumul de ses tâches constitutives. 

> [!NOTE] 
> Lorsque vous mettez en retrait des tâches sous une tâche qui était un nœud feuille avant l’opération de retrait, la tâche récapitulative nouvellement créée perd ses propres dates, effort et nombre de ressources. Il utilise désormais un résumé des valeurs de ses nouvelles tâches constitutives. 

**Mettre une tâche en retrait négatif** Lorsque vous mettez une tâche en retrait négatif, ce n’est plus une tâche constitutive de son parent. Le numéro WBS de cette tâche est automatiquement recalculé pour refléter le nouveau niveau de la tâche dans la hiérarchie. L’effort, le coût et les dates de la tâche parente précédente sont recalculés afin qu’ils excluent cette tâche. 

**Monter et descendre** Lorsque vous cliquez sur **Monter** et **Descendre**, vous modifiez la position d’une tâche dans la hiérarchie de son parent. La position d’une tâche n’affecte pas l’effort, le coût, les dates, ou la durée de la tâche. Cependant, le numéro WBS de cette tâche est automatiquement recalculé pour refléter la nouvelle position de la tâche.

### <a name="schedule-estimation"></a>Planifier l’estimation

Planifier l’estimation est généralement la deuxième étape de la création d’une WBS. Une bonne pratique consiste à effectuer l’estimation du calendrier après avoir créé les tâches. La page **Structure de répartition du travail** dans Finance comporte deux sections. Le volet supérieur est destiné à l’estimation du calendrier et le volet inférieur comprend un onglet **Coûts et produit estimés** permettant d’effectuer l’estimation des coûts. 
**Dépendances de tâches** Dans une WBS, vous pouvez créer une relation de prédécesseur entre les tâches. Lorsque vous affectez des tâches précédentes (ou prédécesseurs) à une tâche, elle ne peut démarrer qu’une fois tous ses prédécesseurs terminés. La date de début prévue de la tâche est automatiquement définie sur la dernière date de fin de tous ses prédécesseurs. 

**Planification des tâches** Les facteurs suivants déterminent la planification des tâches du nœud feuille :

-   Prédécesseurs
-   Effort
-   Le nombre de ressources
-   Les dates de début et de fin

La date de début d’une tâche de nœud terminal qui ne dispose pas de prédécesseurs est définie par défaut à la date de début de planification du projet. La durée d’une tâche de nœud terminal correspond toujours au nombre de jours ouvrables entre ses dates de début et de fin. 

*<strong><em>Règles de planification</em></strong>* Lorsque l’assistance à la planification automatique est activée, les règles suivantes s’appliquent à la planification des tâches pour les tâches du nœud feuille :

-   Les dates de début et de fin d’une tâche doivent être des jours ouvrables, selon le calendrier de planification du projet.
-   La date de début d’une tâche ayant des prédécesseurs est automatiquement définie sur la dernière date de fin de tous ses prédécesseurs.
-   L’effort pour une tâche est calculé automatiquement comme suit :

Nombre de personnes × durée × nombre d’heures dans un jour de travail standard du calendrier de projet. 

Dans certains cas, vous souhaiterez peut-être vous écarter de ces règles. Vous pouvez désactiver la planification automatique pour empêcher Finance de définir ou corriger automatiquement les propriétés des tâches de nœud terminal. Lorsque vous entrez des informations pour une tâche qui entraîne une violation de toute règle de planification, une icône d’erreur de planification s’affiche pour la tâche. Si vous ne souhaitez pas que les erreurs de planification s’affichent, cliquez sur **Les erreurs de planification sont affichées** pour désactiver la fonction. 

> [!NOTE] 
> Les valeurs d’une tâche récapitulative ou de conteneur continuent d’être calculées comme la somme des valeurs des tâches constituantes, que l’aide à la planification automatique soit activée ou désactivée. 

**Correction des erreurs de planification** Lorsque l’assistance de planification automatique est activée, des erreurs de planification ne sont pas susceptibles de se produire. Cependant, si vous désactivez l’assistance à la planification automatique, puis la réactivez ultérieurement, des icônes d’erreur de planification peuvent apparaître dans la WBS. 

**Correction des erreurs de planification par tâche** Lorsque vous double-cliquez sur l’icône d’erreur de planification pour une tâche spécifique, une boîte de dialogue affiche toutes les erreurs de planification pour cette tâche. Vous pouvez décider des erreurs de planification à corriger pour la tâche. 

**Correction de toutes les erreurs de planification** Si vous souhaitez que Finance corrige toutes les erreurs de planification dans la WBS, dans le volet Actions, cliquez sur **Résoudre toutes les anomalies de planification**. 

> [!NOTE] 
> Cette fonctionnalité peut entraîner des modifications importantes de la WBS. Les erreurs sont corrigées dans l’ordre suivant :

1.  L’effort estimé sur toutes les tâches est modifié afin qu’il soit égal à la capacité définie dans le calendrier du projet.
2.  La date de début de chaque tâche est modifiée de sorte que la tâche démarre une fois que toutes ses tâches prédécesseurs sont terminées.
3.  La date de début de chaque tâche est modifiée pour supprimer les écarts dans les dates de début des tâches précédentes.

### <a name="cost-estimation"></a>Estimation des coûts

Comme mentionné précédemment dans ce document, vous saisissez l’estimation du coût pour chaque tâche de nœud terminal en utilisant l’onglet **Coûts et revenus estimés** dans le volet inférieur de la page **Structure de répartition du travail**. 

> [!NOTE] 
> Vous ne pouvez pas modifier l’estimation des coûts pour une tâche récapitulative ou conteneur. L’estimation des coûts d’une tâche récapitulative est égale à la somme de l’estimation des coûts de ses tâches de nœud terminal. Le coût total estimé de chaque tâche est égal à la somme des coûts estimés pour les types de transactions suivants :

-   Main-d’œuvre
-   Article ou matériau
-   Dépenses

Une transaction de type **Frais** est utilisée pour estimer les revenus basés sur les frais. Ce type de transaction n’a pas de composant de coût et n’est donc pas pris en compte lors de l’estimation des coûts. 

Une transaction de type **Sur compte** est utilisée pour enregistrer la valeur de vente contractée dans un type de projet à valeur fixe. Ce type de transaction n’est pas non plus pris en compte lors de l’estimation des coûts. 

Lorsque vous estimez les coûts de main-d’œuvre, de matériel et de dépenses pour chaque tâche, vous devez affecter une catégorie de projet au coût estimé. 

**Estimation des coûts de main-d’œuvre** Pour chaque tâche de nœud terminal, vous affectez un effort de travail en heures et une catégorie par défaut. Par conséquent, lorsque vous configurez un calendrier pour une tâche, l’estimation des coûts de main-d’œuvre pour cette tâche est automatiquement ajoutée dans la catégorie par défaut pour la main-d’œuvre. Cette estimation des coûts s’affiche dans l’onglet **Coûts et produit estimés** de la grille **Détails de ligne** pour cette tâche. Si vous avez besoin d’autres estimations des coûts de main-d’œuvre, vous pouvez les ajouter dans cet onglet. Si vous augmentez ou diminuez le nombre d’heures sur l’estimation des coûts de main-d’œuvre, le calendrier de la tâche est automatiquement recalculé. 

**Estimation des dépenses et des coûts matériels** L’onglet **Coûts et revenus estimés** vous permet également d’estimer les dépenses et les coûts matériels d’une tâche, si vous avez besoin d’estimations. 

Le coût et le prix de vente pour chaque ligne d’estimation de la main-d’œuvre ou des dépenses sont basés sur la configuration définie pour chaque catégorie dans les tableaux de prix à l’adresse **Gestion de projets et comptabilité** &gt; **Configurer** &gt; **Tarification**. Pour les articles, le coût et le prix de vente sont ajoutés par défaut depuis les Accords commerciaux ou chaque élément de la liste **Produits lancés** dans la gestion des informations sur le produit.

## <a name="tracking-progress-on-the-wbs"></a>Suivi des progrès sur la WBS
Certaines industries suivent la progression d’un projet par rapport à une WBS à un niveau très granulaire, tandis que d’autres suivent les progrès à un niveau supérieur de la WBS. Cette section décrit comment vous pouvez utiliser le suivi WBS pour les exigences de votre projet. 

Finance dispose de trois vues pour la WBS d’un projet : la vue Planification, la vue Suivi des efforts et la vue Suivi des coûts.

### <a name="planning-view"></a>Vue Planification

La vue Planification affiche l’estimation planifiée ou de référence du calendrier et des informations sur les coûts. Bien qu’il n’existe aucune fonctionnalité de suivi de la version et de la référence pour un projet WBS, les valeurs de cette vue sont destinées à représenter la version de référence. Les sections Estimation du calendrier et Estimation des coûts de cette rubrique décrivent cette vue et comment elle est utilisée pour créer une WBS.

### <a name="effort-tracking-view"></a>Vue de suivi des efforts

La vue Suivi des efforts suit la progression des tâches dans la planification. Elle compare les heures d’effort réelles accumulées pour une tâche aux heures d’effort planifiées. Les formules suivantes fournissent les valeurs figurant dans la vue de suivi des efforts :

-   Pourcentage de progression = Cumul des efforts réels consacrés ÷ Efforts planifiés pour la tâche
-   Effort restant (également connu sous le nom d’estimation pour terminer \[ETC \]) = Effort planifié - Effort réel à ce jour
-   Estimation à achèvement (EAA) = Efforts restants + Cumul des efforts réels consacrés
-   Écart d’efforts escomptés = Efforts planifiés – EAA

La vue Suivi des efforts affiche une projection de la variance de l’effort pour la tâche, selon que l’EAA est supérieur ou inférieur à l’effort prévu :

-   Si l’EAA excède les efforts planifiés, la tâche est prévue de prendre plus de temps qu’initialement planifié, et est en retard.
-   Si l’EAA est inférieur aux efforts planifiés, la tâche est prévue de prendre moins de temps qu’initialement planifié, et est en avance.

**Nouvelle projection des efforts du chef de projet** Parfois, le chef de projet ou une autre personne qui suit l’avancement d’un projet devra réviser les estimations originales d’une tâche. La tâche peut avancer plus vite ou plus lentement que prévu initialement pour diverses raisons. Par exemple, la portée a été réduite ou les employés ont moins d’expérience que prévu initialement. Les projections de projet sont une perception des estimations du chef de projet, vu l’état actuel de projet. En général, vous ne devez pas modifier vos numéros de référence, car la ligne de référence du projet représente un document publié pour les estimations de planning et de coût du projet convenues par toutes les parties prenantes au projet. 

Il existe deux méthodes de nouvelle projection des efforts sur les tâches que peuvent modifier les chefs de projet :

-   Modifiez l’effort restant qui est automatiquement défini pour mettre à jour l’effort restant réel sur la tâche.
-   Modifiez le pourcentage de progression qui est automatiquement défini pour mettre à jour la progression réelle sur la tâche.

Chacune de ces méthode entraîne un nouveau calcul de l’Estimation avant achèvement, de l’EAA (Estimé à Achèvement) et du pourcentage de progression de la tâche et de l’écart d’efforts escomptés pour une tâche. L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart d’efforts. 

**Effort modifié sur les tâches récapitulatives** Vous pouvez modifier l’effort sur les tâches récapitulatives ou conteneurs. Que vous modifiiez ces valeurs avec les efforts restants ou le pourcentage de progression sur les tâches récapitulatives, les calculs surviennent automatiquement dans l’ordre suivant :

1.  L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de progression sur la tâche sont calculés.
2.  Le nouvel EAA est distribué aux tâches enfants dans la même proportion que l’EAA d’origine.
3.  Le nouveau EEA sur chaque tâche de nœud terminal est calculé.
4.  Les efforts restants et le pourcentage de progression sont recalculés pour toutes les tâches enfants affectées, en fonction de la nouvelle valeur de l’EEA. L’écart de l’effort des tâches est également recalculé.
5.  L’EEA des tâches récapitulatives est également recalculé à partir des nœuds terminaux.

Cliquez sur **Développer au niveau** dans la vue Suivi des efforts pour définir le niveau auquel suivre et maintenir votre WBS. La WBS est automatiquement étendue à ce niveau dans la vue Suivi des efforts chaque fois que vous l’ouvrez.

### <a name="cost-tracking-view"></a>Vue Suivi du coût

La vue Suivi des coûts affiche le suivi de la consommation des coûts pour une tâche. Dans cette vue, le coût réel qui a été dépensé pour une tâche à ce jour est comparé au coût planifié de la tâche. Les formules suivantes fournissent les valeurs figurant dans la vue de suivi des coûts :

-   Pourcentage des coûts consommés = Cumul des coûts réels consacrés ÷ Coût planifié pour la tâche
-   Coût pour terminer = Coûts planifiés – Cumul des coûts réels consacrés
-   Estimation à l’achèvement (EEA) = CTC + Coût réel à ce jour
-   Écart de coûts projetés = Coûts planifiés – EAA

La vue Suivi des coûts affiche une projection de l’écart des coûts pour la tâche, selon que l’EAA est supérieur ou inférieur au coût prévu :

-   Si l’EAA excède le coût planifié, la tâche est prévue de dépenser plus d’argent qu’initialement planifié, et est hors budget.
-   Si l’EAA est inférieur au coût planifié, la tâche est prévue de dépenser moins d’argent qu’initialement planifié, et est inférieur au budget.

**Nouvelle projection des coûts du chef de projet** Les chefs de projet doivent utiliser CTC pour réviser l’estimation des coûts d’origine d’une tâche. Le chef de projet peut modifier la valeur CTC en fonction du coût requis pour terminer la tâche. Si vous modifiez la valeur CTC, le CTC, l’EEA et le pourcentage de coût consommé de la tâche, ainsi que l’écart de coût projeté sur une tâche, sont recalculés. L’Estimation avant achèvement, l’EAA (Estimé à Achèvement) et le pourcentage de coût consommé sur les tâches récapitulatives sont également recalculés, et produisent une nouvelle projection de l’écart de coût. 

> [!NOTE] 
> Lorsque vous révisez l’effort pour une tâche WBS dans la vue Suivi des efforts, le CTC, l’EEA, le pourcentage de coût consommé et l’écart de coût prévu de la tâche sont tous recalculés dans la vue Suivi des coûts. Cependant, les révisions de coût n’affectent pas les valeurs de la vue Suivi des efforts, car le coût par type de transaction (main-d’œuvre, matériel ou dépense) ou par catégorie de projet n’est pas révisé. 

**Révision de la projection des coûts sur les tâches récapitulatives** Vous pouvez réviser les coûts sur les tâches récapitulatives et les calculs sont effectués automatiquement dans l’ordre suivant :

1.  L’EEA, le CTC et le pourcentage de coût consommé sur la tâche sont recalculés.
2.  Le nouvel EAA est distribué aux tâches enfants dans la même proportion que l’EAA d’origine sur les tâches.
3.  Le nouveau EEA pour chaque tâche est calculé.
4.  Le CTS et le pourcentage de coût consommé sont recalculés pour les tâches enfants affectées, en fonction de la valeur EEA. L’écart de coût des tâches est également recalculé.
5.  L’EEA de toutes les tâches récapitulatives est recalculé en fonction de cette modification.

Cliquez sur **Développer au niveau** dans la vue Suivi des coûts pour définir le niveau auquel suivre et maintenir votre WBS. La WBS est étendue à ce niveau dans la vue Suivi des coûts chaque fois que vous l’ouvrez.

### <a name="earned-value-management"></a>Gestion de la valeur acquise

Vous pouvez utiliser la méthode de la valeur acquise pour suivre la progression d’un projet. Vous pouvez afficher les mesures de valeur acquise sur le tableau de bord du chef de projet. Le composant graphique de la valeur acquise affiche les valeurs échelonnées de la valeur planifiée et du coût réel. La valeur acquise à la date actuelle est indiquée sous forme de point. Les données échelonnées sur la valeur acquise ne sont actuellement pas disponibles. 

La phase de temps sur le graphique de la valeur acquise est affichée par semaine ou par mois. Cette section décrit les trois piliers de la méthode de la valeur acquise : la valeur planifiée, la valeur acquise et le coût réel. 

**Valeur planifiée** La théorie concernant la méthode de la valeur acquise stipule que le tracé de la valeur planifiée représente le taux auquel l’équipe du projet prévoyait de gagner de la valeur sur le projet. 

Finance utilise la règle de gain 0:100 lorsqu’il trace la valeur planifiée. Selon cette règle, la valeur de la tâche est publiée dans la tâche à compter de sa date de fin. Aucune valeur n’est publiée tant que la tâche n’est pas terminée à 100 %%. 

Dans Gestion de projets et comptabilité, vous saisissez la date de fin des nœuds terminaux et le coût prévu pour celui-ci. Lorsque le graphique de la valeur planifiée est affiché par semaine, la valeur planifiée est récapitulée par semaine pour toutes les tâches du nœud terminal pendant la durée du projet. 

**Valeur acquise** La théorie concernant la méthode de la valeur acquise stipule que le tracé de la valeur planifiée représente le taux auquel l’équipe du projet est en fait la valeur acquise sur le projet. 

Finance utilise la règle de gain 0:100 lorsqu’il trace la valeur acquise. Selon cette règle, la valeur de la tâche est publiée dans la tâche à compter de sa date de fin. Aucune valeur n’est publiée tant que la tâche n’est pas terminée à 100 %%. 

Lorsque la valeur acquise est calculée, le pourcentage de progression de chaque tâche est pris en compte. En vertu de la règle de gain de 0:100, seules les tâches qui sont achevées au cours d’une période donnée sont prises en compte pour le calcul de la valeur acquise à la fin de cette période. La valeur acquise sur le projet est calculée pour toutes les tâches qui ont été achevées lors de la création du graphique. 

> [!NOTE] 
> Actuellement, le système de suivi WBS ne dispose pas de structures de données pour stocker les pourcentages de progression historiques sur chaque tâche. Par conséquent, la valeur acquise ne peut être signalée qu’à partir du moment où le cube est traité. Traitez le cube régulièrement pour mettre à jour les données de valeur acquise qui sont affichées sur le tableau de bord. 

**Coût actuel** La théorie concernant la méthode de la valeur acquise stipule que le graphique des coûts réels représente le taux auquel l’argent est dépensé pour le projet. 

Les transactions imputées à un projet sont utilisées pour tracer la ligne de coût réel. Les coûts sont résumés par date. Ces données sont ensuite utilisées pour représenter graphiquement les coûts réels par semaine ou par mois sur le graphique de la valeur acquise.

### <a name="how-to-use-the-concepts-of-planned-value-earned-value-and-actual-cost"></a>Comment utiliser les concepts de valeur planifiée, de valeur acquise et de coût réel

**Planifier l’écart** Lors de la planification, vous créez une prévision de travail sur une chronologie. Par conséquent, la valeur planifiée est le rythme auquel les planificateurs de projet pensaient que le travail serait achevé sur le projet. Une fois qu’un projet est en cours, le travail est terminé et le projet gagne de la valeur. En comparant la valeur planifiée à la valeur acquise, vous pouvez voir la progression du travail sur un projet. Le résultat de cette comparaison est appelé écart de planification. 

Si la valeur planifiée pour une période est supérieure à la valeur acquise, la quantité de travail qui a été effectuée sur un projet est inférieure à ce qui était prévu. Par conséquent, le projet est en retard. Étant donné que la valeur planifiée et la valeur acquise sont exprimées en termes monétaires, le temps de latence du projet reçoit également une valeur monétaire. 

Si la valeur planifiée pour une période est inférieure à la valeur acquise, la quantité de travail qui a été effectuée sur un projet est supérieure à ce qui était prévu. Par conséquent, le projet est en avance. Ce délai a également une valeur monétaire.

**Écart de coût** Étant donné que la valeur acquise utilise le prix de revient comme multiplicateur, la valeur acquise indique le coût du travail effectué sur un projet. Au fur et à mesure de l’avancement d’un projet, le journal des transactions fournit un enregistrement de l’argent réellement dépensé pour ce projet. En comparant la valeur acquise au coût réel, vous pouvez voir le montant d’argent dépensé par rapport à la valeur gagnée. Le résultat de cette comparaison est appelé écart de coût. 

Si le coût réel dépensé pour une période est supérieur à la valeur acquise, plus d’argent a été dépensé que gagné. Par conséquent, le projet dépasse le budget. 

Si le coût réel dépensé pour une période est inférieur à la valeur acquise, plus d’argent a été gagné que dépensé. Par conséquent, le projet est inférieur au budget.

## <a name="wbs-templates"></a>Modèles de WBS
Vous pouvez utiliser la fonctionnalité de modèles WBS pour créer des modèles standard pour les projets. Si les projets proposés par votre entreprise impliquent beaucoup de travail répétable, vous devriez envisager de créer un modèle WBS. 

Vous pouvez créer un modèle WBS à partir de la WBS d’un projet existant, de sorte que les connaissances et les meilleures pratiques que vous avez recueillies lors de la planification de ce projet puissent être réutilisées dans des projets similaires à l’avenir. Cependant, parfois, il peut ne pas être judicieux d’enregistrer l’ensemble de la WBS en tant que modèle. Par conséquent, vous pouvez également créer des modèles à partir de parties de la WBS pour un projet.

### <a name="saving-a-projects-wbs-as-a-template"></a>Enregistrer la WBS d’un projet en tant que modèle

Après avoir créé un modèle, vous pouvez l’importer dans la WBS d’un nouveau projet sous le nœud racine, ou sous n’importe quelle tâche dans la WBS du projet.

### <a name="importing-a-wbs-template-into-a-projects-wbs"></a>Importer un modèle WBS dans la WBS d’un projet

Lorsque vous importez des tâches, les tâches du modèle sont organisées en fonction de la date de début de la tâche sous laquelle elles sont importées. Lors de l’importation, le prédécesseur Relations sur les tâches modèles est utilisé pour calculer les dates de début des tâches importées. Le calendrier de travail standard du projet de destination est appliqué pour calculer les dates de fin des tâches importées, de sorte que les jours ouvrables et les heures de travail standard définis dans le calendrier de travail du projet en cours soient conservés. 

Les montants des coûts et les prix de vente sur les lignes d’estimation sont appliqués pour garantir que les prix spécifiques au projet ou au contrat de projet ont des dates valides.

### <a name="differences-between-a-projects-wbs-and-a-wbs-template"></a>Différences entre la WBS d’un projet et un modèle WBS

-   Les tâches des modèles WBS n’ont pas de dates de début et de fin.

Les jours ouvrés et non ouvrés ne sont pas définis pour les modèles WBS.

-   Les modèles WBS utilisent toujours le calendrier de planification configuré comme calendrier par défaut pour tous les projets.

Le calendrier de planification par défaut est utilisé uniquement pour connaître les heures d’une journée de travail standard.

-   Les relations de prédécesseur ne sont pas copiées dans un modèle WBS.

Étant donné que les modèles WBS n’ont pas de dates, la logique de date de début basée sur la date de fin d’un prédécesseur n’est pas requise.

-   Une ligne d’estimation du coût de la main-d’œuvre est automatiquement créée lorsqu’une tâche est créée dans un modèle de WBS. Le prix de vente et le coût de revient sont copiés à partir de l’employé sélectionné.

Les dépenses et les coûts d’article peuvent être créés manuellement, tout comme ils le peuvent sur la WBS d’un projet.

-   Les erreurs de planification sont affichées en cas d’écarts par rapport à la formule suivante :

Effort = Nombre de ressources × Durée × Nombre d’heures dans une journée de travail standard 

Vous pouvez corriger toutes les erreurs de planification en même temps en cliquant sur **Corriger toutes les erreurs de planification**. 

Vous pouvez également corriger les erreurs de planification individuellement en cliquant sur l’icône d’avertissement pour chaque tâche.





[!INCLUDE[footer-include](../includes/footer-banner.md)]