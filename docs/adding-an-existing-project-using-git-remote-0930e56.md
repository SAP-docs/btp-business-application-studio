<!-- loio0930e56885944a2dbef1bc98ac12b4f0 -->

# Adding an Existing Project Using Git Remote

You can add an existing project to your Git Remote so that you can continue working on it in SAP Business Application Studio.

1.  In the Project Explorer, select you project.
2.  Click ![](images/Open_Git_pane_7c27a9f.png) from the left side-menu to open the Git view.
3.  Click ![](images/stage_changes_icon_10076b2.png) to initialize the local repository.

    ![](images/git_init_c09cf66.png)

4.  Click ![](images/stage_changes_icon_10076b2.png) in the *CHANGES* section to add the files in your new local repository. This stages them for the first commit.

    ![](images/changes_menu_da6cd19.png)

5.  Click ![](images/commit_icon_5792efe.png) \(or press  [<Ctrl\>\] + [<Enter\>\] \) to commit the files that you've staged in your local repository.

    ![](images/Commit_all_changes_6e4b257.png)

6.  When prompted, provide a commit message.
7.  Click ![](images/more_actions_new_ab37e83.png) to see more available actions.
8.  Select *Remote* \> *Add Remote*.
9.  When prompted, add the URL for the remote repository where your local repository will be pushed.
10. Push the changes in your local repository to the remote Git repository. See [Push Changes](push-changes-c1d3584.md).

