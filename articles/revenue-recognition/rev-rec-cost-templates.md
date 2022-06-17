---
title: Configurer des modèles de coût
description: Cet article fournit des informations sur la création et l’utilisation de modèles de coût dans Project Operations.
author: sigitac
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ffb45d46cf1305fffd5933f4c10b169bf802046d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918401"
---
# <a name="set-up-cost-templates"></a>Configurer des modèles de coût

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_


Cet article fournit des informations sur la création et l’utilisation de modèles de coût dans Project Operations. Un modèle de coût détermine :

- Les catégories de projet pour les transactions prévues et réelles à inclure dans un pourcentage du calcul d’achèvement du projet. La valeur de pourcentage réalisé est ensuite utilisée pour calculer le chiffre d’affaires reconnu.
- Si le pourcentage réalisé peut être modifié s’il est calculé automatiquement.
- Si le pourcentage réalisé est calculé en fonction des montants ou des unités.

## <a name="cost-template-example"></a>Exemple de modèle de coût

Vous travaillez sur un projet de conception de site Web pour un client dans lequel vous facturez un forfait de USD 10,000. Vous prévoyez qu’il faudra 100 heures (USD 5,000) pour terminer le projet. Vous prévoyez également deux billets d’avion et quatre nuits dans un hôtel pour des déplacements sur le site du client (USD 1,800). Il en résulte un coût total prévu de USD 6,800.

Lorsque vous exécutez le processus de reconnaissance des revenus à prix fixe pour créer une estimation à la fin du mois, vous constatez que vous avez travaillé 35 heures sur le projet. Cela n’inclut pas encore les vols ou les frais d’hôtel. Vous avez également demandé à un assistant d’effectuer cinq heures de recherche pour le projet au coût de USD 100, ce que vous n’aviez pas prévu.

Lorsque vous calculez la valeur de pourcentage réalisé pour ce projet, vous avez les choix suivants à faire :

- Voulez-vous inclure tous les coûts (heures et dépenses) ou seulement les heures ?
- Voulez-vous inclure toutes les heures ou seulement les heures planifiées ?
- Voulez-vous calculer le pourcentage réalisé en fonction du coût en dollars des heures planifiées (USD 5,000) ou simplement en fonction du nombre d’heures (100) ?

Vos réponses à ces questions déterminent les options que vous définissez sur le modèle de coût et les catégories que vous sélectionnez sur les lignes du modèle de coût.

Le tableau suivant illustre les résultats des différentes méthodes de calcul de la valeur de pourcentage réalisé pour ce scénario.

| Réalisé sur la base | Coût en dollars ou unités | Pourcentage réalisé | Calcul |
| --- | --- | --- | --- |
| Toutes les heures, pas de frais | Coût en dollars | 37 %% 35 x USD 50 + USD 100 = USD 1,850 USD 1,850/USD 5,000 |
| Toutes les heures, pas de frais | Unités | 40 %% | 40 heures/100 heures (dont cinq heures non planifiées) |
| Heures planifiées, pas de frais | Coût en dollars ou unité | 35 %% | 35/100 heures ou 35 x USD 50/5,000 |
| Toutes les heures et tous les frais | Coût en dollars | 27,2 %% | USD 1,850/USD 6,800 |

Le choix de l’approche à adopter pour créer un modèle de coût peut dépendre de plusieurs considérations :

- Si vous incluez des heures non planifiées dans le modèle de coût, vous risquez d’atteindre 100 %% d’achèvement avant la fin du projet. En effet, les heures réelles seront supérieures aux heures planifiées. Si vous utilisez l’une des deux premières méthodes répertoriées dans le tableau, vous devez modifier le plan (unités prévues) lorsque vous constatez des écarts. Dans ce cas, vous devrez ajouter ou soustraire des heures en fonction de votre connaissance de ce qui est nécessaire pour terminer le projet. Si le projet nécessite 65 heures supplémentaires, vous ajouterez cinq heures au plan pour un total de 105. Si vous savez que votre assistant effectuera encore cinq heures de recherche, le total deviendra 110 heures.
- Si vous utilisez la troisième méthode répertoriée dans le tableau, vous ne mettrez à jour que les heures planifiées pour votre propre temps pour que le calcul du pourcentage achevé reste précis. Votre rentabilité changera lorsque une fois les heures non planifiées enregistrées, mais vous resterez sur une trajectoire connue de pourcentage réalisé.
- Si vous utilisez la quatrième méthode répertoriée dans le tableau, le risque est que les dépenses surviennent à des moments irréguliers et ne soient pas reflétées dans votre progression. Par conséquent, si les dépenses sont incluses, elles peuvent faire varier votre pourcentage d’achèvement plus qu’il n’est souhaitable. Par exemple, comme vous n’avez pas encore pris de vol, votre pourcentage d’achèvement était de 27 %% au lieu de 35 %% ou 37 %% si vous deviez baser le calcul uniquement sur le temps. Si vous aviez fait un voyage de deux nuits et que vous aviez prévu avec précision les coûts de votre vol et de votre hôtel, le pourcentage réalisé aurait été de 40,4 %% (USD 1850 pour la main-d’œuvre et USD 900 pour les dépenses = USD 2750/6800 USD = 40,4 %%). Par conséquent, engager les dépenses pour un seul voyage en avion ferait passer le pourcentage achevé de 27 %% à 40 %%.

## <a name="create-cost-templates"></a>Créer des modèles de coût
Pour créer des modèles de coût, procédez comme suit :

1. Pour accéder aux modèles de coûts, dans l’environnement Dynamics 365 Finance, accédez à **Gestion de projet et comptabilité** > **Configuration** > **Estimations** > **Modèle de coût**.
2. Sélectionnez **Nouveau** pour créer un modèle de coût. Entrez un nom et une description.
3. Indiquez l’ID de ligne de coût pour chaque type de transaction.
4. Sélectionnez une méthode d’achèvement par défaut :

  - **Automatique** : Le pourcentage d’achèvement est calculé automatiquement sur un projet. Il est impossible de modifier la valeur résultante.
  - **Manuel** : Le pourcentage d’achèvement est calculé automatiquement sur un projet. Il est possible de modifier la valeur résultante.

  > [!NOTE]
  > Pour les calculs manuels, le pourcentage d’achèvement est conservé dans **Calcul manuel** sur l’onglet **Général** de la page **Estimation**.

5. Dans **Achèvement basé sur**, sélectionnez l’une des valeurs suivantes :

  - **Montant** : Le montant en devise comptable calcule le pourcentage d’achèvement.
  - **Unité** : La quantité calcule le pourcentage d’achèvement.
  - **Ligne droite** : Le système calcule le pourcentage d’achèvement sur une base proportionnelle en utilisant les dates de début et de fin du projet pour déterminer la durée du projet.

6. Sélectionner **Lignes de coût** pour passer en revue les lignes de coût du modèle de coût. Au moins une ligne de coût est requise pour chaque type de transaction. Cependant, vous pouvez créer plusieurs lignes de coût pour les mêmes types de transaction et définir les attributs souhaités pour ces lignes.
7. Sur l’onglet **Catégories**, sélectionnez les catégories de projet à inclure sur la ligne du modèle de coût.
8. Sur l’onglet **Général**, sélectionnez si cette ligne sera incluse dans le calcul du pourcentage d’achèvement.
9. Sélectionnez le coût pour compléter la méthode à utiliser lors du calcul du pourcentage d’achèvement.


[!INCLUDE[footer-include](../includes/footer-banner.md)]