---
title: Nouveautés de décembre 2020 – Déploiement simplifié de Project Operations – Traiter la facturation pro forma
description: Cette rubrique fournit des informations sur les mises à jour qualité disponibles dans la version de décembre 2020 du déploiement simplifié de Project Operations – Traiter la facturation pro forma.
author: sigitac
manager: Annbe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: bfa13ab74031eb52c128fed16a31e3a8167e8bde
ms.sourcegitcommit: ec8ab099a03725de9f61edfdeb90fbefae54cd4e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "4707670"
---
# <a name="whats-new-december-2020---project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Nouveautés de décembre 2020 – Déploiement simplifié de Project Operations – Traiter la facturation pro forma

_**S’applique à :** Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique s'applique aux composants et versions suivants de Dynamics 365 Project Operations :

  - Version 4.5.0.134 de Project Operations dans l’environnement Dataverse 

Le tableau suivant répertorie les mises à jour de la version 4.5.0.134 de Project Operations dans l’environnement Dataverse.

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 1986009 | Les lignes de journal créées manuellement ont des performances incohérentes si elles sont confirmées avant que le projet ne soit lié ou dissocié d'une ligne de contrat. |
| Facturation et tarification | 2014153 | Les produits ne sont pas facturés lorsqu'ils sont exécutés à partir du calendrier de facturation. |
| Facturation et tarification | 2014159 | Les produits ne sont pas extraits lorsque la facture est actualisée pour les transactions. |
| Facturation et tarification | 2028174 | Les mises à jour des détails de la ligne de facture doivent suivre la logique du journal de correction. |
| Facturation et tarification | 2028315 | Corrections du comportement de la grille imbriquée modifiable. |
| Facturation et tarification | 2031070 | L'ajustement des détails de la ligne de facture corrective doit suivre la logique du journal de correction. |
| Facturation et tarification | 2034186 | Il doit pouvoir mettre à jour un projet sur une ligne de contrat. |
| Facturation et tarification | 2034206 | Le statut d'ajustement doit être défini lors de l'annulation réelle lors de la dissociation d'un projet d'une ligne de contrat. |
| Facturation et tarification | 2040871 | Autoriser les mises à jour des cellules d'unités et de groupes d'unités sur la grille Estimations de dépenses. |
| Facturation et tarification | 2053754 | Les chiffres réels créés à partir des modifications de factures ne sont pas marqués avec le statut d'ajustement et le statut de facturation. |
| Facturation et tarification | 2057874 | Connexion de transaction correcte créée lors de la modification des détails de la ligne de facture. |
| Facturation et tarification | 2057875 | Origines de transaction correcte créées lors de la modification des détails de la ligne de facture. |
| Facturation et tarification | 2057944 | État à ne pas dépasser défini comme Validé pour les chiffres réels qui ne sont pas prêts pour la facturation à partir d'une correction de facture. |
| Facturation et tarification | 2057963 | Split Create\_Product privilege à partir du provilège Create\_ProjectContract. |
| Facturation et tarification | 2067622 | L'icône de traitement doit être affichée lors de la génération des jalons. |
| Facturation et tarification | 2067624 | Le montant contracté doit être marqué comme Entreprise recommandée lors de la génération des jalons. |
| Facturation et tarification | 2086880 | Masquer le bouton **Suggestion** sur le ruban pour les lignes de devis basées sur un projet. |
| Déploiement et configuration | 2101152 | Dans le nouvel environnement créé à l'aide du modèle Project Operations du Centre d'administration Power Platform, toutes les opérations de post-installation doivent être effectuées. |
|   Gestion des opportunités | 2022204 | La grille de facturation basée sur un projet sur l'onglet **Facturation des tâches** de la page **Projet** doit masquer la grille basée sur un projet s'il n'y a pas de ligne de devis/contrat avec **Toutes les tâches** et inversement. |
|   Gestion des opportunités | 2086601 | Les rôles et catégories désactivés ne doivent pas être copiés dans la liste des rôles facturables et des catégories facturables sur les lignes de devis et les lignes de contrat. |
| Planification et suivi de projets | 1949065 | La visibilité des données fonctionne correctement avec un zoom de 200 % |
| Planification et suivi de projets | 2046317 | Possibilité de renommer l'entité de projet dans Project Operations |
| Planification et suivi de projets | 2057171 | Message d'erreur mis à jour lorsque le champ **Date de début du projet** est vide sur la page **Projet**. |
| Planification et suivi de projets | 2057197 | La copie de ligne d'estimation avec référence de tâche n'est pas prise en charge. |
| Planification et suivi de projets | 2060687 | L'avertissement de fuseau horaire disparaît désormais au terme d'une durée spécifique. |
| Gestion des ressources | 1832887 | L'ID de catégorie de ressource par défaut doit être statique pour garantir des charges de données répétables pour les environnements Dataverse et Finance. |
| Temps et dépenses | 2034882 | Le bouton **Nouveau** s'affiche deux fois sur la barre de commande pour les entrées de temps lorsque Dynamics 365 Field Service est installé. |
| Temps et dépenses | 2056028 | Mettrez à jour la page **Modifier l'heure** pour inclure la chronologie. |
| Temps et dépenses | 1983747 | Le graphique d'entrées de temps affiche des données supplémentaires. |
