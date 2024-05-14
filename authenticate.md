# Organization management through SAML SSO

You need to configure SAML SSO for a GitHub organization with the IdP you're using. If you have specific questions on how to implement SAML SSO with your chosen IdP, you can find details in the documentation for each supported IdP. Here's a list of the SAML IdPs that GitHub currently supports:

- Active Directory Federation Services (AD FS)
- Microsoft Entra ID
- Okta
- OneLogin
- PingOne
- Shibboleth

# Authentication with SAML SSO

- Before enabling SAML SSO with your GitHub Enterprise, an Administrator needs to connect the GitHub organization to a supported IdP.
- Next, when a member accesses resources within an organization that uses SAML SSO, GitHub redirects the member to the IdP to authenticate.
- After successful authentication, the IdP redirects the member back to GitHub, where the member can access the organization's resources. The result means that even after configuring SAML SSO, the GitHub organization's members will continue to be prompted to log into their user accounts on GitHub.

Enforce SAML SSO for your organization:  Under SAML single sign-on, select Require SAML SSO authentication for all members of the organization.

# Multifactor authentication or 2FA
Two-factor authentication is an extra level of security available to GitHub Enterprise accounts. With 2FA, a member in your organization is required to log in with username and password, and also provide a secondary form of authentication

## Options to identify with 2FA

## Security keys
With security keys, your enterprise can achieve a higher level of user security and protection. With two-factor authentication enabled, security keys provide a strong, convenient, and phishing-proof option for 2FA

## TOTP
GitHub recommends using a cloud-based TOTP app to configure 2FA. TOTP applications are more reliable than SMS, especially for locations outside the United States. TOTP apps support the secure backing up your authentication codes in the cloud, and can be restored if you lose access to your devic

## SMS
If your users aren't able to authenticate using a TOTP mobile app, they can authenticate using SMS messages. This form of 2FA relies on the assumption that the user is the only person with access to their mobile devic

# Audit 2FA for user compliance
You can review which organization owners, members, and outside collaborators have enabled two-factor authentication by navigating to the right corner of GitHub.com, clicking your profile photo, selecting Your organizations, then selecting the name of the chosen organization. Under the organization name, select the People tab and select the 2FA option. From here, you can see which members in the organization have enabled 2FA, and which outside contributors have it enabled.

# User authorization

## Authorization with SAML SSO through SCIM
SAML single sign-on (SSO) gives organization owners and enterprise owners on GitHub a way to control and secure access to organization resources like repositories, issues, and pull requests. SCIM was developed to allow synchronization of information between an IdP and multiple applications.

If you use SAML SSO without implementing SCIM, you won't have automatic deprovisioning.

## SSH key and PAT with SAML SSO
SCIM and SAML SSO also have security benefits. 

# Connect your IdP to your organization
To use SAML single sign-on and SCIM, you must connect your identity provider to your GitHub organization. When you enable SAML SSO for your GitHub organization, you connect your identity provider to your organization. Keep in mind that not all SAML identity providers are currently supported by GitHub for SCIM. Following is a list of the GitHub supported identity providers for SCIM:

- Microsoft Entra ID
- Okta
- OneLogin
- If your support request is outside of the scope of what our team can help you with, we might recommend next steps to resolve your issue outside of GitHub Support. Your support request is possibly out of GitHub Support's scope if the request is primarily about:

- Third-party integrations
- Hardware setup
- CI/CD, such as Jenkins
- Writing scripts
- Configuration of external authentication systems, such as SAML identity providers
- Open-source projects


## Team synchronization
If your company is using Microsoft Entra ID or Okta as your IdP for your enterprise in GitHub's cloud, you can use team synchronization to manage team membership within each organization through IdP groups. This feature reduces the need for manual updates and custom scripts. You can centrally manage users' identities, allowing authorization, review, and revocation of permissions.

## Enterprise Managed Users
Team synchronization is also available for organizations and enterprise accounts that use GitHub Enterprise Cloud. Enterprise Managed Users is a feature of GitHub Enterprise Cloud that provides even greater control over enterprise members and resources.

##
Usage limits
When using the team synchronization feature, there are specific usage limits you need to know about. Exceeding these limits can lead to unexpected performance, and might cause synchronization failures.

__Maximum number of members in a GitHub team: 5,000__
__Maximum number of members in a GitHub organization: 10,000__
__Maximum number of teams in a GitHub organization: 1,500__

## Enable team synchronization
With team synchronization, you can use your IdP to manage administrative tasks like onboarding new members, granting new permissions in your organization, and removing member access. When you synchronize a GitHub team with an IdP group, changes made to the IdP group are reflected on GitHub automatically, reducing the need for manual updates and custom scripts

You can enable and use team synchronization, but only with the following supported IdPs:

- Microsoft Entra ID: To enable team synchronization for Microsoft Entra ID, the installation needs the following permissions: read all users' full profiles, sign in and read user profile, and read directory data.

    1. Read all users’ full profiles
    2. Sign in and read user profiles
    3. Read directory data

- Okta

    1. Enable SAML SSO and SCIM for your organization using Okta.
    2. Provide the tenant URL for your Okta instance.
    3. Generate a valid SSWS token with read-only admin permissions for your Okta installation as a service user.




