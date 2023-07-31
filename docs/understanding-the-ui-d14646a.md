<!-- loiod14646ada3a24483b5a47265a8242140 -->

# Understanding the UI

SAP Business Application Studio provides a graphical user interface for executing Git commands and managing your source control and versioning.



<a name="loiod14646ada3a24483b5a47265a8242140__section_svy_5cn_23b"/>

## Understanding the UI

The Git view consists of three major sections. The top section is for authoring the commit messages. It also provides access to a couple of basic Git commands.

![Git view](images/Git_top_section_4e8ae13.png)

Below this, you find the commit section, which lists the changed files by their name and separates them in two groups:

-   *Staged Changes* - A list of the files that have been staged. Click ![Open file icon](images/Git_open_file_787f08b.png) to open the selected file, or ![Unstage icon](images/Git_Unstage_ed68173.png) to unstage it.

    ![Staged changes section](images/staged_changes_bac6983.png)

-   *Changes* - Files listed under the *Changes* section contain unstaged changes. Each file name is followed by a path to its parent directory and an indicator describing the status of the change.

    Click ![Open file icon](images/Git_open_file_787f08b.png) to open the selected file, ![Stage file icon](images/Git_Stage_changes_icon_67e32ee.png) to stage the file, or ![Refresh icon](images/Git_refresh_5d003be.png) to refresh it.

    ![Git Changes section](images/Git_Changes_section_0b3f741.png)


The files can be in any of the following statuses:

-   *A* - A new file that has been staged.
-   *U* - An unstaged file. An unstaged change can be reverted by clicking on the *Discard Changes* action next to the file location.
-   *M* - A modified file. Double-clicking on a modified file will open it in a diff editor. The read-only editor on the left-hand side shows the state from the index. The right-hand side of the editor reflects the state of the working tree, and it lets you to further modify the file.
-   *C* - A copied file \(if blue\) or a conflicted file \(if red\).
-   *D* - A deleted file.

At the bottom of the Git view you can see the last commit section, where a description of the most recent commit is displayed.

After staging the desired files and specifying the commit message, the changes can be committed to the repository. After a successful commit, the Last Commit section is automatically updated.

