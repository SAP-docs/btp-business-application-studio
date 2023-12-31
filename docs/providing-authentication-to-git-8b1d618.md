<!-- loio8b1d618335c64c3aba207084e6254f86 -->

# Providing Authentication to Git

You can use Basic or OAuth to authenticate your Git user.



<a name="loio8b1d618335c64c3aba207084e6254f86__section_rml_hxl_tnb"/>

## Providing Basic Authentication

SAP Business Application Studio supports basic authentication, which means you must provide your username and password to access your Git provider.

> ### Note:  
> SSH is not available for on-premise Git installations.

To work with the Git view in SAP Business Application Studio, you need to store or cache credentials. Once you have enabled one of these methods, you will not have to enter your credentials every time you use Git.

> ### Note:  
> Doing this requires you to entrust your credentials to SAP and to a third party.

-   Cache credentials in memory for a short period of time. See [Git Credential Cache](https://git-scm.com/docs/git-credential-cache).

-   Store credentials indefinitely in a file on your dev space. See [Git Credential Store](https://git-scm.com/docs/git-credential-store).


If it's supported, it's recommended to use a **Personal Access Token** \(PAT\) instead of a password.

For example, you can create a PAT in GitHub following [these instructions](http://help.sap.com/disclaimer?site=https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token). Other Git providers will have different ways of creating PATs.

> ### Note:  
> PATs are an alternative to using passwords for authentication to Git, and as such, they should be frequently renewed.



<a name="loio8b1d618335c64c3aba207084e6254f86__section_qqy_zgs_gzb"/>

## Providing OAuth Authentication to GitHub

In SAP Business Application Studio, when connecting to GitHub, a popup appears with an verification code you can use to set up OAuth authentication.

1.  When the popup with the code appears, click *Copy the code and open GitHub*. A new tab with GitHub opens.

2.  Log in to GitHub, and paste the code obtained before.

3.  Authorize the code.

4.  Back in SAP Business Application Studio, select if you want to save your user authentication per session or per dev space.


> ### Note:  
> You can configure these settings for your user authentication in the Preferences page:
> 
> -   `sapbas.git.github.oauth`: Enables or disables OAuth authentication for [Github.com](https://github.com/).
> 
> -   `sapbas.git.github.enterprise.oauth`: If your administrator has not configured a destination for your subaccount, you can define a host/client ID.

