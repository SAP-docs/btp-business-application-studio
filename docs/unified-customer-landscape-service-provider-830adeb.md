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
    
        Enter the URL of the the SAP S/4HANA Cloud target system.

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
    
        ***true***


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        *WebIDEEnabled*


    
    </td>
    <td valign="top">
    
        ***true***


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        *x-system-type*


    
    </td>
    <td valign="top">
    
        ***SAP S/4HANA Cloud***

    This value is displayed in the *System Landscape* \> *System Details* \> *System Type* field in the SAP BTP cockpit.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        *x-correlation-id*


    
    </td>
    <td valign="top">
    
        ***sap.s4:communicationScenario:SAP\_COM\_<XXXX\>***

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

1.  Click the gray arrow to display the available systems \(![System](images/SC_API_Hub_product_icon_a999bc7.png)\) for the account.
2.  Click the gray arrow to display the packages \(![Package](images/SC_system_icon_5178796.png)\) under a system.

    If the package is available and connected \(![Available Package](images/SC-_system_connected_icon_1c4c936.png)\), you can search for services within it. Click the search icon \(![](images/service_center_search_a1d4e5e.png)\) and select the relevant service from the command palette.

3.  Click the gray arrow to display the services under a package.
4.  Click a service \(![Service](images/SC-_service_icon_fc5c112.png)\) to see its properties, including the service name, protocol, version, URL, and status.

    If there are many destinations available for the Unified Customer Landscape service, you can see the *Connectivity Information* for the specific destination that you're exploring. You can see the destination's name, authentication, proxy, consumption bundle name and ID, and correlation ID.

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



<a name="loio830adebf4ab3470c9c3278188ceef8a1__section_dtd_wx3_qqb"/>

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


