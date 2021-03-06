---
title: "Didacticiel : Intégration d’Azure Active Directory à Hosted Graphite | Microsoft Docs"
description: "Découvrez comment configurer l’authentification unique entre Azure Active Directory et Hosted Graphite."
services: active-directory
documentationCenter: na
author: jeevansd
manager: mtillman
ms.assetid: a1ac4d7f-d079-4f3c-b6da-0f520d427ceb
ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 06/22/2017
ms.author: jeedes
ms.openlocfilehash: 57ee7770193641d0e13da2c7f8aaa6cfc6aefe73
ms.sourcegitcommit: d1f35f71e6b1cbeee79b06bfc3a7d0914ac57275
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/22/2018
---
# <a name="tutorial-azure-active-directory-integration-with-hosted-graphite"></a>Didacticiel : Intégration d’Azure Active Directory à Hosted Graphite

Dans ce didacticiel, vous allez apprendre à intégrer Hosted Graphite à Azure Active Directory (Azure AD).

L’intégration de Hosted Graphite à Azure AD vous offre les avantages suivants :

- Dans Azure AD, vous pouvez contrôler qui a accès à Hosted Graphite.
- Vous pouvez autoriser les utilisateurs à se connecter automatiquement à Hosted Graphite (par le biais de l’authentification unique) avec leur compte Azure AD.
- Vous pouvez gérer vos comptes à partir d’un emplacement central : le portail Azure.

Pour en savoir plus sur l’intégration des applications SaaS avec Azure AD, consultez [Qu’est-ce que l’accès aux applications et l’authentification unique avec Azure Active Directory ?](active-directory-appssoaccess-whatis.md).

## <a name="prerequisites"></a>Prérequis

Pour configurer l’intégration d’Azure AD à Hosted Graphite, vous avez besoin des éléments suivants :

- Un abonnement Azure AD
- Un abonnement Hosted Graphite pour lequel l’authentification unique est activée

> [!NOTE]
> Pour tester les étapes de ce didacticiel, nous déconseillons l’utilisation d’un environnement de production.

Vous devez en outre suivre les recommandations ci-dessous :

- N’utilisez pas votre environnement de production, sauf si cela est nécessaire.
- Si vous n’avez pas d’environnement d’essai Azure AD, vous pouvez obtenir un essai d’un mois [ici](https://azure.microsoft.com/pricing/free-trial/).

## <a name="scenario-description"></a>Description du scénario
Dans ce didacticiel, vous testez l’authentification unique Azure AD dans un environnement de test. Le scénario décrit dans ce didacticiel se compose des deux sections principales suivantes :

1. Ajout de Hosted Graphite à partir de la galerie
2. Configuration et test de l’authentification unique Azure AD

## <a name="adding-hosted-graphite-from-the-gallery"></a>Ajout de Hosted Graphite à partir de la galerie
Pour configurer l’intégration de Hosted Graphite à Azure AD, vous devez ajouter Hosted Graphite à partir de la galerie à votre liste d’applications SaaS gérées.

**Pour ajouter Hosted Graphite à partir de la galerie, procédez comme suit :**

1. Dans le volet de navigation gauche du **[portail Azure](https://portal.azure.com)**, cliquez sur l’icône **Azure Active Directory**. 

    ![Active Directory][1]

2. Accédez à **Applications d’entreprise**. Accédez ensuite à **Toutes les applications**.

    ![APPLICATIONS][2]
    
3. Pour ajouter l’application, cliquez sur le bouton **Nouvelle application** en haut de la boîte de dialogue.

    ![APPLICATIONS][3]

4. Dans la zone de recherche, tapez **Hosted Graphite**.

    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_search.png)

5. Dans le volet des résultats, sélectionnez **Hosted Graphite**, puis cliquez sur le bouton **Ajouter** pour ajouter l’application.

    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_addfromgallery.png)

##  <a name="configuring-and-testing-azure-ad-single-sign-on"></a>Configuration et test de l’authentification unique Azure AD
Dans cette section, vous allez configurer et tester l’authentification unique Azure AD avec Hosted Graphite avec un utilisateur de test appelé « Britta Simon ».

Pour que l’authentification unique fonctionne, Azure AD a besoin de savoir qui est l’utilisateur Hosted Graphite équivalent dans Azure AD. En d’autres termes, une relation entre l’utilisateur Azure AD et l’utilisateur Hosted Graphite associé doit être établie.

Dans Hosted Graphite, affectez la valeur du **nom d’utilisateur** dans Azure AD comme valeur du **nom d’utilisateur** pour établir la relation.

Pour configurer et tester l’authentification unique Azure AD avec Hosted Graphite, vous avez besoin de suivre les indications des sections suivantes :

1. **[Configuration de l’authentification unique Azure AD](#configuring-azure-ad-single-sign-on)** pour permettre à vos utilisateurs d’utiliser cette fonctionnalité.
2. **[Création d’un utilisateur de test Azure AD](#creating-an-azure-ad-test-user)** pour tester l’authentification unique Azure AD avec Britta Simon.
3. **[Création d’un utilisateur de test Hosted Graphite](#creating-a-hosted-graphite-test-user)** pour avoir un équivalent de Britta Simon dans Hosted Graphite lié à la représentation Azure AD associée.
4. **[Affectation de l’utilisateur de test Azure AD](#assigning-the-azure-ad-test-user)** : permet à Britta Simon d’utiliser l’authentification unique Azure AD.
5. **[Testing Single Sign-On](#testing-single-sign-on)** pour vérifier si la configuration fonctionne.

### <a name="configuring-azure-ad-single-sign-on"></a>Configuration de l’authentification unique Azure AD

Dans cette section, vous allez activer l’authentification unique Azure AD dans le portail Azure et configurer l’authentification unique dans votre application Hosted Graphite.

**Pour configurer l’authentification unique Azure AD avec Hosted Graphite, procédez comme suit :**

1. Dans le portail Azure, sur la page d’intégration de l’application **Hosted Graphite**, cliquez sur **Authentification unique**.

    ![Configure Single Sign-On][4]

2. Dans la boîte de dialogue **Authentification unique**, pour le **Mode**, sélectionnez **Authentification basée sur SAML** pour activer l’authentification unique.
 
    ![Configure Single Sign-On](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_samlbase.png)

3. Dans la section **Domaine et URL Hosted Graphite**, si vous voulez configurer l’application en **Mode initié par IDP**, procédez comme suit :

    ![Configure Single Sign-On](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_url.png)

    a. Dans la zone de texte **Identificateur**, tapez une URL au format suivant : `https://www.hostedgraphite.com/metadata/<user id>`

    b. Dans la zone de texte **URL de réponse** , tapez une URL au format suivant : `https://www.hostedgraphite.com/complete/saml/<user id>`

4. Dans la section **Domaine et URL Hosted Graphite**, si vous voulez configurer l’application en **Mode initié par SP**, procédez comme suit :
   
    ![Configure Single Sign-On](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_10.png)
  
    a. Cliquez sur l’option **Afficher les paramètres d’URL avancés**.

    b. Dans la zone de texte **URL de connexion**, tapez une URL au format suivant : `https://www.hostedgraphite.com/login/saml/<user id>/`   

    > [!NOTE] 
    > Notez qu’il ne s’agit pas des valeurs réelles. Vous devez mettre à jour ces valeurs avec l’identificateur, l’URL de réponse et l’URL de connexion réels. Pour obtenir ces valeurs, vous pouvez accéder à Accéder->Configuration de SAML ou contactez [l’équipe de support d’Hosted Graphite](mailto:help@hostedgraphite.com).
    >
 
5. Dans la section **Certificat de signature SAML**, cliquez sur **Téléchargez le certificat (Base64)** puis enregistrez le fichier du certificat sur votre ordinateur.

    ![Configure Single Sign-On](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_certificate.png) 

6. Cliquez sur le bouton **Enregistrer** .

    ![Configure Single Sign-On](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_400.png)

7. Dans la section **Configuration d’Hosted Graphite**, cliquez sur **Configurer Hosted Graphite** pour ouvrir la fenêtre **Configurer l’authentification**. Copiez **l’ID d’entité SAML et l’URL du service d’authentification unique SAML** à partir de la **section Référence rapide**.

    ![Configure Single Sign-On](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_configure.png) 

8. Connectez-vous à votre client Hosted Graphite en tant qu’administrateur.

9. Accédez à la **page de configuration de SAML** dans la barre latérale (**Accéder -> Configuration SAML**).
   
    ![Configurer l’authentification unique côté application](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_000.png)

10. Confirmez que ces URL correspondent à votre configuration de la section **Domaine et URL Hosted Graphite** du portail Azure.
   
    ![Configurer l’authentification unique côté application](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_001.png)

11. Dans les zones de texte **ID d’entité ou d’émetteur** et **URL de connexion à authentification unique**, collez les valeurs **ID d’entité SAML** et **URL du service d’authentification unique SAML** que vous avez copiées à partir du portail Azure. 
   
    ![Configurer l’authentification unique côté application](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_002.png)
   

12. Sélectionnez « **Lecture seule** » comme **Rôle d’utilisateur par défaut**.
    
    ![Configurer l’authentification unique côté application](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_004.png)

13. Ouvrez dans le Bloc-notes votre certificat codé en base 64 téléchargé à partir du portail Azure, copiez son contenu dans le Presse-papiers, puis collez-le dans la zone de texte **Certificat X.509**.
    
    ![Configurer l’authentification unique côté application](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_005.png)

14. Cliquez sur le bouton **Enregistrer** .

> [!TIP]
> Vous pouvez maintenant lire une version concise de ces instructions dans le [portail Azure](https://portal.azure.com), pendant que vous configurez l’application.  Après avoir ajouté cette application à partir de la section **Active Directory > Applications d’entreprise**, cliquez simplement sur l’onglet **Authentification unique** et accédez à la documentation incorporée par le biais de la section **Configuration** en bas. Vous pouvez en savoir plus sur la fonctionnalité de documentation incorporée ici : [Documentation incorporée Azure AD]( https://go.microsoft.com/fwlink/?linkid=845985)
> 

### <a name="creating-an-azure-ad-test-user"></a>Création d’un utilisateur de test Azure AD
L’objectif de cette section est de créer un utilisateur de test appelé Britta Simon dans le portail Azure.

![Créer un utilisateur Azure AD][100]

**Pour créer un utilisateur de test dans Azure AD, procédez comme suit :**

1. Dans le panneau de navigation gauche du **portail Azure**, cliquez sur l’icône **Azure Active Directory**.

    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-hostedgraphite-tutorial/create_aaduser_01.png) 

2. Pour afficher la liste des utilisateurs, accédez à **Utilisateurs et groupes**, puis cliquez sur **Tous les utilisateurs**.
    
    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-hostedgraphite-tutorial/create_aaduser_02.png) 

3. Pour ouvrir la boîte de dialogue **Utilisateur**, cliquez sur **Ajouter** en haut de la boîte de dialogue.
 
    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-hostedgraphite-tutorial/create_aaduser_03.png) 

4. Dans la boîte de dialogue **Utilisateur**, procédez comme suit :
 
    ![Création d’un utilisateur de test Azure AD](./media/active-directory-saas-hostedgraphite-tutorial/create_aaduser_04.png) 

    a. Dans la zone de texte **Nom**, entrez **BrittaSimon**.

    b. Dans la zone de texte **Nom d’utilisateur**, tapez **l’adresse e-mail** de Britta Simon.

    c. Sélectionnez **Afficher le mot de passe** et notez la valeur du **mot de passe**.

    d. Cliquez sur **Créer**.
 
### <a name="creating-a-hosted-graphite-test-user"></a>Création d’un utilisateur de test Hosted Graphite

L’objectif de cette section est de créer un utilisateur appelé Britta Simon dans Hosted Graphite. Hosted Graphite prend en charge l’approvisionnement juste-à-temps, option activée par défaut.

Vous n’avez aucune opération à effectuer dans cette section. Un utilisateur est créé lors d’une tentative d’accès à Hosted Graphite s’il n’existe pas déjà.

>[!NOTE]
>Si vous devez créer un utilisateur manuellement, contactez l’équipe de support d’Hosted Graphite via <mailto:help@hostedgraphite.com>. 

### <a name="assigning-the-azure-ad-test-user"></a>Affectation de l’utilisateur de test Azure AD

Dans cette section, vous allez autoriser Britta Simon à utiliser l’authentification unique Azure en lui accordant l’accès à Hosted Graphite.

![Affecter des utilisateurs][200] 

**Pour affecter Britta Simon à Hosted Graphite, procédez comme suit :**

1. Dans le portail Azure, ouvrez la vue des applications, accédez à la vue des répertoires, accédez à **Applications d’entreprise**, puis cliquez sur **Toutes les applications**.

    ![Affecter des utilisateurs][201] 

2. Dans la liste des applications, sélectionnez **Hosted Graphite**.

    ![Configure Single Sign-On](./media/active-directory-saas-hostedgraphite-tutorial/tutorial_hostedgraphite_app.png) 

3. Dans le menu de gauche, cliquez sur **Utilisateurs et groupes**.

    ![Affecter des utilisateurs][202] 

4. Cliquez sur le bouton **Ajouter**. Ensuite, sélectionnez **Utilisateurs et groupes** dans la boîte de dialogue **Ajouter une affectation**.

    ![Affecter des utilisateurs][203]

5. Dans la boîte de dialogue **Utilisateurs et groupes**, sélectionnez **Britta Simon** dans la liste des utilisateurs.

6. Cliquez sur le bouton **Sélectionner** dans la boîte de dialogue **Utilisateurs et groupes**.

7. Cliquez sur le bouton **Affecter** dans la boîte de dialogue **Ajouter une affectation**.
    
### <a name="testing-single-sign-on"></a>Test de l’authentification unique

L’objectif de cette section est de tester la configuration de l’authentification unique Azure AD à l’aide du volet d’accès.

Quand vous cliquez sur la vignette Hosted Graphite dans le volet d’accès, vous devez être connecté automatiquement à votre application Hosted Graphite.

## <a name="additional-resources"></a>Ressources supplémentaires

* [Liste de didacticiels sur l’intégration d’applications SaaS avec Azure Active Directory](active-directory-saas-tutorial-list.md)
* [Qu’est-ce que l’accès aux applications et l’authentification unique avec Azure Active Directory ?](active-directory-appssoaccess-whatis.md)



<!--Image references-->

[1]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_01.png
[2]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_02.png
[3]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_03.png
[4]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_04.png

[100]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_100.png

[200]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_200.png
[201]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_201.png
[202]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_202.png
[203]: ./media/active-directory-saas-hostedgraphite-tutorial/tutorial_general_203.png

