---
title: Application mobile Gestion des dépenses
description: Cette rubrique donne des informations sur l’espace de travail mobile Gestion des dépenses.
author: suvaidya
ms.date: 11/15/2021
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 14bd76df5f058d2af9f77990471a0a173fe8c15d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588917"
---
# <a name="mobile-expense-app"></a>Application mobile Gestion des dépenses

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

## <a name="prerequisites-if-you-use-dynamics-365-finance"></a>Conditions préalables si vous utilisez Dynamics 365 Finance

Si Finance a été déployé pour votre organisation, l’administrateur système doit publier l’espace de travail mobile **Gestion des dépenses**. 

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
3. Sélectionnez la catégorie de dépense. Une liste affiche les catégories de dépenses chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre catégorie ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par catégorie de dépense ou faites une recherche par type de dépense.
4. Saisissez la date de transaction de la dépense.
5. Facultatif : Saisissez le prestataire de la dépense.
6. Entrez le montant de la dépense.
7. Sélectionnez la devise de la dépense. Une liste affiche les codes de devise chargées dans votre application pour une utilisation hors connexion. Par défaut, 400 devises sont chargées, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre devise ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par devise ou passez à la recherche par nom.
8. Sélectionnez **Prendre une photo** ou **Choisir une image**.
9. Suivez l’une de ces étapes :

    - Si vous avez sélectionné **Prendre une photo**, vous êtes dirigé vers l’appareil photo de votre appareil mobile, afin que vous puissiez prendre une photo du reçu. Lorsque vous avez terminé de prendre la photo, cliquez sur **OK** pour accepter la photo.
    - Si vous avez sélectionné **Choisir une image**, sélectionnez une image dans la liste.

10. Cliquez sur **Terminé**.

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace"></a>Approbation d’une note de frais à l’aide de l’espace de travail mobile Gestion des dépenses

1. Sur votre appareil mobile, ouvrez l’espace de travail **Gestion des dépenses**.
2. **Approbations de dépenses** indique le nombre de notes de frais qui vous sont attribuées pour approbation. Ce nombre est mis à jour environ toutes les 30 minutes. Sélectionnez **Approbations de dépenses**.

    La liste des notes de frais qui vous sont attribuées pour approbation s’affiche.

3. Sélectionnez une note de frais pour afficher les détails des dépenses.
4. Sélectionnez une dépense pour en afficher les détails. Les informations affichées pour une dépense incluent tous les détails de ticket de caisse, d’invité et de justificatif.
5. De retour sur la page **État de dépenses**, choisissez d’approuver ou de rejeter la note de frais.
6. Saisissez des commentaires pour l’action d’approbation.
7. Cliquez sur **Terminé**.

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace"></a>Créez un état de dépenses et soumettez-le pour approbation à l’aide de l’espace de travail mobile Gestion des dépenses

1. Sur votre appareil mobile, ouvrez l’espace de travail **Gestion des dépenses**.
2. Sélectionnez **Entrée de dépense**.
3. Sélectionnez **Nouveau rapport** ou sélectionnez une note de frais existante dans la liste.
4. Pour les nouvelles notes de frais, entrez l’objectif et toute information supplémentaire disponible. Ces informations varient en fonction de la façon dont la gestion des dépenses est configurée pour votre entreprise.
5. Cliquez sur **Terminé**.
6. Pour ajouter des dépenses existantes, telles que des transactions par carte de crédit, à la note de frais, sélectionnez **Joindre**.
7. Sélectionnez une ou plusieurs dépenses dans la liste.
8. Cliquez sur **Terminé**.
9. Pour ajouter une nouvelle dépense à la note de frais, sélectionnez **Nouvelle dépense**.
10. Sélectionnez la catégorie de dépense. Une liste affiche les catégories de dépenses chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre catégorie ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par catégorie de dépense ou faites une recherche par type de dépense.
11. Facultatif : Saisissez le prestataire de la dépense.
12. Saisissez la date de transaction de la dépense.
13. Entrez le montant de la dépense.
14. Sélectionnez la devise de la dépense. Une liste affiche les codes de devise chargées dans votre application pour une utilisation hors connexion. Par défaut, 400 devises sont chargées, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre devise ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par devise ou passez à la recherche par nom.
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

            3. Cliquez sur **Terminé**.

        - Si vous avez sélectionné **Joindre le reçu**, suivez ces étapes :

            1. Sélectionnez une ou plusieurs images dans la liste.
            2. Cliquez sur **Terminé**.

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

            1. Sélectionnez un ou plusieurs invités précédents dans la liste. Vous voyez une liste des invités précédents que vous avez ajoutés aux notes de frais précédentes qui sont chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre invité précédent ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par nom ou passez à une recherche par organisation, pays ou fonction.
            2. Cliquez sur **Terminé**.

        - Si vous avez sélectionné **Collègues**, suivez ces étapes :

            1. Sélectionnez un ou plusieurs collègues dans la liste. Une liste affiche les collègues chargés dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre collègue ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par nom ou passez à une recherche par société ou fonction.
            2. Cliquez sur **Terminé**.

    3. Cliquez sur le bouton **Précédent** pour revenir aux détails des dépenses.

19. Si la politique de l’entreprise exige que le reçu soit détaillé, sélectionnez **Détailler**, puis suivez ces étapes :

    1. Sélectionnez la première date à détailler.
    2. Sélectionnez **Ajouter un justificatif**.
    3. Sélectionnez la sous-catégorie pour la ventilation des dépenses. Une liste affiche les sous-catégories de dépenses chargées dans votre application pour une utilisation hors connexion. Par défaut, 50 éléments sont chargés, mais un développeur peut modifier ce nombre. Pour plus d’informations, les développeurs doivent consulter [Plateforme mobile](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-getting-started). Si votre sous-catégorie ne figure pas dans la liste, sélectionnez **Rechercher** pour faire une recherche en ligne. Recherchez par nom de sous-catégorie de dépenses.
    4. Saisissez le montant de la transaction pour le justificatif.
    5. Modifiez la date de transaction si nécessaire.
    6. Cliquez sur **Terminé**.
    7. Répétez les étapes précédentes jusqu’à ce que vous ayez terminé d’ajouter tous les éléments pour la date sélectionnée.
    8. Pour les jours supplémentaires, vous pouvez sélectionner **Copier au jour suivant** pour copier les justificatifs le jour suivant. Vous pouvez également sélectionner la date à détailler, puis ajouter des éléments comme vous l’avez fait pour la première date.
    9. Une fois que vous avez terminé de détailler la dépense, sélectionnez le bouton **Précédent** pour revenir aux détails des dépenses.

20. Cliquez sur le bouton **Précédent** pour revenir à la page **État de dépenses**.
21. Répétez les étapes précédentes jusqu’à ce que vous ayez fini d’ajouter toutes les dépenses.
22. Cliquez sur **Envoyer**.
23. Saisissez des commentaires pour l’approbateur.
24. Cliquez sur **Terminé**.

## <a name="frequently-asked-questions"></a>Questions fréquentes

### <a name="why-doesnt-the-expense-mobile-app-enter-the-payment-method-by-default"></a>Pourquoi l’application mobile Gestion des dépenses n’entre-t-elle pas dans le mode de paiement par défaut ?

Les organisations peuvent personnaliser le paramètre **Mode de paiement par défaut** pour chaque catégorie de dépenses au fur et à mesure de leur création. De plus, lorsque vous configurez des modes de paiement, vous pouvez définir le champ **Mode de paiement par défaut** sur **Importation uniquement**.

Lorsque l’option **Importation uniquement** est activée pour un mode de paiement, le mode de paiement n’est pas renseigné par défaut. Il sera vierge dans les catégories de dépenses où ce mode de paiement est configuré. Ce comportement est cohérent à la fois dans l’expérience Web et l’expérience mobile.
    
Lorsque l’option **Importation uniquement** n’est pas activée pour un mode de paiement, la valeur définie est saisie par défaut pour les catégories de dépenses où ce mode de paiement est configuré. Cependant, il existe un problème connu où la valeur par défaut n’est pas entrée dans l’application mobile Gestion des dépenses. Pour contourner ce problème, sélectionnez manuellement un mode de paiement avant d’enregistrer la note de frais. 

### <a name="why-cant-i-add-or-edit-financial-dimensions-in-the-expense-mobile-app"></a>Pourquoi ne puis-je pas ajouter ou modifier de dimensions financières dans l’application mobile Gestion des dépenses ?

La saisie de dimensions et de distributions n’est pas prise en charge. Pour contourner cette limitation, vous pouvez définir ces champs par défaut dans l’application mobile en configurant les dimensions financières par défaut par projet ou employé.

### <a name="why-do-i-sometimes-see-a-synchronization-error-in-the-expense-mobile-app"></a>Pourquoi est-ce que je vois parfois une erreur de synchronisation dans l’application mobile Gestion des dépenses ?

Si les lignes de dépense ne répondent pas aux exigences de la politique et que l’utilisateur soumet la note de frais sans répondre à l’avertissement de la politique, les données mobiles ne sont pas synchronisées avec le serveur et un échec de synchronisation se produit. Toutes les notes de frais soumises après un échec de synchronisation resteront dans un état d’échec et provoqueront davantage d’échecs de synchronisation. La seule façon de corriger cette situation est de supprimer manuellement les notifications de synchronisation. Ce problème a été résolu en arrêtant la soumission des notes de frais lorsque les avertissements de la politique n’ont pas reçu de réponse, afin d’éviter les erreurs de synchronisation.

### <a name="why-isnt-project-and-category-validation-correctly-reflected-in-the-expense-mobile-app"></a>Pourquoi la validation de projet et de catégorie n’est-elle pas correctement reflétée dans l’application mobile Gestion des dépenses ?

Cette validation n’est pas actuellement prise en charge. Elle pourrait cependant être ajoutée à l’avenir. 

### <a name="what-document-types-are-supported-in-the-expense-mobile-app"></a>Quels types de documents sont pris en charge dans l’application mobile Gestion des dépenses ?

L’application mobile Gestion des dépenses prend en charge que les images. Elle ne prend actuellement pas en charge les PDF ou autres documents.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
