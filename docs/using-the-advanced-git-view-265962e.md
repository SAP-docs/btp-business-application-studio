<!-- loio265962e20eee43f499516de9011ac2e3 -->

# Using the Advanced Git View

General overview of the advanced Git view, the *SOURCE CONTROL* view, in SAP Business Application Studio.

SAP Business Application Studio provides a graphical user interface for executing Git commands and managing your source control and versioning. You can also manually perform other Git commands from the terminal. This view contains all the options for Git source control.



<a name="loio265962e20eee43f499516de9011ac2e3__section_wlx_4kf_zlb"/>

## Source Control View

To open the *SOURCE CONTROL* view, click ![Open Source Control view](images/Open_Source_Control_view_abdab3a.png) from the activity bar.

![Source Control View](images/Git_View_df291d4.png)

The *SOURCE CONTROL* view is divided into the following sections:

*SOURCE CONTROL* view menu

![](images/source_control_GIT_menu_e10ab7d.png)

-   Click ![Toggle](images/toggle_icon_e7e5e6d.png) to toggle between list and tree views.
-   Click ![commit changes](images/commit_icon_5792efe.png) \(or press [<Ctrl\>\] + [<Enter\>\] \) to commit the changes.
-   Click ![Refresh](images/Git_refresh_5d003be.png) to refresh the Git pane.
-   Click ![Git history](images/Git_history_8341762.png) to view the Git history.
-   Click ![more actions](images/more_actions_new_ab37e83.png) to see more available actions. See [Git Commands](git-commands-5914548.md)

*Message* section

Enter a description for the commit.

*Staged Changes* section

Shows the files that will be included in the next commit.

![Staged Changes section](images/staged_changes_539d922.png)

Hover over the section title to see additional actions.

-   Click ![](images/unstage_changes_icon_684e1d1.png) to unstage all files in the section.

Hover over the files in this section to see additional actions:

-   Click ![](images/unstage_changes_icon_684e1d1.png) to unstage the changes in the file.
-   Click ![open file](images/Git_open_file_787f08b.png) to open the file.

*Changes* section

Shows the files that contain changes.

![Changes section](images/changes_section_d55c5f1.png)

Hover over the section title to see additional actions.

-   Click ![discard changes](images/Discard_changes_954f1c8.png) to discard all changes.
-   Click ![stage all changes](images/Git_Stage_changes_icon_67e32ee.png) to stage all changes.

Hover over the files in this section to see additional actions:

-   Click ![discard changes](images/Discard_changes_954f1c8.png) to discard the changes in the file.
-   Click ![open file](images/Git_open_file_787f08b.png) to open the file.
-   Click ![stage changes](images/Git_Stage_changes_icon_67e32ee.png) to stage the changes in the file.

*Amend* section.

Click *Amend* at the bottom of the pane to make changes to a commit.



<a name="loio265962e20eee43f499516de9011ac2e3__section_rqf_jtf_zlb"/>

## Git Status Bar

At the bottom-left corner of SAP Business Application Studio, you can find indicators describing the status of your Git repository. They show the current branch, dirty indicators, and the number of ahead and behind changes of the current branch.

![Git status bar](images/Git_status_bar_cd1ee90.png)

The dirty indicators are as follows:

*\**: You have unstaged changes in your branch.

*\+*: You have staged changes in your branch, but no unstaged changes.

*!*: You have conflicting changes in your branch.

Clicking on the branch name, opens the command palette showing additional Git commands.

There is also a *Synchronize Changes* action in the status bar, next to the branch indicator, if the currently checked-out branch has an upstream branch configured. Clicking *Synchronize Changes* opens the command palette showing additional Git commands that can be applied to the branch.



<a name="loio265962e20eee43f499516de9011ac2e3__section_gl5_q1g_zlb"/>

## Branches

You can create and check out branches directly within the IDE by using the `Git: Checkout` command in the command palette.

To create a new branch:

1.  Click on the active branch name in the status bar. The command palette opens.
2.  Enter a name for the new branch. A new branch is created and checked out.



<a name="loio265962e20eee43f499516de9011ac2e3__section_trx_bbg_zlb"/>

## Gutter Indicators

If you open a folder that is a Git repository and begin making changes, annotations are added to the gutter and to the overview ruler.

-   A red triangle indicates where lines have been deleted.

-   A green bar indicates new added lines.

-   A blue bar indicates modified lines.


-   **[Connecting an Existing Project to Git](connecting-an-existing-project-to-git-0930e56.md "You can add an existing project to Git.")**  
You can add an existing project to Git.
-   **[Understanding the UI](understanding-the-ui-d14646a.md "SAP Business Application Studio provides a
		graphical user interface for executing Git commands and managing your source control and
		versioning. ")**  
SAP Business Application Studio provides a graphical user interface for executing Git commands and managing your source control and versioning.
-   **[Git Commands](git-commands-5914548.md "SAP Business Application Studio supports Git
		commands from the Git view and from the command palette.")**  
SAP Business Application Studio supports Git commands from the Git view and from the command palette.
-   **[Setting Up Git to Work with Gerrit](setting-up-git-to-work-with-gerrit-82a5dfe.md "Gerrit is a web-based software code review tool for reviewing, approving, or
		rejecting changes to the source code developed by your colleagues. Gerrit works as an
		intermediate environment for source control between the local environment and the remote Git
		repository.")**  
Gerrit is a web-based software code review tool for reviewing, approving, or rejecting changes to the source code developed by your colleagues. Gerrit works as an intermediate environment for source control between the local environment and the remote Git repository.

