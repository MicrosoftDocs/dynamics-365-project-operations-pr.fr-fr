---
title: Nouveautés d’avril 2021 – Project Operations pour les scénarios basés sur les ressources/produits non stockés
description: Cet article fournit des informations sur les mises à jour de qualité disponibles dans la version d’avril 2021 de Project Operations pour les scénarios basés sur les ressources/produits non stockés.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a060bdc4e4c9f37ec666b1cf4d078986ad1571db
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912421"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Nouveautés d’avril 2021 – Project Operations pour les scénarios basés sur les ressources/produits non stockés

_**S’applique à :** Project Operations pour les scénarios selon les ressources/produits hors stock_

Cet article s’applique aux composants et versions de Microsoft Dynamics 365 Project Operations suivants :

- Version 4.9.0.221 de Project Operations dans l’environnement Dataverse
- Gestion de projet et comptabilité dans un environnement Dynamics 365 Finance version 10.0.17

## <a name="features-included-in-this-release"></a>Fonctionnalités incluses dans cette version

Les fonctionnalités suivantes sont incluses dans cette version :

- Matériel non stocké pour les projets. Les fonctionnalités clés comprennent :
  - Estimation et tarification du matériel non stocké pendant le cycle de vente d’un projet. Pour plus d’informations, consultez [Configurer les taux de coûts et de vente pour les produits du catalogue – Simplifié](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Suivi de l’utilisation du matériel non stocké lors de la livraison de projet. Pour plus d’informations, consultez [Enregistrer l’utilisation du matériel sur les projets et les tâches du projet](../material/material-usage-log.md).
  - Facturation des coûts du matériel non stocké utilisé. Pour plus d’informations, consultez [Gérer la réplication de facturation](../proforma-invoicing/manage-billing-backlog.md).
  - Pour plus d’informations sur la configuration de cette fonctionnalité, voir [Configurer le matériel non stocké et les factures fournisseur en attente](../procurement/configure-materials-nonstocked.md)
- Facturation basée sur les tâches : ajout de la possibilité d’associer des tâches de projet à des lignes de contrat du projet, en les soumettant ainsi à la même méthode de facturation, à la même fréquence de facturation et aux mêmes clients que celles de la ligne de contrat. Cette association garantit une facturation, une comptabilité, une estimation des revenus et une reconnaissance précises pour fonctionner conformément à cette configuration sur les tâches du projet.
- Les nouvelles API dans Dynamics 365 Dataverse autorisent les opérations de création, de mise à jour et de suppression avec des **Entités de planification**. Pour plus d’informations, consultez [Utiliser les API de planification pour effectuer des opérations avec des entités de planification](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Mises à jour des mappages à double écriture Project Operations

La liste suivante répertorie les mappages à double écriture qui ont été modifiés ou ajoutés dans la version d’avril 2021 de Project Operations.

| **Mappage d’entité** | **Version mise à jour** | **Commentaires** |
| --- | --- | --- |
| Chiffres réels d’intégration Project Operations (msdyn\_actuals) | 1.0.0.14 | Mappage modifié pour synchroniser les chiffres réels du projet de matériel. |
| Entité d’intégration de Project Operations pour les estimations de dépenses (msdyn\_estimateslines) | 1.0.0.2 | Ajout de la synchronisation des lignes de contrat de projet aux applications de finances et d’opérations pour la prise en charge de la facturation basée sur les tâches. |
| Entité d’intégration de Project Operations pour les estimations d’heures (msdyn\_resourceassignments) | 1.0.0.5 | Ajout de la synchronisation des lignes de contrat de projet aux applications de finances et d’opérations pour la prise en charge de la facturation basée sur les tâches. |
| Table Intégration de Project Operations pour les estimations de matériel (msdyn\_estimatelines) | 1.0.0.0 | Nouvelle carte de table pour synchroniser les estimations de matériaux de Dataverse aux applications de finances et d’opérations. |
| Entité d’exportation des factures fournisseur de projet d’intégration de Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Nouvelle carte de table pour synchroniser les en-têtes de facture de fournisseur des applications de finances et d’opérations à Dataverse. |
| Entité d’exportation des lignes de facture fournisseur de projet d’intégration de Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Nouvelle carte de table pour synchroniser les lignes de facture de fournisseur des applications de finances et d’opérations à Dataverse. |

Vous devez toujours exécuter la version la plus récente du mappage dans votre environnement, et activez tous les mappages de table associés lorsque vous mettez à jour la version de la solution Project Operations Dataverse et de la solution Finance and Operations. Certaines fonctionnalités et capacités peuvent ne pas fonctionner correctement si la dernière version du mappage n’est pas activée. Vous pouvez voir la version active du mappage dans la colonne **Version** de la page **Double écriture**. Vous pouvez activer une nouvelle version du mappage en sélectionnant **Versions du mappage de table**, en sélectionnant la dernière version, puis en enregistrant la version sélectionnée. Si vous avez personnalisé un mappage de table prêt à l’emploi, réappliquez les modifications. Pour en savoir plus, voir [Cycle de vie de l’application](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Si vous rencontrez un problème lors du démarrage du mappage, suivez les instructions de la section [Problème de colonnes de table manquantes sur les mappages](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) du guide de dépannage consacré à la double écriture.

## <a name="quality-updates"></a>Mises à jour qualité

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations dans Dynamics 365 Dataverse

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Facturation et tarification | 2124532 | Le bouton **Corriger la facture** s’affiche sur une facture pro forma lorsque le montant de la provision ou le montant appliqué de la provision est présent sur la facture d’origine. Le bouton s’affiche uniquement pour les environnements dotés de la version Finance 10.0.19 ou d’une version ultérieure. |
| Facturation et tarification | 2224568 | Ajout d’une logique pour permettre les personnalisations qui impliquent l’appel du plug-in de confirmation de facture. |
| Facturation et tarification | 2101098 | Amélioration de la logique des champs par défaut pour les factures proforma : **Adresse de facturation**, **Nom de facturation** et **Modalités de paiement** proviennent désormais par défaut de l’enregistrement client du contrat de projet correspondant. |
| Facturation et tarification | 2021413 | Mise à jour des champs **Coût réel** et **Ventes** sur l’entité **Tâche** pour inclure les valeurs de ventes des dépenses non facturées et facturées sur les tâches. |
| Facturation et tarification | 2182110 | Lors de la copie d’un contrat de projet, l’ID de ligne de contrat est régénéré dans le contrat de projet de destination afin de garantir qu’il est unique. |
| Gestion des opportunités | 2186741 | Ajout de validations pour garantir que le champ **Origine** et le champ **Type de transaction** ne peuvent pas être mis à jour pour les détails de la ligne de devis existante. |
| Gestion des opportunités | 2191353 | Les jalons ne doivent pas être créés sur une ligne de contrat de temps et de matériel. |
| Gestion des opportunités | 2216956 | Résolution des problèmes avec **Mettre à jour les prix**. |
| Planification et suivi | 2182979 | La fonction de copie de projet a été améliorée pour garantir que les lignes d’estimation des dépenses sont copiées à partir du projet d’origine. |
| Planification et suivi | 2184144 | La fonction de copie de projet a été améliorée pour garantir que le nom de la position de la ressource est copié à partir du projet d’origine. |
| Planification et suivi | 2184799 | Copie de projet : contrôle renforcé pour garantir que la date de début estimée ne peut pas être modifiée pendant la copie. |
| Planification et suivi | 2185134 | Copie de projet : la date de début estimée du projet de destination est définie sur la date du jour. |
| Planification et suivi | 2196373 | Copie de projet : assurez-vous que les enregistrements du chef de projet et des membres de l’équipe ne sont pas dupliqués dans l’équipe du projet. |
| Planification et suivi | 2211833 | Copie de projet : les affectations de ressources sont copiées de la tâche du projet source vers le projet de destination. |
| Planification et suivi | 2186541 | Résolution des problèmes dans la grille **Estimations** lors du regroupement par ressource. |
| Planification et suivi | 2166906 | La catégorie de transaction d’une tâche doit être copiée dans l’entité **Attribution de ressource**. |
| Gestion des ressources | 2125362 | Correction de problèmes liés à la création d’un membre d’équipe générique à l’aide d’une méthode d’allocation basée sur les heures. |
| Temps et dépenses | 2113603 | Correction du problème lié à la personnalisation lors de la suppression des attributs de la page **Entrée de temps**. Le système vérifie maintenant si l’attribut existe sur la page avant d’y accéder à l’aide d’un script. |
| Temps et dépenses | 2204377 | Les feuilles de temps copiées doivent s’afficher automatiquement lorsque vous sélectionnez **Copier la semaine** lors de l’entrée de temps. |
| Temps et dépenses | 2209059 | Le champ **Statut** peut être modifié pour les entrées de temps Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Vue d’ensemble de la gestion et comptabilité des projets dans Dynamics 365 Finance

| **Fonctionnalités** | **Numéro de référence** | **Mise à jour qualité** |
| --- | --- | --- |
| Gestion et comptabilité des projets | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | L’élimination des estimations inversées ne fonctionne pas dans la section **Périodique**.  |
| Gestion et comptabilité des projets | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | La fonctionnalité **Ajustement comptable** crée un problème avec les comptes généraux pour lesquels l’option **Ne pas autoriser la saisie manuelle** est sélectionnée. |
| Gestion et comptabilité des projets | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Ajout d’une logique métier pour traiter les factures de correction, y compris le montant de la provision ou le montant appliqué de la provision. |
| Gestion et comptabilité des projets | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | La validation d’une valeur de vente TEC dans la facturation de projets intersociétés sélectionne un compte inattendu. |
| Gestion et comptabilité des projets | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Lorsque vous utilisez des provisions dans Project Operations, la modification du projet par défaut sur un contrat après la facturation des acomptes entraîne des problèmes avec les déductions entrantes. |
| Gestion et comptabilité des projets | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Dans Project Operations, la suppression d’un projet d’un contrat doit réinitialiser le projet par défaut du contrat, si nécessaire. |
| Gestion et comptabilité des projets | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Dans Project Operations, les mauvaises lignes de dépenses s’affichent dans la liste **Ajouter une ligne** sur la facture intersociétés. |
| Gestion et comptabilité des projets | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Dans Project Operations, la page **Contrat d’achat** n’est pas visible dans les entités juridiques Finance intégrées à Project Operations. |
| Gestion et comptabilité des projets | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | En raison d’une erreur d’intégration Dataverse, vous ne pouvez pas attribuer le statut « Conclu » à un devis dans Project Operations. |
| Gestion et comptabilité des projets | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** peut définir l’adresse de facturation de la source de financement d’un autre client.  |
| Gestion et comptabilité des projets | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Dans Project Operations, aucune dimension n’est sélectionnée lorsque vous créez une validation de facture pour une transaction. |
| Frais de déplacement | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Le solde des avance de disponibilités n’est pas mis à jour pour une note de frais s’il est approuvé et publié ligne par ligne. |
| Déplacement et dépenses | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Les taxes pour les notes de frais intersociétés détaillées ne sont pas calculées correctement. |
| Déplacement et dépenses | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Des champs supplémentaires liés aux projets sont affichés sur la page **Rapports de dépenses intersociétés** repensée. |
| Déplacement et dépenses | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Un message d’erreur incorrect apparaît sur les reçus d’en-tête des notes de frais. |
| Déplacement et dépenses | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Une note de frais n’est pas validée correctement dans un scénario intersociétés si la taxe de vente est validée pour l’entité juridique de destination. |
| Déplacement et dépenses | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Les dates de soumission des rapports ne sont pas imprimées sur des notes de frais approuvées. |
| Déplacement et dépenses | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Les champs **Date d’approbation** et **Date de rejet** ne sont pas remplis après l’approbation d’une dépense. |
| Déplacement et dépenses | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Une demande de déplacement créée pour un collaborateur peut être utilisée pour la note de frais d’un autre collaborateur. |
| Déplacement et dépenses | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Les catégories de dépenses sont verrouillées lors de l’ajout d’une nouvelle ligne de dépenses. |
| Déplacement et dépenses | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Le fait de détailler des lignes de note de frais déjà fractionnées entraîne une validation incomplète du document Comptabilité fournisseur\Comptabilité et rompt l’Explorateur de comptabilité source car **TRVEXPTRANS.SOURCEDOCUMENTLINE** est dupliqué. |
| Déplacement et dépenses | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | La politique de demande de déplacement ne fonctionne pas comme prévu. |
| Déplacement et dépenses | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Le nom du compte fournisseur n’apparaît pas sur les transactions de projet validées pour les notes de frais. |
| Déplacement et dépenses | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Dans Project Operations, vous ne pouvez pas approuver le temps avec une tâche pour un projet intersociétés. |
| Déplacement et dépenses | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | La catégorie de retour des avance de disponibilités ne met pas à jour les soldes d’avances de disponibilités lors de la validation. |
| Déplacement et dépenses | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Le prix de vente est calculé de manière incorrecte sur les notes de frais créées dans une devise étrangère à l’aide de transactions par carte de crédit importées et associées à un projet. |
| Déplacement et dépenses | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Annulation de l’entité de données **TrvRequisitionLine** et de l’index unique associé. |
| Déplacement et dépenses | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Ajout de l’instrumentation à la génération **SOURCEDOCUMENTLINE**. |
| Déplacement et dépenses | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Un journal de la comptabilité auxiliaire incorrect s’affiche dans un scénario intersociétés si la taxe de vente est validée pour l’entité juridique de destination. |
| Déplacement et dépenses | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Dans Project Operations, les estimations de dépenses ne sont pas supprimées de Finance lorsqu’elles sont supprimées de Dataverse. |
| Déplacement et dépenses | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Lorsqu’une catégorie de dépenses est une catégorie non liée au projet, les dimensions financières sélectionnées sur la page **Dépenses** ne sont pas copiées dans la note de frais. |
