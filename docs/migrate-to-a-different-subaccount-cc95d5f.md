<!-- loiocc95d5f9053b436c8238234966015fa9 -->

# Migrate to a Different Subaccount

You can migrate your SAP Business Application Studio workspace to a different subaccount.



<a name="loiocc95d5f9053b436c8238234966015fa9__section_nwl_ctn_fwb"/>

## Prerequisites

You have an SAP BTP global account. See [Getting a Global Account](https://help.sap.com/docs/btp/sap-business-technology-platform/getting-global-account).



<a name="loiocc95d5f9053b436c8238234966015fa9__section_vfb_xzs_rfc"/>

## Procedure

To migrate your SAP Business Application Studio instance to a different subaccount:

1.  Create a new subaccount in the relevant region. See [Create a Subaccount](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/05280a123d3044ae97457a25b3013918.html).
2.  Enable the SAP Business Application Studio entitlements for the new subaccount. See [Configure Entitlements and Quotas for Subaccounts](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/5ba357b4fa1e4de4b9fcc4ae771609da.html).
3.  Create an SAP Business Application Studio instance in the new subaccount. See [Subscribe to SAP Business Application Studio](https://help.sap.com/docs/bas/sap-business-application-studio/subscribe-to-sap-business-application-studio).
4.  Create users in the new subaccount. See [Manage Authorizations and Roles](https://help.sap.com/docs/bas/sap-business-application-studio/manage-authorizations-and-roles).
5.  If needed enable a custom identity provider \(IdP\) for SAP Business Application Studio applications. See [Federation Attribute Settings of Any Identity Provider](https://help.sap.com/docs/btp/sap-business-technology-platform/federation-attribute-settings-of-any-identity-provider).
6.  Assign the `BAS_developer` role to the users.
7.  Download the relevant dev space content from the current SAP Business Application Studio instance or use Git source control to move it. See [Download Dev Space Content](https://help.sap.com/docs/bas/sap-business-application-studio/working-in-dev-space-manager#download-dev-space-content).
8.  Launch SAP Business Application Studio in the new subaccount and create a new dev space. [Create a Dev Space](https://help.sap.com/docs/bas/sap-business-application-studio/working-in-dev-space-manager#create-a-dev-space).
9.  Import the dev space content you downloaded before or clone the projects using Git. See [Import Dev Space Content](https://help.sap.com/docs/bas/sap-business-application-studio/working-in-dev-space-manager#import-dev-space-content).
10. Export the destinations from the SAP BTP cockpit of the source SAP Business Application Studio subaccount. See [Export Destinations](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/export-destinations).
11. Import the destinations to the new subaccount. [Import Destinations](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/import-destinations).
12. If needed, establish a cloud connector or trust to the target external system, such as SAP S/4HANA Private Cloud or SAP S/4HANA Public Cloud. See[Cloud Connector](https://help.sap.com/docs/connectivity/sap-btp-connectivity-cf/cloud-connector).
13. Enable the Cloud Foundry environment in the new subaccount. If required for your runtime apps, create spaces and instances required to run your apps. See [Cloud Foundry Tools](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/cloud-foundry-tools?locale=en-US&state=PRODUCTION&version=Cloud).
14. Preview and deploy your apps from the new SAP Business Application Studio subaccount. See [Test and Run](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/test-and-run?locale=en-US&state=PRODUCTION&version=Cloud).

