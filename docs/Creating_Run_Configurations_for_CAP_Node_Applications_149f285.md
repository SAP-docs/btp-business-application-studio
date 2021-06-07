<!-- loio149f285d410642c291855258aa13a46d -->

# Creating Run Configurations for CAP Node Applications

You can create configuration settings for running your projects.

**Prerequisites**

-   Your project was created in a Full Stack Cloud Application dev space. See [Dev Space Types](Dev_Space_Types_4142f78.md).

-   Your project is type *CAP*. See [SAP Business Application Studio in Capire](https://cap.cloud.sap/docs/get-started/tools/#bastudio) .

-   Your project must include the `package.json` file in your root folder.

-   Your project does not include a`pom.xml` file in any folder.




<a name="loio149f285d410642c291855258aa13a46d__section_fx4_jzq_hkb"/>

## Add a New Configuration

1.  From the left-side menu, click *Run Configurations*.

    ![](images/open_run_config_view_7790762.png)

2.  Click **+** \(Create Configuration\).

    ![](images/New_Run_Config_af5e36a.png)

3.  From the command palette, select the runnable object for which you want to create the configuration.

    > ### Note:  
    > By default, the run configuration is created for the "development" profile. If you configured an additional profile for your application, you can create a run configuration that activates and uses this profile.
    > 
    > The dependencies of the application are calculated according to the profile selected.

    A configuration tree appears in the *RUN CONFIGURATIONS* view containing the run configurations that were created for the runnable objects.

    A new configuration is added to your launch.json file.

    > ### Note:  
    > In addition to the launch.json file that is created as part of the new configuration, an environment file is added when creating a run configuration.
    > 
    > The environment configuration file is referenced from your Launch configuration.




<a name="loio149f285d410642c291855258aa13a46d__section_bgk_mb4_2lb"/>

## Bind Dependencies

In the *Run Configurations* view, you can see the available dependencies as defined in the `package.json` file. You can bind or unbind these dependencies to a specific Cloud Foundry service instance or to your local database.

> ### Note:  
> The following Cloud Foundry service types are supported for binding:
> 
> -   `hana` \( `managed-hana` is not supported\)
>     -   PSA-based SAP HANA
>     -   HaaS \(if configured as "Available for all IPs"\)
>     -   SAP HANA Cloud \(if configured as "Available for all IPs"\)
> -   `xsuaa`
> -   `auditlog`
> -   `application-logs`
> 
> You can also bind directly to a destination.

To bind the dependency to a local database:

1.  Open the *Run Configurations* view.
2.  Select the desired configuration.
3.  Select the desired dependency.
4.  Click ![](images/UnbindService_8a3582e.png) \(bind\). The database is now bound to a local database file.

    > ### Note:  
    > -   If you are binding to an SQLite service, a new connection is added to the SQLTools view where your tables and data are displayed.
    > -   Clicking Bind creates a Deploy task \(or triggers it if it already exists\). You can redeploy the database at a later stage by running this task again.

5.  Select the desired service.

To bind the dependency to an SAP HANA database:

1.  Open the *Run Configurations* view.
2.  Select the desired configuration.
3.  Select the desired dependency.
4.  Click ![](images/UnbindService_8a3582e.png) \(bind\). The database is now bound to an SAP HANA database.

    > ### Note:  
    > Clicking Bind creates a Deploy task. Depending on your SAP HANA version, you may be prompted to deploy. You can deploy manually by running the Deploy task.

5.  Select the desired service.

> ### Note:  
> -   If you are binding to an SAP HANA service, a new connection called `'<my_service_instance name>'` is added to the SQLTools view where your tables and data are displayed.
> -   If you define the DB dependency in your `package.json` file with kind `sql`:
>     -   If you are running with the "development" profile, the run configuration shows a dependency to SQLite.
>     -   If you are running with a "production" profile, the run configuration shows a dependency to SAP HANA.

To bind the dependency to a Cloud Foundry service:

1.  Open the *Run Configurations* view.
2.  Select the desired configuration.
3.  Select the desired dependency.
4.  Click ![](images/UnbindService_8a3582e.png) \(bind\).

    If not already logged in, you are prompted to log in to Cloud Foundry.

    A list of all available services that match your dependency type are displayed in the command palette.

5.  Select the desired service.

The dependency is bound to the service.

> ### Note:  
> -   After the dependency is bound to a service, the environment file is populated with all the environment variables required to connect to Cloud Foundry.

To unbind the resource:

1.  Open the *Run Configurations* view.
2.  Select the desired configuration.
3.  Select the desired dependency.
4.  Click ![](images/BindService_35ad62f.png) \(unbind\).

**Bind and mock an external OData service**

To bind the dependency to an external OData service using a destination:

1.  Open the *Run Configurations* view.
2.  Select the desired configuration.
3.  Select a dependency of type OData.
4.  Click ![](images/UnbindService_8a3582e.png) \(bind\).

    If not already logged in, you are prompted to log in to Cloud Foundry.

    A list of all available destinations from your subaccount is displayed in the command palette.

5.  Select the desired destination.

The dependency is bound to the destination.

To mock all OData services that are not bound to a destination:

1.  Turn on the property to mock external OData services.

    All dependencies of type OData that are not bound to a destination appear in the *Run Configuration* tree marked as mocked.




<a name="loio149f285d410642c291855258aa13a46d__section_ekx_f1r_hkb"/>

## Run a Configuration

1.  If you bound your service to a service that requires Chisel to run:
    1.  From the command palette, choose *Task* \> *Run Task*.
    2.  Select `openChiselTunnelFor-<service name>`.

        > ### Note:  
        > If Chisel is already running in the same port and space, skip this step.

2.  Select the desired run configuration.
3.  Click ![](images/Run_Configuration_icon_1897e99.png) \(Run\) to run the application.

    The Debug Console opens.

4.  A notification prompting you to expose and open the port \(if it was not previously exposed\), or to open the service in a new tab is displayed. Click the relevant action to view the service in a new tab. See [Managing Ports](Managing_Ports_91fc8bf.md).
5.  If you need to stop a configuration that is already running, you can do so from the *Debug* view.

> ### Note:  
> Stopping a configuration from the *Debug* view does not stop any running tasks.



<a name="loio149f285d410642c291855258aa13a46d__section_ltq_knh_jkb"/>

## Edit a Run Configuration

1.  Right-click a run relevant configuration to do the following:
    -   *Configure Environment* - Open the environment file to view the binding configuration.

    -   *Rename* - Provide a new name for the selected run configuration.

    -   *Show in File* - Open the JSON file containing the set of configuration properties, with the name highlighted.

    -   *Delete* - Delete the set of configuration properties from the JSON file.




<a name="loio149f285d410642c291855258aa13a46d__section_xs1_sth_jkb"/>

## Delete a Run Configuration

1.  Right-click a run relevant configuration and choose *Delete*.

    > ### Note:  
    > If you delete the launch configuration, it is removed from the `launch.json` file but the tasks remain.


