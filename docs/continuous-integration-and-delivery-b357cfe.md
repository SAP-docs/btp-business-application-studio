<!-- loiob357cfe698f3424cb76c7a3070d9a2b3 -->

# Continuous Integration and Delivery

SAP Continuous Integration and Delivery lets you configure and run predefined continuous integration and delivery \(CI/CD\) pipelines that automatically build, test, and deploy your code changes to speed up your development and delivery cycles.



<a name="loiob357cfe698f3424cb76c7a3070d9a2b3__section_ozk_2b4_m1c"/>

## Prerequisites

Make sure you run the *Get started with SAP Business Application Studio* booster,

Make sure you added the Continuous Integration and Delivery service as part of the *Get started with SAP Build Code* booster.



<a name="loiob357cfe698f3424cb76c7a3070d9a2b3__section_ikz_3lz_2xb"/>

## Procedure

From the *CI/CD* view, you can see all jobs configured for the current project, as long as the project is connected to a Git repository.

In SAP Business Application Studio, you can create 1 `config.yaml`-based job for your project using a CI/CD pipeline.

1.  From the activity bar, click to open the *CI/CD* view.

2.  Click *Create Job*.

    > ### Note:  
    > If you already have a `config.yaml`-based job in your project, this option will be disabled.


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


