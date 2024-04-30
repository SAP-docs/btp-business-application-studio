<!-- loio1a2f306c9f9b4628bfa143f8e404ef0a -->

# SAP Business Accelerator Hub Service Provider

The SAP Business Accelerator Hub \(formerly known as the SAP API Business Hub\) service provider includes SAP Business Accelerator Hub products, packages, services, and events. You can use the services as data sources in your application or for application development.

> ### Note:  
> The Service Center only shows SAP Business Accelerator Hub products and packages that contain OData services.



## Explore SAP Business Accelerator Hub Services

1.  In the Service Center, from the *Select Provider* dropdown list, select *SAP Business Accelerator Hub*.
2.  The following products are available in the *Select Product* dropdown list:

    -   SAP S/4HANA Cloud
    -   SAP S/4HANA
    -   SAP SuccessFactors
    -   SAP Customer Experience
    -   SAP Business Technology Platform

    Select a product to display its packages.

3.  To explore events, choose the *Event* radio button at the top of the Service Center. For more information, see [Explore SAP S/4HANA or SAP S/4HANA Cloud Events](https://help.sap.com/docs/bas/developing-cap-application-in-sap-business-application-studio/adding-sap-s-4hana-cloud-events-to-your-project#explore-sap-s%2F4hana-or-sap-s%2F4hana-cloud-events) for the *Full Stack Cloud Application* dev space and [Explore SAP S/4HANA or SAP S/4HANA Cloud Events](https://help.sap.com/docs/bas/developing-business-applications-using-productivity-tools/add-sap-s-4hana-cloud-events#explore-sap-s%2F4hana-or-sap-s%2F4hana-cloud-events) for the *Full-Stack Application Using Productivity Tools* dev space.
4.  Click the package to display the services \(APIs\).
5.  Click a service \(![Service icon](images/SC-_service_icon_fc5c112.png)\) and log in with your SAP Business Accelerator Hub credentials, if needed.

    > ### Note:  
    > You must log in with your SAP Business Accelerator Hub credentials once at the beginning of your session.

    After you log in to a service, there's a dot next to the icon \(![Connected Service icon](images/green_dot-_system_available_ac1aa72.jpg)\).

    The service editor displays the service's properties, including the service name, protocol, status, and product.

    You can navigate to the API package by clicking the link with the package name.

    You can also navigate to the service in the SAP Business Accelerator Hub by clicking the service name. From the SAP Business Accelerator Hub, you can click *Try Out* to test the API in the sandbox environment.

6.  Click an entity to see the service details, including entity details and live data:
    1.  You can see the entity's metadata, details, and live data in the *Entities* tab. This helps you choose an entity for your application.

        > ### Note:  
        > The live data only displays up to 20 rows of data for simple data types.

        You can also search for an entity.

    2.  You can see details about the service in the *Properties* tab.

7.  You can click *View Diagram* to see the service entities, their properties, and the relationships between the entities in a new tab.



<a name="loio1a2f306c9f9b4628bfa143f8e404ef0a__section_wgt_3z3_qqb"/>

## Service Actions for Development



### Create a Project from a Service

1.  Click *Create Project*.

    The template wizard displays the projects that you can create from a service. For example, an HTML5 project or an SAP Fiori application. See [Create an HTML5 Project](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/e46be902c7b54f9baaab1870ca553303.html) or [SAP Fiori Elements](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/1488469a315c442fa116ab4449d4ad27.html) for more information.

2.  Use the template wizard to create the relevant project.

    > ### Note:  
    > To run your project with the SAP Business Accelerator Hub sandbox, see the prerequisites in[Developing an HTML5 Application for Cloud Foundry](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/3daa8d63fccb40959cdd0f52aab2d931.html).




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




### Add SAP S/4HANA or SAP S/4HANA Cloud Events

To add SAP S/4HANA or SAP S/4HANA Cloud events for consumption to your project, see [Adding SAP S/4HANA or SAP S/4HANA Cloud Events to Your Project](https://help.sap.com/docs/bas/developing-cap-application-in-sap-business-application-studio/adding-sap-s-4hana-cloud-events-to-your-project) for the *Full Stack Cloud Application* dev space and [Add SAP S/4HANA or SAP S/4HANA Cloud Events](https://help.sap.com/docs/bas/developing-business-applications-using-productivity-tools/add-sap-s-4hana-cloud-events?q=SAP%20System%20Service%20Provider) for the *Full-Stack Application Using Productivity Tools* dev space.

