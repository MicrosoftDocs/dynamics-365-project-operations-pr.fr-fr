---
title: Demandes d’articles pour les contrats de projet avec plusieurs sources de financement
description: Cette rubrique offre des informations sur la configuration et l’utilisation des demandes d’articles avec plusieurs sources de financement.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d4af03e02d3c2eb0d442e6213ff5b9cf583d54b3
ms.sourcegitcommit: 30242d7754bca300b594b0887eb4212d10bea1c4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2022
ms.locfileid: "8728108"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Demandes d’articles pour les contrats de projet avec plusieurs sources de financement

_**S’applique à :** Project Operations pour les scénarios basés sur les produits stockés/ordres de fabrication_

Certains accords contractuels pour les livrables basés sur des projets peuvent nécessiter plusieurs sources de financement. Cette rubrique explique comment sélectionner et configurer les sources de financement souhaitées lorsque plusieurs sources sont requises pour un projet ou un contrat de projet.

## <a name="terminology"></a>Terminologie

- **Source de financement** – Entité qui finance les travaux du contrat de projet. Cette entité peut être une organisation interne ou un compte de facturation externe (client ou subvention).
- **Client du projet** – Entité à laquelle le travail du projet est livré.
- **Compte de facturation** – Entité externe qui paie les travaux du projet.

## <a name="example"></a>Exemple

Contoso a remporté un contrat de renouvellement d’équipement avec deux de ses clients : Adatum US et Adatum Corporate. Le contrat comprend le matériel et les services d’installation qui seront livrés à Adatum US (le client du projet). Le matériel sera financé par Adatum Corporate (compte de facturation 1) et les travaux d’installation seront financés par Adatum US (compte de facturation 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Configurer les règles par défaut du compte de facturation pour les demandes d’articles

### <a name="prerequisites"></a>Conditions préalables

- Microsoft Dynamics 365 Finance and Operations **version 10.0.27 ou ultérieure** est nécessaire pour utiliser les demandes d’articles ayant plusieurs comptes de facturation.
- Votre système administrateur doit activer la fonctionnalité **Autoriser les demandes d’articles avec plusieurs sources de financement pour les scénarios basés sur les stocks/la production de Project Operations** dans l’espace de travail **Gestion des fonctionnalités**.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Configurer les règles par défaut du compte de facturation

Pour configurer les règles par défaut pour le compte de facturation, procédez comme suit.

1. Accédez à **Gestion et comptabilité des projets** \> **Configuration** \> **Paramètres de gestion et comptabilité des projets**.
1. Sur l’onglet **Général**, dans la section **Commandes client et demandes d’articles**, définissez l’option **Autoriser les projets avec plusieurs sources de financement** sur **Oui**.
1. Dans le champ **Client par défaut**, spécifiez d’où vient le client de livraison du projet sur la demande d’article par défaut :

    - **En provenance de la source de financement** – Le client de livraison de projet par défaut provient de la source de financement. Si plusieurs sources de financement sont associées au contrat de projet, la première source de financement de la liste sera utilisée.
    - **En provenance du projet** – Le client de livraison de projet par défaut provient du client sélectionné dans le champ **Compte d’enregistrement du projet**.

1. Facultatif : définissez ou modifiez le compte de facturation par défaut dans les enregistrements de projet :

    1. Accédez à **Gestion de projet et comptabilité** \> **Projets** \> **Tous les projets**, et ouvrez les détails de l’enregistrement du projet.
    2. Sur l’onglet **Général**, définissez ou mettez à jour le champ **Compte de facturation par défaut**. Le compte que vous spécifiez sera utilisé comme compte de facturation par défaut pour les nouvelles demandes d’articles créées pour le projet. Si vous laissez le champ vide, le compte de facturation de la première source de financement du contrat de projet sera utilisé par défaut. Cependant, les utilisateurs pourront modifier le compte lorsqu’ils enregistreront l’enregistrement.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Sélectionnez le compte de facturation à utiliser lorsque vous créez une demande d’articles

Pour sélectionner le compte de facturation à utiliser lorsque vous créez une demande d’articles, procédez comme suit.

1. Accédez à **Gestion de projet et comptabilité** \> **Projets** \> **Tous les projets**, et sélectionnez l’enregistrement du projet.
1. Sur l’onglet **Plan**, sélectionnez **Demandes d’articles**.
1. Création d’un enregistrement de demande d’article.

    - Par défaut, le champ **Compte de facturation** dans l’enregistrement est défini sur le compte de facturation défini pour le projet. Vous pouvez modifier la valeur du champ **Compte de facturation**, puis enregistrez l’enregistrement. Une fois l’enregistrement enregistré, vous ne pouvez plus mettre à jour la valeur **Compte de facturation**. Si vous devez mettre à jour la valeur **Compte de facturation** pour la demande d’article, supprimez la demande d’article existante, puis créez-en une nouvelle ayant la valeur souhaitée.
    - Par défaut, le champ **Client** pour la demande d’article est défini en fonction de la valeur **Client par défaut** définie sur la page **Paramètres de gestion et comptabilité des projets**.

    Lorsque l’enregistrement de demande d’article est sauvegardé, le système l’associe à l’enregistrement de l’en-tête **Commande client de demande d’article**. Si aucun en-tête de commande client en cours n’a le compte de facturation sélectionné, le système en créera un et y associera la ligne de demande d’articles.

> [!NOTE]
> Les demandes d’articles sont toujours entièrement facturées sur le compte de facturation défini dans l’enregistrement. Le système ne prend actuellement pas en charge les règles d’allocation de financement ayant des demandes d’articles, et il ne divisera pas la publication en fonction de la configuration des règles d’allocation de financement.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Créer une demande d’articles à partir d’un enregistrement de prévision d’articles

Pour créer une demande d’articles à partir d’un enregistrement de prévision d’articles, procédez comme suit.

1. Accédez à **Gestion de projet et comptabilité** \> **Projets** \> **Tous les projets** et sélectionnez l’enregistrement du projet.
1. Sur l’onglet **Plan**, sélectionnez **Prévisions d’articles**.
1. Création d’un enregistrement de prévision d’article.
1. Facultatif : sur l’onglet **Projet**, dans le champ **Source de financement**, sélectionnez le compte de facturation souhaité.
1. Sélectionnez **Créer une demande d’article**, et confirmez le message que vous recevez.

    > [!NOTE]
    > Le système copie la valeur **Source de financement** depuis l’enregistrement de prévision d’article vers l’enregistrement de demande d’article nouvellement créé.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Compte de facturation par défaut lorsque le système crée automatiquement une demande d’articles à partir d’une ligne de commande fournisseur

Si l"option **Créer une exigence d’article** est définie sur **Oui** sur la page **Paramètres de gestion et comptabilité des projets**, le système crée automatiquement une demande d’articles lorsqu’une nouvelle ligne de commande fournisseur de projet est enregistrée. Par défaut, les champs **Compte de facturation** et **Demande d’article** sont définis sur la valeur du champ **Compte de facturation par défaut** dans l’enregistrement du projet. Le système ne prend actuellement pas en charge la mise à jour ou la modification du compte de facturation pour les enregistrements de ce type.
