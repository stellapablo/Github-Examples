## Branches 
Branches are isolated workspaces where you can develop your work without affecting others in the repository. They allow you to develop features, fix bugs, and safely experiment with new ideas in a contained area of your repository.

# Merging branches
Although having each developer work on a separate branch is great for individual productivity, it opens a new challenge. At some point, each developer's branch needs to be merged into a common branch, like main.

# Pull Request
A pull request is a way to document branch changes and communicate that the changes from the developer’s branch are ready to be merged into the base (main) branch. Pull requests enable stakeholders to review and discuss the proposed changes to ensure that the code quality in the base branch is kept as high as possible.

In order for the two branches to be merged, they must be different from one another:

- The compare branch is the developer’s own branch, which contains the specific changes they made.
- The base branch, also referred to as the main branch, is the branch that the changes need to be merged into.

# Pull request statuses
Now let’s review the different statuses of a pull request.

__Draft pull request__ - When you create a pull request, you can choose to either create a pull request that’s ready for review or a draft pull request. A pull request with a draft status can’t be merged, and code owners aren’t automatically requested to review draft pull requests.

__Open pull request__ - An open status means the pull request is active and not yet merged to the base branch. You can still make commits and discuss and review potential changes with collaborators.

__Closed pull request__ - You can choose to close a pull request without merging it into the base/main branch. This option can be handy if the changes proposed in the branch are no longer needed, or if another solution is proposed in another branch.

__Merged pull request__ - The merged pull request status means that the updates and commits from the compare branch were combined with the base branch. Anyone with push access to the repository can complete the merge.

# Merge a pull request

1. Under your repository name, select Pull requests.
2. In the Pull requests list, select the pull request you'd like to merge.
3. Scroll down to the bottom of the pull request. Depending on the merge options enabled for your repository, you can:
    a. Merge all of the commits into the base branch by selecting the Merge pull request button.
    b. Squash and merge allows you to take all of your commits and combine them into one
    c. The Rebase and merge option allows you to make commits without a merge commit.
4. If prompted, enter a commit message, or accept the default message.
5. If you have more than one email address associated with your account on GitHub.com
6. Select Confirm merge, Confirm squash and merge, or Confirm rebase and merge.
7. Optionally, you can delete the compare branch to keep the list of branches in your repository tidy.

Cada vez que se ejecuta git merge, se crea un merge commit extra. Siempre que trabajes en tu repositorio local, tener demasiados merge commits puede hacer que el historia del commits parezca confuso. Una forma de evitar el merge commit es usar git rebase en su lugar.

# Searching GitHub

1. Global search
2. Context search
3. Using search filters

is:open is:issue assignee:@me   	    Open issues assigned to the current user (@me)
is:closed is:pr author:contoso	        Closed pull requests created by @contoso
is:pr sidebar in:comments	            Pull requests where "sidebar" is mentioned in the comments
is:open is:issue label:bug -linked:pr	Open issues labeled as bugs that do not have a linked pull request

# Git blame?
Despite its ominous name, git blame is a command that displays the commit history for a file. It makes it easy for you to see who made what changes and when

# Cross-linking issues, commits, and more

1. Autolinked references
2. Looping in users with @mention
