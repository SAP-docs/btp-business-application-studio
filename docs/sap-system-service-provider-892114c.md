<!-- loio892114ce078b4e17a9ff7e751e6330cc -->

# SAP System Service Provider

The SAP System service provider includes systems from your SAP Business Application Studio subaccount. You can use the services as data sources in your application or for application development.

Login occurs automatically, using the SAP Business Application Studio user credentials.



<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_fpr_sx3_qqb"/>

## Explore SAP System Services

1.  Click the gray arrow to display the SAP Business Application Studio subaccount's destinations \(![Destination](images/SC_API_Hub_product_icon_a999bc7.png)\).
2.  Click the system \(![System](images/SC_system_icon_5178796.png)\) to see the system properties, including the name, description, URL, authentication type, and status.

    There are different types of systems displayed using the SAP Business Application Studio subaccount's destinations:

    -   ABAP Service Catalog

        The destination points to the ABAP system directly. The system shows its service catalogs with a list of services \(V2 and V4, for example\). To see the list of services, click the system and log in with your user credentials, if needed.

        If the service catalog is available and connected \(![Available System](images/SC-_system_connected_icon_1c4c936.png)\), you can search for services within it. Click the search icon \(![](images/service_center_search_a1d4e5e.png)\) and select the relevant service from the command palette.

    -   Service Host

        The destination points to a host. To log in, enter the service path and your credentials, if needed, and click *CONNECT*.

    -   Service URL

        The destination points directly to the service.

    -   Cloud for Customer Catalog

        The destination points to the SAP Cloud for Customer system directly. The system shows its service catalog with a list of services \(V2\). To see the list of services, click the system and log in with your user credentials, if needed.

        If the service catalog is available and connected \(![Available System](images/SC-_system_connected_icon_1c4c936.png)\), you can search for services within it. Click the search icon \(![](images/service_center_search_a1d4e5e.png)\) and select the relevant service from the command palette.

    -   SAP Business One

        The destination points to the SAP Business One system directly. Adding this system enables you to create an SAP BTP application consuming an SAP Business One service.

        > ### Note:  
        > -   Only *No Authentication* or *Basic Authentication* types are supported.
        > -   You must use SAP Business One 10.0 Feature Package \(FP\) 2305 to enable adding a system.

        For more information about SAP Business One and the catalog that exposes a list of services, see [Service Layer API Reference](https://help.sap.com/doc/056f69366b5345a386bb8149f1700c19/10.0/en-US/Service%20Layer%20API%20Reference.html) and [What's New in SAP Business One 10.0, version for SAP HANA](https://help.sap.com/whats-new/753529e7d6144b59b353c94f0cdddbd0?locale=en-US).


    If you maintain credentials in the destination configuration of the account, login can occur automatically. If a system is available, the icon has a green dot \(![Available System](images/SC-_system_connected_icon_1c4c936.png)\).

    If you don't maintain the credentials in the destination configuration of the account, you need to log in manually to open the system information.

3.  Click the gray arrow to display the list of services.
4.  Click a service \(![Service](images/SC-_service_icon_fc5c112.png)\) to see its properties, including the service name, URL, and status.

    If a service is available, the icon has a green dot \(![Available Service](images/green_dot-_system_available_ac1aa72.jpg)\).

5.  Click an entity to see the service details, including entity data and live data:
    1.  You can see the entity's metadata from the *Entity Details* tab.
    2.  You can see a preview of the live production data associated with the entity set from the *Live Data* tab.

        This helps you choose an entity for your application.

        > ### Note:  
        > The live data only displays:
        > 
        > -   Up to 20 rows of data
        > -   Data for simple data types


6.  You can click *View Diagram* to see the service entities, their properties, and the relationships between the entities in a new tab.



<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_dtd_wx3_qqb"/>

## Service Actions for Development



### Create a Project from a Service

1.  Click *Service Actions* \> *Create Project from Service*.

    The template wizard displays the projects that you can create from a service. For example, an HTML5 project or an SAP Fiori application. See [Create an HTML5 Project](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/e46be902c7b54f9baaab1870ca553303.html) or [SAP Fiori Elements](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/1488469a315c442fa116ab4449d4ad27.html) for more information.

2.  Use the template wizard to create the relevant project.



### Add an External Data Model to a CAP Project

You can select a service from the Service Center and add it as an external data model to a CAP Node project:

1.  Open a service and click *Service Actions* \> *Add External Data Model to CAP Project*.
2.  Select the target CAP Node project to add the external data model to.
3.  \(Optional\) You can generate a sample service and select the relevant entities.
    1.  Select *Yes* to add a sample service.
    2.  Select the entities that you want to add.

4.  Click *Add*.

    You added the external data model to the CAP project. The following changes happen:

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




<a name="loio892114ce078b4e17a9ff7e751e6330cc__section_n2k_zx3_qqb"/>

## Add a System

You can add a new system to your SAP Business Application Studio subaccount:

> ### Note:  
> -   If your account isn't a trial account, make sure that the *Business\_Application\_Studio\_Administrator* role is assigned to you in the cockpit. See [Manage Authorizations and Roles](manage-authorizations-and-roles-01e69c5.md).
> -   If you're adding a system based on an ABAP Service Catalog, the following prerequisites apply:
>     -   For SAP S/4HANA on-premise, SAP ERP, or another on-premise ABAP, make sure that the Cloud Connector is set up. See this [blog post](https://blogs.sap.com/2021/08/31/connect-to-external-data-sources-with-sap-business-application-studio/) \(under the **Create a Data Source \(Destination\)** heading in the **Service Catalog** section\).
>     -   For SAP S/4HANA Cloud or the SAP BTP ABAP environment, which both use SAML Bearer Assertion authentication, see [Create a Destination to Connect to SAP Business Application Studio](https://help.sap.com/viewer/6aa39f1ac05441e5a23f484f31e477e7/Latest/en-US/0af2819bbe064a3da455753c8518dd81.html).

1.  Click the relevant button to add a system:
    -   If you are adding a system for the first time, click *Add System*.
    -   If you already have a system, hover over the subaccount and click ![](images/Add_system-_service_center-_plus_icon_3701d6b.jpg) \(Add system\).

        A new tab opens.


2.  Enter the system name and URL and select the system type, proxy, authentication method, and product, if needed.

    > ### Note:  
    > You can select *Basic Authentication* and enter the username and password for your system. This configuration enables you to view the system information without needing to log in each time.

3.  Click *Add*.

