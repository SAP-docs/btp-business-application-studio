<!-- loiod5e4d02d976f40feabe9b4c57443b7a5 -->

# Build and Deploy

Use our dedicated tools to build and deploy your application.



<a name="loiod5e4d02d976f40feabe9b4c57443b7a5__section_rwn_j12_5qb"/>

## **Prerequisites**

1.  You've logged in to your `Cloud Foundry` account, see [Login to Cloud Foundry](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/9ad5cf8dc1444f3081f0e847c8588fc0.html?version=Cloud#login-to-cloud-foundry).

2.  To create an `SAP HANA Cloud` instance for seamless business application development and deployment:

    -   You've added the *SAP HANA Cloud*, *SAP HANA Schemas & HDI Containers* entitlement to your subaccount. For details on adding entitlements to your subaccount, see [Configure Entitlements and Quotas from Your Subaccount](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/5ba357b4fa1e4de4b9fcc4ae771609da.html#configure-entitlements-and-quotas-from-your-subaccount) \(you'll be directed to the SAP Business Technology Platform documentation\).

    -   You've created an *SAP HANA Cloud database* instance from *SAP HANA Cloud Central*.

        For details on subscribing to SAP HANA Cloud Administration Tools and accessing *SAP HANA Cloud Central*, see [Subscribing to the SAP HANA Cloud Administration Tools \(Multi-Environment\)](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-administration-guide/subscribing-to-sap-hana-cloud-administration-tools#procedure) \(you'll be directed to the SAP HANA Cloud documentation\).

        For details on creating an *SAP HANA Cloud database* instance from *SAP HANA Cloud Central* using cf CLI, see [Using the Cloud Foundry Command Line interface \(cf CLI\) with SAP HANA Cloud](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-administration-guide/using-cloud-foundry-command-line-interface-cf-cli-with-sap-hana-cloud#creating-instances) \(you'll be directed to the SAP HANA Cloud documentation\).

        > ### Note:  
        > When using a trial account, use the default values for each step of the `SAP HANA Database` instance setup wizard, except for the *SAP HANA Database Advanced Settings* step.
        > 
        > Set *Allowed connections* to *Allow all IP addresses* and select *Review and Create*.

        For details on managing your SAP HANA Cloud instance, see [Managing SAP HANA Database Instances](https://help.sap.com/viewer/9ae9104a46f74a6583ce5182e7fb20cb/hanacloud/en-US/649092e9d9be41c59930179ce4f3d59e.html) \(you'll be directed to the SAP HANA Cloud documentation\).


3.  If you are subscribed to the Trial plan, make sure you also have the following:
    -   You've added the `SAP Build Work Zone, standard edition` entitlement to your subaccount and subscribed to `SAP Build Work Zone, standard edition` on *Service Marketplace*. For details, see [Initial Setup](https://help.sap.com/docs/Launchpad_Service/8c8e1958338140699bd4811b37b82ece/fd79b232967545569d1ae4d8f691016b.html#procedure) \(you'll be directed to the `SAP Build Work Zone` documentation\).

        > ### Note:  
        > If you already have the entitlement and subscription for *SAP Build Work Zone, advanced edition*, you don't need the subscription and entitlement for *SAP Build Work Zone, standard edition*.

    -   You've assigned the *Launchpad\_Admin* role collection to the user. For details on assigning role collections to users, see [Assigning Role Collections to Users or User Groups](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/31532c77bd61421e9d40d100fd75ef52.html) \(you'll be directed to the SAP Business Technology Platform documentation\).

    -   You've added the *Cloud Foundry Runtime* entitlements to your subaccount. For details on adding entitlements to your subaccount, see [Configure Entitlements and Quotas from Your Subaccount](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/5ba357b4fa1e4de4b9fcc4ae771609da.html#configure-entitlements-and-quotas-from-your-subaccount) \(you'll be directed to the SAP Business Technology Platform documentation\).

        > ### Note:  
        > You can adjust the units of *Cloud Foundry Runtime* assigned to your subaccount depending on your business requirements.


4.  If you are subscribed to the Free or the Trial plan, make sure you also have the following:
    -   You've added the `SAP Build Work Zone, standard edition` entitlement to your subaccount and subscribed to `SAP Build Work Zone, standard edition` on *Service Marketplace*. For details, see [Initial Setup](https://help.sap.com/docs/Launchpad_Service/8c8e1958338140699bd4811b37b82ece/fd79b232967545569d1ae4d8f691016b.html#procedure) \(you'll be directed to the `SAP Build Work Zone` documentation\).

        > ### Note:  
        > If you already have the entitlement and subscription for *SAP Build Work Zone, advanced edition*, you don't need the subscription and entitlement for *SAP Build Work Zone, standard edition*.

    -   You've assigned the *Launchpad\_Admin* role collection to the user. For details on assigning role collections to users, see [Assigning Role Collections to Users or User Groups](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/31532c77bd61421e9d40d100fd75ef52.html) \(you'll be directed to the SAP Business Technology Platform documentation\).

    -   You've added the *Cloud Foundry Runtime* entitlements to your subaccount. For details on adding entitlements to your subaccount, see [Configure Entitlements and Quotas from Your Subaccount](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/5ba357b4fa1e4de4b9fcc4ae771609da.html#configure-entitlements-and-quotas-from-your-subaccount) \(you'll be directed to the SAP Business Technology Platform documentation\).

        > ### Note:  
        > You can adjust the units of *Cloud Foundry Runtime* assigned to your subaccount depending on your business requirements.





<a name="loiod5e4d02d976f40feabe9b4c57443b7a5__section_uwh_rxr_s1c"/>

## Deployment Options

Use the SAP Business Application Studio development tools for working with multitarget applications. See [MTA Development](mta-development-a629398.md).

You can also find documentation for scenario-specific deployment options.

-   If you want to deploy an SAP Fiori application, see [Deploy an Application](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/607014e278d941fda4440f92f4a324a6.html).
-   If you want to deploy an SAP HANA application, see[Maintaining the Multitarget Application Development & Deployment Descriptors](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/b2e355a5137c4799932f776716b292c9.html).

-   **[Task Explorer](task-explorer-1232c72.md "You can create, modify, and run tasks for specific SAP scenarios.")**  
You can create, modify, and run tasks for specific SAP scenarios.
-   **[MTA Development](mta-development-a629398.md "Learn how to use the SAP Business Application
                            Studio development tools for working with multitarget applications. ")**  
Learn how to use the SAP Business Application Studio development tools for working with multitarget applications.
-   **[Continuous Integration and Delivery](continuous-integration-and-delivery-b357cfe.md "SAP Continuous Integration and Delivery lets you configure and run predefined
		continuous integration and delivery (CI/CD) pipelines that automatically build, test, and
		deploy your code changes to speed up your development and delivery cycles.")**  
SAP Continuous Integration and Delivery lets you configure and run predefined continuous integration and delivery \(CI/CD\) pipelines that automatically build, test, and deploy your code changes to speed up your development and delivery cycles.

