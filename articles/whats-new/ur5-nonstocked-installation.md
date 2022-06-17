---
title: Mettre à jour Project Operations dans votre environnement Finance
description: Cet article fournit des informations sur la mise à jour de Project Operations dans votre environnement Dynamics 365 Finance.
author: ruhercul
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 0cf9da8cc9d1f29dc41d4b119278e545047020bc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912467"
---
# <a name="update-project-operations-in-your-finance-environment"></a>Mettre à jour Project Operations dans votre environnement Finance

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_


Cet article fournit des informations sur la mise à jour de Dynamics 365 Project Operations dans votre environnement Dynamics 365 Finance. Trois procédures sont nécessaires pour mettre à jour Project Operations vers la mise à jour 5 (UR5) :

- [Importez le package dans votre projet de prévisualisation](#import)
- [Appliquez la mise à jour](#apply)
- [Mettez à jour votre environnement Dataverse](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importez le package dans votre projet LCS

1. Se connecter à [Lifecycle Services (LCS)](https://lcs.dynamics.com/) en tant que propriétaire de projet ou responsable environnement.
2. Dans la liste de vos projets, sélectionnez votre projet LCS.
3. Sur la page **Projet**, dans le groupe **Environnements**, ouvrez l’environnement que vous souhaitez mettre à jour.
4. Assurez-vous que l’environnement s’exécute. S’il n’est pas démarré, démarrez l’environnement.
5. Dans la section **Nouvelle version** sous **Mises à jour disponibles**, sélectionnez **Afficher la mise à jour** pour 10.0.15.

![Bouton Afficher la mise à jour.](media/view-update.png)

6. Sur la page **Mises à jour binaires**, cliquez sur **Enregistrer le package**.
7. Sur la page **Consulter et enregistrer les mises à jour**, cliquez sur **Enregistrer le package**.
8. Sur le volet **Enregistrer le package dans la bibliothèque d’actifs** qui s’ouvre, saisissez le nom du package, puis cliquez sur **Enregistrer le package**.
9. Lorsque LCS a terminé d’enregistrer le package, le bouton **Terminé** est activé. Cliquez sur **Terminé**. LCS vérifiera le package. La vérification peut prendre quelques minutes ou jusqu’à une heure.


## <a name="apply-the-package-update"></a><a name="apply"></a>Appliquez la mise à jour du package

1. Dans LCS, sur la page **Détails de l’environnement**, sélectionnez **Mettre à jour** > **Appliquer les mises à jour**.
2. Dans la liste, sélectionnez le package que vous avez enregistré précédemment, puis sélectionnez **Appliquer**.
3. Cliquez sur **Oui** pour confirmer le déploiement du package.

![Boîte de dialogue Confirmer le déploiement du package.](media/confirm-package-deployment.png)

4. Cliquez sur **Oui** pour confirmer la mise à jour de l’application.

![Boîte de dialogue Confirmer la mise à jour de l’application.](media/confirm-application-update.png)

Le déploiement et la mise à jour de l’application commenceront. 

Sur la page **Détails de l’environnement**, dans le coin supérieur droit, le statut de l’environnement sera mis à jour sur **Maintenance**. Dans environ deux heures, la mise à jour sera terminée. Les informations de version de l’application seront mises à jour pour **Microsoft Dynamics 365 for Finance and Operations 10.0.15** et le statut de l’environnement sera mis à jour sur **Déployé**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Mettez à jour votre environnement Dataverse

1. Connectez-vous au [centre d’administration Power Platform](https://admin.powerplatform.com/).
2. Dans la liste, recherchez et ouvrez l’environnement que vous avez utilisé pour installer Project Operations.
3. Sur la page **Environnements**, sélectionnez **Ressource** > **Applications Dynamics 365**.
4. Dans la liste, recherchez **Microsoft Dynamics 365 Project Operations**, et dans la colonne **Statut**, sélectionnez **Mise à jour disponible**.
5. Cochez la case **J’accepte les conditions d’utilisation**, puis sélectionnez **Mettre à jour**. La dernière version de la solution sera installée.

Une fois l’installation terminée, vous aurez la version 4.5.0.134 installée.

## <a name="configure-new-features"></a>Configurer de nouvelles fonctionnalités

### <a name="enable-dual-write-mapping"></a>Activer le mappage de la double écriture

Après avoir terminé la mise à jour sur les environnements Finance et Dataverse, vous pouvez activer les mappages à double écriture requis. Terminez les procédures suivantes pour activer les mappages de table de double écriture.

- [Mettre à jour les paramètres de sécurité sur l’environnement Customer Engagement](#security)
- [Actualiser les entités de données](#refresh)
- [Mettez à jour et exécutez les mappages en double écriture](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Mettre à jour les paramètres de sécurité sur l’environnement Dataverse

Les mises à jour suivantes des privilèges de sécurité pour les entités sont requises dans le cadre de la mise à jour vers UR5.

1. Dans votre environnement Dataverse, allez à **Paramètres**, et dans le groupe **Système**, sélectionnez **Sécurité**.

![Paramètres de l’environnement Dataverse.](media/Picture21.png)

2. Sélectionnez **Rôles de sécurité**.
3. Dans la liste des rôles, sélectionnez **Utilisateur d’application à double écriture** et sélectionnez l’onglet **Entités personnalisées**. 
4. Vérifiez que le rôle a les autorisations en **Lecture** et **Ajouter à** pour :

      - **Type de taux de change devise**
      - **Plan comptable** 
      - **Calendrier fiscal** 
      - **Registre**

5. Une fois le rôle de sécurité mis à jour, accédez à **Paramètres** > **Sécurité** > **Équipes**. Vérifiez que le rôle **Utilisateur d’application à double écriture** a été appliqué à l’équipe. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Actualiser les entités de données à partir de la mise à jour

1. Dans votre environnement Finance, ouvrez l’espace de travail **Gestion de données**, puis ouvrez la page **Paramètres du cadre**.
2. Sur l’onglet **Paramètres d’entité**, sélectionnez **Actualiser la liste des entités**.
3. Sélectionnez **Fermer** pour confirmer l’actualisation de l’entité.

 > [!NOTE]
 > Ce processus prendra environ 20 minutes. Vous serez averti lorsque l’actualisation sera terminée.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Mettre à jour les mappages de la double écriture

1. Dans l’espace de travail **Gestion des données**, sélectionnez **Double écriture**.
2. Sélectionnez **Appliquer des solutions**, sélectionnez les deux solutions dans la liste, puis sélectionnez **Appliquer**.
3. Sur la page **Double écriture**, sélectionnez les cartes de table suivantes, puis sélectionnez **Arrêter**.

    - **Intégration des chiffres réels Project Operations (msdyn_actuals)**
    - **Catégories de dépenses de projet d’intégration de Project Operations (msdyn_expensecategories)**
    - **Catégories de l’entité d’exportation des dépenses de projet de chiffres réels d’intégration de Project Operations (msdyn_expenses)**

4. Sur la page **Version carte de table**, appliquez une nouvelle version de la carte à chacune des trois entités.
5. Sur la page **Double écriture**, sélectionnez Exécuter pour redémarrer les cartes.
6. Dans la liste des cartes, sélectionnez la carte **Registre (msdyn_ledgers)** avec tous les prérequis et cocher la case **Synchronisation initiale**. 
7. Dans le champ **Sélection principale pour la synchronisation initiale**, sélectionnez **Applications de finances et d’opérations**, puis sélectionnez **Exécuter**.
 
 ![Synchronisation du mappage du registre.](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]