<!-- loio1a2f306c9f9b4628bfa143f8e404ef0a -->

# SAP API Business Hub Service Provider

The SAP API Business Hub service provider includes SAP API Business Hub products, packages, and services. The services can be used as data sources in your application or for application development.

> ### Note:  
> Only SAP API Business Hub products and packages that contain OData services are displayed in the Service Center.

When the Service Center opens, the SAP API Business Hub is displayed with the following SAP API Business Hub products:

-   SAP S/4HANA Cloud
-   SAP S/4HANA
-   SAP SuccessFactors
-   SAP Customer Experience
-   SAP Business Technology Platform



## Explore SAP API Business Hub Services

1.  To display the packages, click the gray arrow next to the product.
2.  To display the services, click the gray arrow next to the package.
3.  Click a service and log in with your SAP API Business Hub credentials.

    > ### Note:  
    > You must log in with your SAP API Business Hub credentials one time per session.

    The service's properties, including the service name, protocol, status, product, package, URL, and entity details are displayed in the service editor.

    You can navigate to the API package by clicking ![](images/API_package_icon_dca6894.jpg).

    You can navigate to the service in the SAP API Business Hub by clicking the URL. From the SAP API Business Hub, you can click *Try Out* to test the API in the sandbox environment.




<a name="loio1a2f306c9f9b4628bfa143f8e404ef0a__section_wgt_3z3_qqb"/>

## Service Actions for Development

1.  You can create a project from a service:
    1.  Click *Service Actions* \> *Create Project from Service*.

        The template wizard displays the projects that can be created from a service. For example, an HTML5 project or an SAP Fiori application. See [Create an HTML5 Project](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/e46be902c7b54f9baaab1870ca553303.html) or [SAP Fiori Elements](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/1488469a315c442fa116ab4449d4ad27.html) for more information.

    2.  Use the template wizard to create the relevant project.

        > ### Note:  
        > To run your project with the SAP API Business Hub sandbox, see the prerequisites in [Run Your HTML5 Application with the SAP API Business Hub](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/3fca8fcfe27a43c0b8bbde8fe2113e82.html "You can run an HTML5 application locally with an SAP API Business Hub service.") :arrow_upper_right:.

2.  You can select a service from the Service Center and add it as an external data model to a CAP Node project:
    1.  Open a service and click *Service Actions* \> *Add Data Model to CAP Project*.
    2.  Select the target CAP Node project to add the data model to.
    3.  \(Optional\) You can generate a sample service and select the relevant entities.
        1.  Select *Add a Sample Service*.
        2.  Select the entities that you want to add.
    4.  Click *Add*.

        You added the data model to the CAP project. The following changes happen:

        -   The `<service_name>.xml` and `<service_name>.csn` files appear in the *srv* \> *external* folder of the project.
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

        If you added a sample service with the relevant entities, the `<service_name>.cds` and the `<service_name>.js` files appear in the *srv* \> *external* folder of the CAP project.


