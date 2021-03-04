---
title: Dépenser via mobile
description: Cette rubrique donne des informations sur l’espace de travail mobile Gestion des dépenses.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51da574143b91df636d99f91d37470905a9b0529
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120900"
---
# <a name="expense-using-mobile"></a>Dépenser via mobile

_**S’applique à :** Project Operations pour les scénarios basés sur les ressources/produits non stockés Déploiement simplifié – Traiter la facturation pro forma_

Cette rubrique donne des informations sur l’espace de travail mobile **Gestion des dépenses** . Cet espace de travail permet aux utilisateurs de capturer et de télécharger un reçu, afin de pouvoir le joindre à une note de frais ultérieurement. Les utilisateurs peuvent également créer rapidement une ligne de dépenses en utilisant un reçu joint, et créer et gérer leurs notes de frais. De plus, les approbateurs peuvent utiliser l’espace de travail mobile **Gestion des dépenses** pour afficher les notes de frais qui leur sont affectées et les approuver ou les rejeter.

Cet espace de travail mobile est destiné à être utilisé avec l’application mobile Dynamics 365 Unified Ops.

De nombreuses organisations exigent qu’une copie d’un reçu soit jointe à une note de frais de voyage ou d’affaires qu’un employé soumet pour remboursement. L’espace de travail mobile **Gestion des dépenses** permet aux utilisateurs de créer rapidement de nouvelles lignes de dépenses sur l’appareil mobile de leur choix en joignant la photo d’un reçu. Ils peuvent également prendre une photo d’un reçu, puis la joindre ultérieurement à une note de frais. Les employés peuvent également créer et gérer leurs notes de frais, puis les soumettre pour approbation et remboursement en utilisant leur appareil mobile.

L’espace de travail mobile **Gestion des dépenses** en particulier permet aux utilisateurs d’effectuer ces tâches :

- Prendre une photo d’un reçu. Télécharger la photo du reçu et la joindre ultérieurement à une note de frais.
- Télécharger un fichier en tant que reçu capturé. Vous pouvez joindre ce fichier à une note de frais ultérieurement.
- Créez une nouvelle ligne de dépense en utilisant un reçu joint. Vous pouvez ensuite ajouter l’élément de ligne à une note de frais ultérieurement et le soumettre pour approbation et remboursement.

Vous pouvez également utiliser ces fonctionnalités :

- Créer une note de frais.
- Joindre les transactions par carte de crédit et autres dépenses précédemment créées à une note de frais.
- Créer de nouvelles dépenses pour une note de frais.
- Joindre un reçu à toute dépense pour une note de frais, soit en prenant une photo du reçu ou en téléchargeant un fichier comme reçu capturé.
- Selon la politique de dépenses de l’entreprise, ajoutez la liste des invités à une dépense.
- En fonction de la politique de dépenses de l’entreprise, détaillez les dépenses.
- Soumettez un rapport de dépenses pour approbation et remboursement.
- Approuvez ou rejetez les notes de frais pour lesquelles vous êtes un approbateur désigné.

## <a name="prerequisites"></a>Conditions préalables
Les conditions préalables varient en fonction de la version qui a été déployée pour votre organisation.

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Prérequis si vous utilisez Dynamics 365 Finance 
Si Finance a été déployé pour votre organisation, l’administrateur système doit publier l’espace de travail mobile **Gestion des dépenses**. 

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>Conditions préalables si vous utilisez la version 1611 avec la mise à jour de la plateforme 3 (ou version ultérieure)
Si la version 1611 avec la mise à jour de la plateforme 3 (ou version ultérieure) a été déployée pour votre organisation, l’administrateur système doit remplir les conditions préalables suivantes. 

<table>
<thead>
<tr class="header">
<th>Éléments requis</th>
<th>Rôle</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Implémentez KB 4019015.</td>
<td>Administrateur système</td>
<td>KB 4019015 est une mise à jour X++ ou un correctif de métadonnées qui contient l’espace de travail mobile <strong>Gestion des dépenses</strong>. Pour implémenter KB 4019015, votre administrateur système doit procéder comme suit.
<ol>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs">Télécharger les mises à jour de Lifecycle Services (LCS)</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Installez le correctif des métadonnées</a>.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">Créez un package déployable</a> qui contient les modèles <strong>ApplicationSuite</strong> et <strong>ExpenseMobile</strong>, puis téléchargez le package déployable sur LCS.</li>
<li><a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">Appliquez le package déployable</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td>Publiez l’espace de travail mobile <strong>Gestion des dépenses</strong>.</td>
<td>Administrateur système</td>
<td>Voir <a href="https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">Publier un espace de travail mobile</a>.</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-unified-ops-mobile-app"></a>Téléchargez et installez l’application mobile Dynamics 365 Unified Ops
Téléchargez et installez l’application mobile Dynamics 365 Unified Ops :

- [Pour les téléphones Android](https://go.microsoft.com/fwlink/?linkid=850662)
- [Pour les iPhones](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>Se connecter à l’application mobile
1. Démarrez l’application sur votre appareil mobile.
2. Tapez votre URL Dynamics 365.
4. La première fois que vous vous connectez, vous êtes invité à saisir votre nom d’utilisateur et votre mot de passe. Entrez vos informations d’identification.
5. Une fois connecté, les espaces de travail disponibles pour votre entreprise s’affichent. Si votre administrateur système publie un nouvel espace de travail ultérieurement, vous devez actualiser la liste des espaces de travail mobiles.

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>Capturer un reçu à l’aide de l’espace de travail mobile Gestion des dépenses

1. Sur votre appareil mobile, ouvrez l’espace de travail **Gestion des dépenses**.
2. Sélectionnez **Capturer le reçu**.
3. Sélectionnez **Prendre une photo** ou **Choisir une image**.
4. Suivez l’une de ces étapes :

   - Si vous avez sélectionné **Prendre une photo**, suivez ces étapes :

      1. Vous êtes dirigé vers l’appareil photo de votre appareil mobile, afin de pouvoir prendre une photo du reçu. 
      2. Lorsque vous avez terminé de prendre la photo, cliquez sur **OK** pour accepter la photo.
      3. Facultatif : Saisissez un nom pour la photo et saisissez des notes.

    - Si vous avez sélectionné **Choisir une image**, suivez ces étapes :

        1. Sélectionnez une image dans la liste.
        2. Facultatif : Saisissez un nom pour l’image et saisissez des notes.

5. Cliquez sur **Terminé**.

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>Saisir rapidement des dépenses à l’aide de l’espace de travail mobile Gestion des dépenses

1. Sur votre appareil mobile, ouvrez l’espace de travail **Gestion des dépenses**.
2. Sélectionnez **Saisie rapide des dépenses**.
3. Sélectionnez la catégorie de dépense. Une liste affiche les catégories de dépenses chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre catégorie ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par catégorie de dépense ou faites une recherche par type de dépense.
4. Saisissez la date de transaction de la dépense.
5. Facultatif : Saisissez le prestataire de la dépense.
6. Entrez le montant de la dépense.
7. Sélectionnez la devise de la dépense. Une liste affiche les codes de devise chargées dans votre application pour une utilisation hors connexion. Par défaut, 400 devises sont chargées, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre devise ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par devise ou passez à la recherche par nom.
8. Sélectionnez **Prendre une photo** ou **Choisir une image**.
9. Suivez l’une de ces étapes :

    - Si vous avez sélectionné **Prendre une photo**, vous êtes dirigé vers l’appareil photo de votre appareil mobile, afin que vous puissiez prendre une photo du reçu. Lorsque vous avez terminé de prendre la photo, cliquez sur **OK** pour accepter la photo.
    - Si vous avez sélectionné **Choisir une image**, sélectionnez une image dans la liste.

10. Cliquez sur **Terminé**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Approuver une note de frais à l’aide de l’espace de travail mobile Gestion des dépenses (si vous utilisez la mise à jour de juillet 2017)

1. Sur votre appareil mobile, ouvrez l’espace de travail **Gestion des dépenses**.
2. **Approbations de dépenses** indique le nombre de notes de frais qui vous sont attribuées pour approbation. Ce nombre est mis à jour environ toutes les 30 minutes. Sélectionnez **Approbations de dépenses**.

    La liste des notes de frais qui vous sont attribuées pour approbation s’affiche.
    
3. Sélectionnez une note de frais pour afficher les détails des dépenses.
4. Sélectionnez une dépense pour en afficher les détails. Les informations affichées pour une dépense incluent tous les détails de ticket de caisse, d’invité et de justificatif.
5. De retour sur la page **État de dépenses**, choisissez d’approuver ou de rejeter la note de frais.
6. Saisissez des commentaires pour l’action d’approbation.
7. Cliquez sur **Terminé**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>Créez une note de frais et soumettez-la pour approbation à l’aide de l’espace de travail mobile Gestion des dépenses (si vous utilisez la mise à jour de juillet 2017)

1. Sur votre appareil mobile, ouvrez l’espace de travail **Gestion des dépenses**.
2. Sélectionnez **Entrée de dépense**.
3. Sélectionnez **Nouveau rapport** ou sélectionnez une note de frais existante dans la liste.
4. Pour les nouvelles notes de frais, entrez l’objectif et toute information supplémentaire disponible. Ces informations varient en fonction de la façon dont la gestion des dépenses est configurée pour votre entreprise.
5. Cliquez sur **Terminé**.
6. Pour ajouter des dépenses existantes, telles que des transactions par carte de crédit, à la note de frais, sélectionnez **Joindre**.
7. Sélectionnez une ou plusieurs dépenses dans la liste.
8. Cliquez sur **Terminé**.
9. Pour ajouter une nouvelle dépense à la note de frais, sélectionnez **Nouvelle dépense**.
10. Sélectionnez la catégorie de dépense. Une liste affiche les catégories de dépenses chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre catégorie ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par catégorie de dépense ou faites une recherche par type de dépense.
11. Facultatif : Saisissez le prestataire de la dépense.
12. Saisissez la date de transaction de la dépense.
13. Entrez le montant de la dépense.
14. Sélectionnez la devise de la dépense. Une liste affiche les codes de devise chargées dans votre application pour une utilisation hors connexion. Par défaut, 400 devises sont chargées, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre devise ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par devise ou passez à la recherche par nom.
15. Cliquez sur **Terminé**.
16. Pour ajouter plus de détails à la dépense, sélectionnez **Ajouter plus de détails**. Les champs disponibles dépendent de la configuration de la gestion des dépenses de votre entreprise.
17. Si la politique de l’entreprise exige un reçu pour la dépense, sélectionnez **Reçus**, puis suivez ces étapes :

    1. Sélectionnez **Capturer le reçu** ou **Joindre le reçu**.
    2. Suivez l’une de ces étapes :

        - Si vous avez sélectionné **Capturer le reçu**, suivez ces étapes :

            1. Sélectionnez **Prendre une photo** ou **Choisir une image**.
            2. Suivez l’une de ces étapes :

                - Si vous avez sélectionné **Prendre une photo**, suivez ces étapes :

                    1. Vous êtes dirigé vers l’appareil photo de votre appareil mobile, afin de pouvoir prendre une photo du reçu. Lorsque vous avez terminé de prendre la photo, cliquez sur **OK** pour accepter la photo.
                    2. Facultatif : Saisissez un nom pour la photo et saisissez des notes.

                - Si vous avez sélectionné **Choisir une image**, suivez ces étapes :

                    1. Sélectionnez une image dans la liste.
                    2. Facultatif : Saisissez un nom pour l’image et saisissez des notes.

            3.  Cliquez sur **Terminé**.

        - Si vous avez sélectionné **Joindre le reçu**, suivez ces étapes :

            1.  Sélectionnez une ou plusieurs images dans la liste.
            2.  Cliquez sur **Terminé**.

    3. Cliquez sur le bouton **Précédent** pour revenir aux détails des dépenses.

18. Si la politique de l’entreprise exige des invités pour la dépense, sélectionnez **Invités**, puis suivez ces étapes :

    1. Sélectionnez **Invité**, **Invités précédents** ou **Collègues**.
    2. Suivez l’une de ces étapes :

        - Si vous avez sélectionné **Invité**, suivez ces étapes :

            1. Entrez le nom de l’invité.
            2. Facultatif : Saisissez l’organisation et/ou le pays de l’invité.
            3. Facultatif : Saisissez la fonction de l’invité.
            4. Cliquez sur **Terminé**.

        - Si vous avez sélectionné **Invités précédents**, suivez ces étapes :

            1. Sélectionnez un ou plusieurs invités précédents dans la liste. Vous voyez une liste des invités précédents que vous avez ajoutés aux notes de frais précédentes qui sont chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre invité précédent ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par nom ou passez à une recherche par organisation, pays ou fonction.
            2. Cliquez sur **Terminé**.

        - Si vous avez sélectionné **Collègues**, suivez ces étapes :

            1. Sélectionnez un ou plusieurs collègues dans la liste. Une liste affiche les collègues chargés dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre collègue ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par nom ou passez à une recherche par société ou fonction.
            2. Cliquez sur **Terminé**.

    3. Cliquez sur le bouton **Précédent** pour revenir aux détails des dépenses.

19. Si la politique de l’entreprise exige que le reçu soit détaillé, sélectionnez **Détailler**, puis suivez ces étapes :

    1. Sélectionnez la première date à détailler.
    2. Sélectionnez **Ajouter un justificatif**.
    3. Sélectionnez la sous-catégorie pour la ventilation des dépenses. Une liste affiche les sous-catégories de dépenses chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre sous-catégorie ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par nom de sous-catégorie de dépenses.
    4. Saisissez le montant de la transaction pour le justificatif.
    5. Modifiez la date de transaction si nécessaire.
    6. Cliquez sur **Terminé**.
    7. Répétez les étapes précédentes jusqu’à ce que vous ayez terminé d’ajouter tous les éléments pour la date sélectionnée.
    8. Pour les jours supplémentaires, vous pouvez sélectionner **Copier au jour suivant** pour copier les justificatifs le jour suivant. Vous pouvez également sélectionner la date à détailler, puis ajouter des éléments comme vous l’avez fait pour la première date.
    9. Une fois que vous avez terminé de détailler la dépense, sélectionnez le bouton **Précédent** pour revenir aux détails des dépenses.

20. Cliquez sur le bouton **Précédent** pour revenir à la page **État de dépenses**.
21. Répétez les étapes précédentes jusqu’à ce que vous ayez fini d’ajouter toutes les dépenses.
22. Sélectionnez **Soumettre**.
23. Saisissez des commentaires pour l’approbateur.
24. Cliquez sur **Terminé**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]