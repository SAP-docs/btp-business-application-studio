<!-- loio830adebf4ab3470c9c3278188ceef8a1 -->

# Unified Customer Landscape Service Provider

After registering an SAP S/4HANA Cloud system, you can explore APIs, preview live data, and view entity details of APIs from the Unified Customer Landscape.

**Prerequisites**

-   Your administrator connected an SAP S/4HANA Cloud system with an SAP BTP global account. See [Registering an SAP System](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/2ffdaff0f1454acdb046876045321c91.html?locale=en-US&version=Cloud).

-   Your administrator created a *Developing with SAP Business Application Studio* formation type in the SAP BTP cockpit to assign the SAP S/4HANA Cloud system to a subaccount. See [Including SAP Systems in a Formation](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/68b04fa73aa740cb96ed380a85a4761a.html?locale=en-US&version=Cloud).
-   You created a destination in your SAP Business Application Studio subaccount from the cockpit with the following fields:


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

    Select the authentication based on your S/4HANA Cloud system security policy.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *User*


    
    </td>
    <td valign="top">

    Enter your username.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *Password*


    
    </td>
    <td valign="top">

    Enter your password.


    
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

    The system type is displayed in the *System Type* column of the *System Landscape* page in the SAP BTP cockpit.

    This property is required.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *x-correlation-id*


    
    </td>
    <td valign="top">

    ***sap.s4:communicationScenario:SAP\_COM\_0001***

    The number should be changed to the specific com\_scenario for which the destination is relevant.

    This property is required.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *x-system-url*


    
    </td>
    <td valign="top">

    ***https://myXXXXX.s4hana.ondemand.com***

    The URL is displayed in the *URL* column of the *System Landscape* page in the SAP BTP cockpit.

    This property is optional.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    *x-system-name*


    
    </td>
    <td valign="top">

    Enter the name of the SAP S/4HANA Cloud target system.

    The name is displayed in the *System Name* column of the *System Landscape* page in the SAP BTP cockpit.

    This property is optional.


    
    </td>
    </tr>
    </table>
    



<a name="loio830adebf4ab3470c9c3278188ceef8a1__section_fpr_sx3_qqb"/>

## Explore SAP System Services

1.  Click the gray arrow to display the SAP Business Application Studio subaccount's destinations \(![](images/SC_API_Hub_product_icon_a999bc7.png)\).
2.  Click the system \(![](images/SC_system_icon_5178796.png)\) to see the system properties, including the name, description, URL, authentication type, and status.

    There are different types of systems displayed using the SAP Business Application Studio subaccount's destinations:

    -   ABAP Service Catalog

        The destination points to the ABAP system directly. The system shows its service catalogs with a list of services \(V2 and V4, for example\). To see the list of services, click the system and log in with your user credentials, if needed.

        If the service catalog is available and connected \(![](images/SC-_system_connected_icon_1c4c936.png)\), you can search for services within it. Click the search icon \(![](images/service_center_search_a1d4e5e.png)\) and select the relevant service from the command palette.

    -   Service Host

        The destination points to a host. To log in, enter the service path and your credentials, if needed, and click *CONNECT*.

    -   Service URL

        The destination points directly to the service.


    If you maintain credentials in the destination configuration of the account, login can occur automatically. If a system is available, the icon has a green dot \(![](images/SC-_system_connected_icon_1c4c936.png)\).

    If you don't maintain the credentials in the destination configuration of the account, you need to log in manually to open the system information.

3.  Click the gray arrow to display the list of services.
4.  Click a service \(![](images/SC-_service_icon_fc5c112.png)\) to see its properties, including the service name, protocol, URL, and status.

    If a service is available, the icon has a green dot \(![](images/green_dot-_system_available_ac1aa72.jpg)\).

5.  Click an entity to see the service details, including entity data and live data:
    1.  You can see the entity's metadata from the *Entity Details* tab.
    2.  You can see a preview of the live production data associated with the entity set from the *Live Data* tab.

        This helps you choose an entity for your application.

        > ### Note:  
        > The live data only displays:
        > 
        > -   Up to 20 rows of data
        > -   Data for simple data types





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


