---
title: Remplacements de prix avec date d’effet
description: Cet article explique comment configurer des remplacements de prix pour des prix spécifiques dans la liste de prix.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2022
ms.locfileid: "9445967"
---
# <a name="date-effective-price-overrides"></a>Remplacements de prix avec date d’effet 

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits hors stock Déploiement simplifié – Traiter la facturation pro forma_

Les *Remplacements de prix à la date d’effet* fournissent un moyen de remplacer ou de modifier des prix spécifiques dans la liste de prix. Par exemple, vous avez une liste de prix standard qui est en vigueur du 1er janvier 2022 au 31 décembre 2022. Cette liste de prix contient des prix pour de nombreux rôles. Le prix fixé pour le rôle **Technicien réseau** est de 100 dollars américains (USD) par heure. Lorsqu’un technicien réseau enregistre du temps entre le 1er janvier 2022 et le 31 décembre 2022, le temps est facturé à 100 USD. Le 1er octobre 2022, vous devez ajuster le prix *seulement* pour le rôle **Technicien réseau**, de 100 USD par heure à 110 USD par heure. La fonctionnalité **Date d’entrée en vigueur des remplacements de prix** vous permet de configurer ce changement comme un remplacement de la ligne pour ce prix de rôle spécifique. Par conséquent, vous n’avez pas besoin de copier toute la liste de prix et de modifier le prix d’une seule ligne.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Remplacements de prix à la date d’effet pour la tarification de la main-d’œuvre

Le processus de configuration des remplacements de prix à date effective pour le temps de travail sur un projet se compose de deux étapes de base.

1. Activer la fonctionnalité **Remplacements de prix avec date d’effet**.
1. Configurez un remplacement de prix avec date d’effet.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Activer la fonctionnalité Remplacements de prix avec date d’effet

> [!NOTE]
> Une fois la fonctionnalité **Remplacements de prix avec date d’effet** activée, elle ne peut pas être désactivée.

Pour activer la fonctionnalité **Remplacements de prix avec date d’effet**, procédez comme suit.

1. Accédez à **Paramètres** \> **Paramètres**.
1. Ouvrir l’enregistrement **Paramètres**.
1. Dans le volet Actions, sur l’onglet **Contrôle des fonctionnalités**, sélectionnez **Activer les remplacements de prix avec date d’effet**.
1. Dans la boîte de dialogue de confirmation, sélectionnez **OK**.
1. Après quelques instants, actualisez votre navigateur. Les capacités de remplacement des prix avec date d’effet devraient maintenant être disponibles. Vous saurez que ces fonctionnalités ont été activées si le bouton **Activer les remplacements de prix avec date d’effet** n’apparaît plus dans le volet Actions.

### <a name="set-up-a-date-effective-price-override"></a>Configurer un remplacement de prix avec date d’effet

Les remplacements de prix avec date d’effet peuvent être configurés sur les tarifs **Coût**, **Vente** ou **Achat**.

> [!NOTE]
>Le comportement de la fonctionnalité **Remplacements de prix avec date d’effet** présente actuellement les limitations suivantes :
>
> - Seuls les prix de rôle et les majorations de prix de rôle prennent en charge la fonctionnalité **Remplacements de prix avec date d’effet** dans Project Operations.
> - Lorsque vous copiez une liste de prix à l’aide de l’action **Copier** sur la page **Détails des tarifs** et lorsque vous créez une liste de prix de projet à partir d’une liste de prix standard ou personnalisée lors de la création du contrat, les remplacements de prix avec date d’effet **ne sont pas** copiés à partir de la liste de prix source.

Pour configurer un remplacement de prix à la date d’effet pour un prix de rôle ou une majoration de prix de rôle, procédez comme suit.

1. Ouvrez la page de la liste de prix pour laquelle vous souhaitez configurer le remplacement du prix à la date d’effet.
1. Sélectionnez l’onglet **Tarifs des rôles**. Cet onglet répertorie tous les enregistrements **Prix du rôle** dans les tarifs.
1. Sélectionnez l’enregistrement **Prix du rôle** pour lequel vous souhaitez configurer un nouveau prix de remplacement avec date d’effet, puis appuyez deux fois (ou double-cliquez) sur **Prix du rôle** pour ouvrir la page **Détails du prix du rôle**.
1. Sélectionnez l’onglet **Remplacements avec date d’effet**. La grille de cet onglet répertorie tous les remplacements de prix à date d’effet pour l’enregistrement **Prix du rôle** sélectionné.
1. Dans la barre d’outils au-dessus de la grille, sélectionnez **Remplacement du prix du nouveau rôle**. Le curseur **Remplacement du prix du nouveau rôle** s’ouvre.
1. Spécifiez la date de début d’effet, l’unité et le nouveau prix pour le remplacement de prix. Puis sélectionnez **Enregistrer**, puis fermez le formulaire.

> [!NOTE]
> - Un remplacement de prix avec date d’effet pour un prix de rôle ou une majoration de prix de rôle s’applique à la même combinaison de valeurs de dimension de tarification qui existe sur la ligne parente **Prix du rôle** ou **Majoration du prix du rôle**.
> - La date sélectionnée dans le champ **Effectif à compter de** doit se situer dans les dates d’effet des tarifs parents. La dérogation de prix prendra effet à la date sélectionnée dans le champ **Effectif à compter de** et s’appliquera jusqu’à la fin de la date de fin des tarifs parents. Si vous configurez un autre remplacement de prix à date d’effet pour le même prix de rôle, le premier remplacement de prix prendra effet à la date sélectionnée dans le champ **Effectif à compter de** et s’appliquera jusqu’au début de la deuxième dérogation.

## <a name="examples"></a>Examples

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Exemple 1 : Détermination de la date d’effet pour un prix de rôle qui a des remplacements de prix de rôle

L’exemple suivant montre comment l’effectivité de la date est déterminée pour un prix de rôle spécifique pour lequel des remplacements de prix de rôle sont configurés.

**Liste de prix A : du 1er janvier au 30 juin**

*Prix du rôle*

| Prix du rôle | Unité | Tarif | Effet sur la tarification des transactions entrantes |
|---|---|---|---|
| Technicien réseau | heure | 100 | Ce prix sera utilisé pour toutes les transactions dont la date de transaction se situe entre le 1er janvier et le 14 mars. |

*Remplacement du prix du rôle*

| Effectif à partir de | Unité | Tarif | Effet sur la tarification des transactions entrantes |
|---|---|---|---|
| Mars 15 | heure | 110 | Ce prix sera utilisé pour toutes les transactions dont la date de transaction se situe entre le 15 mars et le 30 mars. |
| Avril 1 | heure | 120 | Ce prix sera utilisé pour toutes les transactions dont la date de transaction se situe entre le 1 er avril et le 30 juin. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Exemple 2 : Détermination de la date d’effet pour une majoration du prix de rôle qui a des remplacements de majoration de prix de rôle

L’exemple suivant montre comment l’effectivité de la date est déterminée pour une majoration de prix de rôle spécifique pour lequel des remplacements de majoration de prix de rôle sont configurés.

**Liste de prix A : du 1er janvier au 30 juin**

*Prix du rôle*

| Prix du rôle | Heures de travail | Unité | Tarif | Effet sur la tarification des transactions entrantes |
|---|---|---|---|---|
| Technicien réseau | Régulier | heure | 100 | Ce prix sera utilisé pour toutes les transactions dont la date de transaction se situe entre le 1er janvier et le 14 mars. |

*Majoration du prix du rôle*

| Unité d’organisation | Heures de travail | % de majoration |
|---|---|---|
| Contoso US | Heures supplémentaires | 10 % |

*Remplacement de la majoration du prix du rôle*

| Effectif à partir de | Tarif | Effet sur la tarification des transactions entrantes |
|---|---|---|
| Mars 15 | 20 % | Ce pourcentage de majoration sera utilisé pour toutes les transactions dont la date de transaction se situe entre le 15 mars et le 30 mars. |
| Avril 1 | 25 %% | Cette majoration sera utilisée pour toutes les transactions dont la date de transaction se situe entre le 1 er avril et le 30 juin. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
