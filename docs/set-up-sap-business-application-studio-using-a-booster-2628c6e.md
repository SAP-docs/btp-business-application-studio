<!-- loio2628c6e3880249379409c454dd6956ca -->

# Set Up SAP Business Application Studio Using a Booster

Use the *Get started with SAP Business Application Studio* booster to complete the initial setup and start creating your business applications using productivity tools.



<a name="loio2628c6e3880249379409c454dd6956ca__section_enb_bhq_j5b"/>

## Prerequisites

You've set up your global account for building applications using SAP Business Application Studio. See [Set Up SAP Business Application Studio](set-up-sap-business-application-studio-19611dd.md).



<a name="loio2628c6e3880249379409c454dd6956ca__section_zxw_3hq_j5b"/>

## Context

The booster performs the following tasks:

-   Creates a new subaccount or uses an existing subaccount for developing business applications using productivity tools on SAP Business Application Studio

-   Creates a Cloud Foundry runtime instance for the subaccount

-   Assigns the following entitlements and quotas:

    -   `Cloud Identity Services`

    -   `HTML5 Application Repository`

    -   `Master Data Integration (Orchestration)`

    -   `SaaS Provisioning Service`

    -   `SAP Business Application Studio`

    -   `SAP Content Agent Service`

    -   `Service Manager`

    -   \(Optional\) `SAP Continuous Integration and Delivery` \(app and service\)

        > ### Note:  
        > The `SAP Continuous Integration and Delivery` \(app and service\) entitlement is optional. You can ignore warnings, if any, issued by the booster at the *Check Prerequisites* stage and proceed with running the booster.


-   Enables subscriptions for SAP Business Application Studio

-   Assigns role collections, such as `BAS_Administrator` and `BAS_Developer`




<a name="loio2628c6e3880249379409c454dd6956ca__section_kkx_zhq_j5b"/>

## Procedure

1.  Access your [global account](https://account.hana.ondemand.com/#/home/welcome) in the SAP BTP cockpit and choose *Boosters* from the navigation pane.

2.  Select the *Extension Suite – Developer Efficiency* filter and search for the *Get started with SAP Business Application Studio* booster.

    > ### Note:  
    > The *Get started with SAP Business Application Studio* booster is compatible with all regions, except China.

3.  Open the booster to see the overview, components, and additional resources to learn more about the high productivity tools provided in the Productivity Toolkit.

4.  Choose *Start*.

    The booster wizard guides you through the process of enabling the tools, configuring entitlements, and assigning members on the SAP BTP cockpit.

    The booster checks for required authorizations, compatible providers, and regions, as prerequisites for successful execution.

5.  Choose *Next*.

6.  Choose whether to create a new subaccount or select an existing subaccount based on your requirements.

7.  In the *Entitlements* field, select either a *free* or *standard-edition* service plan for the `SAP Business Application Studio` and `Continuous Integration & Delivery` \(optional\).

    You can upgrade to the *standard-edition* plan anytime. See [Application Plans](application-plans-2c72917.md).

8.  Add users and assign them to the relevant roles.

9.  Review the details of your subaccount and subdomain, and added users with the required roles.

10. Choose *Finish*.

    > ### Note:  
    > After running the *Get started with SAP Business Application Studio* booster to develop business applications using productivity tools, you then need to manually assign entitlements according to your business requirements to deploy your applications. See [Deploy](https://help.sap.com/viewer/f9814e8df1cb43e1890e0f8d25374b8f/Cloud/en-US/1d4feada3bd1448dbfd6426246bcbc8e.html "After previewing, you can deploy your applications.") :arrow_upper_right:.

11. After running the booster, on the popup window, choose *Navigate to Subaccount*.

12. In the navigation pane of your subaccount, select *Services* \> *Instances and Subscriptions*.

13. Under the *Subscriptions* tile, choose *SAP Business Application Studio* to open SAP Business Application Studio.




<a name="loio2628c6e3880249379409c454dd6956ca__section_l4w_sby_hfc"/>

## Configuring Authorizations

The following role collections are created. You can assign appropriate role collections to the members in your subaccount according to their business needs.


<table>
<tr>
<th valign="top">

Role Collection

</th>
<th valign="top">

Roles

</th>
<th valign="top">

Authorization

</th>
</tr>
<tr>
<td valign="top" rowspan="4">

`BAS_Administrator`

</td>
<td valign="top">

`Administrator`

</td>
<td valign="top" rowspan="4">

-   Permission to access *Projects*, allowing you to perform the following actions in `SAP Build`:
    -   Create projects.
    -   Edit and view projects.

-   Permission to access applications in SAP Business Application Studio.

-   Permission to create application components using productivity tools in SAP Business Application Studio.



</td>
</tr>
<tr>
<td valign="top">

`Developer`

</td>
</tr>
<tr>
<td valign="top">

`RegistryAdmin`

</td>
</tr>
<tr>
<td valign="top">

`RegistryDeveloper`

</td>
</tr>
<tr>
<td valign="top" rowspan="2">

`BAS_Developer` 

</td>
<td valign="top">

`Developer`

</td>
<td valign="top" rowspan="2">

-   Permission to access applications in SAP Business Application Studio.

-   Permission to create application components using productivity tools in SAP Business Application Studio.



</td>
</tr>
<tr>
<td valign="top">

`RegistryDeveloper`

</td>
</tr>
</table>

