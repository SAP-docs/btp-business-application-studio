<!-- loio7e49887e6fd34182bebeca5a6841a0cc -->

# Connecting to External Systems

To connect any on-premise system from SAP Business Application Studio, you must create a destination. Additionally, some business cases will also require a destination to perform OData service exploration and to select an OData service for creating and viewing applications.



<a name="loio7e49887e6fd34182bebeca5a6841a0cc__context_rjk_wrf_3kb"/>

## Context

 SAP Business Application Studio dev spaces include a built-in web proxy that allows you access to on premise systems \(such as ABAP systems, Git on-premise, npm on-premise, etc.\)

> ### Note:  
> Always protect your access to an external system, including a Private Artifact Repository manager, an on-premise system, or a trusted system.

The proxy requires destination configuration to your on-premise system from your Cloud Foundry subaccount.

HTTP requests including the host and port provided with this destination URL made from the dev space using the proxy, will be transferred through this destination.

You can create a destination that points to your system, either from the Service Center or from the SAP BTP cockpit.



<a name="loio7e49887e6fd34182bebeca5a6841a0cc__steps_orm_myk_m4"/>

## Procedure

1.  **Create a Destination from the Service Center for OData Services**

    See [Add a System](sap-system-service-provider-892114c.md#loio892114ce078b4e17a9ff7e751e6330cc__section_n2k_zx3_qqb) to add a destination from the Service Center with all the required properties.

    **Create a Destination from the SAP BTP Cockpit**

2.  Open the SAP BTP cockpit in the Cloud Foundry environment and go to the subaccount that is subscribed to SAP Business Application Studio.

3.  Create a destination with the system endpoint URL. For more information, see [Create HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/783fa1c418a244d0abb5f153e69ca4ce.html).

4.  Add the following additional properties to the created destination:


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
    
5.  Set the *WebIDEUsage* property for your destination type:


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
    
        **ABAP System**


    
    </td>
    <td valign="top">
    
        *WebIDEUsage* value: `odata_abap,dev_abap` 

    `odata_abap`:

    For exploring ABAP service catalogs

    `dev_abap`:

    For deploying to the SAPUI5 ABAP Repository and developing extension projects.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        **SAP Cloud for Customer**


    
    </td>
    <td valign="top">
    
        *WebIDEUsage* value: `odata_c4c`

    Used to explore SAP Cloud for Customer catalogs.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        **Service URL**


    
    </td>
    <td valign="top">
    
        *WebIDEUsage* value: `odata_gen` 

    For an absolute URL, you can use the full URL option \(*WebIDEAdditionalData* property and *full\_url* as the value\). For a service host, the relative URL should be added upon login.


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
        **SAP API Business Hub**


    
    </td>
    <td valign="top">
    
        *WebIDEUsage* value: `apihub_sandbox`


    
    </td>
    </tr>
    </table>
    
6.  Choose *Save*.

7.  If you are using an on-premise system, configure the Cloud Connector so that your system is correctly exposed. See [Cloud Connector](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/e6c7616abb5710148cfcf3e75d96d596.html).

    If you don't have any Cloud Connector to use, you can set up a Cloud Connector on your local machine/VM.

    > ### Note:  
    > In the *Access Control* tab of the Cloud Connector, grant access to all relevant URL paths \(Resources\) to access the system \(for*Access Policy*, select the *Path and all sub-paths* option\).
    > 
    > For example: `/sap/opu/odata`, `/sap/bc/adt`, and `/sap/bc/ui2/app_index/` .

8.  Once the destination has been created, SAP Business Application Studio developers can use it in their dev spaces. See [Accessing On Premise Systems](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/e72930c96b664e3ea4ce5288eb84075f.html).

    > ### Note:  
    > If you cannot access the on-premise system and there is an allowlist in your network, make sure you allowed BAS inbound IPs as described in [SAP Business Application Studio Availability](sap-business-application-studio-availability-8509485.md).


