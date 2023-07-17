<!-- loiob357cfe698f3424cb76c7a3070d9a2b3 -->

# Continuous Integration and Delivery

SAP Continuous Integration and Delivery lets you configure and run predefined continuous integration and delivery \(CI/CD\) pipelines that automatically build, test, and deploy your code changes to speed up your development and delivery cycles.



<a name="loiob357cfe698f3424cb76c7a3070d9a2b3__section_ap4_mlz_2xb"/>

## Prerequisites

Perform the following configuration steps to use SAP Continuous Integration and Delivery in SAP Business Application Studio:

1.  You must subscribe to the *Continuous Integration & Delivery* service, assign the required roles and permissions, add the relevant service plan, and add the relevant instance.

    See [Initial Setup](https://help.sap.com/docs/CONTINUOUS_DELIVERY/99c72101f7ee40d0b2deb4df72ba1ad3/719acaf61e4b4bf0a496483155c52570.html?language=en-US) in the SAP Continuous Integration and Delivery documentation or run the *Get Started with SAP Business Application Studio* booster to automate these steps. See [Initial Setup](https://help.sap.com/docs/bas/developing-business-applications-using-productivity-tools/initial-setup) in the Developing Business Applications Using Productivity Tools documentation.

2.  In the SAP BTP cockpit, make sure to check that you have the following:
    -   A subscription to **SAP Business Application Studio** and *Continuous Integration & Delivery*.
    -   An instance for SAP Continuous Integration and Delivery.

        If you ran the booster, the instance name is *default\_cicd-service*. If you completed the manual steps, the instance name is the name that you chose.

        See [Enabling the API Usage](https://help.sap.com/docs/CONTINUOUS_DELIVERY/99c72101f7ee40d0b2deb4df72ba1ad3/1aedc23d3d8a4802b66f4a3bb795030e.html?language=en-US).


3.  Open a dev space in SAP Business Application Studio.
4.  Open a project in the terminal.
5.  Enter the following command to get the space GUID:

    ```
    cf space dev --guid
    ```

6.  Open the *Continuous Integration & Delivery* service from the SAP BTP cockpit.
7.  In SAP Continuous Integration and Delivery, click ![Settings Button](images/settings_cicd_7551c3e.png) \(Settings\).
8.  Click ![Plus Button](images/add_guid_6b91159.png) \(Add space to allow list\), enter the space GUID that you obtained in Step 5, and click *OK*.
9.  Click *Save*.
10. In the SAP BTP cockpit, navigate to *Connectivity* \> *Destinations*.
11. Click *New Destination*.
12. Click the *Service Instance* tab and create a destination with the following configurations:


    <table>
    <tr>
    <th valign="top">

    Property


    
    </th>
    <th valign="top">

    Value


    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
        *Service Instance*


    
    </td>
    <td valign="top">
    
        <the instance created earlier\>


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        *Name*


    
    </td>
    <td valign="top">
    
        `cicd-backend`


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        *Additional Property* \> ***HTML5.DynamicDestination*


    
    </td>
    <td valign="top">
    
        `true`


    
    </td>
    </tr>
    </table>
    
13. Click *Next*.
14. Leave the default values, but change *Authentication* to *OAuth2UserTokenExchange* and click *Save*.
15. Create a new dev space or restart your existing dev space to use the SAP Continuous Integration and Delivery service.



<a name="loiob357cfe698f3424cb76c7a3070d9a2b3__section_ikz_3lz_2xb"/>

## Procedure

The *CI/CD* view in SAP Business Application Studio, allows you to see all jobs configured for the current project, as long as the project is connected to a Git repository.

You can create a job for your project using a CI/CD pipeline.

1.  From the left-side menu, select *View* \> *Command Palette*.

2.  Search for *Guide Center: Create a CI/CD Job*. Select the guide and follow the instructions.


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

