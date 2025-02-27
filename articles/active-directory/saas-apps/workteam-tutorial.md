---
title: 'Tutorial: Azure Active Directory single sign-on (SSO) integration with Workteam | Microsoft Docs'
description: Learn how to configure single sign-on between Azure Active Directory and Workteam.
services: active-directory
author: jeevansd
manager: CelesteDG
ms.reviewer: celested
ms.service: active-directory
ms.subservice: saas-app-tutorial
ms.workload: identity
ms.topic: tutorial
ms.date: 09/02/2021
ms.author: jeedes
---

# Tutorial: Azure Active Directory single sign-on (SSO) integration with Workteam

In this tutorial, you'll learn how to integrate Workteam with Azure Active Directory (Azure AD). When you integrate Workteam with Azure AD, you can:

* Control in Azure AD who has access to Workteam.
* Enable your users to be automatically signed-in to Workteam with their Azure AD accounts.
* Manage your accounts in one central location - the Azure portal.

## Prerequisites

To get started, you need the following items:

* An Azure AD subscription. If you don't have a subscription, you can get a [free account](https://azure.microsoft.com/free/).
* Workteam single sign-on (SSO) enabled subscription.

## Scenario description

In this tutorial, you configure and test Azure AD SSO in a test environment.

* Workteam supports **SP and IDP** initiated SSO.
* Workteam supports [Automated user provisioning](workteam-provisioning-tutorial.md).

## Add Workteam from the gallery

To configure the integration of Workteam into Azure AD, you need to add Workteam from the gallery to your list of managed SaaS apps.

1. Sign in to the Azure portal using either a work or school account, or a personal Microsoft account.
1. On the left navigation pane, select the **Azure Active Directory** service.
1. Navigate to **Enterprise Applications** and then select **All Applications**.
1. To add new application, select **New application**.
1. In the **Add from the gallery** section, type **Workteam** in the search box.
1. Select **Workteam** from results panel and then add the app. Wait a few seconds while the app is added to your tenant.

## Configure and test Azure AD SSO for Workteam

Configure and test Azure AD SSO with Workteam using a test user called **B.Simon**. For SSO to work, you need to establish a link relationship between an Azure AD user and the related user in Workteam.

To configure and test Azure AD SSO with Workteam, perform the following steps:

1. **[Configure Azure AD SSO](#configure-azure-ad-sso)** - to enable your users to use this feature.
    1. **[Create an Azure AD test user](#create-an-azure-ad-test-user)** - to test Azure AD single sign-on with B.Simon.
    1. **[Assign the Azure AD test user](#assign-the-azure-ad-test-user)** - to enable B.Simon to use Azure AD single sign-on.
1. **[Configure Workteam SSO](#configure-workteam-sso)** - to configure the single sign-on settings on application side.
    1. **[Create Workteam test user](#create-workteam-test-user)** - to have a counterpart of B.Simon in Workteam that is linked to the Azure AD representation of user.
1. **[Test SSO](#test-sso)** - to verify whether the configuration works.

## Configure Azure AD SSO

Follow these steps to enable Azure AD SSO in the Azure portal.

1. In the Azure portal, on the **Workteam** application integration page, find the **Manage** section and select **single sign-on**.
1. On the **Select a single sign-on method** page, select **SAML**.
1. On the **Set up single sign-on with SAML** page, click the pencil icon for **Basic SAML Configuration** to edit the settings.

   ![Edit Basic SAML Configuration](common/edit-urls.png)

1. On the **Basic SAML Configuration** section the application is pre-configured in **IDP** initiated mode and the necessary URLs are already pre-populated with Azure. The user needs to save the configuration by clicking the **Save** button.

1. Click **Set additional URLs** and perform the following step if you wish to configure the application in **SP** initiated mode:

    In the **Sign-on URL** text box, type the URL:
    `https://app.workte.am`

1. On the **Set up single sign-on with SAML** page, in the **SAML Signing Certificate** section,  find **Certificate (Base64)** and select **Download** to download the certificate and save it on your computer.

	![The Certificate download link](common/certificatebase64.png)

1. On the **Set up Workteam** section, copy the appropriate URL(s) based on your requirement.

	![Copy configuration URLs](common/copy-configuration-urls.png)

### Create an Azure AD test user

In this section, you'll create a test user in the Azure portal called B.Simon.

1. From the left pane in the Azure portal, select **Azure Active Directory**, select **Users**, and then select **All users**.
1. Select **New user** at the top of the screen.
1. In the **User** properties, follow these steps:
   1. In the **Name** field, enter `B.Simon`.  
   1. In the **User name** field, enter the username@companydomain.extension. For example, `B.Simon@contoso.com`.
   1. Select the **Show password** check box, and then write down the value that's displayed in the **Password** box.
   1. Click **Create**.

### Assign the Azure AD test user

In this section, you'll enable B.Simon to use Azure single sign-on by granting access to Workteam.

1. In the Azure portal, select **Enterprise Applications**, and then select **All applications**.
1. In the applications list, select **Workteam**.
1. In the app's overview page, find the **Manage** section and select **Users and groups**.
1. Select **Add user**, then select **Users and groups** in the **Add Assignment** dialog.
1. In the **Users and groups** dialog, select **B.Simon** from the Users list, then click the **Select** button at the bottom of the screen.
1. If you're expecting any role value in the SAML assertion, in the **Select Role** dialog, select the appropriate role for the user from the list and then click the **Select** button at the bottom of the screen.
1. In the **Add Assignment** dialog, click the **Assign** button.

## Configure Workteam SSO

1. To automate the configuration within Workteam, you need to install **My Apps Secure Sign-in browser extension** by clicking **Install the extension**.

	![My apps extension](common/install-myappssecure-extension.png)

2. After adding extension to the browser, click on **Setup Workteam** will direct you to the Workteam application. From there, provide the admin credentials to sign into Workteam. The browser extension will automatically configure the application for you and automate steps 3-6.

	![Setup configuration](common/setup-sso.png)

3. If you want to setup Workteam manually, open a new web browser window and sign into your Workteam company site as an administrator and perform the following steps:

4. In the top right corner click on **profile logo** and then click on **Organization settings**. 

	![Screenshot shows the Workteam settings.](./media/workteam-tutorial/settings.png)

5. Under **AUTHENTICATION** section, click on **Settings logo**.

     ![Screenshot shows the Workteam azure.](./media/workteam-tutorial/azure.png)

6. On the **SAML Settings** page, perform the following steps:

	 ![Screenshot shows the Workteam SAML.](./media/workteam-tutorial/certificate.png)

	a. Select **SAML IdP** as **AD Azure**.

	b. In the **SAML Single Sign-On Service URL** textbox, paste the value of **Login URL**, which you have copied from the Azure portal.

	c. In the **SAML Entity ID** textbox, paste the value of **Azure AD Identifier**, which you have copied from the Azure portal.

	d. In Notepad, open the **base-64 encoded certificate** that you downloaded from the Azure portal, copy its content, and then paste it into the **SAML Signing Certificate (Base64)** box.

	e. Click **OK**.

### Create Workteam test user

To enable Azure AD users to sign in to Workteam, they must be provisioned into Workteam. In Workteam, provisioning is a manual task.

**To provision a user account, perform the following steps:**

1. Sign in to Workteam as a Security Administrator.

2. On the top middle of the **Organization settings** page, click **USERS** and then click **NEW USER**.

	![Screenshot shows the Workteam user.](./media/workteam-tutorial/user.png)

3. On the **New employee** page, perform the following steps:

	![Screenshot shows the Workteam new user.](./media/workteam-tutorial/new-user.png)

	a. In the **Name** text box, enter the first name of user like **B.Simon**.

	b. In **Email** text box, enter the email of user like `B.Simon\@contoso.com`.

	c. Click **OK**.

> [!NOTE]
> Workteam also supports automatic user provisioning, you can find more details [here](./workteam-provisioning-tutorial.md) on how to configure automatic user provisioning.

## Test SSO 

In this section, you test your Azure AD single sign-on configuration with following options. 

#### SP initiated:

* Click on **Test this application** in Azure portal. This will redirect to Workteam Sign on URL where you can initiate the login flow.  

* Go to Workteam Sign-on URL directly and initiate the login flow from there.

#### IDP initiated:

* Click on **Test this application** in Azure portal and you should be automatically signed in to the Workteam for which you set up the SSO. 

You can also use Microsoft My Apps to test the application in any mode. When you click the Workteam tile in the My Apps, if configured in SP mode you would be redirected to the application sign on page for initiating the login flow and if configured in IDP mode, you should be automatically signed in to the Workteam for which you set up the SSO. For more information about the My Apps, see [Introduction to the My Apps](../user-help/my-apps-portal-end-user-access.md).

## Next steps

Once you configure Workteam you can enforce session control, which protects exfiltration and infiltration of your organization’s sensitive data in real time. Session control extends from Conditional Access. [Learn how to enforce session control with Microsoft Defender for Cloud Apps](/cloud-app-security/proxy-deployment-aad).
