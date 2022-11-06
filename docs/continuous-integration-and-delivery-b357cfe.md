<!-- loiob357cfe698f3424cb76c7a3070d9a2b3 -->

# Continuous Integration and Delivery

SAP Continuous Integration and Delivery lets you configure and run predefined continuous integration and delivery \(CI/CD\) pipelines that automatically build, test, and deploy your code changes to speed up your development and delivery cycles.

> ### Note:  
> To use SAP Continuous Integration Delivery, you must first subscribe to the service. See [Enabling the Service](https://help.sap.com/docs/CONTINUOUS_DELIVERY/99c72101f7ee40d0b2deb4df72ba1ad3/c8ed09df9ebd4556ae2375feac829c24.html?version=Cloud&language=en-US).

The *CI/CD* view in SAP Business Application Studio, allows you to see all jobs configured for the current project, as long as the project is connected to a Git repository.

You can create a job for your project using a CI/CD pipeline.

1.  From the left-side menu, select *View* \> *Command Palette*.

2.  Search for *Guided Development: Create a CI/CD Job*. Select the guide and follow the instructions.


Each job is configured using a `config.yaml` file in the project Git repository.

The *CI/CD* view shows the latest build triggered by the user. To see all builds, open the SAP Continuous Integration and Delivery service. See [SAP Continuous Integration and Delivery](https://help.sap.com/docs/CONTINUOUS_DELIVERY/99c72101f7ee40d0b2deb4df72ba1ad3/618ca03fdca24e56924cc87cfbb7673a.html?version=Cloud&language=en-US) to learn about this service. You can see the build details for each job, such as the creation date and status.

Once a new build is triggered, the view is updated with the latest build.

From the job’s context menu, you can:

-   See the build steps and logs.

    Click *View Build Log* to open.

-   Manually trigger a build.

    Click *Trigger a Build*. The best practice is to use Git webhooks to automatically trigger a build with each build action. Nevertheless, you can manually trigger a build without pushing changes to Git.

-   Open the code editor.

    Click *Edit* to open the `config.yaml` file in the code editor.

-   Delete the job.

    Click *Delete* to remove the job from the SAP Continuous Integration and Delivery service and the configuration file is deleted from the repository. This affects all users working in the repository.


From the *CI/CD JOBS* view menu bar, you can click ![](images/Settings_8317c84.png) \(Settings\) to open the Settings page, or *\+* to add a new job.

