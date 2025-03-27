<!-- loio830adebf4ab3470c9c3278188ceef8a1 -->

# Unified Customer Landscape Service Provider

The Unified Customer Landscape service provider includes packages and services from registered SAP S/4HANA Cloud systems in SAP BTP. You can use the services as data sources in your application or for application development.

**Prerequisites**

-   Your administrator registered an SAP S/4HANA Cloud system in an SAP BTP global account.

    See [Enabling System Landscape for SAP Business Application Studio](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/272ca23a7ebf4532922b226dc0310c45.html).

-   Your administrator created a *Developing with SAP Business Application Studio* formation type in the SAP BTP cockpit to assign the SAP S/4HANA Cloud system to an SAP Business Application Studio subaccount.
-   You created a destination in your SAP Business Application Studio subaccount for each consumption bundle from the SAP BTP cockpit with the following fields:


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
    
    *Name*
    
    </td>
    <td valign="top">
    
    Provide a name of your choice.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Type*
    
    </td>
    <td valign="top">
    
    *HTTP*
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *URL*
    
    </td>
    <td valign="top">
    
    Enter the URL of the SAP S/4HANA Cloud target system.

    This value is displayed in the *System Landscape* \> *System Details* \> *URL* field in the SAP BTP cockpit.

    > ### Note:  
    > You must be a global account administrator to see the *System Landscape*.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Proxy Type*
    
    </td>
    <td valign="top">
    
    *Internet*
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Authentication*
    
    </td>
    <td valign="top">
    
    Select the authentication based on your SAP S/4HANA Cloud system inbound communication settings.
    
    </td>
    </tr>
    </table>
    
    In the *Additional Properties* section, you configured the following:


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
    
    *HTML5.DynamicDestination*
    
    </td>
    <td valign="top">
    
    `true`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *WebIDEEnabled*
    
    </td>
    <td valign="top">
    
    `true`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *x-system-type*
    
    </td>
    <td valign="top">
    
    `SAP S/4HANA Cloud`

    This value is displayed in the *System Landscape* \> *System Details* \> *System Type* field in the SAP BTP cockpit.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *x-correlation-id*
    
    </td>
    <td valign="top">
    
    `sap.s4:communicationScenario:SAP_COM_<XXXX>`

    Replace the number based on the relevant com\_scenario for the destination.

    This value is displayed in the *System Landscape* \> *System Details* \> *Consumption Bundles* \> *Correlation IDs* column in the SAP BTP cockpit.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *x-system-id*
    
    </td>
    <td valign="top">
    
    Enter the name of the system ID.

    This value is displayed in the *System Landscape* \> *System Details* \> *System ID* field in the SAP BTP cockpit.
    
    </td>
    </tr>
    </table>
    



<a name="loio830adebf4ab3470c9c3278188ceef8a1__section_fpr_sx3_qqb"/>

## Explore Unified Customer Landscape Services

1.  Use the *Service* or *Event* radio button in the Service Center to filter for the relevant providers.

    For more information, see [Explore SAP S/4HANA or SAP S/4HANA Cloud Events](https://help.sap.com/docs/bas/developing-cap-application-in-sap-business-application-studio/adding-sap-s-4hana-cloud-events-to-your-project#explore-sap-s%2F4hana-or-sap-s%2F4hana-cloud-events) for the *Full Stack Cloud Application* dev space and [Explore SAP S/4HANA or SAP S/4HANA Cloud Events](https://help.sap.com/docs/bas/developing-business-applications-using-productivity-tools/add-sap-s-4hana-cloud-events#explore-sap-s%2F4hana-or-sap-s%2F4hana-cloud-events) for the *Full-Stack Application Using Productivity Tools* dev space.

2.  From the *Select a Provider* dropdown list, select *Unified Customer Landscape*.
3.  Select a system to display its packages \(![Package icon](images/SC_system_icon_5178796.png)\) under a system.

    If the package is available and connected \(![Connected Package icon](images/SC-_system_connected_icon_1c4c936.png)\), you can search for services within it.

4.  Click a package to display its services.
5.  Click a service \(![Service icon](images/SC-_service_icon_fc5c112.png)\) to display its properties, including the service name, protocol, version, URL, and status.

    In the *Connectivity Information*, you can see the consumption bundle name, ID, and correlation ID. If there is a destination, you can select it and see its name and authentication.

    If a service is connected, there's a dot next to the icon \(![Connected Service](images/green_dot-_system_available_ac1aa72.jpg)\).

6.  Click an entity to see the service details, including entity details and live data:
    1.  You can see the entity's metadata, details, and live data in the *Entities* tab. This helps you choose an entity for your application.

        > ### Note:  
        > The live data only displays up to 20 rows of data for simple data types.

        You can also search for an entity.

    2.  You can see details about the service in the *Properties* tab.

7.  You can click *View Diagram* to see the service entities, their properties, and the relationships between the entities in a new tab.



<a name="loio830adebf4ab3470c9c3278188ceef8a1__section_dtd_wx3_qqb"/>

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




### Add SAP S/4HANA or SAP S/4HANA Cloud Events

To add SAP S/4HANA or SAP S/4HANA Cloud events for consumption to your project, see [Adding SAP S/4HANA or SAP S/4HANA Cloud Events to Your Project](https://help.sap.com/docs/bas/developing-cap-application-in-sap-business-application-studio/adding-sap-s-4hana-cloud-events-to-your-project) for the *Full Stack Cloud Application* dev space and [Add SAP S/4HANA or SAP S/4HANA Cloud Events](https://help.sap.com/docs/bas/developing-business-applications-using-productivity-tools/add-sap-s-4hana-cloud-events?q=SAP%20System%20Service%20Provider) for the *Full-Stack Application Using Productivity Tools* dev space.

