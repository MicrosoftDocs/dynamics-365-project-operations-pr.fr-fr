---
title: Nouveautés de février 2022 – Project Operations pour les scénarios selon les ressources/produits non stockés
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version de février 2022 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932983"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés de février 2022 – Project Operations pour les scénarios selon les ressources/produits non stockés

*S’applique à : Project Operations pour les scénarios basés sur les ressources/hors stock*

Cet article s’applique aux composants et versions suivants de Microsoft Dynamics 365 Project Operations :

- Project Operations dans un environnement Dataverse, version 4.28.0.120
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.24

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

- À partir de cette version, vous pouvez ajouter jusqu’à 300 membres d’équipe à un seul projet. Auparavant, la limite du nombre de membres de l’équipe s’élevait à 150. Pour plus d’informations, consultez [Limites de projet](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Mises à jour du mappage à double écriture Project Operations

La liste suivante présente les cartes en double écriture qui ont été modifiées ou ajoutées dans la version de février 2022 de Project Operations.

| Mappage d’entité | Version mise à jour | Commentaires |
| --- | --- | --- |
| Entité d’exportation des dépenses de projet d’intégration de Project Operations (msdyn\_expenses) | 1.0.0.3 | Étendu pour la synchronisation des activités de projet vers Dataverse. |

Pour la liste actuelle et les versions des mappages en double écriture de Project Operations, voir [Versions de mappage en double écriture de Project Operations](../environment/resource-dual-write-maps.md).

Exécutez toujours la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance. Certaines fonctions et fonctionnalités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez afficher la version active du mappage dans la colonne **Version** de la page **Double écriture**. Pour activer une nouvelle version du mappage, sélectionnez **Versions du mappage de table**, sélectionnez la dernière version, puis enregistrez la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les cartes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage de la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-on-dataverse"></a>Project Operations sur Dataverse

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Facturation et tarification | 2415109 | La valeur par défaut dans le champ **Modalités de paiement des opérations** doit être l’enregistrement client du contrat de projet et l’enregistrement de la facture proforma. |
| Facturation et tarification | 2497369 | La correction matérielle doit suivre la valeur de la date dans les paramètres **Correction**. |
| Facturation et tarification | 2498697 | Amélioration de la configuration de sécurité pour **Rappel d’entrée de temps**. |
| Facturation et tarification | 2513824 | Pour les scénarios basés sur les ressources, l’ID de catégorie de transaction ne doit pas dépasser 28 caractères dans Project Operations. |
| Facturation et tarification | 2517455 | L’action **Actualiser les transactions de ligne de facture** ne doit pas pouvoir être déclenchée plusieurs fois simultanément pour la même facture. |
| Facturation et tarification | 2517465 | L’action **Désactiver les détails de la ligne de facture** est bloquée, car elle n’est pas prise en charge. |
| Facturation et tarification | 2556660 | Correction des vérifications d’effectivité de la date qui sont effectuées sur la liste de prix jointe à un enregistrement de paramètres de projet. |
| Gestion des opportunités | 2369202 | Correction de la logique métier qui vérifie que les listes de prix dont les dates d’effet se chevauchent peuvent être jointes au même contrat de projet. |
| Gestion des opportunités | 2385965 | Correction du comportement sur l’onglet **Clients** de la page **Contrat de projet** lorsque vous sélectionnez **Enregistrer et fermer**. |
| Temps et dépenses | 2538503 | Une tâche de projet doit être disponible dans l’entité **Chiffres réels du projet** après la publication d’une note de frais. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets sur Dynamics 365 Finance

| Fonctionnalités | Numéro de référence | Mise à jour qualité |
| --- | --- | --- |
| Gestion et comptabilité des projets | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Lors de l’importation des notes de crédit fournisseur, une erreur se produit. Le message d’erreur indique : « Le montant de la retenue ne peut pas être supérieur au montant net restant. » |
| Gestion et comptabilité des projets | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Si une proposition de facture inclut des transactions sans frais qui sont des ventes réelles non facturées, la facturation ne peut pas avoir lieu. |
| Gestion et comptabilité des projets | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Le coût validé n’est pas correct après la mise à jour du prix d’achat et **Activer la gestion des modifications** est activé.|
| Gestion et comptabilité des projets | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Le devis de validation d’un projet à prix fixe utilise la devise et le montant incorrects dans le bordereau de devis, même lorsque la fonctionnalité **Activer la devise du contrat de projet pour le calcul de l’estimation** est activée. |
| Gestion et comptabilité des projets | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Extension** ne doit pas effectuer d’appel pour activer le suivi des modifications sans intercepter les exceptions pour les entités dont les clés de configuration ne sont pas activées. |
| Gestion et comptabilité des projets | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Le travail par lots est corrigé lorsque plusieurs journaux avancés sont publiés et qu’une erreur se produit. |
| Déplacement et dépenses | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | En raison d’un problème de règlement lié aux avances de fonds sur les notes de frais, le montant de la taxe n’est pas couvert dans le cadre de l’avance de fonds. |
| Déplacement et dépenses | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Les informations sur la taxe de vente ne sont pas incluses sur le rapport **Dépense - Transactions validées**. |
| Déplacement et dépenses | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | La violation de la politique de dépenses **Reçus obligatoires** affiche à tort un avertissement sur les notes de frais. |
| Déplacement et dépenses | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Une transaction de projet n’inclut pas la taxe de vente non récupérable dans le montant total des ventes lorsque la transaction résulte d’une dépense de kilométrage. |
| Déplacement et dépenses | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Lorsqu’une ligne détaillée comporte des taxes, vous ne pouvez pas modifier la date de la ligne détaillée et une erreur d’état du document source se produit. |

## <a name="removed-and-deprecated-features"></a>Fonctionnalités supprimées et obsolètes

L’article [Fonctionnalités supprimées ou obsolètes dans Project Operations](removed-depreciated-features-project.md) décrit les fonctionnalités qui ont été supprimées ou obsolètes pour Dynamics 365 Project Operations.

- Une fonctionnalité supprimée n’est plus disponible dans le produit.
- Une fonction déconseillée n’est pas en développement actif et peut être supprimée dans une prochaine mise à jour.

Une annonce d’obsolescence apparaît dans l’article [Fonctionnalités supprimées ou obsolètes dans Project Operations](removed-depreciated-features-project.md) 12 mois avant le retrait.

Pour les dernières modifications qui n’affectent que le temps de compilation, mais qui sont compatibles d’un point de vue binaire avec les environnements sandbox et de production, le temps d’obsolescence sera inférieur à 12 mois. Ce sont généralement des mises à jour fonctionnelles qui doivent être apportées au compilateur.
