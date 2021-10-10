<!-- loioa47db8bde00647cdb0ea2b06737ad14a -->

# Connecting to a Public Git Repository

Using SAP Business Application Studio, can connect to all public git services, such as GitHub, GitLab, and GitBucket.



<a name="loioa47db8bde00647cdb0ea2b06737ad14a__section_rml_hxl_tnb"/>

## Providing Authentication

SAP Business Application Studio supports the following authentication methods. Once you have enabled one of these methods, you will not have to enter your credentials every time you use Git.

-   ****Basic authentication**** - Access your Git provider using your username and password.

    To work with the Git view in SAP Business Application Studio, you need to store or cache credentials.

    > ### Note:  
    > Doing this requires you to entrust your credentials to SAP and to a third party.

    -   Cache credentials in memory for a short period of time. See [Git Credential Cache](https://git-scm.com/docs/git-credential-cache).

    -   Store credentials indefinitely in a file on your dev space. See [Git Credential Store](https://git-scm.com/docs/git-credential-store).

    You can use a **Personal Access Token** \(PAT\) instead of a password.

    For example, you can create a PAT in GitHub following [these instructions](http://help.sap.com/disclaimer?site=https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token). Other Git providers will have different ways of creating PATs.

-   **SSH** - SSH \(Secure Shell\) keys are used for managing networks, operating systems, and configurations. The ssh command provides a secure encrypted connection between two hosts over a network.



<a name="loioa47db8bde00647cdb0ea2b06737ad14a__section_ysr_hxl_tnb"/>

## Connecting to Git

In SAP Business Application Studio, public Git works out-of-the-box.

You can start by cloning a project to your local workspace. See [Cloning Repositories](Cloning_Repositories_7a68bfa.md).



<a name="loioa47db8bde00647cdb0ea2b06737ad14a__section_wtl_mbm_tnb"/>

## Using Git

Learn how to use Git in the SAP Business Application Studio Developer Guide. See [Git Source Control](Git_Source_Control_9689c07.md).

