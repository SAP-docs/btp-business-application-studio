<!-- loiod54ddfc1bc4f45b19dabfa0950799685 -->

# Connecting to a Corporate Git Repository

As an administrator, you can work with on-premise Git repositories once an appropriate destination has been created in your subaccount or OAuth has been enabled.



<a name="loiod54ddfc1bc4f45b19dabfa0950799685__section_ysr_hxl_tnb"/>

## Connecting to Git

Make sure to use the same host and port as defined in the destination URL property.

> ### Note:  
> The corporate Git connectivity supports only secure HTTPS connections. HTTP, SSH, and other protocols are not supported.

1.  Install and configure a Cloud Connector. For more information, see [Cloud Connector](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e6c7616abb5710148cfcf3e75d96d596.html).

2.  Configure the Cloud Connector to open a channel to your Git system. Follow the instructions as described in [Configure Access Control](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/f42fe4471d6a4a5fb09b7f3bb83c66a4.html). Use the following settings:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Value
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Back-end Type* 
    
    </td>
    <td valign="top">
    
    *Non-SAP System* 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Protocol*
    
    </td>
    <td valign="top">
    
    *HTTPS* 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Internal Host / Port* 
    
    </td>
    <td valign="top">
    
    Enter the internal host and port for your Git system.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Host / Port* 
    
    </td>
    <td valign="top">
    
    Enter a virtual host and port for your Git system. You can use the same host and port as for the virtual host and port.
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Principal Type* 
    
    </td>
    <td valign="top">
    
    *None* 
    
    </td>
    </tr>
    </table>
    
    For the system you just added, specify the resources to enable, using the following settings:


    <table>
    <tr>
    <th valign="top">

    Field
    
    </th>
    <th valign="top">

    Value
    
    </th>
    </tr>
    <tr>
    <td valign="top">
    
    *Enabled* 
    
    </td>
    <td valign="top">
    
    Checked
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *URL Path* 
    
    </td>
    <td valign="top">
    
    `/` 
    
    </td>
    </tr>
    <tr>
    <td valign="top">
    
    *Access Policy* 
    
    </td>
    <td valign="top">
    
    *Path and all sub-paths* 
    
    </td>
    </tr>
    </table>
    
3.  Upload your organization's Git server certificate to the cloud connector \(if your Git server is using certificate-based authentication\).
4.  If you defined a custom identity provider, make sure that you have configured the assertion-based attributes mapping for this identity provider. For more information, see [Configure Trust to the SAML Identity Provider](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/dc618538d97610148155d97dcd123c24.html#loiob6cfc4bb4bff4ace90afc71b0962fcb5).
5.  Define your corporate Git destination.
    1.  In the SAP BTP cockpit, select *Connectivity* \> *Destinations*.
    2.  Select *New Destination*.
    3.  In the *Destination Configuration* section, set the *Proxy Type* to *OnPremise*.
    4.  In the *Additional Properties* section, configure the following:


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
        
        WebIDEEnabled
        
        </td>
        <td valign="top">
        
        true
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        HTML5.DynamicDestination
        
        </td>
        <td valign="top">
        
        true
        
        </td>
        </tr>
        <tr>
        <td valign="top">
        
        HTML5.Timeout

        \(Optional property\)
        
        </td>
        <td valign="top">
        
        60000
        
        </td>
        </tr>
        </table>
        
        ![Additional properties for creating Git destinations](images/Create_destination_for_Git_328ecee.png)



> ### Note:  
> To start consuming the new configurations, users can either restart their dev space or reload the destinations into the dev space. See [Accessing On Premise Systems](accessing-on-premise-systems-e72930c.md).



<a name="loiod54ddfc1bc4f45b19dabfa0950799685__section_c41_3ls_gzb"/>

## Enabling OAuth in GitHub Enterprise

1.  Create an OAuth app as described in the [GitHub documentation](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app). Make sure to click *Enable Device Flow* when creating the app since OAuth app will use the device flow to identify and authorize users.

2.  Once the app is created, from the *General* tab of the application, copy the *Client ID* number.

3.  Add the `GitHubEnterpriseClientID` as an additional property to the GitHub Enterprise destination, where the value is the *Client ID* number you copied before.



<a name="loiod54ddfc1bc4f45b19dabfa0950799685__section_wtl_mbm_tnb"/>

## Using Git

Learn how to use Git in the SAP Business Application Studio Developer Guide. See [Git Source Control](git-source-control-9689c07.md).

