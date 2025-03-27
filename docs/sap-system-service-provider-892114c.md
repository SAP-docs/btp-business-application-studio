<!-- loio892114ce078b4e17a9ff7e751e6330cc -->

# SAP System Service Provider

The SAP System service provider includes systems from your SAP Business Application Studio subaccount. You can use the services as data sources in your application or for application development.

Login occurs automatically, using the SAP Business Application Studio user credentials. If you don't maintain the credentials in the destination configuration of the account, you need to log in manually to open the system information.



<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_fpr_sx3_qqb"/>

## Explore SAP System Services

1.  Use the *Service* radio button in the Service Center to filter for the relevant providers.

2.  From the *Select a Provider* dropdown list, select *SAP System*.
3.  The Service Center displays a list of catalogs and a separate list of single services.

    > ### Note:  
    > If a system is connected, there's a dot next to the icon \(![Connected System icon](images/SC-_system_connected_icon_1c4c936.png)\) and you can click it to see the services that it contains.
    > 
    > Use the search field \(![Search icon](images/service_center_search_a1d4e5e.png)\) to filter the list.

    -   The *Catalog of Services* list contains the following types of systems:
        -   ABAP Service Catalog

            The destination points to the ABAP system directly. The system shows its service catalogs with a list of services \(V2 and V4, for example\). To see the list of services, click the catalog and log in with your user credentials, if needed.

        -   Cloud for Customer Catalog

            The destination points to the SAP Cloud for Customer system directly. The system shows its service catalogs with a list of services \(V2\). To see the list of services, click the catalog and log in with your user credentials, if needed.


    -   The *Services* list displays the following types of systems:
        -   Service Host

            The destination points to a host. To log in, enter the service path and your credentials, if needed, and click *CONNECT*.

        -   Service URL

            The destination points directly to the service.

        -   SAP Business One

            The destination points to the SAP Business One system directly. Adding this system enables you to create an SAP BTP application consuming an SAP Business One service.

            > ### Note:  
            > -   Only *No Authentication* or *Basic Authentication* types are supported.
            > -   You must use SAP Business One 10.0 Feature Package \(FP\) 2305 to enable adding a system.

            For more information about SAP Business One and the catalog that exposes a list of services, see [Service Layer API Reference](https://help.sap.com/doc/056f69366b5345a386bb8149f1700c19/10.0/en-US/Service%20Layer%20API%20Reference.html) and [What's New in SAP Business One 10.0, version for SAP HANA](https://help.sap.com/whats-new/753529e7d6144b59b353c94f0cdddbd0?locale=en-US).



4.  Click a catalog \(![Connected catalog icon](images/SC-_system_connected_icon_1c4c936.png)\) to open it and display the list of services, or click a service \(![Service icon](images/SC-_service_icon_fc5c112.png)\) to see its properties, including the name, description, authentication type, status, and URL.
5.  Click an entity to see the service details. You can see the entity's metadata, details, and live data in the *Entities* tab. This helps you choose an entity for your application.

    > ### Note:  
    > The live data only displays up to 20 rows of data for simple data types.

    You can also search for an entity.

    You can see details about the system and service in the *Properties* tab.

6.  You can click *View Diagram* to see the service entities, their properties, and the relationships between the entities in a new tab.



<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_ywd_331_tcc"/>

## Explore SAP System Business Objects and ABAP CDS Views

If you don't find the correct UI service for your project, you can explore business objects or CDS views and their properties in SAP S/4HANA Public Cloud and then generate an OData V4 service from an ABAP business object or CDS view. The service enables you to develop an SAP Fiori application based on your own custom UI service and deploy it to SAP BTP or SAP S/4 HANA Cloud.

**Prerequisites**:

To explore business objects and CDS views, make sure you have performed the following steps:

-   You must use SAP S/4HANA Cloud or ABAP Cloud only and connect with *SAMLAssertion* authentication to SAP BTP.

    See [Integrating SAP Business Application Studio](https://help.sap.com/docs/SAP_S4HANA_CLOUD/0f69f8fb28ac4bf48d2b57b9637e81fa/22bc724fd51a4aa4a4d1c5854db7e026.html?locale=en-US) and [Creating a Destination for Cross-Subaccount Communication](https://help.sap.com/docs/btp/sap-business-technology-platform/creating-destination-for-cross-subaccount-communication).

-   You must connect to the SAP S/4HANA Development Tenant \(usually Client 80\).
-   You must have a business user in SAP S/4HANA with the *BR\_DEVELOPER* business role.



### Create an SAP Fiori Project

1.  Create an SAP Fiori dev space and open it.
2.  Create an SAP Fiori project from the Lobby and open it.
3.  Click *\+New Project* from the *Get Started* page and enter a name for the empty project.
4.  If the storyboard doesn't open automatically, open it.



### Explore an ABAP Business Object or an ABAP CDS View

1.  Under *External Resources* in the storyboard, click *\+*.
2.  Use the *Business Object***/CDS** radio button to filter for the relevant entries.
3.  Click a system from the list to connect to the system.

    Lists of business objects and CDS views are displayed.

4.  Click a business object or CDS view from the list to see its entities and properties.

    The list of properties is also displayed for each entity.

5.  Click the*Add to SAP Fiori Project* button.

    > ### Note:  
    > If the business object or CDS view isn't optimized for UI creation, a notification will be displayed.




### Add the Custom UI Service to the Project

1.  Follow the *UI Service Generator* wizard steps, provide the required information, and click *Finish*.

    The UI OData service is generated from the business object or CDS view and is published in the V4 service catalog.

    See [UI Service Generation](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/1a7aad346618443a86ebd7250bac0ef0.html) for more information.

2.  Navigate to the storyboard.

    The new UI service is displayed under *External Resources* and is also available in the Service Center.




### Create a UI Application

1.  Under *UI Applications* in the storyboard, click *\+*.
2.  Follow the *SAP Fiori generator* wizard steps, provide the required information, and click *Finish*.

    See [Generating an Application](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/db44d45051794d778f1dd50def0fa267.html) for more information.

    The new UI application is displayed under *UI Applications* in the storyboard.

3.  Run the application to preview it.



<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_yq5_3sq_wcc"/>

## Explore SAP System Functions

A Remote Function Call \(RFC\) is the standard SAP interface for communication between SAP systems. RFC calls a function to be executed in a remote system.

You can add an RFC to a *Full-Stack Application Using Productivity Tools* project and then explore functions in the Service Center.

**Prerequisites**:

-   You can only explore systems that are configured with the Remote Function Call \(RFC\) type of authentication protocol.
-   Create and maintain systems with the *Type* RFC in the *Destination Configuration* of the SAP BTP cockpit. See [RFC Destinations](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/rfc-destinations).
-   In addition to any other RFC calls that you use in your app, you must maintain the Cloud Connector for RFC with the following function names set up:

    -   *DOCU\_GET*
    -   *RFC\_FUNCTION\_SEARCH*
    -   *RFC\_METADATA\_GET*

    See [Initial Configuration \(RFC\)](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/configure-access-control-rfc) and [Configure Access Control \(RFC\)](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/configure-access-control-rfc).

-   The following *Additional Properties* are required for the RFC destination:
    -   `jco.client.ashost`
    -   `jco.client.client`
    -   `jco.client.sysnr`

-   Only manual credential entry \(`CONFIGURED_USER`\) for the `Authorization Type` is supported when you log in to the system from the Service Center.

**Procedure**:

1.  Create a *Full-Stack Application Using Productivity Tools* project.
2.  If the storyboard doesn't open automatically, open it.
3.  Under *External Resources* in the storyboard, click *\+*.
4.  Use the *Function* radio button in the Service Center.

    Systems that fit the prerequisites are displayed.

5.  Click on the desired system and log in with your username and password, if needed.

    A list of functions is displayed.

    *Classic APIs* are delivered by SAP, are stable, will not change, and are therefore recommended. See this [blog](https://community.sap.com/t5/technology-blogs-by-sap/classic-apis-for-tier-2-abap-cloud-development-in-sap-s-4hana-cloud-private/ba-p/13620329) about Classic APIs.

6.  Choose the desired API to open it.

    The import parameters, export parameters, tables, and general information for the function are available in the Service Center editor.

7.  Click the *Add to Project* button.

    > ### Note:  
    > If you have several projects in your workspace, you will be prompted to select a project.

8.  To preview, you must create a user in the Repository-Based Shipment Channel \(RBSC\). See [Viewing Licenses and Repository Endpoints](https://help.sap.com/docs/RBSC/0a64be17478d4f5ba45d14ab62b0d74c/74a9a6cd668842cc88e623ed39d8373c.html?locale=en-US).
9.  When adding a function to the project for the first time, you need to enter your RBSC credentials and click *Add*. This will enable you to run the function later.

    See [Managing Technical Users in Repository-Based Shipment Channel](https://help.sap.com/docs/RBSC/0a64be17478d4f5ba45d14ab62b0d74c/7e83dfc309834942b441fc2106c5b7f5.html).

    If you need to set up or change your RBSC credentials, select *CDS: Configure RBSC for @sap/cds-rfc library* from the command palette and follow the prompts.

    > ### Note:  
    > RBSC credentials are stored in the project's `.npmrc` file. The `.npmrc` file will be added to the `.gitignore` file. You will be prompted for credentials only one time per project. If you manually remove the RBSC credentials from the .npmrc file, you will be prompted to enter the credentials again.

    The function is added to the project and the following changes occur:

    -   The `npmrc` file is updated with your RBSC credentials, enabling access to the RFC library. The RFC library is added as a dependency to the project. See [SAP Cloud Application Programming Model- RFC Integration](https://www.npmjs.com/package/@sap/cds-rfc?activeTab=readme).
    -   Under the `srv>external` resource folder, the function is translated to a `cds` file.
    -   The run configuration for running the external resource is updated automatically.

        > ### Note:  
        > When adding a function to a project, you may be prompted to approve the copying of your system login credentials. You can agree, disagree, or choose not to decide at that moment. Your decision can be changed later in the Service Center settings. Upon approval, credentials from the Service Center will be copied to the project for running locally.

    -   The function is displayed in the *External Resources* section of the storyboard.
    -   The `package.json` file is updated with the destination:

        ```
              "<YourDestination>": {
                "kind": "rfc",
                "model": "srv/external/<YourDestination>",
                "[production]": {
                  "credentials": {
                    "destination": "<YourDestination>"
                  }
                }
              }
        ```





<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_dtd_wx3_qqb"/>

## Service Actions for Development



### Create a Project from a Service

1.  Click *Create Project*.

    The template wizard displays the projects that you can create from a service. For example, an HTML5 project or an SAP Fiori application. See [Create an HTML5 Project](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/e46be902c7b54f9baaab1870ca553303.html) or [SAP Fiori Elements](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/1488469a315c442fa116ab4449d4ad27.html) for more information.

2.  Use the template wizard to create the relevant project.



### Add an External Service to an SAP Fiori Project

You can add a service to an empty SAP Fiori project or to an SAP Fiori project that doesn't have a service:

1.  Click the *Add to SAP Fiori Project* button.

    If you only have one empty project:

    -   The service is added and is displayed in the *External Resources* section of the storyboard.
    -   The `.service.metadata` file is added to the project folder in the file explorer.

        You can then add a UI and integrate the service.


    If the SAP Fiori project already had a UI, the added service is integrated into the UI.

    If you have more than one empty SAP Fiori project, you must select the project where you want to add the service.




### Add an External Service to a CAP Project

You can select a service from the Service Center and add it as an external service to a CAP Node project:

1.  Open a service and click the *Add to Project* button.
2.  If prompted, select the target CAP Node project to add the external service to.
3.  \(Optional\) You can generate a sample service and select the relevant entities.

    1.  Select *Yes* to add a sample service.
    2.  Select the entities that you want to add.

    > ### Note:  
    > Sample service generation is only available for a project created in the *Full Stack Cloud Application* dev space. It's not available for a project created in the *Full-Stack Application Using Productivity Tools* dev space.

4.  Click *Add*.

    You added the external service to the CAP project. The following changes happen:

    -   The `<service_name>.xml` and `<service_name>.cds` files appear in the *srv* \> *external* folder of the project.
    -   A service section appears in the `package.json` file of the CAP project, which refers to the *srv* \> *external* \> *<service\_name\>.xml* file. This file has the metadata of the service:

        ```
        "<service_name>": {
          "kind": "odata",
          "model": "srv/external/<service_name>"
          "credentials": {
            "destination": "<service_name>"
          }
        }
        ```

    -   The external service is added to the storyboard and *Project Overview*, under *External Resources*.
    -   A run configuration is generated.




### Add an External Service to a Java Project

You can select an OData service from the Service Center and add it as an external resource to a CAP Java project:

1.  From the *Project Overview*, click ![Create new element icon](images/Create_New_icon_5bf149a.png) on the *External Resources* row to add an external resource to the project.

    The Service Center opens.

2.  Click on an OData service to open it and click the *Add to Project* button.

    You added the external service to the Java project. The following changes happen:

    -   The external service is added under the *srv* \> *external* folder.

        You can also see the new service in the *Project Overview*.

    -   The `application.yaml` configuration file is updated for the productive profile and for the local preview, and includes the new service and its destination.
    -   A Maven dependency named `cds-feature-remote-odata`, which is required to enable Remote Services for OData V2 or V4 APIs in the application, is added to the project's `pom.xml` file.

    For more information about what is configured by the Service Center when adding the service to your project, see [Configuring Remote Services](https://cap.cloud.sap/docs/java/cqn-services/remote-services#configuring-remote-services).

    Once the service has been added to the project, you can do the following:

    -   Continue modeling your service. See [Project Overview](https://help.sap.com/docs/bas/developing-cap-application-in-sap-business-application-studio/project-overview-9c8a4d616ab8482a9fc6b0ad660d2257).
    -   Implement a custom handler and consume your external service. See [Consuming Remote Services](https://cap.cloud.sap/docs/java/cqn-services/remote-services#consuming-remote-services).
    -   Test your project. See [Creating Run Configurations for CAP Java Applications](https://help.sap.com/docs/bas/developing-cap-application-in-sap-business-application-studio/creating-run-configurations-for-cap-java-applications).

    For more information, see [CAP Service SDK for Java](https://cap.cloud.sap/docs/java/).




<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_n2k_zx3_qqb"/>

## Add a System

You can add a new system to your SAP Business Application Studio subaccount:

> ### Note:  
> -   If your account isn't a trial account, make sure that the *Business\_Application\_Studio\_Administrator* role is assigned to you in the cockpit. See [Manage Authorizations and Roles](https://help.sap.com/docs/bas/sap-business-application-studio/manage-authorizations-and-roles?version=Cloud&q=SAP%20System%20Service%20Provider).
> -   If you're adding a system based on an ABAP Service Catalog, the following prerequisites apply:
>     -   For SAP S/4HANA on-premise, SAP ERP, or another on-premise ABAP, make sure that the Cloud Connector is set up. See this [blog post](https://blogs.sap.com/2021/08/31/connect-to-external-data-sources-with-sap-business-application-studio/) \(under the **Create a Data Source \(Destination\)** heading in the **Service Catalog** section\).
>     -   For SAP S/4HANA Cloud or the SAP BTP ABAP environment, which both use SAML Bearer Assertion authentication, see [Create a Destination to Connect to SAP Business Application Studio](https://help.sap.com/viewer/6aa39f1ac05441e5a23f484f31e477e7/Latest/en-US/0af2819bbe064a3da455753c8518dd81.html).

1.  Next to the *Systems* search field, click ![Add system icon](images/Add_system-_service_center-_plus_icon_3701d6b.jpg) to add a system.
2.  Enter the system name and URL, and select the system type, proxy, authentication method, and product, if needed.

    > ### Note:  
    > You can select *Basic Authentication* and enter the username and password for your system. This configuration enables you to view the system information without needing to log in each time.

3.  Click *Add*.

