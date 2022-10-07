<!-- loioad40d52d0bea4d79baaf9626509caf33 -->

# Working in the Dev Space Manager

You can create, delete, stop, and start dev spaces. You can also download dev space content, and import dev space content.



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_bpd_nst_njb"/>

## Create a Dev Space

You can generate a dev space to create and manage applications. You can select the application type that includes the extensions that you need to do a development task.

1.  Open SAP Business Application Studio and log in with your credentials.
2.  Click *Create Dev Space*.
3.  Enter a name for the dev space.
4.  Select the relevant application type.
5.  \(Optional\) Select the relevant additional extensions to enhance your space.

    You can also add or remove extensions later. See the [Add Extensions to Your Dev Space](working-in-the-dev-space-manager-ad40d52.md#loioad40d52d0bea4d79baaf9626509caf33__section_s2p_4ts_fnb) section.

6.  Click *Create Dev Space*.

    > ### Note:  
    > You can only click the button if you entered a dev space name.


> ### Note:  
> Dev Space creation is influenced by the application plan you are using.
> 
> -   If you are using a productive account, see SAP Business Application Studio [Restrictions](restrictions-76db362.md).
> 
> -   If you are using a free account, see [Free Plan Restrictions](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/2c72917df87e47c290e061a556d92398.html/#free-plan-restrictions).
> 
> -   If you are using a trial account, see [Trial Account Restrictions](trial-account-restrictions-a45742a.md).

> ### Note:  
> The maximum size limit of the dev space is 10 GB of disk space for productive accounts in the standard-edition plan. For trial accounts and accounts using the free plan, the maximum size limit of the dev space is 4 GB. Exceeding the maximum size limit can cause loss of data and other issues, including the inability to start the dev space. Note that additional restrictions apply to dev spaces in trial accounts. See [Trial Account Restrictions](trial-account-restrictions-a45742a.md).



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_b3b_1gs_33b"/>

## Stop, Start, or Delete Your Dev Space

If you don't need to work with your dev space for a while, you can stop your dev space. When your dev space is running, it consumes memory, energy, and CPU. If you don't use your dev space and it sits idle for a while, the dev space is stopped.

When you restart your stopped dev space, all content in your dev space, including files and settings, are available. If you want to apply updates to extensions and bug fixes, you must stop your dev space and start it again.

You can also delete your dev space.

> ### Note:  
> By creating a dev space, you create a project and file system for yourself. If you delete your dev space, you can't recover it. We recommend syncing, backing up, and saving your project to a Git repository. See [Connect to Your Git Source Control System](connect-to-your-git-source-control-system-e7a42bc.md).



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_s2p_4ts_fnb"/>

## Add Extensions to Your Dev Space

You can add extensions to an existing dev space from the Dev Space Manager.

To add extentions, the dev space must be in the stopped state.

1.  From the Dev Space Manager, click ![Edit icon](images/Edit_Dev_Space_Button_7f87f6e.jpg) to edit the dev space.
2.  Select the additional SAP extensions that you want to add.
3.  Click *Save Changes*.



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_b5r_zhm_5jb"/>

## Download Dev Space Content

You can download the dev space content in the following situations:

-   When your dev space is in the *RUNNING* state to save the dev space contents.
-   When your dev space is in the *ERROR* state to recover your data and move the contents to another dev space.

To download the content of your dev space, click ![Download icon](images/Download_Dev_space_content_87493f9.png) and then *Download*.

If your dev space is in the *ERROR* state, after the download begins, the dev space state changes to *STARTING*. The dev space state then changes to *SAFE MODE* and then the `tar` file downloads.

After the dev space changes to *SAFE MODE*, it's not possible to return to the *RUNNING* state. You can only download the dev space content and delete the dev space.

When the export process is complete, the `tar` file, with the dev space content, is downloaded.

> ### Note:  
> After exporting the dev space content, check the size of the dev space before uploading. Make sure that the size doesn't exceed 10 GB.



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_kjb_krb_hmb"/>

## Import Dev Space Content

After downloading the dev space content, you can import the content to another dev space:

1.  Create a new dev space, start it, and open it.
2.  Click *Open Folder*.

    The `user` folder is selected.

3.  Click *Open*.
4.  Click to select the `projects` folder.
5.  Click *File* \> *Upload Files*.
6.  From the *Downloads* folder, choose the file with the dev space content.
7.  Right-click the `projects` folder and select ***Open in Terminal***.
8.  Enter the following command to uncompress the uploaded file:

    ```
    tar xvzf <yourFileName>.tar.gz
    ```


