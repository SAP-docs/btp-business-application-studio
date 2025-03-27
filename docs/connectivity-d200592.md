<!-- loiod2005922d0854834b5bbdfb8b9c693cd -->

# Connectivity

Steps you can take if you have connectivity issues.



<a name="loiod2005922d0854834b5bbdfb8b9c693cd__section_rk3_g23_fdc"/>

## Problems Connecting to External Systems

If you encounter problems when connecting to external systems from an SAP Business Application Studio dev space, follow the steps below to identify the root cause of the issue and resolve it.



### Destination configuration in the SAP BTP cockpit

**Reason**

You are either missing a destination pointing to your on-premise system in your SAP BTP subaccount, or there is a problem with the destination configuration in the SAP BTP cockpit.

**Solution**

**Option 1: Verify the SAP BTP destinations.**

1.  Log in to your SAP BTP cockpit. If you do not have the appropriate permissions, go to [Option 2](connectivity-d200592.md#loiod2005922d0854834b5bbdfb8b9c693cd__option2) or [Option 3](connectivity-d200592.md#loiod2005922d0854834b5bbdfb8b9c693cd__option3).
2.  Navigate to the subaccount that is subscribed to SAP Business Application Studio.
3.  From the left navigation menu, under *Connectivity*, select *Destinations*.

    All the available destinations are displayed.

4.  Select the specific destination that you are trying to consume \(you can also filter the list by the destination name\), and verify the following:
    -   If there is no destination pointing to the system that you are trying to access from your SAP Business Application Studio dev space, create one.

        See [Connecting to External Systems](https://help.sap.com/docs/bas/sap-business-application-studio/connecting-to-external-systems?version=Cloud).

    -   If you are consuming a specific destination name from the dev space \(as defined in your project resources, or as selected in different tools triggered from your dev space\), make sure that the destination pointing to the desired system in the SAP BTP cockpit is defined with the same name as that used in the dev space.
    -   Verify that the destination's *Additional Properties* contain the following:

        ```
        HTML5.DynamicDestination = true
        WebIDEEnabled = true
        ```

    -   Verify that the destination's *Additional Properties* contain all the required properties according to the type of system to which it is pointing. Specifically, pay attention to the values of the *WebIDEUsage* and *WebIDEAdditionalData* properties, as defined in [Connecting to External Systems](https://help.sap.com/docs/bas/sap-business-application-studio/connecting-to-external-systems?version=Cloud).
    -   When the destination points to an ABAP system, verify that its *Additional Properties* contain the *sap-client* property with the correct SAP client value for the ABAP system that you want to use.
    -   Verify that the authentication-related properties are set up correctly, according to the selected authentication method, as defined in the [SAP BTP destination documentation](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/http-destinations?version=Cloud).
    -   Verify that the destination URL can be accessed using the *Check Connection* option for the destination in the SAP BTP cockpit.

5.  After creating the missing destination or editing its properties in the SAP BTP cockpit, make sure to restart your dev space and retest your scenario.

**Option 2: Verify the destinations on your dev space**

1.  Open your dev space.
2.  From the main menu, select *Terminal* \> *New Terminal* and run the following curl commands:

    Refresh destination list:

    ```
    curl localhost:8887/reload
    ```

    Generate destination list:

    ```
    curl $H2O_URL/api/listDestinations -o dests.json
    ```

    The generated `dests.json` file contains a list of all the destinations available on your subaccount.

3.  Open the `dests.json` file, right-click anywhere on the file, and select *Format Document* to make it more readable.
4.  Locate the specific destination that you are trying to consume and verify the following:
    -   Verify that the destination that appears in the list is exactly the same as that consumed from your dev space.
    -   Verify that the destination *Host* property points to the desired system URL.
    -   Verify that the destination contains the following properties:

        ```
        "HTML5.DynamicDestination" : "true"
        "WebIDEEnabled" : "true"
        ```

    -   Verify that the destination contains all the required properties according to the type of the system to which it is pointing. Specifically, pay attention to the values of the *WebIDEUsage* and *WebIDEAdditionalData* properties, as defined in [Connecting to External Systems](https://help.sap.com/docs/bas/sap-business-application-studio/connecting-to-external-systems?version=Cloud).
    -   When the destination points to an ABAP system, verify that its *Additional Properties* contain the *sap-client* property with the correct SAP client value for the ABAP system that you want to use.

5.  If the destination is missing from the list, or its properties are not configured correctly, create or edit the destination in the SAP BTP cockpit. See[Connecting to External Systems](https://help.sap.com/docs/bas/sap-business-application-studio/connecting-to-external-systems?version=Cloud).

    If you do not have the appropriate permissions, contact your subaccount administrator.

    > ### Note:  
    > You cannot check the authentication-related configurations in the destination from your dev space. If you suspect an authentication issue, make sure to check the authentication-related properties in the SAP BTP cockpit as explained in [Option 1](connectivity-d200592.md#loiod2005922d0854834b5bbdfb8b9c693cd__option1) above. If you do not have the appropriate permissions, contact your subaccount administrator.


**Option 3: Additional verifications for destinations used for SAP Fiori application development**

If the destination is used from your dev space for SAP Fiori application development:

-   Perform an environment check:
    1.  In SAP Business Application Studio, from the main menu, select *View* \> *Find Command* and enter `Fiori: Open Environment Check`.

        A list of all available subaccount destinations appears.

    2.  Select your specific destination.
    3.  If your destination requires authentication, provide your username and password when prompted.
    4.  Select *Save and view results* and save to a known area, for example `/home/user/projects`.

        This generates a report on your chosen destination and lists all the destinations available to you on your subaccount.

        The generated report tries to retrieve the OData service catalog \(for OData V2 and V4\). If your destination is not an ABAP back end with these catalog requests supported, the report summary highlights this.


-   Perform more verifications for the destination configurations required for SAP Fiori application development as described in these Guided Answers entries:
    -   [Configure an SAP BTP Destination](https://ga.support.sap.com/dtp/viewer/index.html#/tree/3046/actions/45995:48363:53594:54336)
    -   [Validate Destination Configuration](https://ga.support.sap.com/dtp/viewer/index.html#/tree/3046/actions/45995:48363:53594:48364:51208)




### Cloud Connector configuration for accessing on-premise systems

**Reason**

To access an on-premise system, a cloud connector must be properly configured to handle the system requests called from a dev space.

**Solution**

-   Verify that the Cloud Connector is configured with your system URL and connected to the SAP BTP subaccount subscribed to SAP Business Application Studio:
    1.  In the SAP BTP cockpit, from the left navigation menu, under *Connectivity*, select *Cloud Connectors*.

        All the exposed back-end systems from your cloud connector are displayed.

    2.  Verify that the system virtual URL \(host and port\) from the Cloud Connector is defined exactly as in the URL property of the matching destination from the SAP BTP cockpit. The URL should include only host and port \(with no specific path\) both in the Cloud Connector and in the destination configurations.
    3.  Verify that the system protocol is defined as HTTP.
    4.  Verify that the internal system URL \(host and port\) is the correct URL in your internal network to access the desired system. For an ABAP on-premise system, you can find the correct system port by using the <code><i>/NSMICM</i></code> transaction in your ABAP system. Then, from the system menu, click *More* \> *Go to* \> *Services* and locate the correct port according to the desired protocol.
    5.  Add the missing Cloud Connector entry or edit its properties if needed directly from the Cloud Connector. For more information, see [Cloud Connector](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/cloud-connector).

-   Make sure that the configurations from the Cloud Connector to access all required system paths are correct:
    1.  In the *Access Control* tab of the Cloud Connector, grant access to all relevant URL paths \(Resources\) to access the system. \(For *Access Policy*, select the *Path and all sub-paths* option.\)

        For example, for an on-premise ABAP system, the following paths \(and their sub-paths\) must be allowed: `/sap/opu/odata/`, `/sap/bc/ui5_ui5/`, `/sap/bc/adt/`, and `/sap/bc/ui2/app_index/`.


-   Retrieve the Cloud Connector logs and search for the errors that occurred when accessing the system from SAP Business Application Studio. See [Cloud Connector Troubleshooting](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/cloud-connector-troubleshooting?version=Cloud).
-   If the Cloud Connector fails to open a tunnel to the on-premise system, and the `Tunnel handshake failed` error is displayed in the Cloud Connector logs:
    -   Verify that no proxies or network policies block the Cloud Connector from connecting SAP Business Application Studio and the on-premise system.
    -   Make sure that you have an internet connection to the SAP Business Application Studio connectivity service host, to which you can connect your Cloud Connector. To find theSAP Business Application Studio connectivity service host for your region, see [SAP Business Application Studio Availability](https://help.sap.com/docs/bas/sap-business-application-studio/sap-business-application-studio-availability?version=Cloud).
    -   Follow the instructions described in this [SAP Note](https://me.sap.com/notes/3035686).




### Cannot use an on-premise ABAP system in SAP Business Application Studio, even though it can be accessed through a destination

**Prerequisites**

The destination and the Cloud Connector are configured correctly to access the system from SAP Business Application Studio.

See [Destination Configuration in the SAP BTP cockpit](https://ga.support.sap.com/dtp/viewer/index.html#/tree/2065/actions/26547:26549:28901:41344:41346:57775:57776) and [Configuring the Cloud Connector for accessing on-premise systems](https://ga.support.sap.com/dtp/viewer/index.html#/tree/2065/actions/26547:26549:28901:41344:41346:57775:57777).

**Reason**

There could be an issue with the specific system, or additional configurations are required according to the specific scenario you are using when accessing the system.

**Solution**

Follow these instructions according to your scenario.

**Consuming an OData Service**

If you have an issue consuming an OData service from an on-premise ABAP system, we recommend that you verify the access to the system by using Basic Authentication.

Make sure to use a destination configured with the "BasicAuthentication" option \(and provide the user credentials in the destination\), or with the "NoAuthentication" option \(and then provide your user credentials from SAP Business Application Studio when prompted\).

Then, verify that you can access the system from the Service Center in SAP Business Application Studio:

1.  Open your dev space.
2.  Open the Service Center view.

    See [Explore Services Using the Service Center](https://help.sap.com/docs/bas/sap-business-application-studio/explore-services-using-service-center?version=Cloud).

3.  Locate the destination for your on-premise ABAP system and expand it to see the OData service list in the system.

    If the services are not displayed, try to access the on-premise system OData Catalog from your internal network:

    1.  In the internal network that has access to the on-premise system, open a new browser tab.
    2.  Double-click the system to see the system properties from the Service Center in your dev space, and copy the value under the *URL*.
    3.  Paste the copied URL in the new browser tab using the following pattern:

        `https://<copied system url>/sap/opu/odata/IWFND/CATALOGSERVICE;v=2/ServiceCollection`

    4.  If prompted, provide your system credentials.
    5.  If you get an error or cannot retrieve data using this URL from the internal network, check your on-premise ABAP system configurations. Specifically, verify that the `sap-opu-iwfnd-catalogservice` service is active using the */NSICF* system transaction.
    6.  If the service list data is returned by calling the URL in the internal network from your browser, but cannot be displayed from the Service Center in your dev space, re-verify the system configurations in the destination from the SAP BTP cockpit \(including credentials, if provided\) and in the Cloud Connector.

        See [Destination Configuration in the SAP BTP cockpit](https://gad5158842f.us2.hana.ondemand.com/dtp/viewer/#/tree/2827/actions/41344:41346:57775:57776/?version=current).

        Specifically, make sure that the following properties are defined correctly within the SAP BTP destination for the system:

        -   The *WebIDEUsage* property has the *odata\_abap,dev\_abap* value.
        -   No *WebIDEAdditionalData* property is defined.
        -   The *URL* property defines the URL for the on-premise ABAP system virtual endpoint \(as defined in the Cloud Connector\), with no path \(host and port only\).


4.  From the Service Center, select the relevant OData service from the service list under your system destination entry.
5.  Connect to the system and verify that you can see data in the *Entity Details* and *Live Data* tabs. See [SAP System Service Provider](https://help.sap.com/docs/bas/sap-business-application-studio/sap-system-service-provider?version=Cloud).
6.  If the entity data or live data cannot be displayed from the Service Center, try to access the on-premise OData service from your internal network:
    1.  Make sure you are connected to the internal network that has access to the on-premise system.
    2.  From the service page that you opened from the Service Center in [Step 4](connectivity-d200592.md#loiod2005922d0854834b5bbdfb8b9c693cd__step4), click the service URL to open it in a new browser tab.
    3.  If prompted, provide your system credentials.
    4.  If you get an error or cannot retrieve data using this URL from the internal network, check your on-premise ABAP system configurations. Specifically, verify that the `sap-opu-iwfnd-catalogservice` service is active using the */NSICF* transaction from the system.


If you can access the system using the Service Center with Basic Authentication, but you still have access issues using a destination configured with another authentication option, make sure to verify the authentication configuration in your destination. For principal propagation authentication, see the [section](connectivity-d200592.md#loiod2005922d0854834b5bbdfb8b9c693cd__principalprop) below.

**More Development Flows with SAP Fiori Applications**

When developing an SAP Fiori application, check the solution for your specific issue when working in SAP Business Application Studio as described in the following Guided Answers entries:

-   [OData service list is not displayed when generating a new SAP Fiori application](https://ga.support.sap.com/dtp/viewer/index.html#/tree/3046/actions/45995:48363:53594:48366)
-   [Deploy SAP Fiori Application to ABAP system](https://ga.support.sap.com/dtp/viewer/index.html#/tree/3046/actions/45995:45996:50742:46000%20)

**Extending an SAPUI5 Extension Project**

When extending an SAP Fiori application from an on-premise ABAP system using an SAPUI5 extension project, open your local browser when connected to the internal network and verify you can access the relevant services from the back-end system:

1.  Open your dev space.
2.  Locate the failing request to the back-end system:
    -   If the failure occurs when previewing the SAPUI5 extension project or when using the *Add Extension* wizard, open the browser's network trace, filter the request using the */sap/bc/* path, and copy the full URL of the failing request.
    -   If the failure occurs during the generation of a new SAPUI5 extension project, locate a failing request to your back end using the */sap/bc/* path in the cloud connector logs, and copy the full request from it.

3.  Locate your back-end system's internal host and port as defined in your cloud connector entry. Make sure to locate the same system associated with the virtual host and port that are defined in your destination's *URL* property.
4.  Try to access the failing request to your on-premise system from your internal network:
    1.  In the internal network that has access to the on-premise system, open a new browser tab.
    2.  Paste the URL that you copied in step 2 and replace its host and port with the internal back-end host and port you located in step 3.

        For example, if the failing request from the SAP Business Application Studio network trace is: `https://port8888-workspaces-ws-xxxx.eu10.applicationstudio.cloud.sap/destinations/MYDEST/sap/bc/adt/filestore/ui5-bsp/objects/EPMRA_POAPV%2Fcontroller%2FApp.controller.js/content`, replace it with the following URL:

        `https://<my-internal-host>:<my-internal-port>/sap/bc/adt/filestore/ui5-bsp/objects/EPMRA_POAPV%2Fcontroller%2FApp.controller.js/content`

    3.  If prompted, provide your system credentials. Make sure to use the same credentials as used for accessing this system from SAP Business Application Studio.
    4.  If you get an error or cannot retrieve data by using this URL from the internal network, check your on-premise ABAP system configurations. Specifically, verify that the `sap-bc-adt` service is active using the */NSICF* transaction from the system.
    5.  If the request data is returned by calling the URL in the internal network from your browser, but cannot be accessed from your dev space, re-verify the system configurations in the destination from the SAP BTP cockpit \(including credentials, if provided\) and in the Cloud Connector. See [Destination Configuration in the SAP BTP cockpit](https://gad5158842f.us2.hana.ondemand.com/dtp/viewer/#/tree/2827/actions/41344:41346:57775:57776/?version=current). Specifically verify that the URL property defines the URL for the on-premise ABAP system virtual endpoint \(as defined in the Cloud Connector\), with no path \(host and port only\).


**Accessing the On-Premise System with Principal Propagation Authentication**

When defining the destination to use the authentication type of principal propagation to access your ABAP on-premise system, make sure to verify your setup by following these guides:

-   [Configuring Principal Propagation](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/configuring-principal-propagation)
-   [Principal Propagation in an HTTPS Scenario](https://community.sap.com/t5/technology-blogs-by-sap/how-to-guide-principal-propagation-in-an-https-scenario/ba-p/13325048)

**Still need help**? Open a support ticket with component **CA-BAS-CNSM** and add the information and result of all steps performed here \(including the prerequisite checks\).



### Cannot access the SAP S/4HANA Cloud system in SAP Business Application Studio

**Prerequisites**

The destination is configured correctly to access the system from SAP Business Application Studio.

See [Destination Configuration in the SAP BTP cockpit](https://ga.support.sap.com/dtp/viewer/index.html#/tree/2065/actions/26547:26549:28901:41344:41346:57775:57776).

**Reason**

Additional configurations are required according to the specific scenario that you are using when accessing the system.

**Solution**

Follow the steps in the links below to correctly establish trust with SAP S/4HANA Cloud and manually create the appropriate destination in the SAP BTP subaccount subscribed to SAP Business Application Studio:

-   [Integrating SAP Business Application Studio](https://help.sap.com/docs/SAP_S4HANA_CLOUD/0f69f8fb28ac4bf48d2b57b9637e81fa/22bc724fd51a4aa4a4d1c5854db7e026.html?version=2408.500)
-   [Connect SAP Business Application Studio and SAP S/4HANA Cloud System](https://developers.sap.com/tutorials/abap-custom-ui-bas-connect-s4hc.html)
-   [Configuring the Extension Application's Connectivity to SAP S/4HANA Cloud](https://help.sap.com/docs/btp/sap-business-technology-platform/configuring-extension-application-s-connectivity-to-sap-s-4hana-cloud?version=Cloud)

If the error occurs when trying to get a list of OData services during the creation of an SAP Fiori project, see also the [Accessing OData service with a SAP S/4HANA Cloud communication user](https://ga.support.sap.com/dtp/viewer/index.html#/tree/3046/actions/45995:48363:53594:52803) Guided Answers entry.

For issues when following the steps from the guides above, open a support ticket for component: *BC-SRV-APS-EXT-BAS*

If the deployment target of your developed application is Cloud Foundry and not SAP S/4HANA cloud, the destination can also be created automatically. Make sure you have followed the steps for creating the appropriate setup to extend SAP S/4HANA Cloud in Cloud Foundry described in [Extending SAP S/4HANA Cloud in the Cloud Foundry and Kyma Environment](https://help.sap.com/docs/btp/sap-business-technology-platform/extending-sap-s-4hana-cloud-in-cloud-foundry-and-kyma-environment?version=Cloud). If there are issues when following these steps, open a support ticket for component: *BC-SRV-APS-COM*



<a name="loiod2005922d0854834b5bbdfb8b9c693cd__section_cwq_j4f_wmb"/>

## SAP Business Application Studio takes longer than expected to load

**Reason**

This might be due to a high latency or a network issue.

**Solution**

-   Check that you are connected to the data center closer to your location. Open the [Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/business-application-studio?tab=service_plan&region=all), and click the *View service regions on map* \(![](images/View_service_regions_on_map_e14185f.png)\) icon to see the details.
-   Make sure you have a stable internet connection.
-   Make sure you are using a supported browser. See the *Availability* section in [What Is SAP Business Application Studio?](what-is-sap-business-application-studio-8f46c6e.md).



<a name="loiod2005922d0854834b5bbdfb8b9c693cd__section_jl4_kmf_dmb"/>

## When working in Mozilla FireFox, the table records are not loaded in the SQLTools view

**Reason**

This is related to an [open bug](https://bugzilla.mozilla.org/show_bug.cgi?id=1413615) in Mozilla Firefox.

**Solution**

1.  Open SAP Business Application Studio and go to your dev space.
2.  Once the dev space has loaded, right-click the SAP logo in the top-left corner and select *This frame* \> *Show only this frame*. A new tab opens.
3.  From the new tab's URL, copy the domain value starting from the second subdomain. For example:

    **URL:** `subdomain1.subdomain2.subdomain3.sap/path1/path2`

    **Copy only:** `subdomain2.subdomain3.sap`

4.  Click the Mozilla Firefox menu button and select *Settings*.
5.  Search for *Cookies and Site Data*.
6.  Make sure that the *Delete cookies and site data when Firefox is closed* checkbox is not selected.
7.  Click *Manage Exceptions*.
8.  In the *Address of website* field, enter the domain value that you copied earlier.
9.  Click *Allow*.
10. Click *Save Changes*.



<a name="loiod2005922d0854834b5bbdfb8b9c693cd__section_onw_b1n_b4b"/>

## Problems deploying a native SAP HANA application or database artifact to the HDI container

**Reason**

By default, SAP HANA Cloud denies access from all IP addresses except for IP addresses in SAP BTP. If an SAP Business Application Studio IP address is denied access, you will receive a connection failure error during deployment.

**Solution**

If you are working on an Azure account or you are trying to connect an SAP HANA instance from a different region, you must configure SAP HANA Cloud to allow connections from the IP address hosting SAP Business Application Studio for your Cloud region and the underlying platform.

To learn how to change the SAP HANA Cloud allowed connections, see [SAP HANA Database Configuration](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-administration-guide/sap-hana-database-configuration?locale=en-US).

To find out your SAP Business Application Studio IP address, see [SAP Business Application Studio Availability](sap-business-application-studio-availability-8509485.md).



<a name="loiod2005922d0854834b5bbdfb8b9c693cd__section_dlm_fzb_x4b"/>

## The "The workbench failed to connect to the server" error appears when opening your dev space

**Solution**

Make sure that your network allows a websocket connection to SAP Business Application Studio.

See the [documentation](https://help.sap.com/docs/bas/sap-business-application-studio/sap-business-application-studio-availability?version=Cloud#inbound-ip-address).

