GitHub administration

As a GitHub administrator, your goal is to keep everything working smoothly for your users. In this unit, you'll learn about the different levels in the GitHub organizational hierarchy and the administration tasks associated with each level.

Members of a team with team maintainer or repository admin permissions can:

- Create a new team, and select or change the parent team.
- Delete or rename a team.
- Add or remove organization members from a team, or synchronize a GitHub team's membership with an IdP group.
- Add or remove outside collaborators (people who aren't explicitly members of your organization, such as consultants or temporary employees) from team repositories.
- Enable or disable team discussions on the team's page.
- Change the visibility of the team within the organization.
- Manage automatic code review assignment for pull requests, utilizing GitHub's review assignment routing algorithm.
- Schedule reminders.
- Set the team profile picture.

# Best practices for team-level administration

- Create nested teams to reflect your group or company's hierarchy within your GitHub organization.
- Create teams based on interests or specific technology (JavaScript, data science, etc.) to help streamline PR review processes. Individuals can choose to join these teams according to their interests or skills.
- Enable team synchronization between your identity provider (IdP) and GitHub to allow organization owners and team maintainers to connect teams in your organization with IdP groups. When you synchronize a GitHub team with an IdP group, you can replicate changes to GitHub automatically, reducing the need for manual updates and custom scripts. You can use an IdP with team synchronization to manage administrative tasks such as onboarding new members, granting new permissions, and removing member access to the organization.

# Administration at organization level

Members of an organization with the owner permission can perform a wide range of activities at the organization level including:

- Invite users to join the organization and remove members from the organization.
- Organize users into a team, and grant "team maintainer" permissions to organization members.
- Add or remove outside collaborators (people who aren't explicitly members of your organization, such as consultants or temporary employees) to organizational repositories.
- Grant repository permission levels to members, and set the base (default) permission level for a given repository.
- Set up organization security.
- Set up billing or assign a billing manager for the organization.
- Extract various types of information about repositories via the use of custom scripts.
- Apply organization-wide changes such as migrations via the use of custom scripts.

We recommend setting up only one organization for your users and repositories. If specific constraints in your company require you to create multiple organizations

# Administration at enterprise level

Enterprise accounts include GitHub Enterprise Cloud and Enterprise Server instances and enable owners to centrally manage policy and billing for multiple organizations.

At the enterprise level, members of an enterprise with the owner permissions can:

Enable SAML single sign-on for their enterprise account, allowing each enterprise member to link their external identity on your identity provider (IdP) to their existing GitHub account.
Add or remove organizations from the enterprise.
Set up billing or assign a billing manager for all organizations in the enterprise.
Set up repository management policies, project board policies, team policies, and other security settings that apply to all the organizations, repositories, and members in the enterprise.
Extract various types of information about organizations via the use of custom scripts.
Apply enterprise-wide changes such as migrations via the use of custom scripts.


# GitHub's authentication options

- Username and password
- Personal access tokens
- SSH keys
- Deploy keys: GitHub attaches the public part of the key directly to the repository instead of a personal user account, and the private part of the key remains on the user's server. Deploy keys are read-only by default, but you can give them write access when adding them to a repository.


# GitHub's added security options

- Two-factor authentication: Two-factor authentication (2FA), sometimes known as multifactor authentication (MFA), is an extra layer of security used when logging into websites or apps. With 2FA, users have to sign in with their username and password and provide another form of authentication that only they have access to

- SAML SSO: This type of authentication gives organization and enterprise owners on GitHub a way to control and secure access to organization resources like repositories, issues, and pull requests. Organization owners can invite GitHub users to join the organization that uses SAML SSO, which allows those users to contribute to the organization and retain their existing identity and contributions on GitHub.


- LDAP


# How does GitHub organization and permissions work?


In the previous unit, you explored the different ways that users can authenticate themselves with GitHub. In this unit, you'll learn about permissions for each hierarchical level:

1. Repository permissions
2. Team permissions
3. Organization permissions
4. Enterprise permissions

# Repository permission levels
You can customize access to a given repository by assigning permissions. There are five repository-level permissions:

- Read - Recommended for non-code contributors who want to view or discuss your project. This level is good for anyone that needs to view the content within the repository but doesn't need to actually make contributions or changes.
- Triage - Recommended for contributors who need to proactively manage issues and pull requests without write access. This level could be good for some project managers who manage tracking issues but don't make any changes.
- Write - Recommended for contributors who actively push to your project. Write is the standard permission for most developers.
- Maintain - Recommended for project managers who need to manage the repository without access to sensitive or destructive actions.
- Admin - Recommended for people who need full access to the project, including sensitive and destructive actions like managing security or deleting a repository. These people are repository owners and administrators.


# Team permission levels

- Member
- Maintainer

# Organization permission levels

- Owner
- Member
- Moderator
- Billing manager
- Security managers
- Outside collaborator

For improved management and security, you might also consider giving default read permissions to all members of your organization and adjusting their access to repositories on a case-by-case basis

# Enterprise permission levels

- Owner
- Member
- Billing manager

In addition to these three levels, you can also set a policy of default repository permissions across all your organizations:

# Repository security and management

- Create protection rules
- Add a CODEOWNERS file
- View traffic by using Insights
