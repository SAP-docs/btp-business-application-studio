<!-- loio53dfab0d97d0476b8327d0ab63342e62 -->

# Connecting to Cloud Foundry Using Identity Providers

Connect to Cloud Foundry using the UI or the command line.

The manner in which you can connect to Cloud Foundry depends on the identity provider \(IdP\) you use.



<a name="loio53dfab0d97d0476b8327d0ab63342e62__section_ncw_4jf_drb"/>

## Comparison Between the Different Identity Providers for Cloud Foundry Login in SAP Business Application Studio


<table>
<tr>
<th>

 



</th>
<th>

SAP ID Service



</th>
<th>

Custom IdP



</th>
<th>

Corporate IdP



</th>
</tr>
<tr>
<td>

 SAP Business Application Studio UI-based login



</td>
<td>

Supported



</td>
<td>

Not supported



</td>
<td>

Not supported



</td>
</tr>
<tr>
<td>

 SAP Business Application Studio CLI-based login



</td>
<td>

Supported



</td>
<td>

Supported



</td>
<td>

Supported



</td>
</tr>
<tr>
<td>

CLI-based login example



</td>
<td>

Reference

`cf login`



</td>
<td>

Reference

`cf login --origin <origin>`



</td>
<td>

Reference

`cf login --sso`



</td>
</tr>
<tr>
<td>

Authorization flow



</td>
<td>

OAuth Resource Owner Password



</td>
<td>

OAuth Resource Owner Password



</td>
<td>

OAuth Authorization Code Grant \(browser flow\) + One-Time Passcode



</td>
</tr>
</table>

For more information, see [this blog](https://blogs.sap.com/2021/04/21/connecting-from-sap-business-application-studio-to-sap-btp-cloud-foundry-environment/).

