---
title: Installation d’un exemple de données
description: Cette rubrique fournit des informations sur l’installation d’exemples de données dans Project Service Automation.
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.service: project-operations
ms.reviewer: kfend
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: aaeb4163c7ace1c3bf4db61f1a10a13cfbdc4fc2
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144500"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Installation d’exemples de données pour l’application Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

Pour vous aider à créer vos propres environnements de démonstration, Microsoft fournit des packages d’exemples de données téléchargeables qui présentent les fonctionnalités de vos applications. Il existe deux types de packages d’exemples de données :
- les données de configuration/référence
- les données de démonstration (données de configuration/référence et transactionnelles, telles que des ordres de travail et les projets)

Les packages d’exemples de données de **référence** sont téléchargeables en trois packages distincts, ainsi vous pouvez installer les données uniquement pour Project Service, ou uniquement pour Field Service, ou vous pouvez installer les exemples de données pour les deux applications en même temps.

Les packages d’exemples de données de configuration/référence sont :

- [**V902PSMasterData** - Project Service version 3.x uniquement](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - Field Service version 8.x uniquement](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x et Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

Le package de données de **démonstration** les plus récent est :

 - [**FPSDemoData** - Field Service 8.x et Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   Les instructions d’installation diffèrent légèrement dans la section sur la création et de configuration pour les utilisateurs mais le reste est le même que dans le précédent [**billet de blog**](https://aka.ms/fpsdemodatablog). Ce package comprend un jeu de données de démonstration réduit et son installation dure environ 3 heures.

Ces packages d’exemples de données ne sont disponibles qu’en anglais

> [!IMPORTANT]
> **Il n’existe aucun moyen de désinstaller les exemples de données.** Vous devez installer uniquement ces packages lors de démonstrations, d’évaluations, de formations ou de test des systèmes. Notez également que l’installation d’un package individuel, puis l’installation de l’autre package individuel, n’est pas prise en charge. (En d’autres termes, vous ne pouvez pas définir **FSMasterData** suivi de **PSMasterData**, ou vice versa.) Si vous avez besoin d’exemples de données pour les deux applications par la suite, vous devez installer le package **v902FPSMasterData**.

Lorsque vous installez l’un des packages d’exemples de données, le processus d’installation effectue les actions suivantes :

- Crée ou définit des paramètres par défaut pour utiliser Project Service, Field Service, ou les deux applications (le cas échéant).

- Importe des exemples de données pour les applications, telles que des ressources pouvant être réservées, des rôles spécifiques à l’application, des listes de prix de vente et de revient, des unités d’organisation, des enregistrements de processus de vente, ainsi que d’autres entités pour démontrer les fonctionnalités clés.  

Avec le package de **données de démonstration**, vous obtenez les données transactionnelles ci-dessus et supplémentaires, telles que des ordres de travail et des projets.

Vous voulez savoir quelles fonctionnalités vous pouvez démontrer à l’aide des exemples de données ? Consultez le scénario fictif de Fabrikam Robotics dans [Notes techniques](#technical-notes).

Si vous avez des questions concernant l’installation de ces packages d’exemples de données, [envoyez-nous un courrier électronique à l’adresse fpsdemodata@microsoft.com](mailto:fpsdemodata@microsoft.com).

## <a name="requirements"></a>Besoins

Le protocole d’installation assume ce qui suit concernant votre instance cible (org) :

- La langue de base est l’anglais et la devise de base est le dollar américain (USD,$).

- L’organisation n’a encore aucune donnée Project Service ou Field Service, ou n’a que des données de base par défaut fournies avec une nouvelle organisation.

- La version adéquate de l’application métier est déjà installée :
       
    - **Pour FPSDemoData ou v902FPSMasterData :** L’organisation a la version 8.x de Field Service et la version 3.x de Project Service installée.

    - **Pour v902PSMasterData :** L’organisation a la version 3.x de Project Service installée.

    - **Pour v902FSMasterData :** L’organisation a la version 8.x de Field Service installée.

> [!NOTE]
> Si vous devez installer les exemples de données sur un environnement de version d’évaluation ou de démonstration Project Service et Field Service existant qui possède déjà des données (non recommandé), vous devrez interrompre les prévérifications de sécurité effectuées par le programme d’installation. Pour plus d’informations, consultez les Notes techniques ci-dessous.

## <a name="prepare-for-installation"></a>Préparer l’installation

Vous devez exécuter le programme d’installation sur un ordinateur disposant d’une version récente de Windows (Windows 10 privilégié).

Vous devez prévoir que l’ordinateur reste connecté à un réseau, et pour que l’installation s’exécute jusqu’à **1 heure** pour les **données de configuration/référence**. (Normalement l’installation prend environ 30 minutes pour **FPSMasterData**, qui comprend des exemples de données pour les deux applications.) Pour **FPSDemoData**, l’installation prend environ **3 heures**.

L’ordinateur doit avoir la fonction d’économiseur d’écran désactivée. Sinon, les informations d’identification de session pour l’installation peuvent être perdues lorsque l’économiseur d’écran s’active (sauf si vous conservez une session active tout du long).

> [!div class="mx-imgBorder"]
> ![Capture d’écran des paramètres de l’économiseur d’écran, avec l’économiseur d’écran désactivé](media/sample-data-1.png)

## <a name="download-and-unpack"></a>Téléchargez et décompresser

Le programme d’installation des exemples de données de Project Service et de Field Service est distribué en tant qu’exécutable à extraction automatique. Les noms de fichiers peuvent varier selon le package d’exemple de données, mais sinon les étapes sont les mêmes quel que soit le package que vous installez.

Après le téléchargement d’un package, exécutez le fichier .exe, puis acceptez les conditions générales pour décompresser le fichier zip compressé. Vous devez ensuite extraire le contenu de ce fichier dans un dossier de l’ordinateur.

En fonction du système d’exploitation et des paramètres de sécurité, vous devrez peut-être procéder comme suit après avoir décompacté le fichier zip :

1. Cherchez et cliquez avec le bouton droit sur le fichier **FPSDemoData.dll** dans le dossier **v902FPSMasterData** / **PackageDeployer_FPSDemoData**.

2. Choisissez **Débloquer**.

3. Sélectionnez **Appliquer**.

4. Sélectionnez **OK**.


## <a name="create-or-configure-users"></a>Créer ou configurer les utilisateurs

Le package **FPSDemoData** nécessite six utilisateurs tandis que les packages **FPSMasterData** nécessitent un utilisateur. Reportez-vous à celui qui est approprié pour votre exemple de package de données.

## <a name="create-or-configure-users---setupreference-data-packages"></a>Créer ou configurer des utilisateurs - packages de données de configuration/référence

Le package **FPSMasterData** est conçu pour l’installation avec un utilisateur appelé Spencer Low avec les paramètres décrits ici. Pour installer le package correctement, vous devez créer (ou renommer temporairement) les utilisateurs dans votre environnement pour faire correspondre la configuration des exemples de données entrantes.

Pour créer et configurer les utilisateurs, accédez à **Paramètres** > **Sécurité** > **Utilisateurs**, et procédez comme suit :

1. Définissez UserFullname="Spencer Low" avec le nom d’utilisateur "spencerl" (**minuscules**) pour les rôles de Responsable du projet et de Gestionnaire des recommandations.

2. Sélectionnez l’utilisateur **Spencer Low**, puis **Gérer les rôles**. Recherchez et sélectionnez le rôle **Administrateur système**, puis sélectionnez **OK** pour accorder les droits d’administration complets à Spencer Low. Cette étape est nécessaire pour garantir que les exemples d’enregistrements sont créés avec la propriété d’utilisateur correcte et par conséquent pour renseigner les vues correctement.

3. Dans le package téléchargé, vous devez mettre à jour un dossier de mappage de données contenant des adresses de messagerie du contexte de l’utilisateur par défaut. Pour ce faire, ouvrez **PkgFolder**, puis recherchez et ouvrez le fichier **ImportUserMapFile.xml** dans le Bloc-notes (ou un éditeur Visual Studio ou XML autre). Définissez le champ **DefaultUserToMapTo=** sur l’adresse de messagerie de l’utilisateur Spencer Low.

4. Si vous n’utilisez pas Spencer Low avec le nom d’utilisateur **spencerl**, vous devez mettre à jour un fichier supplémentaire. Ouvrez le fichier **DemoDataPreImportConfig.xml**, puis rechercher la balise **userstocreateandconfigure**. Mettez à jour la balise **\<login\>** avec le nom d’utilisateur de votre utilisateur Spencer Low. Pour plus de détails, consultez les [Notes techniques](#technical-notes).

## <a name="create-or-configure-users---demo-data-package"></a>Créer ou configurer des utilisateurs - Package de données de démonstration

Le package de données de démonstration nécessite six utilisateurs. Pour que le package s’installe correctement, procédez comme suit :

 1. Créez ou renommez temporairement les utilisateurs existants pour qu’ils correspondent à la configuration des exemples de données en accédant à **Paramètres** > **Sécurité** > **Utilisateurs**.
 
    Ces rôles sont nécessaires uniquement des démonstrations basées sur des personnages.  
    - Nom complet de l’utilisateur = « David » comme technicien de service après-vente   
    - Nom complet de l’utilisateur = « Jamie Reding » comme distributeur de service clientèle et de service après-vente   
    - Nom complet de l’utilisateur = « Molly Clark » comme gestionnaire de comptes   
    - Nom complet de l’utilisateur = « Spencer Low » comme gestionnaire des recommandations pratiques et responsable de projet  
    - Nom complet de l’utilisateur = « Veronica Quek » comme membre d’équipe   
    - Nom complet de l’utilisateur = « William Contoso »
  
2. Dans le cadre de l’importation de données de démonstration, affectez aux six utilisateurs ci-dessus le rôle d’administrateur afin que les exemples d’enregistrements s’importent correctement. 

3. Ouvrez **PkgFolder** puis recherchez et ouvrez **ImportUserMapFile.xml**. Mettez à jour les champs **New=** avec les adresses de messagerie des utilisateurs correspondants dans votre système.

   > [!div class="mx-imgBorder"]
   > ![Capture d’écran de UserMapFile](media/sample-data-7.png)

4. Si votre utilisateur avec le nom complet « Spencer Low » a ID utilisateur autre que **« spencerl »**, vous devez mettre à jour un fichier supplémentaire. Ouvrez **DemoDataPreImportConfig.xml** et rechercher la balise **userstocreateandconfigure**. Mettez à jour la balise **\<login\>** avec le loginId (sensible à la casse). 

5. Le calendrier du premier utilisateur (dans la balise **userstocreateandconfigure**) est utilisé pour exécuter les heures de travail de toutes les ressources pouvant être réservées à l’importation des données de démonstration. Accédez à **Paramètres** > **Sécurité** > **Utilisateurs**, recherchez votre utilisateur « Spencer Low », puis ouvrez l’option « Heures de travail ». Modifiez les heures de travail existantes, sélectionnez l’option **Planification hebdomadaire récurrente complète du début à la fin**. Assurez-vous que **Les heures de travail sont définies de 8 h 00 à 17 h 00 (9 heures), du lundi au vendredi et que le fuseau horaire est défini sur l’heure du Pacifique (É.-U. et Canada)**. Ceci est indispensable pour que la projet et le tableau de planification s’affichent comme prévu.

**Recommandation :** Envisagez de créer une sauvegarde de votre organisation maintenant, au cas où vous auriez à revenir à votre point de départ si une opération se passe mal pendant l’installation des exemples de données. Pour plus d’informations, voir [Sauvegarder et restaurer les instances](https://docs.microsoft.com/dynamics365/customer-engagement/admin/backup-restore-instances).

## <a name="run-the-package-deployer"></a>Exécuter l’Package Deployer

1. Cherchez et exécutez **PackageDeployer.exe** dans le dossier **v902FPSMasterData** OU **PackageDeployer_FPSDemoData**.

2. Acceptez les conditions générales.

3. Dans la fenêtre suivante :

   a. Sélectionnez le type de déploiement **Office 365**.

   b. Utilisez l’utilisateur et le mot de passe de l’utilisateur Administrateur système configuré dans « Créer ou configurer des utilisateurs » (« Spencer Low » avec le nom d’utilisateur « spencerl »).

   c. Assurez-vous que la case à cocher **Afficher la liste des organisations disponibles** est activée.

      > [!div class="mx-imgBorder"]
      > ![Capture d’écran de la fenêtre de Package Deployer avec « Afficher la liste des organisations disponibles » sélectionnée](media/sample-data-2.png)

4. Sélectionnez l’organisation dans laquelle vous souhaitez installer les exemples de données.

5. Sélectionnez **Suivant** jusqu’à ce que la boîte de dialogue **Paramétrage de données de démonstration** s’affiche.

   > [!div class="mx-imgBorder"]
   > ![Capture d’écran de la fenêtre du statut du programme d’installation des données de démonstration](media/sample-data-3.png)

6. Avant de continuer, notez que l’installation des exemples de données peut prendre jusqu’à une heure (normalement ~10 minutes). Vous devrez vous assurer que l’ordinateur reste activé et connecté à un réseau tout au long du processus d’installation, et que votre session reste active.   

7. Lorsque vous êtes prêt, cliquez sur **Suivant** pour démarrer le processus d’installation des exemples de données. Une fois les exemples de données chargées, cliquez sur **Terminer**.

## <a name="verify-the-sample-data-installation"></a>Vérifier l’installation des exemples de données

Pour une vérification de validité, vérifiez que le nombre d’enregistrements et les types d’entités répertoriées dans le scénario fictif de Fabrikam Robotics apparaissent comme prévu.

Une fois les exemples de données complètement chargées, connectez-vous comme utilisateur Spencer Low et confirmez comme suit :

- Si l’application Project Service est installée, accédez à **Project Service** > **Paramètres** > **Tarifs**. Vérifiez que vos taux de factures et de coûts existent dans la devise appropriée pour chaque pays/région dans le jeu de données.

- Si l’application Project Service est installée, accédez à **Universal Resource Scheduling** > **Paramètres** > **Unités d’organisation**. Vérifiez qu’une liste de prix de revient dans la devise appropriée a été associée à chaque unité d’organisation (à l’exclusion des entrées par ville). S’il en manque, recherchez et associez la liste de prix de revient correcte.

- Si l’application Field Service est installée, accédez à **Project Service** > **Paramètres** > **Tarifs**. Vérifiez que vos taux de factures et de coûts existent. Accédez à **Field Service** > **Paramètres** > **Tarifs** et vérifiez que vos taux de factures et de coûts existent, avec la devise appropriée, pour chaque pays/région dans le jeu de données.

  > [!div class="mx-imgBorder"]
  > ![Capture d’écran des tarifs actifs](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![Capture d’écran des unités d’organisation actives](media/sample-data-5.png)

## <a name="technical-notes"></a>Notes techniques

Voir ci-dessous pour plus de détails techniques sur l’installation de ces données.

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>Installation d’exemples de données sur des données existantes (non recommandé)

Si vous devez installer les exemples de données sur un environnement de version d’évaluation ou de démonstration Field Service et Project Service existant qui possède déjà des données, vous devrez interrompre les prévérifications de sécurité effectuées par le programme d’installation.

Pour ce faire, accédez au dossier **PkgFolder** pour rechercher et ouvrir le fichier **DemoDataPreImportConfig.xml** avec Bloc-notes (ou un autre éditeur XML).

Cherchez la valeur suivante, puis modifiez le paramètre de True vers False :

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

Ce changement permet au programme d’installation de contourner certaines vérifications de sécurité critiques, notamment :

- Confirmation qu’il n’existe pas plus d’un enregistrement **Unité d’organisation** actif, puis le renommant en **Fabrikam US**.

- Confirmer qu’il n’existe pas plus d’un enregistrement **Modèle d’emploi** actif.

- Confirmation qu’il n’existe pas plus d’un enregistrement **Paramètre du projet** actif, puis en renommant cette entrée en **Paramètres**.

### <a name="configuration-components"></a>Composants de configuration

Un certain nombre d’autres composants de configuration dans ce fichier de configuration pré-importation. Pour les utilisateurs techniques, citons notamment :

- **\<RequiredSolutions\>** indique les installations de solution et leur numéros de version requis.

- **\<InstallSampleData\>** contrôle si les exemples de données prêts à l’emploi pour les applications sont installés.

    - false - ignore l’installation de ces données intégrées (amovible)

    - true - installe les exemples de données intégrées en même temps que l’installation des exemples de données FS et PSA

- **\<PreImportDataCollection\>** indique les mappages de données de fichier plat et les enregistrements associés à importer avant l’installation du principal exemple de données.

- **\<EntitiesToEnableScheduling\>** indique quelles entités doivent être activées pour les réservations dans Microsoft Dynamics Scheduling (aussi appelée Universal Resource Scheduling).

- **\<UsersToCreateAndConfigure\>** indique les ressources pouvant être réservées qui seront créés (si elles n’existent pas déjà) avant que l’importation d’exemple de données s’exécute. Notez que la ressources réservable d’exemple de données système source correspond aux enregistrements de ressource réservable système cible sur le FullName et la connexion de chaque ressource. Par conséquent, il n’est PAS possible de modifier les noms de ce fichier de préconfiguration sauf si vous importez d’abord un exemple de données dans un système cible à l’aide de ces noms, puis que vous renommez les ressources pouvant être réservées avec le nom souhaité défini dans les enregistrements d’utilisateurs activés, puis que vous exportez de nouveau les données pour les importer dans votre système de destination final (en mettant à jour d’anciennes et de nouvelles entrées **ImportUserMapFile.xml** en conséquence.)

- **\<PluginsToDisable\>** indique les plug-ins de ligne de produit très légers qui doivent être désactivés lors de l’importation de l’exemple de données et réactivés par la suite.

### <a name="fabrikam-robotics-fictitious-scenario"></a>Scénario fictif de Fabrikam Robotics

Les packages d’exemples de données de référence Field Service et Project Service installent la **solution de données principales de Fabrikam Robotics (v 3.0.0.0)**, avec environ 4 000 enregistrements et environ 40 entités différentes. Les packages d’exemples de données distincts de Field Service ou de Project Service contiennent un sous-ensemble d’exemples de données **v902FPSMasterData** pour cette application. Le package **Données de démonstration** installe la **solution de données de démonstration de Fabrikam Manufacturing (v3.0.0.7)** avec environ 22 000 enregistrements dans 148 entités.

La société fictive, Fabrikam Robotics, est fabricant de robots de lignes d’assemblage d’appareils électronique et est connue pour la qualité de ses produits, un service clientèle innovant et fiable, notamment ses services de planification de l’installation, de mise en œuvre, et de maintenance permanente. Fabrikam a son siège aux États-Unis (Fabrikam US), et offre ses services basés sur des projets en France, en Inde, au Royaume-Uni, et en Suisse.

Les opérations de service après-vente sont centrées sur les États-Unis, principalement dans la région métropolitaine de Seattle. La société s’appuie sur la connectivité de l’Internet des objets (IoT) pour analyser les performances des actifs clients et fournir des services sur site de plus en plus proactifs.

Ci-dessous une vue d’ensemble globale des exemples de données :

- Éléments d’exemple de données courants (inclus dans les deux applications)

    - 1 utilisateur

    - 71 comptes

    - 137 contacts

    - Différents types de transactions et de catégories

    - 50 produits et 1 tarification de produits

    - 14 listes des prix/coûts

    - 31 caractéristiques (compétences de ressources) dans 2 modèles d’évaluation avec 3 niveaux (valeurs d’évaluation)

- Project Service

    - 8 unités d’organisation

    - 6 niveaux d’utilisation spécifiques aux rôles

    - Plus de 2 800 spécifications de prix et de rôles

- Field Service

    - 4 secteurs de vente

    - 5 types d’ordres de travail

    - 22 actifs de client

    - 9 types d’incident avec une plage de caractéristiques de ressource associées (9), des services (13) et des tâches de services (13)
   
Le package **Données de démonstration** installe environ 179 ordres de travail, 12 projets et des données transactionnelles connexes. 

### <a name="change-the-work-hours-for-sample-resources"></a>Modifier les heures de travail des exemples de ressources

Par défaut, toutes les ressources pouvant être réservées ont un calendrier de 24 heures de travail.

Si vous devez modifier les heures de travail pour des exemples de ressources pouvant être réservées, accédez à **Universal Resource Scheduling** > **Planification** > **Ressources**.

Sélectionnez un utilisateur (par exemple, Spencer Low) et modifiez les heures de travail de Spencer avec les heures que vous souhaitez appliquer à plusieurs utilisateurs. Accédez à **Universal Resource Scheduling** > **Paramètres** > **Modèles d’heures de travail** et modifiez l’enregistrement **Modèle de travail par défaut**. Dans le champ **Modèle de ressource**, sélectionnez un utilisateur avec les heures de travail à appliquer à d’autres ressources. Accédez à **Universal Resource Scheduling** > **Planification** > **Ressources** > **Ressources pouvant être réservées actives**. Sélectionnez les ressources à modifier, puis sélectionnez **Définir le calendrier**. Dans la liste déroulante **Modèle d’emploi**, sélectionnez le modèle **Heure de travail par défaut** ou un autre modèle avec la ressource de création de modèles correcte. Lorsque vous accédez au tableau de planification, vous devriez voir maintenant que les ressources ont mis à jour les heures de travail.

> [!div class="mx-imgBorder"]
> ![Capture d’écran de ressources pouvant être réservées actives](media/sample-data-6.png)
