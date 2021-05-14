<!-- loioa23487f0c2354c01a6fd8aa651a3138a -->

# Getting Started in China \(Shanghai\) Region

Here's a checklist for setting up your system so you can develop applications using SAP Business Application Studio.


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

[Getting a Global Account](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/82f9ff522f754e26ae89e0cd7ec7aa11.html)



</td>
</tr>
<tr>
<td>

**Create subaccounts in the Cloud Foundry environment.**



</td>
<td>

When you create a subaccount in the SAP BTP, Cloud Foundry environment, a Cloud Foundry organization is automatically created for that subaccount.



</td>
<td>

[Create a Subaccount in the Cloud Foundry Environment \[Feature Set B\]](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/261ba9ca868f469baf64c22257324a75.html)



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

[Members and Roles in the Cloud Foundry environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cc1c676b43904066abb2a4838cbd0c37.html)



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

 [Subscribe to SAP Business Application Studio](https://help.sap.com/viewer/9d1db9835307451daa8c930fbd9ab264/Cloud/en-US/b53e2618988d4fe99e459d738d2d9960.html) 



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

[Manage Authorizations](Manage_Authorizations_4168f83.md)



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

