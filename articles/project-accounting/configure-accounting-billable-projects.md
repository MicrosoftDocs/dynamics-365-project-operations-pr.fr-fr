---
title: Configurer la comptabilité des projets facturables
description: Cet article fournit des informations sur les options de comptabilisation des projets facturables.
author: sigitac
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5020c978f0667543aed2b373d262dcda9688b02c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916423"
---
# <a name="configure-accounting-for-billable-projects"></a>Configurer la comptabilité des projets facturables

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Dynamics 365 Project Operations prend en charge diverses options de comptabilité pour les projets facturables qui comprennent des transactions en régie et à prix fixe.

- **Transactions de temps et de matériaux et à prix fixe** : Ces transactions sont facturées au fur et à mesure de l’avancement des travaux en fonction de la consommation d’heures, de dépenses, d’articles ou d’honoraires sur le projet. Ces coûts de transaction peuvent être rapprochés du produit de chaque transaction et le projet est facturé à mesure de l’avancement des travaux. Le produit du projet peut également être provisionné au moment de la transaction. Lors de la facturation, les revenus sont constatés et le cas échéant, les revenus à recevoir sont contrepassés.
- **Transactions à prix fixe** : Ces transactions sont facturées selon un calendrier de facturation basé sur le contrat de projet. Le produit des transactions à prix fixe peut être constaté lors de la facturation ou calculé et validé périodiquement, selon le mode **Contrat complété** ou **Pourcentage d’achèvement**.

Un projet est considéré comme facturable lorsqu’il est associé à une ou plusieurs lignes de contrat. Une ligne de contrat de projet définit pour elle-même le mode de facturation et les types de transaction autorisés.

À titre d’exemple, Fabrikam Robotics a remporté un contrat de projet avec Adatum Corporation pour l’optimisation des équipements. Adatum paiera un montant fixe de 10 000 $ USD pour couvrir les dépenses engagées pour le projet. Il s’agit d’une méthode de facturation à prix fixe. Le temps et les frais du projet seront facturés par utilisation. Il s’agit d’une méthode de facturation du temps et du matériel. Tous les travaux seront suivis sous un seul projet nommé, l’optimisation des équipements Adatum.

Un membre de l’équipe de projet envoie huit heures de travail sur le projet Optimisation des équipements Adatum. Lorsque le chef de projet approuve cette durée, le système utilise le mode de facturation en régie pour créer des transactions réelles, une facture et un compte. Cette transaction ne sera pas incluse dans le calcul de l’estimation des revenus à prix fixe.

Un autre membre de l’équipe du projet soumet des frais de déplacement pour 2 000,00 $ USD dans le cadre du projet d’optimisation de l’équipement Adatum. Lorsque le chef de projet approuve cet envoi, le système utilise un mode de facturation à prix fixe pour créer des transactions réelles et un compte pour cette dépense de projet. Le client ne sera pas facturé sur la base de cette transaction. À la place, il sera facturé à l’aide de jalons de facturation configurés séparément. Cette transaction de dépense sera incluse conjointement avec les estimations des dépenses dans le calcul de l’estimation du produit à prix fixe.

Les principes comptables relatifs aux transactions de projet sont définis dans les profils de coût et de produit de projet. Pour chaque transaction de projet, le système détermine le profil de coût et de revenu du projet approprié en utilisant les règles de profil de coût et de revenu du projet qui ont été configurées.

## <a name="define-project-cost-and-revenue-profiles"></a>Définir les profils de coût et de revenu du projet 

Les profils de coûts et de revenus du projet déterminent les règles comptables des transactions du projet. Ces profils sont configurés dans le module Gestion et comptabilité de projet. 

Effectuez les étapes suivantes pour créer un profil de coût et de revenu du projet. 

1. Aller à **Gestion de projets et comptabilité** > **Configurer** > **Validation** > **Profils de coûts et de revenus du projet**. 
2. Sélectionnez **Nouveau** pour créer un profil de coût et de revenu du projet.
3. Dans le champ **Nom**, saisissez le nom et une brève description du profil.
4. Dans le champ **Mode de facturation**, sélectionnez **Régie** ou **Prix fixe**.
5. Développez le raccourci **Comptabilité**. Les champs de cet onglet définissent les principes comptables utilisés lorsque les transactions de projet sont journalisées à l’aide de la feuille Intégration Project Operations, puis facturées au moyen de la proposition de facture de projet.
6. Sélectionnez les informations adéquates dans les champs suivants sur le raccourci **Comptabilité** :

    - **Valider les coûts – heure** :

       - *Aucune comptabilité* : Le coût des transactions de temps ne sera pas validé dans la Comptabilité lorsque le journal d’intégration de Project Operations est validé. Cependant, le comptable peut enregistrer les coûts à l’aide de la fonction Valider les coûts ultérieurement.
       - **Solde** : Le coût des transactions de temps sera débité sur le type de compte Comptabilité, *TEC - Valeur de coût* et crédité au *Compte de répartition de la paie* dans la configuration de la Validation dans la comptabilité. Le comptable utilisera la fonction de comptabilisation des coûts pour déplacer ce coût d’un compte de solde vers un compte de résultat sur une base périodique.
       - **Compte de résultat** : Lors de la validation du journal d’intégration de Project Operations, le coût de la transaction de temps sera débité du compte Comptabilité de type *Coût*, et crédité au *Compte de répartition de la paie* défini sur l’onglet **Coût** sur la page **Configuration de la validation comptable** (**Gestion de projets et comptabilité** \> **Configurer** \> **Validation** \> **Configuration de la validation comptable**). Il s’agit de la configuration la plus courante pour les transactions de temps et de matériel.
        - *Jamais de comptabilité* : Le coût des transactions de temps ne sera jamais enregistré dans la comptabilité.

    - **Valider les coûts – dépenses** :

         - **Solde** : Lors de la validation du journal d’intégration de Project Operations, le coût de transaction de dépenses sera débité du compte de comptabilité de type *TEC – Valeur de coût* tel que défini sur l’onglet **Coût** sur la page **Configuration de la validation comptable** et crédité sur le compte de contrepartie sur la ligne de journal. Les comptes de contrepartie par défaut pour les dépenses sont définis dans **Gestion de projets et comptabilité** > **Configurer** \> **Validation** \> **Compte de contrepartie par défaut pour les dépenses**. Le comptable utilisera la fonction de **comptabilisation des coûts** pour déplacer ce coût d’un compte de solde vers un compte de résultat sur une base périodique.
        - **Compte de résultat** : Lors de la validation du journal d’intégration de Project Operations, le coût de transaction de dépenses sera débité du compte de comptabilité de type *TEC – Valeur de coût* tel que défini sur l’onglet **Coût** sur la page **Configuration de la validation comptable** et crédité sur le compte de contrepartie sur la ligne de journal. Les comptes de contrepartie par défaut pour les dépenses sont définis dans **Gestion de projets et comptabilité** \> **Configurer** \> **Validation** \> **Compte de contrepartie par défaut pour les dépenses**.
      
    - **Coûts de validation – article** :

         - **Solde** : Lors de la validation du journal d’intégration de Project Operations, le coût de transaction de l’article sera débité du type de compte général *Travaux en cours – Valeur de coût – article* tel que défini sur l’onglet **Coût** de la page **Paramétrage de la validation dans la comptabilité** et crédité à :
    
              - Pour le type de document Utilisation : compte **Coût - article** sur **Paramétrage de la validation dans la comptabilité**.  
              - Pour le type de document Achat : **Compte d’intégration d’approvisionnement** sur **Paramètres de gestion et comptabilité des projets**.
           Le comptable utilisera la fonction de **comptabilisation des coûts** pour déplacer ce coût d’un compte de solde vers un compte de résultat sur une base périodique.
        - **Résultat** : Lors de la validation du journal d’intégration de Project Operations, le coût de transaction de l’article sera débité du type de compte général *Coût* tel que défini sur l’onglet **Coût** de la page **Paramétrage de la validation dans la comptabilité** et crédité à :
         
             - Pour le type de document Utilisation : compte **Coût - article** sur **Paramétrage de la validation dans la comptabilité**.  
             - Pour le type de document Achat : **Compte d’intégration d’approvisionnement** sur **Paramètres de gestion et comptabilité des projets**.
       
    - **À la facturation du compte** :

        - **Solde** : Lors de la validation de la proposition de facture de projet, une transaction sur le compte (étape de facturation) sera créditée sur le compte de comptabilité de type *TEC facturés – sur compte* tel que défini sur l’onglet **Revenu** sur la page **Configuration de la validation comptable**, et débité sur le compte du solde client.
         - **Compte de résultat** : Lors de la validation de la proposition de facture de projet, une transaction sur le compte (étape de facturation) sera créditée sur le compte de comptabilité de type *Revenu facturé – sur compte* tel que défini sur l’onglet **Revenu** sur la page **Configuration de la validation comptable**, et débité sur le compte du solde client. Les comptes de solde client sont définis dans **Comptabilité client** \> **Configuration** \> **Profils de validation client**.

   Lorsque vous définissez les profils de validation pour les méthodes de facturation du temps et du matériel, vous avez la possibilité de générer des revenus par type de transaction (heure, dépense, article et frais). Si l’option **Revenus à recevoir** est définie sur **Oui**, les transactions de vente non facturées dans le journal d’intégration de Project Operations seront enregistrées dans la comptabilité. La valeur des ventes est débitée du compte **Travaux en cours – compte de valeur des ventes** et crédité au compte **Revenus à recevoir – valeur des ventes** créé sur la page **Configuration de la validation comptable**, sur l’onglet **Revenu**. 
  
  > [!NOTE]
  > L’option, **Revenus à recevoir** est disponible uniquement lorsque le type de transaction correspondant **Coût** est comptabilisé dans le compte de résultat.
    
7. Développez le raccourci **Estimation**. Les champs de cet onglet définissent les paramètres de calcul des estimations du produit à prix fixe. Les champs de cet onglet s’appliquent uniquement aux profils de coût et de revenus du projet avec une méthode de facturation de **Prix fixe**.
8. Sélectionnez les informations adéquates dans les champs suivants sur le raccourci **Estimation** :

    - **Principe utilisé pour les calculs d’achèvement de projet** :

        - **Contrat terminé** : Le rapprochement des coûts et la constatation des revenus ne se produisent qu’à la fin du projet. Les coûts sont reflétés comme TEC dans le solde jusqu’à ce que le projet soit terminé.
        - **Pourcentage terminé** : Les revenus à recevoir sont calculés et enregistrés dans la comptabilité à chaque période en fonction du pourcentage d’achèvement du projet. Il existe plusieurs méthodes disponibles pour calculer le pourcentage d’achèvement. Ces méthodes peuvent être automatiques en fonction de la configuration ou manuelles.
        - **Pas de TEC** : Cette configuration est utilisée pour les projets à prix fixe avec une courte période et où la facture et les coûts se produisent dans la même période. Dans ce cas, la valeur du champ **Facturation en compte** du raccourci **Comptabilité** est définie automatiquement sur **Résultat** pour s’assurer que le produit est constaté lors de la facturation. Le processus d’estimation des revenus ne sera pas utilisé pour ce profil de coûts et de revenus du projet.

    - **Principe du rapprochement** : Ce champ détermine comment la valeur des ventes calculée (revenus à recevoir) sera validé dans la comptabilité.

        - À l’aide du principe **Valeur des ventes**, le système calcule la valeur des ventes en rapprochant les coûts et le produit, puis en la validant sous forme de montant unique.
        - En utilisant le principe de **Production et profit**, le système divisera la valeur des ventes en coûts réalisés et en bénéfices calculés. Ceux-ci sont validés séparément.

    - **Modèles de coût** : Autorisez le regroupement des transactions de projet en fonction du type de transaction et de la catégorie de projet et définissez les règles de calcul du pourcentage d’achèvement pour ces groupes.
    - **Codes de période** : Définissez la fréquence à laquelle les estimations de revenus sont calculées pour un profil de coûts et de revenus de projet donné.
    - **Catégories pour estimation** : Utilisées pour la comptabilisation de la valeur des ventes (revenus à recevoir) dans les transactions du projet. Commencez par configurer la catégorie de projet dédiée pour un type de transaction **Frais**, puis définissez l’indicateur **Estimation** pour cette catégorie de projet. Ensuite, en fonction du principe de rapprochement sélectionné, choisissez cette catégorie de projet dans la valeur **Ventes** ou le champ **Marge** dans le profil Coût et revenu du projet.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Exemples de configurations pour les profils de coûts et de revenus du projet

Temps et matériel – aucun TEC

![Profil des coûts et des revenus : Temps et matériel – aucun TEC.](media/time-material-no-wip.png)

Temps et matériel – TEC (revenu)

![Profil des coûts et des revenus : Temps et matériel – TEC.](media/time-material-with-wip.png)

Prix fixe – aucun TEC

![Profil de coût et de revenu : Prix fixe – aucun TEC.](media/fixed-price-no-wip.png)

Prix fixe – contrat terminé

![Profil de coût et de revenu : Prix fixe – contrat terminé.](media/fixed-price-completed-contract.png)

Prix fixe – pourcentage d’achèvement

![Profil de coût et de revenu : Prix fixe – pourcentage d’achèvement.](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Exemples d’événement comptable pour les exemples de profils de coûts et de revenus du projet.

| Événement comptable                  | Temps et matériel – aucun TEC                       | Temps et matériel – TEC                                                                                           | Prix fixe – aucun TEC                                            | Prix fixe – contrat terminé                                                                            | Prix fixe – pourcentage d’achèvement                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Journalisation des transactions de temps    | Débit – Coût <br>Crédit – Répartition de la paie          | Débit – Coût <br>Crédit – Répartition de la paie <br>Débit – Valeur des ventes TEC <br>Crédit – Valeur des ventes de revenus à recevoir                | Débit – Coût <br>Crédit – Répartition de la paie                         | Débit – Coût <br>Crédit – Répartition de la paie                                                                    | Débit – Coût <br>Crédit – Répartition de la paie                       |
| Journalisation des transactions de dépenses | Débit – Coût <br>Crédit – Compte de contrepartie des dépenses | Débit – Coût <br>Crédit – Compte de contrepartie des dépenses <br>Débit – Valeur des ventes TEC <br>Crédit – Valeur des ventes de revenus à recevoir      | Débit – Coût <br>Crédit – Compte de contrepartie des dépenses                 | Débit – Coût<br> Crédit – Compte de contrepartie des dépenses                                                            | Débit – Coût <br>Crédit – Compte de contrepartie des dépenses               |
| Client de facturation                | Débit – Solde client <br>Crédit – Revenu facturé | Débit – Solde client <br>Crédit – Revenu facturé <br>Crédit – Débit de valeur des ventes TEC – Valeur des ventes du revenu à recevoir | Débit – Solde client <br>Crédit – Revenus facturés – sur compte | Débit – Solde client <br>Crédit – TEC – Facturés sur compte                                                  | Débit – Solde client <br>Crédit – TEC – Facturés sur compte    |
| Valider l’estimation de revenu             | Non applicable                                   | Non applicable                                                                                                    | Sans objet                                                  | Débit – Valeur du coût TEC <br>Crédit – Coût                                                                         | Débit – TEC – Valeur des ventes <br>Crédit – Valeur des ventes de revenus à recevoir |
| Éliminer                         | Non applicable                                   | Non applicable                                                                                                    | Sans objet                                                  | Crédit – Valeur du coût TEC <br>Débit – Coût <br>Crédit – Revenus à recevoir – Valeur des ventes <br>Débit – TEC Facturés sur compte | Débit – TEC – Facturés sur compte <br>Crédit – Valeur des ventes TEC     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Configurer les règles de profil de coût et de revenu du projet

Les règles de profil de coût et de revenu du projet déterminent le profil de coût et de revenu du projet qui doit être utilisé lors du traitement des transactions de projet facturables. Définissez les règles en accédant à **Gestion de projets et comptabilité** \> **Configurer** \> **Validation** \> **Règles de profil de coût et de revenu du projet**.

Les règles peuvent être définies par contrat de projet, groupe de projet ou par projet spécifique. Le système choisira toujours en premier la règle de granularité la plus élevée.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
