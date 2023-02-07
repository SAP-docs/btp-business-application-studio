<!-- loio7e49887e6fd34182bebeca5a6841a0cc -->

# Connecting to External Systems

For applications that do not need to run on Cloud Foundry, establish a connection to an external system by creating one destination for multi-usage.



<a name="loio7e49887e6fd34182bebeca5a6841a0cc__context_rjk_wrf_3kb"/>

## Context

You can access on-premise SAP ABAP systems using a built-in Web Proxy. Your dev space includes a built-in Web Proxy \(`http://localhost:8887`\) that allows you access to on-premise systems. It is already configured with the HTTP\_PROXY and the HTTPS\_PROXY environment variables. The proxy requires destination configuration to your on-premise system from your Cloud Foundry Subaccount.

You can create a destination that points to your system, either from the Service Center or from the SAP BTP cockpit.



<a name="loio7e49887e6fd34182bebeca5a6841a0cc__steps_orm_myk_m4"/>

## Procedure

1.  **Create a Destination from the Service Center**

    See [Add a System](sap-system-service-provider-892114c.md#loio892114ce078b4e17a9ff7e751e6330cc__section_n2k_zx3_qqb) to add a destination from the Service Center with all the required properties.

    **Create a Destination from the SAP BTP Cockpit**

2.  Open the SAP BTP cockpit in the Cloud Foundry environment and go to the subaccount that is subscribed to SAP Business Application Studio.

3.  Add the following properties in the SAP BTP cockpit:


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

    `WebIDEEnabled`


    
    </td>
    <td valign="top">

    `true`


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    `HTML5.DynamicDestination`


    
    </td>
    <td valign="top">

    `true`


    
    </td>
    </tr>
    </table>
    
4.  Set the *WebIDEUsage* property for your destination type:


    <table>
    <tr>
    <th valign="top">

    Destination Type


    
    </th>
    <th valign="top">

    Properties


    
    </th>
    </tr>
    <tr>
    <td valign="top">

    **ABAP Service Catalog**


    
    </td>
    <td valign="top">

    **WebIDEUsage** includes `odata_abap` and `dev_abap`.

    `odata_abap`:

    For exploring ABAP service catalogs

    `dev_abap`:

    For deploying to the SAPUI5 ABAP Repository


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    **SAP Cloud for Customer Service Catalog**


    
    </td>
    <td valign="top">

    *WebIDEUsage* includes `odata_c4c` to explore SAP Cloud for Customer catalogs.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    **Service URL**


    
    </td>
    <td valign="top">

    *WebIDEUsage* includes `odata_gen`.

    For an absolute URL, you can use the full URL option \(*WebIDEAdditionalData* property and *full\_url* as the value\). For a service host, the relative URL should be added upon login.


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    **SAP API Business Hub**


    
    </td>
    <td valign="top">

    *WebIDEUsage* includes `apihub_sandbox`.


    
    </td>
    </tr>
    </table>
    
5.  If you are using an on-premise system, configure the Cloud Connector so that your system is correctly exposed. See Cloud Connector.

    If you don't have any Cloud Connector to use, you can set up a Cloud Connector on your local machine/VM.

6.  Choose *Save*.

    See [HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/783fa1c418a244d0abb5f153e69ca4ce.html) for more information. HTTP requests including the host and port provided with this destination URL made from your dev space using the proxy, will be transferred through this destination.


-   **[Requirements for Connecting to ABAP Systems](requirements-for-connecting-to-abap-systems-49df13c.md "The following is prerequisite information for connecting to ABAP systems.")**  
The following is prerequisite information for connecting to ABAP systems.

