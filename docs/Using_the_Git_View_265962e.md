<!-- loio265962e20eee43f499516de9011ac2e3 -->

# Using the Git View

General overview of the Git view in SAP Business Application Studio.

SAP Business Application Studio provides a graphical user interface for executing Git commands and managing your source control and versioning. You can also manually perform other Git commands from the terminal.



<a name="loio265962e20eee43f499516de9011ac2e3__section_wlx_4kf_zlb"/>

## Git View

To open the Git view, click ![](images/Open_Git_pane_7c27a9f.png) from the left side-menu.

![](images/Git_view_44295cf.jpg)

The Git view is divided into the following sections:

*SOURE CONTROL: GIT* view menu

![](images/source_control_GIT_menu_e10ab7d.png) 

-   Click ![](images/toggle_icon_e7e5e6d.png) to toggle between list and tree views.
-   Click ![](images/commit_icon_5792efe.png) \(or press  [<Ctrl\>\] + [<Enter\>\] \) or to commit the changes.
-   Click ![](images/refresh_icon_new_baea6eb.png) to refresh the Git pane.
-   Click ![](images/sign_off_2702bdd.png) to add your name to the commit.
-   Click ![](images/more_actions_new_ab37e83.png) to see more available actions. See [Git Commands](Git_Commands_5914548.md)

 *Message* section

Enter a description for the commit.

*STAGED CHANGES* section

Shows the files that will be included in the next commit.

![](images/staged_changes_menu_89ea9de.png)

Hover over the section title to see additional actions.

-   Click ![](images/unstage_changes_icon_684e1d1.png) to unstage all files in the section.

Hover over the files in this section to see additional actions:

-   Click ![](images/unstage_changes_icon_684e1d1.png) to unstage the changes in the file.
-   Click ![](images/open_file_icon_2380fb5.png) to open the file.

*CHANGES* section

Shows the files that contain changes.

![](images/changes_menu_da6cd19.png)

Hover over the section title to see additional actions.

-   Click ![](images/discard_changes_icon_b9f9b23.png) to discard all changes.
-   Click ![](images/stage_changes_icon_10076b2.png) to stage all changes.

Hover over the files in this section to see additional actions:

-   Click ![](images/discard_changes_icon_b9f9b23.png) to discard the changes in the file.
-   Click ![](images/open_file_icon_2380fb5.png) to open the file.
-   Click ![](images/stage_changes_icon_10076b2.png) to stage the changes in the file.

*Amend* section.

Click *Amend* at the bottom of the pane to make changes to a commit.



<a name="loio265962e20eee43f499516de9011ac2e3__section_rqf_jtf_zlb"/>

## Git Status Bar

At the bottom-left corner of SAP Business Application Studio, you can find indicators describing the status of your Git repository. They show the current branch, dirty indicators, and the number of ahead and behind changes of the current branch.

![](images/Git_Status_Bar_a3be78e.png)

The dirty indicators are as follows:

*\**: You have unstaged changes in your branch.

*+*: You have staged changes in your branch, but no unstaged changes.

*!*: You have conflicting changes in your branch.

Clicking on the branch name, opens the command palette showing additional Git commands.

There is also a *Synchronize Changes* action in the status bar, next to the branch indicator, if the currently checked-out branch has an upstream branch configured. Clicking *Synchronize Changes* opens the command palette showing additional Git commands that can be applied to the branch.



<a name="loio265962e20eee43f499516de9011ac2e3__section_gl5_q1g_zlb"/>

## Branches

You can create and check out branches directly within the IDE by using the ***Git: Checkout*** command in the command palette.

To create a new branch:

1.  Click on the active branch name in the status bar. The command palette opens.
2.  Enter a name for the new branch. A new branch is created and checked out.



<a name="loio265962e20eee43f499516de9011ac2e3__section_trx_bbg_zlb"/>

## Gutter Indicators

If you open a folder that is a Git repository and begin making changes, annotations are added to the gutter and to the overview ruler.

-   A red triangle indicates where lines have been deleted.

-   A green bar indicates new added lines.

-   A blue bar indicates modified lines.


-   **[Git Commands](Git_Commands_5914548.md "SAP Business Application Studio supports Git
		commands from the Git view and from the command palette.")**  
SAP Business Application Studio supports Git commands from the Git view and from the command palette.

