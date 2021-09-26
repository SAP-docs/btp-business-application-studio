<!-- loio6331319fd9ea4f0ea5331e21df329539 -->

# Subscribe to SAP Business Application Studio

Before you can work in SAP Business Application Studio, the account administrator must subscribe the subaccount to the SAP Business Application Studio application.



<a name="loio6331319fd9ea4f0ea5331e21df329539__section_vdm_nmz_tkb"/>

## Prerequisites

-   If your global account uses the subscription-based commercial model, then you must have purchased a SaaS license for SAP Business Application Studio. See [Pricing and Packaging](https://www.sap.com/products/cloud-platform/pricing.html). You can also contact us on [SAP BTP](https://cloudplatform.sap.com/index.html) or via an SAP sales representative.

-   You have created a subaccount in Cloud Foundry. See [Create a Subaccount](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/05280a123d3044ae97457a25b3013918.html).

-   You are an administrator of the subaccount.




<a name="loio6331319fd9ea4f0ea5331e21df329539__section_ajs_4mz_tkb"/>

## Procedure

1.  Open your global account in the cockpit.
2.  Go to your subaccount.
3.  In the navigation area, choose *Service Marketplace*.

    A list of the applications to which your global account is entitled in the Cloud Foundry environment is displayed.

    > ### Note:  
    > The *Instances and Subscriptions* page displays all subscriptions and instances in your subaccount.

4.  Search for ***Studio***. The SAP Business Application Studio tile is displayed.

    > ### Note:  
    > If the SAP Business Application Studio tile does not appear in the results, check the entitlement configuration for your subaccount. See [Configure Entitlements and Quotas for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).

5.  Click the application name to open its *Overview* page.
6.  Click *Create*.
7.  From the *New Instance or Subscription* dialog box, select the desired application plan. For information on the difference between the plans, see [Application Plans](Application_Plans_2c72917.md).
8.  Click *Create*.
9.  From the *New Instance or Subscription* dialog box, leave the default selections and click *Create*.
10. From the *Creation in Progress* dialog box, click *View Subscription*.
11. Grant user permissions to work with SAP Business Application Studio. See [Manage Authorizations and Roles](Manage_Authorizations_and_Roles_01e69c5.md).
12. From the SAP Business Application Studio *Overview* page in the cockpit, click the ellipsis, and then click *Go to Application*.

    ![](images/Go_to_Application_7223fda.png)


> ### Note:  
> To remove a subscribed application, go back to the *Overview* page of the subscribed application, click the ellipsis, and then click *Delete*. All data related to the application will be deleted in the respective subaccount.

