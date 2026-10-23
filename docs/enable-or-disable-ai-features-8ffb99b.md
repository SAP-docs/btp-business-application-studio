<!-- loio8ffb99b1e77a4dceb656c0a6f835a324 -->

# Enable or Disable AI Features

Describes how administrators enable or disable AI features in SAP Business Application Studio, such as AI Chat and Joule, based on the subscription plan.



## Enable or Disable AI in the SAP Build \(build-default\) Plan

In the **build-default** plan, AI features are controlled using a tenant-level setting.

AI is **disabled by default** and must be explicitly enabled by an administrator \(SAP Business Application Studio and Lobby\) using the *Generative AI* toggle available in the *Control Tower* of the Lobby.

For information about enabling or disabling AI features in SAP Build, see [Enabling Generative AI](https://help.sap.com/docs/build-service/build-service-guide/enabling-generative-ai).

> ### Note:  
> The *Generative AI* toggle is available only in the build-default plan.



<a name="loio8ffb99b1e77a4dceb656c0a6f835a324__add_destination"/>

## Disable AI Chat in Other Plans Using a Destination

In all other plans where no Generative AI toggle is available, the **AI Chat feature is controlled using a destination configuration**.

By default, **AI Chat is enabled** and is disabled only when the destination is defined with the appropriate properties.

For general information about creating destinations, see [Create HTTP Destinations](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/create-http-destinations).



### Procedure

1.  Open your subaccount in the SAP BTP cockpit.
2.  Navigate to *Connectivity* \> *Destinations*.

3.  Create a new destination with the following properties:

    ```
    Name: bas-ai-config  
    Type: HTTP  
    Authentication: NoAuthentication  
    URL: https://dummy
    ```

    > ### Note:  
    > -   The destination name and property values must match exactly.
    > -   The URL can be any public or placeholder URL \(for example, `https://dummy`\), as it is not used at runtime.

4.  Add the following additional properties to the destination:


    <table>
    <tr>
    <th valign="top">

    Key
    
    </th>
    <th valign="top">

    Value
    
    </th>
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
    
    *WebIDEAdditionalData*
    
    </td>
    <td valign="top">
    
    `bas_ai_disabled`
    
    </td>
    </tr>
    </table>
    
    > ### Note:  
    > The property names and values must match exactly.




### Result

The AI Chat feature is disabled for all users in the subaccount.



### To Re-Enable AI Chat

-   Delete the **WebIDEAdditionalData** property, or
-   Change its value so that AI Chat is enabled.



## Disable AI Features in the SAP Build Code Plan

In SAP Build Code \(build-code\) plans, AI Chat and generative AI features \(for example, Joule\) are **enabled by default**.



### Disable AI Chat

Configure the destination as described [above](enable-or-disable-ai-features-8ffb99b.md#loio8ffb99b1e77a4dceb656c0a6f835a324__add_destination) to disable the AI Chat feature.



### Disable Generative AI \(Joule\)

To disable Joule, unsubscribe from the *SAP Build Code* service. See [Accessing SAP Build Code](https://help.sap.com/docs/build_code/d0d8f5bfc3d640478854e6f4e7c7584a/07698d7c31284e4db370acdf017cfd14.html#accessing-sap-build-code).

