<!-- loio02e3226ccc25465d8d480e327a8c86bd -->

# Free Plan Restrictions

Learn about the restrictions for working in the free plan.



<a name="loio02e3226ccc25465d8d480e327a8c86bd__section_v4w_f1z_tpb"/>

## Free Plan Restrictions

> ### Note:  
> Only community support is available for free service plans and these are not subject to SLAs. Use of free tier service plans are subject to additional terms and conditions as provided in the [SAP Business Technology Platform Supplement](https://www.sap.com/about/trust-center/agreements/cloud/cloud-services.html?tag=language:english&search=Supplement%20Business%20Technology%20Platform&sort=latest_desc).

In addition to the regular SAP Business Application Studio [Restrictions](restrictions-76db362.md), when using a free plan, the following restrictions also apply:

-   A user can only have up to 2 dev spaces.
-   A user can only have 1 dev space in the RUNNING state at a time.
-   A user can only have a disk space of up to 4 GB per dev space.
-   When working in the *Full-Stack Application Using Productivity Tools* dev space, a user can deploy a maximum of 2 times.
-   There is a limited monthly quota of AI requests per user for using Joule.



### Deploying an App Created With the Free Plan

The free plan does not include a subscription to Cloud Foundry. Therefore, if you want to deploy an app created in SAP Build Code, free plan, you have 2 options:

-   Deploy to a subaccount where you have a subscription to Cloud Foundry.

-   Subscribe to Cloud Foundry from your current subaccount.

    > ### Note:  
    > If you subscribe to the free plan of Cloud Foundry, there is no charge, but if you subscribe to the standard plan, there is a charge. See the [Discovery Center](https://discovery-center.cloud.sap/serviceCatalog/cloud-foundry-runtime?commercialModel=payg&region=all&tab=service_plan) for detailed pricing information.


