---
title: Authenticating with AAD SSO for Teams
description: Authentication in Teams apps using AAD SSO
ms.topic: conceptual
ms.localizationpriority: medium
keywords: teams authentication SSO Microsoft Azure Active Directory (Azure AD), OIDC, username, password
---
# Authenticate with AAD SSO

Azure Active Directory (Azure AD) is a cloud-based identity and access management service. It helps your app users access external resources, such as Microsoft 365, the Azure portal, and thousands of other SaaS applications. Your users can also access internal resources, such as apps on your corporate network and intranet, along with any cloud apps from your own organization.

Use Azure AD as a standards-based approach for adding single sign-on (SSO) to your app. SSO is an authentication method that lets users sign in using one set of credentials to multiple independent software systems. Using SSO means a user doesn't have to sign in to every application they use. With SSO, users can access all needed applications without being required to authenticate using different credentials.

## AAD SSO for Teams

You can use AAD SSO to implement authentication for your Teams app users. When you register your Teams app with AAD, it becomes the main identity provider (IdP) for validating access to Azure-based systems and applications.

Some prerequisites for implementing authentication with AAD SSO are:

- **Create a Teams app**: Your Teams app can have single or multiple capabilities, such as tabs, bots, messaging extensions, and more. Teams offers a different UI and UX experience for each feature. It makes your Teams app fully compatible with AAD SSO functionality irrespective of its features.
- **Register your app with AAD**: Establish a trust relationship between AAD and your Teams app. AAD serves as an IdP for your app users and will be able to authenticate them. To register your app, provide app ID, configure access permissions, and define scope for user access on the Azure portal.
- **Register users with AAD**: All valid app users are registered with AAD. Users registered with AAD will get authenticated. After first successful sign in, they don't need to log in again. They can access all Azure resources and subsystems.
