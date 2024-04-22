```
Administration at team level
```
In GitHub, each user is an organization member that you can add to a team. You can create teams in your organization with cascading access permissions and mentions to reflect your company or group's structure. Teams are useful for refining repository permissions on a more granular level and enabling communication and notification between team members.

Additionally, GitHub allows you to sync your teams with identity provider (IdP) groups such as Microsoft Entra ID. When you synchronize a GitHub team with Microsoft Entra ID, you can replicate changes to GitHub automatically, which reduces the need for manual updates and custom scripts. You can use Microsoft Entra ID with team synchronization to manage administrative tasks such as onboarding new members, granting new permissions, and removing member access to the organization.

Members of a team with team maintainer or repository admin permissions can:

Create a new team, and select or change the parent team.
Delete or rename a team.
Add or remove organization members from a team, or synchronize a GitHub team's membership with an IdP group.
Add or remove outside collaborators (people who aren't explicitly members of your organization, such as consultants or temporary employees) from team repositories.
Enable or disable team discussions on the team's page.
Change the visibility of the team within the organization.
Manage automatic code review assignment for pull requests, utilizing GitHub's review assignment routing algorithm.
Schedule reminders.
Set the team profile picture.

```
Administration at organization level
```

In GitHub, organizations are shared spaces enabling users to collaborate across many projects at once. Owners and administrators can manage member access to the organization's data and repositories with sophisticated security and administrative features.

Members of an organization with the owner permission can perform a wide range of activities at the organization level including:

- Invite users to join the organization and remove members from the organization.
- Organize users into a team, and grant "team maintainer" permissions to organization members.
- Add or remove outside collaborators (people who aren't explicitly members of your organization, such as consultants or temporary employees) to organizational repositories.
- Grant repository permission levels to members, and set the base (default) permission level for a given repository.
- Set up organization security.
- Set up billing or assign a billing manager for the organization.
- Extract various types of information about repositories via the use of custom scripts.
- Apply organization-wide changes such as migrations via the use of custom scripts.

```
Administration at organization level
```

Enterprise accounts include GitHub Enterprise Cloud and Enterprise Server instances and enable owners to centrally manage policy and billing for multiple organizations.

At the enterprise level, members of an enterprise with the owner permissions can:

Enable SAML single sign-on for their enterprise account, allowing each enterprise member to link their external identity on your identity provider (IdP) to their existing GitHub account.
Add or remove organizations from the enterprise.
Set up billing or assign a billing manager for all organizations in the enterprise.
Set up repository management policies, project board policies, team policies, and other security settings that apply to all the organizations, repositories, and members in the enterprise.
Extract various types of information about organizations via the use of custom scripts.
Apply enterprise-wide changes such as migrations via the use of custom scripts.




```
GitHub's authentication options
```
1. Username and password
2. Personal access tokens
3. SSH keys
4. Deploy keys

Deploy keys are another type of SSH key in GitHub that grants a user access to a single repository. GitHub attaches the public part of the key directly to the repository instead of a personal user account, and the private part of the key remains on the user's server. Deploy keys are read-only by default, but you can give them write access when adding them to a repository.

5. GitHub's added security options

a. Two-factor authentication
b. SAML SSO

    Active Directory Federation Services (AD FS)
    Microsoft Entra ID
    Okta
    OneLogin
    PingOne

c. LDAP: GitHub Enterprise Server integrates with popular LDAP services like:

    Active Directory
    Oracle Directory Server Enterprise Edition
    OpenLDAP
    Open Directory

```
Repository permission levels
```

You can customize access to a given repository by assigning permissions. There are five repository-level permissions:

Read - Recommended for non-code contributors who want to view or discuss your project. This level is good for anyone that needs to view the content within the repository but doesn't need to actually make contributions or changes.
Triage - Recommended for contributors who need to proactively manage issues and pull requests without write access. This level could be good for some project managers who manage tracking issues but don't make any changes.
Write - Recommended for contributors who actively push to your project. Write is the standard permission for most developers.
Maintain - Recommended for project managers who need to manage the repository without access to sensitive or destructive actions.
Admin - Recommended for people who need full access to the project, including sensitive and destructive actions like managing security or deleting a repository. These people are repository owners and administrators.

```
Team permission levels
```

Member:	Team members have the same set of abilities as organization members
Maintainer	Team maintainers can do everything team members can, plus:
- Change the team's name, description, and visibility
- Request that the team change parent and child teams
- Set the team profile picture
- Edit and delete team discussions
- Add and remove organization members from the team
- Promote team members to also have the team maintainer permission
- Remove the team's access to repositories
- Manage code review assignment for the team
- Manage scheduled reminders for pull requests

```
Organization permission levels
```

Owner:	Organization owners can do everything that organization members can do, and they can add or remove other users to and from the organization. This role should be limited to no less than two people in your organization.

Member:	Organization members can create and manage organization repositories and teams.
Moderator:	Organization moderators can block and unblock nonmember contributors, set interaction limits, and hide comments in public repositories that the organization owns.
Billing manager:	Organization billing managers can view and edit billing information.
Security managers:	Organization security managers can manage security alerts and settings across your organization. They can also read permissions for all repositories in the organization.
Outside collaborator:	Outside collaborators, such as a consultant or temporary employee, can access one or more organization repositories. They aren't explicit members of the organization.

In addition to these levels, you can also set default permissions for all members of your organization:

```
Enterprise permission levels
```

Owner: Enterprise owners have complete control over the enterprise and can take every action, including:
- Managing administrators
- Adding and removing organizations to and from the enterprise
- Managing enterprise settings
- Enforcing policies across organizations
- Managing billing settings
Member: Enterprise members have the same set of abilities as organization members
Billing manager: Enterprise billing managers can only view and edit your enterprise's billing information and add or remove other billing managers

```
Repository security and management
```
You can oversee the security and management of your repositories in several ways.

1. Create protection rules

To manage changes to content within your repository, you can create branch protection rules to enforce certain workflows for one or more branches. Protection rules that can be applied to a branch include:

- Require a pull request before merging.
- Require status checks to pass before merging.
- Require conversation resolution before merging.
- Require signed commits.
- Require linear history.
- Require merge queue.
- Require deployments to succeed before merging.
- Lock the branch by making it read-only.
- Restrict who can push to matching branches.

2. Add a CODEOWNERS file
3. View traffic by using Insights

