<!-- loio19611ddbe82f4bf2b493283e0ed602e5 -->

# Getting Started

Here's a checklist for setting up your system so you can develop applications using SAP Business Application Studio.

> ### Note:  
> If you are woking in a trial account, follow the procedure in [Getting Started with a Trial Account](Getting_Started_with_a_Trial_Account_48ed55e.md).


<table>
<tr>
<th>

Step



</th>
<th>

Description



</th>
<th>

Links/Information



</th>
</tr>
<tr>
<td>

 **Sign up for a global account.** 



</td>
<td>

You require a global account to enable SAP Business Application Studio.



</td>
<td>

[Getting a Global Account](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/d61c2819034b48e68145c45c36acba6e.html)



</td>
</tr>
<tr>
<td>

**Create subaccounts in the Cloud Foundry environment.**

Select a region according to the guidelines in the [Neo and Cloud Foundry Regions](https://help.sap.com/viewer/825270ffffe74d9f988a0f0066ad59f0/CF/en-US/975b3207acf94599a9a48beb36257ebc.html) topic.



</td>
<td>

When you create a subaccount in the SAP BTP, Cloud Foundry environment, a Cloud Foundry organization is automatically created for that subaccount.



</td>
<td>

 [Create a Subaccount in the Cloud Foundry Environment \[Feature Set A\]](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/05280a123d3044ae97457a25b3013918.html) 



</td>
</tr>
<tr>
<td>

 **Create spaces** 



</td>
<td>

You can create and delete spaces in a Cloud Foundry organization using the SAP BTP cockpit or the console client \(Cloud Foundry command line interface\).

We recommend at least one space for a development team working on the same project \(that is, one space per project\).

For staging/test and production organizations, one space is sufficient.



</td>
<td>

[Create Spaces](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/2f6ed22ccf424dae84345f4500c2d8ea.html)



</td>
</tr>
<tr>
<td>

 **Assign members to your Cloud Foundry organizations and spaces** 



</td>
<td>

Enable your developers to work with your SAP BTP, Cloud Foundry environments.

Your developers should be assigned to the space developer role to be able to use the space from SAP Business Application Studio.



</td>
<td>

[Managing Members](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cc1c676b43904066abb2a4838cbd0c37.html)



</td>
</tr>
<tr>
<td>

 **Subscribe to SAP Business Application Studio** 



</td>
<td>

You need to subscribe to the SAP Business Application Studio.



</td>
<td>

 [Subscribe to SAP Business Application Studio](Subscribe_to_SAP_Business_Application_Studio_6331319.md) 



</td>
</tr>
<tr>
<td>

**Grant user permissions**



</td>
<td>

To enable working with SAP Business Application Studio, developers need to be assigned the `Business_Application_Studio_Developer` role.



</td>
<td>

 [Manage Authorizations](Manage_Authorizations_01e69c5.md) 



</td>
</tr>
<tr>
<td>

**OPTIONAL: Enable identity provider \(IdP\)-based authentication for SAP Business Application Studio applications \(optional\)**



</td>
<td>

If you define a custom identity provider for your subaccount, be sure to configure the assertion-based attributes mapping for this IdP.



</td>
<td>

 [Configure Trust to the SAML Identity Provider](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/dc618538d97610148155d97dcd123c24.html#loiob6cfc4bb4bff4ace90afc71b0962fcb5) 



</td>
</tr>
</table>

-   **[Connecting to External Systems](Connecting_to_External_Systems_7e49887.md)**  
For applications that do not need to run on Cloud Foundry, establish a connection to an external system by creating one destination for multi-usage.

