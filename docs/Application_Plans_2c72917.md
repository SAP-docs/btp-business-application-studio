<!-- loio2c72917df87e47c290e061a556d92398 -->

# Application Plans

SAP Business Application Studio provides 2 types of application plans: free and standard-edition. Both plans are provided only in Enterprise accounts.

You select the plan when subscribing to the application. See [Subscribe to SAP Business Application Studio](Subscribe_to_SAP_Business_Application_Studio_6331319.md). The type of plan you choose determines pricing, conditions of use, and resources.

Both plans provide preinstalled runtimes and tools tailored for developing key scenarios such as: SAP S/4HANA extensions, full stack business applications, SAP Fiori applications, and more. However, the free plan contains some restrictions. See [Free Plan Restrictions](Application_Plans_2c72917.md#loio2c72917df87e47c290e061a556d92398__section_v4w_f1z_tpb).

Each subaccount has only 1 subscription. If you selected the free service plan and want to upgrade to the standard-edition plan, you can do so as described in [Upgrading to the Standard-Edition Plan](Application_Plans_2c72917.md#loio2c72917df87e47c290e061a556d92398__section_dzc_j1z_tpb).

You can use different plans in separate subaccounts.



<a name="loio2c72917df87e47c290e061a556d92398__section_v4w_f1z_tpb"/>

## Free Plan Restrictions

-   The free plan is available in the following regions only:

    -   AWS: Australia \(Sydney\), Europe \(Frankfurt\), Japan \(Tokyo\), US East \(VA\).

    -   Microsoft Azure: Europe \(Netherlands\), Japan \(Tokyo\), Singapore, US East \(VA\), US West \(WA\).

-   A user can only have up to 2 dev spaces.

-   A user can only have 1 dev space in the RUNNING state at a time.

-   The maximum size limit of a dev space is 4 GB.


> ### Note:  
> Only community support is available for free service plans and these are not subject to SLAs. Use of free tier service plans are subject to additional terms and conditions as provided in the [SAP Business Technology Platform Supplement](https://www.sap.com/about/trust-center/agreements/cloud/cloud-services.html?tag=language:english&search=Supplement%20Business%20Technology%20Platform&sort=latest_desc).



<a name="loio2c72917df87e47c290e061a556d92398__section_dzc_j1z_tpb"/>

## Upgrading to the Standard-Edition Plan

To upgrade the application subscription from the free plan to the standard-edition plan:

1.  Save the content of all the dev spaces created in SAP Business Application Studio from the subaccount where you want to upgrade the subscription. For example, developers can upload projects to a Git repository or export the dev spaces.
2.  In the SAP BTP cockpit, unsubscribe from the SAP Business Application Studio application.

    > ### Caution:  
    > All dev spaces created in SAP Business Application Studio from this subaccount and their content will be removed.

3.  Follow the instructions in [Subscribe to SAP Business Application Studio](Subscribe_to_SAP_Business_Application_Studio_6331319.md) and select the standard-edition plan.
4.  Assign permissions to developers as described in [Manage Authorizations and Roles](Manage_Authorizations_and_Roles_01e69c5.md).

