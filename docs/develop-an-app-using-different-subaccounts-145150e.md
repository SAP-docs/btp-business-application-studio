<!-- loio145150e367f44831ab7cfc2c2c320971 -->

# Develop an App Using Different Subaccounts

You can develop your application with different subaccounts. You use one subaccount to create and run your application in SAP Business Application Studio. You use the other subaccount, in a different region, to deploy your application to Cloud Foundry.

This scenario is useful in the following situations:

-   You're using a single development subaccount to develop many target accounts.
-   Your development account isn't in the same region as your target account.

Develop an app with two subaccounts as follows:

1.  From your global account in the SAP BTP cockpit, create two subaccounts in two different regions. See [Create a Subaccount \[Feature Set B\]](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/05280a123d3044ae97457a25b3013918.html?locale=en-US#create-a-subaccount-%5Bfeature-set-b%5D).

    One subaccount is for the design time environment and the other is for the runtime environment.

2.  Complete the following steps in the design time subaccount:
    1.  Add the relevant SAP Business Application Studio service plan. See [Configure Entitlements and Quotas from Your Subaccount](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/5ba357b4fa1e4de4b9fcc4ae771609da.html?locale=en-US#configure-entitlements-and-quotas-from-your-subaccount).
    2.  [Subscribe to SAP Business Application Studio](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/6331319fd9ea4f0ea5331e21df329539.html?locale=en-US).

3.  Navigate to the *Overview* page of your runtime subaccount and click *Enable Cloud Foundry*. This enables you to deploy the application to Cloud Foundry. See [Create Orgs](https://help.sap.com/docs/BTP/65de2977205c403bbc107264b8eccf4b/a9b1f5445a17427f844a5a43ac53d378.html?locale=en-US).
4.  If you're using an external data source \(outside SAP BTP\) for your application, create the same destination, with the same name, in **both** subaccounts. See [Create HTTP Destinations](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/783fa1c418a244d0abb5f153e69ca4ce.html) and [Add a System](https://help.sap.com/products/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/892114ce078b4e17a9ff7e751e6330cc.html?locale=en-US&version=Cloud#add-a-system).
5.  [Log in to Cloud Foundry](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/9ad5cf8dc1444f3081f0e847c8588fc0.html?locale=en-US&version=Cloud#login-to-cloud-foundry). Make sure to update the Cloud Foundry endpoint with the region of the runtime subaccount \(for example, change <code>https://api.cf.<b>us10</b>.hana.ondemand.com</code> to <code>https://api.cf.<b>eu10</b>.hana.ondemand.com</code>\).
6.  [Create a Project](create-a-project-fa59c5a.md) in the design time subaccount. Make sure to connect to the relevant destination during data source and service selection.
7.  Test your application by [creating a run configuration](https://help.sap.com/products/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/e3cbf81c81d64cddb66151b3b7ad6bef.html?locale=en-US&version=Cloud). Make sure to bind the relevant destination.
8.  [Build and deploy](https://help.sap.com/products/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/97ef204c568c4496917139cee61224a6.html?locale=en-US&version=Cloud) your application.

    Your application uses the runtime subaccount to deploy to Cloud Foundry.


