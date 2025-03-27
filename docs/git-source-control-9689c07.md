<!-- loio9689c07b64364bbea43725dad9f27320 -->

# Git Source Control

SAP Business Application Studio enables you to connect and interact with the Git source control system, letting you connect and interact with remote Git repositories.

**Prerequisite**

-   Before you can work with the Git view, you or your administrator must establish a connection to your corporate Git system.See [Connect to Your Git Source Control System](https://help.sap.com/docs/bas/sap-business-application-studio/connect-to-your-git-source-control-system?version=Cloud).

-   Ask your administrator which is the recommended authentication method for your company. See [Connect to Your Git Source Control System](https://help.sap.com/docs/bas/sap-business-application-studio/connect-to-your-git-source-control-system?version=Cloud).


You can perform all your Git tasks using the terminal, but SAP Business Application Studio allows you to use the the *SIMPLIFIED GIT* view or the *SOURCE CONTROL* view, if you prefer. See [Using the Simplified Git View](https://help.sap.com/docs/bas/sap-business-application-studio/using-simplified-git-view?version=Cloud&q=Git%20source%20control) and [Using the Advanced Git View](https://help.sap.com/docs/bas/sap-business-application-studio/using-git-view?version=Cloud&q=Git%20source%20control).



<a name="loio9689c07b64364bbea43725dad9f27320__section_bgs_x2d_vnb"/>

## Workflow

Using Git is easy. The basic workflow is as follows:

1.  **Clone:** Clone a repository from a remote Git source control system. All the information about the repository is copied, and a local master branch is created and is visible in your workspace. If the remote repository has several branches, you can create additional local branches based on those remote branches.

2.  **Develop:** Once you have the code, you can develop – add files, delete files, modify files. Your changes are visible. When you are ready, you can stage your changes and commit them.

3.  **Fetch and Merge/Rebase:** \(Optional\) Before sending back your changes to the remote repository, you can fetch all the changes made by others. Then you can merge or rebase the changes into your changes to make sure there are no conflicts. If there are conflicts, you can adjust your code.

4.  **Push:** Add your changes to the remote repository.




<a name="loio9689c07b64364bbea43725dad9f27320__section_rtx_gbt_32c"/>

## Disclaimer

Dev space owners are responsible for maintaining any code cloned from source control systems. Open-source repositories are maintained and supported according to their open-source licenses and documentation.

SAP Business Application Studio supports only specific versions of runtime tools \(such as NPM and Java\). If your code isn't supported by the default dev space configurations, you can either use a [different runtime version](https://help.sap.com/docs/bas/sap-business-application-studio/runtime-version-management) or contact the repository owner to adjust the code.

-   **[Using the Simplified Git View](using-the-simplified-git-view-16eaaa6.md "Use the
		SIMPLIFIED GIT view to perform Git operations and manage Git
		repositories in SAP Business Application
                            Studio.")**  
Use the *SIMPLIFIED GIT* view to perform Git operations and manage Git repositories in SAP Business Application Studio.
-   **[Using the Advanced Git View](using-the-advanced-git-view-265962e.md "General overview of the advanced Git view, the SOURCE CONTROL
		view, in SAP Business Application
                            Studio.")**  
General overview of the advanced Git view, the *SOURCE CONTROL* view, in SAP Business Application Studio.
-   **[Providing Authentication to Git](providing-authentication-to-git-8b1d618.md "You can use Basic or OAuth to authenticate your Git user.")**  
You can use Basic or OAuth to authenticate your Git user.

