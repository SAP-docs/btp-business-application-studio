<!-- loioad40d52d0bea4d79baaf9626509caf33 -->

# Working in the Dev Space Manager

You can create, delete, stop, and start dev spaces. You can also download dev space content, and import dev space content.



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_bpd_nst_njb"/>

## Create a Dev Space

You can generate a dev space to create and manage applications. You can select the application type that includes the extensions that you need for performing a development task.

1.  Open SAP Business Application Studio and log in with your credentials.
2.  Click *Create Dev Space*.
3.  Enter a name for the dev space.
4.  Select the relevant application type.
5.  \(Optional\) Select the relevant additional extensions to enhance your space. \(Don't worry, you can add extensions to your dev space later, see below.\)
6.  Click *Create Dev Space*.

    > ### Note:  
    > The button is only enabled if you entered a dev space name.


> ### Note:  
> The maximum size limit of the dev space is 10 GB for productive accounts in the standard-edition plan, and 4 GB for trial accounts and accounts using the free plan. Exceeding this limit may cause loss of data and other problems, including the inability to start the dev space. Note that additional restrictions apply to dev spaces in trial accounts. See [Restrictions](Restrictions_a45742a.md).



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_b3b_1gs_33b"/>

## Stop, Start, or Delete Your Dev Space

If you don't need to work with your dev space for a while, you can stop your dev space. When your dev space is running, it consumes memory, energy, and CPU. If you don't use your dev space and it sits idle for too long, the dev space will be stopped.

When you restart your stopped dev space, all content in your dev space, including files and settings, remain and will be available. If you want to apply updates to extensions and bug fixes, you must stop your dev space and start it again.

You can also delete your dev space.

> ### Note:  
> By creating a dev space, you create a project and file system for yourself. If you delete your dev space, it can't be recovered. We recommend syncing, backing up, and saving your project to a Git repository. See [Connect to Your Git Source Control System](Connect_to_Your_Git_Source_Control_System_e7a42bc.md).



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_s2p_4ts_fnb"/>

## Add Extensions to Your Dev Space

You can add extensions to an existing dev space from the Dev Space Manager.

To add extentions, the dev space must be in the stopped state.

1.  From the Dev Space Manager, click ![](images/Edit_Dev_Space_Button_7f87f6e.jpg) to edit the dev space.
2.  Select the desired additional SAP extensions.
3.  Click *Save Changes*.



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_b5r_zhm_5jb"/>

## Download Dev Space Content

You can download the dev space content in the following situations:

-   When your dev space is in the *RUNNING* state to save the dev space contents.
-   When your dev space is in the *ERROR* state to recover your data and move the contents to another dev space.

To download the content of your dev space, click ![](images/Download_Dev_space_content_87493f9.png) and then *Download*.

After the download begins, the dev space state changes to *STARTING*. The dev space state then changes to *SAFE MODE* and then the `tar` file downloads.

When the download is complete, the `tar` file appears, which contains the dev space content.

> ### Note:  
> After the dev space content is exported, check the total size of the dev space before uploading it to make sure that the size does not exceed 10 GB.



<a name="loioad40d52d0bea4d79baaf9626509caf33__section_kjb_krb_hmb"/>

## Import Dev Space Content

After downloading the dev space content, you can import the content to another dev space by performing the following steps:

1.  Create a new dev space and open it.
2.  Click *Open Folder*.

    The `user` folder is selected by default.

3.  Click *Open*.
4.  Click the `projects` folder to select it.
5.  Click *File* \> *Upload Files*.
6.  From the *Downloads* folder, choose the file with the dev space content.
7.  Right-click the `projects` folder and select ***Open in Terminal***.
8.  Enter the following command to uncompress the uploaded file:

    ```
    tar xvzf <yourFileName>.tar.gz
    ```


