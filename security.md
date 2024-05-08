```
How to maintain a secure GitHub repository
```

There are many aspects to building and deploying secure applications. Here are three things to consider:

There's a general knowledge problem: Many developers and other staff members assume they understand security, but they don't. Cybersecurity is a constantly evolving discipline. A program of ongoing education and training is essential.

Code must be created correctly and securely: We need to be sure that the code is created correctly and securely implements the required features. We also need to make sure that the features were designed with security in mind.

Applications must comply with rules and regulations: We need to make sure that the code complies with required rules and regulations. We have to test for compliance while building the code and then retest periodically, even after deployment

# Security tab features

From the Security tab, you can add features to your GitHub workflow to help avoid vulnerabilities in your repository and codebase. These features include:

* Security policies that allow you to specify how to report a security vulnerability in your project by adding a **SECURITY.md** file to your repository.
* Dependabot alerts that notify you when GitHub detects that your repository is using a vulnerable dependency or malware.
* Security advisories that you can use to privately discuss, fix, and publish information about security vulnerabilities in your repository.
* Code scanning that helps you find, triage, and fix vulnerabilities and errors in your code.


1. Communicate a security policy with SECURITY.md
2. GitHub Security Advisories
3. Keep sensitive files out of your repository with .gitignore
4. Remove sensitive data from a repository
5. Branch protection rules
6. Add a CODEOWNERS file

~~~~
A grading script exists under .github/workflows/grading.yml. You don't need to modify this workflow to complete this exercise. Altering the contents in this workflow can break the exercise's ability to validate your actions, provide feedback, or grade the results.
~~~~


# Automated security

Detect and fix outdated dependencies with security vulnerabilities

1. Repository dependency graphs
2. Dependabot alerts: Dependabot scans your repository's dependency manifests and notifies you via pull request whenever a version you rely is marked as insecure.
3. Automated dependency updates with Dependabot
4. Automated code scanning
5. Secret scanning



