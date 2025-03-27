<!-- loio5648ce03dfe54d9f9e288dfa21c96ef7 -->

# Security Recommendations and Considerations

The following sections present an overview of security recommendations and considerations for SAP Business Application Studio developers and administrators.



<a name="loio5648ce03dfe54d9f9e288dfa21c96ef7__section_xbh_zr5_txb"/>

## Security Recommendations

The following security recommendations are included in the list of [SAP BTP security recommendations](https://help.sap.com/docs/BTP/c8a9bb59fe624f0981efa0eff2497d7d/531f33def8074ccdb6f1f784a34dafcb.html?seclist-service=SAP%20Business%20Application%20Studio).


<table>
<tr>
<th valign="top">

Summary

</th>
<th valign="top">

Recommendation

</th>
</tr>
<tr>
<td valign="top">

Limit the number of administrators with full management permissions.

</td>
<td valign="top">

[BTP-BAS-0001](https://help.sap.com/docs/BTP/c8a9bb59fe624f0981efa0eff2497d7d/531f33def8074ccdb6f1f784a34dafcb.html?seclist-index=BTP-BAS-0001)

</td>
</tr>
</table>



<a name="loio5648ce03dfe54d9f9e288dfa21c96ef7__section_o34_zv5_txb"/>

## Security Considerations

Decisions you make when using SAP Business Application Studio can have an impact on the security of your applications. The information provided is meant to help you decide.


<table>
<tr>
<th valign="top">

Summary

</th>
<th valign="top">

More Information

</th>
</tr>
<tr>
<td valign="top">

Use caution when installing third-party extensions while using SAP Business Application Studio, when working on a browser or using a remote connection.

</td>
<td valign="top">

See [Access SAP Business Application Studio from VS Code](access-sap-business-application-studio-from-vs-code-6b18cc8.md) and [Explore and Install VS Code Extensions](explore-and-install-vs-code-extensions-d83a580.md).

</td>
</tr>
<tr>
<td valign="top">

When connecting to corporate Git source control systems, use Personal Access Tokens \(PATs\) whenever possible.

> ### Note:  
> PATs are an alternative to using passwords for authentication to Git, and as such, they should be frequently renewed. See [Managing your personal access tokens](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).



</td>
<td valign="top">

See [Connecting to a Corporate Git Repository](connecting-to-a-corporate-git-repository-d54ddfc.md).

</td>
</tr>
<tr>
<td valign="top">

Always protect your access to an external system.

</td>
<td valign="top">

See [Connecting to External Systems](connecting-to-external-systems-7e49887.md).

</td>
</tr>
<tr>
<td valign="top">

Make sure you only install secured artifacts with your custom SAP Business Application Studio extension.

</td>
<td valign="top">

See [Create and Deploy an SAP Business Application Studio Extension](create-and-deploy-an-sap-business-application-studio-extension-2064b4e.md).

</td>
</tr>
<tr>
<td valign="top">

When exporting personal data from specific dev spaces, use the downloaded data with care as it contains unprotected personal data.

</td>
<td valign="top">

See [Export and Download Personal Data from Specific Users](export-and-download-personal-data-from-specific-users-8091e47.md).

</td>
</tr>
<tr>
<td valign="top">

**If you are using the build-code service plan:**

When using features with Generative AI, the project’s source code files can be used as context for AI, to improve accuracy. Therefore, please ensure these files do not contain any personal data.

</td>
<td valign="top">

See [Generative AI-Powered Development](https://help.sap.com/docs/build_code/d0d8f5bfc3d640478854e6f4e7c7584a/337848fc83f24738a9f3a15a88f1fa76.html?version=SHIP).

</td>
</tr>
</table>

