<!-- loio892114ce078b4e17a9ff7e751e6330cc -->

# SAP System Service Provider

The SAP System service provider includes systems from your SAP Business Application Studio subaccount. You can use the services as data sources in your application or for application development.

Login occurs automatically, using the SAP Business Application Studio user credentials. If you don't maintain the credentials in the destination configuration of the account, you need to log in manually to open the system information.



<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_fpr_sx3_qqb"/>

## Explore SAP System Services

1.  From the *Select Provider* dropdown list, select *SAP System*.
2.  The Service Center displays a list of catalogs and a separate list of single services.

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



3.  Click a catalog \(![Connected catalog icon](images/SC-_system_connected_icon_1c4c936.png)\) to open it and display the list of services, or click a service \(![Service icon](images/SC-_service_icon_fc5c112.png)\) to see its properties, including the name, description, authentication type, status, and URL.
4.  Click an entity to see the service details. You can see the entity's metadata, details, and live data in the *Entities* tab. This helps you choose an entity for your application.

    > ### Note:  
    > The live data only displays up to 20 rows of data for simple data types.

    You can also search for an entity.

    You can see details about the system and service in the *Properties* tab.

5.  You can click *View Diagram* to see the service entities, their properties, and the relationships between the entities in a new tab.



<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_dtd_wx3_qqb"/>

## Service Actions for Development



### Create a Project from a Service

1.  Click *Create Project*.

    The template wizard displays the projects that you can create from a service. For example, an HTML5 project or an SAP Fiori application. See [Create an HTML5 Project](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/e46be902c7b54f9baaab1870ca553303.html) or [SAP Fiori Elements](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/1488469a315c442fa116ab4449d4ad27.html) for more information.

2.  Use the template wizard to create the relevant project.



### Add an External Service to an SAP Fiori Project

You can add a service to an empty SAP Fiori project or to an SAP Fiori project that doesn't have a service:

1.  Click *Add to SAP Fiori Project*.

    If you only have one empty project:

    -   The service is added and is displayed in the *External Resources* section of the storyboard.
    -   The `.service.metadata` file is added to the project folder in the file explorer.

        You can then add a UI and integrate the service.


    If the SAP Fiori project already had a UI, the added service is integrated into the UI.

    If you have more than one empty SAP Fiori project, you must select the project where you want to add the service.




### Add an External Service to a CAP Project

You can select a service from the Service Center and add it as an external service to a CAP Node project:

1.  Open a service and click *Add to CAP Project*.
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

    -   If you added a sample service with the relevant entities, the `<service_name>.cds` and the `<service_name>.js` files appear in the *srv* \> *external* folder of the CAP project.
    -   The external service is added to the storyboard, under *External Resources*.




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

