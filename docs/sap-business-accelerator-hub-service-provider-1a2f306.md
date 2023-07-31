<!-- loio1a2f306c9f9b4628bfa143f8e404ef0a -->

# SAP Business Accelerator Hub Service Provider

The SAP Business Accelerator Hub \(formerly known as the SAP API Business Hub\) service provider includes SAP Business Accelerator Hub products, packages, and services. You can use the services as data sources in your application or for application development.

> ### Note:  
> The Service Center only shows SAP Business Accelerator Hub products and packages with OData services.



## Explore SAP Business Accelerator Hub Services

1.  From the Service Center, click the gray arrow to display the SAP Business Accelerator Hub products:

    SAP S/4HANA Cloud, SAP S/4HANA, SAP SuccessFactors, SAP Customer Experience, and SAP Business Technology Platform

2.  Click the gray arrow next to the product \(![Product](images/SC_API_Hub_product_icon_a999bc7.png)\) to display the packages.

    If the package is available and connected \(![Available Package](images/SC-_system_connected_icon_1c4c936.png)\), you can search for services within it. Click the search icon \(![](images/service_center_search_a1d4e5e.png)\) and select the relevant service from the command palette.

3.  Click the gray arrow next to the package \(![Available Package](images/SC-_system_connected_icon_1c4c936.png)\) to display the services \(APIs\).
4.  Click a service \(![Service](images/SC-_service_icon_fc5c112.png)\) and log in with your SAP Business Accelerator Hub credentials, if needed.

    > ### Note:  
    > You must log in with your SAP Business Accelerator Hub credentials one time at the beginning of your session.

    After you log in to a service, the icon has a green dot \(![Available Service](images/green_dot-_system_available_ac1aa72.jpg)\).

    The service editor displays the service's properties, including the service name, protocol, status, and product.

    You can navigate to the API package by clicking ![Open API Package](images/go_to_API_59e0aba.png).

    You can also navigate to the service in the SAP Business Accelerator Hub by clicking the URL. From the SAP Business Accelerator Hub, you can click *Try Out* to test the API in the sandbox environment.

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



<a name="loio1a2f306c9f9b4628bfa143f8e404ef0a__section_wgt_3z3_qqb"/>

## Service Actions for Development



### Create a Project from a Service

1.  Click *Service Actions* \> *Create Project from Service*.

    The template wizard displays the projects that you can create from a service. For example, an HTML5 project or an SAP Fiori application. See [Create an HTML5 Project](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/e46be902c7b54f9baaab1870ca553303.html) or [SAP Fiori Elements](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/1488469a315c442fa116ab4449d4ad27.html) for more information.

2.  Use the template wizard to create the relevant project.

    > ### Note:  
    > To run your project with the SAP Business Accelerator Hub sandbox, see the prerequisites in[Developing an HTML5 Application for Cloud Foundry](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/3daa8d63fccb40959cdd0f52aab2d931.html).




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




### Add SAP S/4HANA Cloud Events

To add SAP S/4HANA Cloud events for consumption to your project, see [Adding SAP S/4HANA Cloud Events to Your Project](https://help.sap.com/viewer/9c36fdb911ae4cadab467a314d9e331f/Cloud/en-US/bf6fa41b00f54a4cb1699975edc7fa94.html "Add events for consumption from SAP S/4HANA Cloud to your Full Stack Cloud Application project.") :arrow_upper_right: for the *Full Stack Cloud Application* dev space and [Add SAP S/4HANA Cloud Events](https://help.sap.com/viewer/f9814e8df1cb43e1890e0f8d25374b8f/Cloud/en-US/5d3cebeddeee458186f1896cfe656f6a.html "Add events for consumption from SAP S/4HANA Cloud to your Full-Stack Application Using Productivity Tools project.") :arrow_upper_right: for the *Full-Stack Application Using Productivity Tools* dev space.

