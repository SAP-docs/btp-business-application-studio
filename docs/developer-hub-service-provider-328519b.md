<!-- loio328519b3b7c04871b63a41350190d4d5 -->

# Developer Hub Service Provider

The Developer Hub service provider offers products and services that are published in the Developer Hub. You can use the services as data sources in your application or for application development.

**Prerequisite**

You created a service instance in the Developer Hub. See [Creating a Service Instance in the API Management, Developer Hub](https://help.sap.com/docs/sap-api-management/sap-api-management/api-access-plan-for-api-business-hub-enterprise?version=Cloud#creating-a-service-instance-in-the-api-management%2C-developer-hub).



<a name="loio328519b3b7c04871b63a41350190d4d5__section_n2k_zx3_qqb"/>

## Add a System

You can add a new system, referring to the Developer Hub instance, from the SAP BTP cockpit in the SAP Business Application Studio subaccount. This destination will be used **to register new developers to the Developer Hub and to subscribe them to new products**, if needed.

> ### Note:  
> To add a system, you must meet these criteria:
> 
> -   You're assigned the *Business\_Application\_Studio\_Administrator* role in the cockpit. See [**Manage Authorizations and Roles**](https://help.sap.com/docs/bas/sap-business-application-studio/manage-authorizations-and-roles?version=Cloud).
> -   You're connected to a space with a subscription to the Developer Hub.

1.  Hover over the subaccount and click ![Add system icon](images/Add_system-_service_center-_plus_icon_3701d6b.jpg) \(Add system\).

    A new tab opens.

2.  Enter the system name and URL and select the system type, proxy, authentication method, and product.

    > ### Note:  
    > You can select *Basic Authentication* and enter the username and password for your system. This configuration enables you to view the system information without needing to log in each time.

3.  Click *Add*.
4.  Create a destination in your SAP Business Application Studio subaccount from the cockpit with the following fields:


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
    
    Provide a name for the system.
    
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
    
    Use the `url` value from the service key of the Developer Hub instance.

    You can find the service key for the service instance that you created \(in the Prerequisite\) in the SAP BTP cockpit, under the *API Management,***Developer Hub** service.

    ![URL value from the service key of the Developer Hub instance](images/service_instance_key-_ABHE-_cropped_9439c8c.png)
    
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
    
    *OAuth2ClientCredentials*
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Client ID*
    
    </td>
    <td valign="top">
    
    Use the `clientId` value from the service key of the Developer Hub instance.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Client Secret*
    
    </td>
    <td valign="top">
    
    Use the `clientSecret` value from the service key of the Developer Hub instance.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Token Service URL*
    
    </td>
    <td valign="top">
    
    Use the `tokenUrl` value from the service key of the Developer Hub instance.
    
    </td>
    </tr>
    </table>
    
5.  In the *Additional Properties* section, configure the following:


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
    
    *WebIDEUsage*
    
    </td>
    <td valign="top">
    
    `apihub_enterprise`
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *apiBusinessHubEnterpriseURL*
    
    </td>
    <td valign="top">
    
    Adding this property is optional.

    This property enables navigation from the Service Center to the Developer Hub.

    Use the following format:

    <subscribed subaccount name\>.<devportal\_url\>.cfapps.<region\>.hana.ondemand.com

    Replace the placeholders with the following information:


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
    
    subscribed subaccount name
    
    </td>
    <td valign="top">
    
    Use the first part of the `tokenUrl` from the destination system of the Developer Hub.

    For example, if the URL is https://abcd123trial.authentication.eu10.hana.ondemand.com/oauth/token

    Use **abcd123trial** for the subscribed subaccount name.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    devportal\_url
    
    </td>
    <td valign="top">
    
    -   For trial, use **integrationsuitetrial-devportal**
    -   For production, use **apibhubenterprise**


    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    region
    
    </td>
    <td valign="top">
    
    Find it in the `tokenUrl`.

    For example, if the `tokenUrl` is https://abcd123trial.authentication.eu10.hana.ondemand.com/oauth/token

    The region is **eu10**.
    
    </td>
    </tr>
    </table>
    

    
    </td>
    </tr>
    </table>
    



<a name="loio328519b3b7c04871b63a41350190d4d5__section_fpr_sx3_qqb"/>

## Explore Developer Hub Services

> ### Note:  
> The Service Center only shows Developer Hub systems and products with OData services.

1.  If it's not already selected, use the *Service* radio button in the Service Center to filter for the relevant providers.
2.  From the *Select a Provider* dropdown list, select Developer Hub.

    Each system points to a Developer Hub instance.

3.  Select a system from the dropdown list to display the products within it.

    There are 2 types of products:

    -   *SAP S/4HANA Cloud Products*

        These products are created from the SAP S/4HANA Cloud business system, which has been connected to the Developer Hub.

        To see the list of products, the following prerequisites apply:

        1.  The Global Account Administrator registered the SAP S/4HANA Cloud system in the SAP BTP cockpit and linked it to the Integration Suite. See [How to discover APIs from business systems in Developer Hub](https://help.sap.com/docs/integration-suite/sap-integration-suite/discover-apis-within-integration-suite-from-various-business-systems#how-to-discover-apis-from-business-systems-in-developer-hub-).
        2.  You have created products from the SAP S/4HANA Cloud system in the Developer Hub. See [Create Products from Business Systems](https://help.sap.com/docs/integration-suite/sap-integration-suite/create-products-from-consumption-bundles).

    -   *Custom Products*

        You must be onboarded to the Developer Hub and subscribed to access the service details for these products.


    Multiple APIs are grouped into a product.

    If the product is available and connected \(![Connected Product icon](images/SC-_system_connected_icon_1c4c936.png)\), you can search for services within it.

4.  Click a product \(![Product icon](images/ABHE_product_icon_c456c90.png)\) to display the services \(APIs\).
5.  Click a service \(![Service icon](images/SC-_service_icon_fc5c112.png)\) to see its properties, including the service name, protocol, and status.

    **SAP S/4HANA Cloud Products**

    You can see the *Entity Details*, *Service Properties*, and *Connectivity Information*, which lets you connect to the live data of the service, if there is a matching destination. The destination is copied from the target system in the Developer Hub to the SAP Business Application Studio account whenever you fetch live data or when you add a service to the project.

    > ### Note:  
    > -   You must have an SAP Business Application Studio Administrator role to create a new destination while fetching live date or adding a service to a project.
    > -   Only destinations created with *BasicAuthentication* are supported.

    If a service is connected, there's a dot next to the icon \(![Connected Service icon](images/green_dot-_system_available_ac1aa72.jpg)\).

    **Custom Products**

    To see the service details, you must be onboarded to the Developer Hub and subscribed to the selected product:

    -   If you aren't onboarded to the Developer Hub, enter your first name, last name, and subscription name and click *Subscribe*.

        You're now subscribed to the product and all services associated with it.

    -   If you're onboarded to the Developer Hub, but you aren't subscribed to the product, enter a subscription name and click *Subscribe*.

        You can now access the service.


    After you're subscribed to the selected product, you'll see the following information:

    -   Subscription details

        This section includes a link to the product in the Developer Hub, the subscription name with a link to the subscription in the Developer Hub, and the subscription date.

    -   Service properties

        This section includes the service name, protocol, and status.


    If a service is connected, there's a dot next to the icon \(![Connected Service icon](images/green_dot-_system_available_ac1aa72.jpg)\).

    > ### Note:  
    > -   If a service is unavailable and the target endpoint of the service requires authentication, make sure that the target endpoint is configured to be authenticated via [Basic Authentication](https://help.sap.com/docs/SAP_CLOUD_PLATFORM_API_MANAGEMENT/66d066d903c2473f81ec33acfe2ccdb4/693c0d1720644d57918ed77acc6a95ef.html?locale=en-US&version=Cloud). See the "Configure API Management to Use the Basic Authentication Policy" section in this [blog post](https://blogs.sap.com/2019/05/23/securing-your-microservice-on-sap-cloud-platform-using-api-management-with-basic-authentication-for-last-mile-security/).
    > -   We recommend using the [verify API key](https://help.sap.com/docs/SAP_CLOUD_PLATFORM_API_MANAGEMENT/66d066d903c2473f81ec33acfe2ccdb4/4d15a0427494452dbb42a319e9bb420f.html?locale=en-US&version=Cloud) policy to ensure secure access to the service. This policy is added in the PreFlow of the ProxyEndpoint of the corresponding API proxy.

6.  Click an entity to see the service details, including entity details and live data:
    1.  You can see the *Entity Details* and *Live Data* in the *Entities* tab. This helps you choose an entity for your application.

        > ### Note:  
        > The *Live Data* only displays up to 20 rows of data for simple data types.

        You can also search for an entity.

    2.  You can see *Service Properties* in the *Properties* tab.

7.  You can click *View Diagram* from the *Entities* tab to see the service entities, their properties, and the relationships between the entities in a new tab.



<a name="loio328519b3b7c04871b63a41350190d4d5__section_dtd_wx3_qqb"/>

## Service Actions for Development

If the SAP Business Application Studio Administrator role is assigned to you, after creating a project or adding an external service, the destination to the selected product subscription is generated in the SAP BTP cockpit. The destination enables you to preview live data and run your deployed application. For *Custom Products*, the destination includes information about the product subscription, including the subscription's API key and the subscription's ID.

If you don’t have the SAP Business Application Studio Administrator role, the destination isn't generated with your subscription.



### Create a Project from a Service

1.  Click *Create Project*.

    The template wizard displays the projects that you can create from a service. For example, an HTML5 project or an SAP Fiori application. See [Create an HTML5 Project](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/e46be902c7b54f9baaab1870ca553303.html) or [SAP Fiori Elements](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/1488469a315c442fa116ab4449d4ad27.html) for more information.

2.  Use the template wizard to create the relevant project.

> ### Note:  
> For *Custom Products* only: If the deployed application to Cloud Foundry fails to bring data from the service, make sure that in the Developer Hub, the [Assign Message](https://help.sap.com/docs/SAP_CLOUD_PLATFORM_API_MANAGEMENT/66d066d903c2473f81ec33acfe2ccdb4/523efe6d0a9d43beb5d62ad07937578f.html?locale=en-US&version=Cloud) policy is used in the PreFlow of the ProxyEndpoint of the API proxy.
> 
> We use the Assign Message policy to override the HTTP request Accept-Encoding header:
> 
> ```
> <!-- This policy can be used to create or modify the standard HTTP request and response messages -->
> <AssignMessage async="false" continueOnError="false" enabled="true" xmlns='http://www.sap.com/apimgmt'>
> 
>     <!-- Sets a new value to the existing parameter -->
>     <Set>
>         <Headers>
>              <Header name="Accept-Encoding">identity</Header>
>          </Headers>
>     </Set>
>     <IgnoreUnresolvedVariables>false</IgnoreUnresolvedVariables>
>     <AssignTo createNew="false" type="request"></AssignTo>
> </AssignMessage>
> 
> ```



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
    -   A service section appears in the `package.json` file of the CAP project, which refers to the *srv* \> *external* \> *<service\_name\>.cds* file. This file has the metadata of the service:

        ```
        "<service_name>": {
          "kind": "odata",
          "model": "srv/external/<service_name>"
          "[production]": {
          "credentials": {
            "destination": "<service_name>",
            "path": "<service_path>"
          }
        },
        "csrf": true,
        "csrfInBatch": true
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


