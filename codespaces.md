```
The Codespace lifecycle
```

GitHub Codespaces is configurable, allowing you to create a customized development environment for your project. By configuring a custom development environment for your project, you can have a repeatable Codespace configuration for all users of your project.

1. Creating a Codespace
2. Rebuilding a Codespace
3. Stoppping a Codespace
4. Deleting a Codespace


```
Create a Codespace
```
https://learn.microsoft.com/en-us/training/github/code-with-github-codespaces/media/codespace-connection-editor.png


You can create a Codespace on GitHub.com, in Visual Studio Code, or by GitHub CLI. There are four ways to create a Codespace:

From a GitHub template or any template repository on GitHub.com to start a new project.
From a branch in your repository for new feature work.
From an open pull request to explore work-in-progress.
From a commit in a repository's history to investigate a bug at a specific point in time.

When you create a GitHub Codespace, four processes occur:

1. VM and storage are assigned to your Codespace.
2. A container is created.
3. A connection to the Codespace is made.
4. A post-creation setup is made.



# Timeouts for a Codespace
The default timeout is after 30 minutes of inactivity. When a Codespace times out, your data is kept from the last time your changes were saved.


# Close or stop a Codespace
If you exit the Codespace without running the stop command (for example, by closing the browser tab) or leave the Codespace running without interaction, the Codespace and its running processes continue during the inactivity timeout period. The default inactivity timeout period is 30 minutes.

# Rebuild a Codespace
You can rebuild your Codespace to implement changes to your dev container configuration. For most uses, you can create a new Codespace as an alternative to rebuilding a Codespace. When you rebuild your Codespace, images from the cache speed-up the rebuild process. You can also perform a full rebuild to clear the cache and rebuild the container with fresh images.


# Delete a Codespace
You can create a Codespace for a particular task. After you push your changes to a remote branch, then you can safely delete that Codespace.


