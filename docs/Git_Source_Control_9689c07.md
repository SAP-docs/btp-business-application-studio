<!-- loio9689c07b64364bbea43725dad9f27320 -->

# Git Source Control

SAP Business Application Studio enables you to connect and interact with the Git source control system, letting you connect and interact with remote Git repositories.

**Prerequisite**

-   Before you can work with the Git view, your administrator must establish a connection to your corporate Git system. See [Connect to Your Git Source Control System](Connect_to_Your_Git_Source_Control_System_e7a42bc.md).

-   Ask your administrator which is the recommended authentication method for your company. See [Connect to Your Git Source Control System](Connect_to_Your_Git_Source_Control_System_e7a42bc.md).


You can perform all your Git tasks using the terminal, but SAP Business Application Studio allows you to use the Git view if you prefer.



<a name="loio9689c07b64364bbea43725dad9f27320__section_bgs_x2d_vnb"/>

## Workflow

Using Git is easy. The basic workflow is as follows:

1.  **Clone:** Clone a repository from a remote Git source control system. All the information about the repository is copied, and a local master branch is created and is visible in your workspace. If the remote repository has several branches, you can create additional local branches based on those remote branches.

2.  **Develop:** Once you have the code, you can develop – add files, delete files, modify files. Your changes are visible in the status table of the *Git* pane. When you are ready, you can stage your changes and commit them.

3.  **Fetch and Merge/Rebase:** \(Optional\) Before sending back your changes to the remote repository, you can fetch all the changes made by others. Then you can merge or rebase the changes into your changes to make sure there are no conflicts. If there are conflicts, you can adjust your code.

4.  **Push:** Add your changes to the remote repository.


-   **[Adding an Existing Project Using Git Remote](Adding_an_Existing_Project_Using_Git_Remote_0930e56.md "You can use the terminal to add an existing project to your Git Remote so that you can
		continue working on it in SAP Business Application Studio.")**  
You can use the terminal to add an existing project to your Git Remote so that you can continue working on it in SAP Business Application Studio.
-   **[Understanding the UI](Understanding_the_UI_d14646a.md "SAP Business Application Studio provides a
		graphical user interface for executing Git commands and managing your source control and
		versioning. ")**  
SAP Business Application Studio provides a graphical user interface for executing Git commands and managing your source control and versioning.
-   **[Using the Git View](Using_the_Git_View_265962e.md "General overview of the Git view in SAP Business Application Studio.")**  
General overview of the Git view in SAP Business Application Studio.

**Related Information**  


[Cloning Repositories](Cloning_Repositories_7a68bfa.md "Add an existing project to your local workpace by cloning its repository from Git.")

[Adding an Existing Project Using Git Remote](Adding_an_Existing_Project_Using_Git_Remote_0930e56.md "You can use the terminal to add an existing project to your Git Remote so that you can continue working on it in SAP Business Application Studio.")

[Using the Git View](Using_the_Git_View_265962e.md "General overview of the Git view in SAP Business Application Studio.")

[Connect to Your Git Source Control System](Connect_to_Your_Git_Source_Control_System_e7a42bc.md "SAP Business Application Studio allows you to connect to public and corporate repositories.")

[Connecting to a Corporate Git Repository](Connecting_to_a_Corporate_Git_Repository_d54ddfc.md "As an administrator, you can work with on premise Git repositories once an appropriate destination has been created in your subaccount.")

[Connecting to a Public Git Repository](Connecting_to_a_Public_Git_Repository_a47db8b.md "Using SAP Business Application Studio, can connect to all public git services, such as GitHub, GitLab, and Gitbucket.")

[Troubleshooting](Troubleshooting_73e1a38.md "")

