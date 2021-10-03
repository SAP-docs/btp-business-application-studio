<!-- loio7e49887e6fd34182bebeca5a6841a0cc -->

# Connecting to External Systems

For applications that do not need to run on Cloud Foundry, establish a connection to an external system by creating one destination for multi-usage.



<a name="loio7e49887e6fd34182bebeca5a6841a0cc__context_rjk_wrf_3kb"/>

## Context

You can access on-premise SAP ABAP systems using a built-in Web Proxy. Your dev space includes a built-in Web Proxy \(`http://localhost:8887`\) that allows you access to on-premise systems. It is already configured with the HTTP\_PROXY and the HTTPS\_PROXY environment variables. The proxy requires destination configuration to your on-premise system from your Cloud Foundry Subaccount.



<a name="loio7e49887e6fd34182bebeca5a6841a0cc__steps_orm_myk_m4"/>

## Procedure

1.  Open SAP BTP cockpit in the Cloud Foundry environment and go to the subaccount that is subscribed to SAP Business Application Studio.

2.  Create a destination of type HTTP that points to your system. For more information, see [HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/783fa1c418a244d0abb5f153e69ca4ce.html). HTTP requests including the host and port provided with this destination URL made from your dev space using the proxy, will be transferred through this destination.

3.  Add these new properties:


    <table>
    <tr>
    <th>

    Property


    
    </th>
    <th>

    Value


    
    </th>
    </tr>
    <tr>
    <td>

    `WebIDEEnabled`


    
    </td>
    <td>

    `true`


    
    </td>
    </tr>
    <tr>
    <td>

    `HTML5.DynamicDestination`


    
    </td>
    <td>

    `true`


    
    </td>
    </tr>
    </table>
    
4.  Set the *WebIDEUsage* property for your destination type:


    <table>
    <tr>
    <th>

    Destination Type


    
    </th>
    <th>

    Properties


    
    </th>
    </tr>
    <tr>
    <td>

    **Service Catalog**


    
    </td>
    <td>

    *WebIDEUsage* includes `odata_abap` and `dev_abap` \(to deploy\).

    See [Developing an SAP Fiori Application Based on an SAP S/4HANA System](https://help.sap.com/viewer/584e0bcbfd4a4aff91c815cefa0bce2d/Cloud/en-US/22f3401b2e464344943f2a6abf05d092.html).


    
    </td>
    </tr>
    <tr>
    <td>

    **Service URL**


    
    </td>
    <td>

    *WebIDEUsage* includes `odata_gen`. You can use the full URL option or not.

    See [Consume an OData Service](https://help.sap.com/viewer/584e0bcbfd4a4aff91c815cefa0bce2d/Cloud/en-US/ff9d287ba8ef4011baaad58d516dce3f.html).


    
    </td>
    </tr>
    <tr>
    <td>

    **SAP API Business Hub**


    
    </td>
    <td>

    *WebIDEUsage* includes `apihub_catalog` and `api_sandbox`.

    See [Run Your Application with the SAP API Business Hub](https://help.sap.com/viewer/584e0bcbfd4a4aff91c815cefa0bce2d/Cloud/en-US/54ce98a4f9cf454e8b18224623c00aba.html).


    
    </td>
    </tr>
    </table>
    
5.  If you are using an on-premise system:

    1.  Configure the Cloud Connector so that your system is correctly exposed. See [Cloud Connector](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e6c7616abb5710148cfcf3e75d96d596.html).

        If you don't have any Cloud Connector to use, you can set up a Cloud Connector on your local machine/VM by following [this tutorial](https://developers.sap.com/tutorials/cp-connectivity-install-cloud-connector.html).

    2.  Add a new property with *WebIDEEnabled* as the name and *true* as the value.

6.  Choose *Save*.


