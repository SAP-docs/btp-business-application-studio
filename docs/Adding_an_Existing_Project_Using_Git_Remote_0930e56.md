<!-- loio0930e56885944a2dbef1bc98ac12b4f0 -->

# Adding an Existing Project Using Git Remote

You can use the terminal to add an existing project to your Git Remote so that you can continue working on it in SAP Business Application Studio.

1.  Change the current working directory to your local project.

2.  Set the Git committer.

    ```
    $ git config --global user.email "<your email>" 
    $ git config --global user.name "<your user name>" 
    ```

3.  Initialize the local directory as a Git repository.

    ```
    $ git init
    ```

4.  Add the files in your new local repository. This stages them for the first commit.

    ```
    $ git add .
    ```

5.  Commit the files that you've staged in your local repository.

    ```
    $ git commit -m "First commit"
    ```

6.  Create a new `Main` branch.

    > ### Note:  
    > The name of the branch was changed from `Master` to `Main`.

    ```
    $ git branch -M main
    ```

7.  In the Command prompt, add the URL for the remote repository where your local repository will be pushed.

    ```
    $ git remote add origin https://<Git-Host-URL>/<full-path-to-repository>
    ```

8.  Push the changes in your local repository to Git.

    ```
    $ git push origin main
    ```


