---
title: Configurer les paramètres de gestion des dépenses
description: Cette rubrique décrit les paramètres qui contrôlent le comportement général dans la gestion des dépenses.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1cabb0be624f7f6c12761e4fb6d5a095396a5940a37616bb3a304798e1f97808
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007773"
---
# <a name="configure-expense-management-parameters"></a>Configurer les paramètres de gestion des dépenses

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits non stockés_

Cette rubrique décrit les paramètres qui contrôlent le comportement général dans la gestion des dépenses.

## <a name="general"></a>GÉNÉRAL

| Champ                                                    | Description |
|----------------------------------------------------------|-------------|
| Taux kilométrique standard                                 | Saisissez le taux de remboursement des frais kilométriques. Ce taux est multiplié par le kilométrage saisi pour la dépense afin de calculer le montant remboursé pour les frais de déplacement. |
| Valider l’objet de la dépense                                 | Activez cette option pour limiter les utilisateurs à un ensemble de valeurs existant configuré dans le champ **Objectif de la note de frais** lorsqu’ils créent des notes de frais. |
| Dépenses personnelles payées par                                | Sélectionnez le responsable du paiement des montants de transaction par carte de crédit classés comme personnels. |
| Afficher l’intégralité de la note de frais en remontant               | Sélectionnez cette option pour afficher toutes les dépenses d’une note de frais lorsque les détails du document d’origine sont affichés pour un n° document spécifique généré lors de la validation de la note de frais. |
| La pré-autorisation de voyage est obligatoire                 | Sélectionnez cette option pour exiger qu’une demande de déplacement soit soumise et approuvée avant qu’un employé puisse soumettre une note de frais. |
| Autoriser la modification des répartitions avant la validation            | Indiquez si les répartitions d’une note de frais peuvent être modifiées avant d’être validées. |
| Évaluer les stratégies de gestion des dépenses                     | Sélectionnez le moment où les dépenses sont évaluées pour déterminer si une stratégie de dépenses a été enfreinte. Les dépenses peuvent être évaluées pour les infractions lorsque l’entrée de dépenses est saisie et enregistrée, ou lorsque la dépense est soumise pour approbation. Règles de stratégie pour les reçus requis seront évaluées lors de l’enregistrement de la ligne de dépense. |
| Autoriser les lignes de dépenses intersociétés                         | Indiquez si les dépenses d’autres entités juridiques peuvent être saisies dans une note de frais. |
| Autoriser la modification du taux de change des dépenses par carte de crédit | Sélectionnez cette option pour permettre à l’utilisateur de modifier le taux de change des dépenses de carte de crédit importées. |
| Champs de hiérarchie à plusieurs niveaux à afficher                  | Sélectionnez les champs d’approbateur affichés lorsque le type d’affectation de workflow est défini comme une hiérarchie et la sélection **Hiérarchie** est définie pour utiliser la hiérarchie d’approbation, l’approbation à plusieurs niveaux des dépenses. Lorsque la hiérarchie d’approbation à plusieurs niveaux est utilisée pour un workflow, les champs sélectionnés seront affichés sur la note de frais et peuvent être modifiés. |
| Entrer le numéro de carte de crédit de l’employé                        | Sélectionnez si un nombre à 15 ou 16 caractères peut être saisi et enregistré dans le champ **ID de la carte** sur la page **Cartes de crédit** pour un employé. |
| Valider l’objet de la demande de déplacement                      | Activez cette option pour limiter les utilisateurs à un ensemble de valeurs existant configuré dans le champ **Objectif de la note de frais** lorsqu’ils créent des demandes de déplacement. |

## <a name="financial"></a>Finance

| Champ                                                                                    | Description |
|------------------------------------------------------------------------------------------|-------------|
| Nom du journal comptable                                                                | Sélectionnez le nom du journal comptable dans lequel les notes de frais approuvées sont imputées. |
| Activer le recouvrement fiscal des dépenses                                                        | Sélectionnez cette option pour activer le recouvrement fiscal sur les dépenses éligibles. Cette option ne peut pas être sélectionnée si la taxe de vente américaine et l’utilisation des règles fiscales sont activées. |
| Enregistrer immédiatement les avances de fonds                                                           | Sélectionnez cette option pour comptabiliser une avance de fonds approuvée lorsque le processus de paiement et de transfert est terminé. Si cette option n’est pas sélectionnée, le processus de paiement et de transfert génère un journal des opérations diverses non validé. |
| Corriger la date comptable lors de la comptabilisation                                                   | Sélectionnez cette option pour mettre à jour la date comptable lorsque les dépenses sont validées, si la période en cours est suspendue ou fermée. La date comptable sera fixée à la prochaine période ouverte. |
| Autoriser le regroupement des transactions en fonction du compte de contrepartie spécifié dans le mode de paiement       | Sélectionnez cette option pour résumer les transactions de dépenses pour une note de frais, en fonction du compte de contrepartie spécifié dans le mode de paiement des dépenses. |
| Taxe incluse                                                                             | Sélectionnez cette option pour inclure la taxe dans le montant des dépenses par défaut. |
| Libérer les engagements lors de la clôture des demandes de déplacement                                      | Sélectionnez cette option pour libérer les fonds engagés lorsqu’une demande de déplacement approuvée est clôturée. |
| Autoriser la soumission des demandes de déplacement en cas de dépassement de budget pour le registre budgétaire et le budget du projet | Sélectionnez cette option pour permettre aux employés d’envoyer des demandes de déplacement pour approbation, même si elles dépassent le budget autorisé défini dans le registre budgétaire ou le budget autorisé pour un projet. |
| Autoriser la soumission des notes de frais en cas de dépassement de budget pour le registre budgétaire et le budget du projet     | Sélectionnez cette option pour permettre aux employés d’envoyer des notes de frais pour approbation, même si elles dépassent le budget autorisé défini dans le registre budgétaire ou le budget autorisé pour un projet. |
| Autoriser l’approbation des notes de frais en cas de dépassement de budget pour le registre budgétaire uniquement                 | Sélectionnez cette option pour permettre aux approbateurs d’approuver les notes de frais qui dépassent le budget autorisé défini dans le registre budgétaire. |

## <a name="per-diem"></a>Indemnité quotidienne

| Champ                                 | Description |
|---------------------------------------|-------------|
| Nombre minimal d’heures pour les indemnités journalières            | Entrez le nombre minimal d’heures par défaut qu’un employé doit travailler dans une journée pour être admissible à une indemnité journalière pour les frais de déplacement. Cette valeur est utilisée comme valeur par défaut uniquement pour le champ **Nombre minimal d’heures** pour les niveaux de taux d’indemnités journalières. |
| Pourcentage de repas                          | Entrez le pourcentage par défaut de l’indemnité journalière pour les repas qui est utilisé le premier et le dernier jour de la dépense liée au voyage lorsque le champ **Calculer la réduction de repas par** est défini sur **Type de repas par jour** ou **Nombre de repas par jour**. La journée de travail du premier et du dernier jour peut être plus courte qu’une journée de travail standard. Par conséquent, le montant de l’indemnité journalière de ces jours peut différer du montant standard. Si le pourcentage est défini sur **0** (zéro), les déductions pour le premier et le dernier jour seront de 0,00. |
| Pourcentage de l’hôtel                         | Entrez le pourcentage par défaut de l’indemnité journalière pour les hôtels qui est utilisé le premier et le dernier jour des dépenses liées au voyage. La journée de travail du premier et du dernier jour peut être plus courte qu’une journée de travail standard. Par conséquent, le montant de l’indemnité journalière de ces jours peut différer du montant standard. Si le pourcentage est défini sur **0** (zéro), les déductions pour le premier et le dernier jour seront de 0,00. |
| Autre pourcentage                         | Entrez le pourcentage par défaut de l’indemnité journalière pour les frais divers qui est utilisé le premier et le dernier jour des dépenses liées au voyage. La journée de travail du premier et du dernier jour peut être plus courte qu’une journée de travail standard. Par conséquent, le montant de l’indemnité journalière de ces jours peut différer du montant standard. Si le pourcentage est défini sur **0** (zéro), les déductions pour le premier et le dernier jour seront de 0,00. |
| Réduction en pourcentage pour le petit déjeuner | Saisissez le montant de la réduction de l’indemnité journalière pour le petit-déjeuner. Par exemple, si un employé reçoit un petit-déjeuner gratuit, vous souhaiterez peut-être réduire le montant de l’indemnité journalière de 10 %%. |
| Réduction en pourcentage pour le déjeuner     | Saisissez le montant de la réduction de l’indemnité journalière pour le déjeuner. Par exemple, si un employé reçoit un déjeuner gratuit, vous souhaiterez peut-être réduire le montant de l’indemnité journalière de 15 %%. |
| Réduction en pourcentage pour le dîner    | Saisissez le montant de la réduction de l’indemnité journalière pour le dîner. Par exemple, si un employé reçoit un dîner gratuit, vous souhaiterez peut-être réduire le montant de l’indemnité journalière de 25 %%. |
| Calculer la réduction de repas par           | Spécifiez comment le système doit calculer la réduction de repas par jour, en sélectionnant si la réduction est basée sur le type de repas par trajet ou par jour, ou si elle est basée sur le nombre de repas autorisés par jour. |
| Arrondi des indemnités journalières                     | Sélectionnez le type d’arrondi utilisé pour les dépenses journalières. Si vous sélectionnez l’arrondi normal, toute dépense journalière d’un montant de 0,50 est arrondie à 1,00, et toute dépense journalière dont le montant est inférieur à 0,50 est arrondie à 0,00. |
| Calcul des indemnités journalières de base sur          | Indiquez si le montant de l’indemnité journalière est basé sur un jour civil ou une période de 24 heures. |

## <a name="fax-cover-pages"></a>Pages de garde de télécopie

| Champ                          | Description |
|--------------------------------|-------------|
| Instructions                   | Entrez les instructions que les employés doivent suivre lorsqu’ils créent une page de garde pour une télécopie utilisée pour envoyer des reçus liés à une note de frais. Pour saisir un texte spécifique à la langue qui sera affiché, en fonction de la langue de l’utilisateur, sélectionnez **Traductions**. |
| ID utilisateur (informations de code à barres) | Sélectionnez cette option pour stocker l’identificateur unique d’un employé dans le code à barres utilisé sur la page de garde du fax. |
| Code-barres                       | Sélectionnez le code à barres utilisé sur la page de garde du fax. Les codes à barres 39 et 128 sont pris en charge dans la gestion des dépenses. |

## <a name="anti-corruption"></a>Anti-corruption

| Champ                                 | Description |
|---------------------------------------|-------------|
| Afficher l’attestation anti-corruption   | Sélectionnez cette option pour afficher le texte anti-corruption lors de la création d’une note de frais. Des catégories de dépenses spécifiques peuvent alors être activées, ce qui nécessitera que l’attestation anti-corruption soit sélectionnée sur la note de frais. Par exemple, une catégorie de cadeau liée à une dépense officielle du gouvernement peut exiger que l’employé confirme que la dépense respecte la politique de l’entreprise relative aux fonctionnaires. |
| Message anti-corruption pour l’expéditeur | Saisissez le texte qui doit être présenté à un employé qui crée une note de frais. Pour saisir un texte spécifique à la langue qui sera affiché, en fonction de la langue de l’utilisateur, sélectionnez **Traductions**. |
| Message anti-corruption pour l’approbateur  | Saisissez le texte qui doit être présenté à l’approbateur lorsqu’une note de frais est créée. Pour saisir un texte spécifique à la langue qui sera affiché, en fonction de la langue de l’utilisateur, sélectionnez **Traductions**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]