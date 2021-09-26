<!-- loio97ef204c568c4496917139cee61224a6 -->

# Building and Deploying Multitarget Applications

Build and deploy multitarget applications to SAP Cloud Foundry.



<a name="loio97ef204c568c4496917139cee61224a6__section_av4_hbz_mkb"/>

## Building Multitarget Applications

**Prerequisites**

-   Your dev space must contain a multitarget application.

There are several ways for building multitarget applications in SAP Business Application Studio:

-   From the context menu.
    1.  Right-click on the `mta.yaml` file.
    2.  Choose *Build MTA*.
-   From the command palette.
    1.  Enter ***MTA***.
    2.  Choose *Build MTA*.
    3.  Select the desired `mta.yaml` file.

        > ### Note:  
        > If there’s only one `mta.yaml` available, the build starts automatically.

-   From the *Task Explorer*.

    1.  From the left sidebar, click ![](images/task_explorer_46d3c3f.png) to open the *Task Explorer* view.
    2.  Click *+* \(Create Task\).
    3.  Click *Build*.
    4.  Select the MTA project descriptor of the project you want to build.
    5.  Click *Configure* to edit the build configuration parameters.
    6.  Save your changes.
    Use the *Task Explorer* to change the default MTA Build options, for example, to change the default location of the MTA archive or to provide an MTA extension for the build. In the *Task Explorer*, you can save this build configuration for later use.

-   From the CLI. See [Cloud MTA Build Tool](https://sap.github.io/cloud-mta-build-tool/usage/).

The terminal opens showing the output of the build. Once the build is complete, a folder named `mta_archives` is added to the project that contains the relevant MTA archive \(MTAR file\).

> ### Note:  
> If you changed the default configurations using the Task Explorer, the output will correspond to the specified build parameters.



<a name="loio97ef204c568c4496917139cee61224a6__section_azc_fbz_mkb"/>

## Deploying Multitarget Applications

**Prerequisites**

-   You must have permissions to deploy to your Cloud Foundry space.
-   Your dev space must contain a multitarget application.
-   Your workspace must contain an MTA archive \(MTAR\) file.

There are several ways for deploying multitarget applications to SAP Cloud Foundry:

-   From the context menu.
    1.  Right-click on the relevant MTAR file.
    2.  Choose *Deploy MTA Archive*.
-   From the command palette.
    1.  Enter ***MTA***.
    2.  Choose *Deploy MTA Archive*.
    3.  Select the desired MTAR file.

        > ### Note:  
        > If there’s only one MTAR file available, the deployment starts automatically. If you are not logged into Cloud Foundry, you need to do this before deployment starts.

-   From the *Task Explorer*.

    1.  From the left sidebar, click ![](images/task_explorer_46d3c3f.png) to open the *Task Explorer* view.
    2.  Click *+* \(Create Task\).
    3.  Click *Deploy*.
    4.  Select the MTA archive of the project you want to build.
    5.  Click *Configure* to edit deployment configuration parameters.
    6.  Save your changes.
    Use the *Task Explorer* to change the default MTA deploy options. In the *Task Explorer*, you can save this configuration for later use.

-   From the CLI. See [Deploy Commands](https://github.com/cloudfoundry-incubator/multiapps-cli-plugin).

The terminal opens showing the output of the deploy process.

