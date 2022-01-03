<!-- loio9ff1a8d6bced40a8a611b4ba7871e061 -->

# Auditing and Logging Information

Here you can find a list of the security events that are logged by SAP Business Application Studio.

<a name="loio9ff1a8d6bced40a8a611b4ba7871e061__table_dqf_pkf_p4b"/>Security events written in audit logs


<table>
<tr>
<th valign="top">

Event grouping



</th>
<th valign="top">

What events are logged



</th>
<th valign="top">

How to identify related log events



</th>
</tr>
<tr>
<td valign="top" rowspan="2">

BAS GW



</td>
<td valign="top">

BAS GW - Invalid scope



</td>
<td valign="top">

Attempting to log in to BAS GW with an Invalid scope

\(JWT details - scope, tenant, user, ...\)



</td>
</tr>
<tr>
<td valign="top">

BAS GW - Expired JWT



</td>
<td valign="top">

Attempting to log in to BAS GW with an expired JWT

\(JWT details - scope, tenant, user, ...\)



</td>
</tr>
<tr>
<td valign="top" rowspan="15">

Dev Space



</td>
<td valign="top">

Dev space - Invalid JWT

\(Unparsed, wrong client ID, or nonexistent tenant.\)



</td>
<td valign="top">

Attempting to log in to DevSpace router with an Invalid JWT



</td>
</tr>
<tr>
<td valign="top">

Dev space - Invalid scope



</td>
<td valign="top">

Attempting to log in to DevSpace router with an Invalid scope.

\(JWT details - scope, tenant, user, ...\)



</td>
</tr>
<tr>
<td valign="top">

Dev space - Expired JWT



</td>
<td valign="top">

Attempting to log in to DevSpace router with expired JWT



</td>
</tr>
<tr>
<td valign="top">

Access to dev space by the administrator



</td>
<td valign="top">

User: \{userEmail\}

Tenant: \{tenantName\}

DataType: "DevSpace"

DataID: \{"ClusterId": \{ClusterId\}, "WorkspaceId": \{wsId\} \}

Role: "admin"

AccessedData: \[\{targetUrl\}\]



</td>
</tr>
<tr>
<td valign="top">

Access dev space with no dev permissions



</td>
<td valign="top">

Workspace owner is attempting to access DevSpace router without developer permissions \{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Access dev space with no admin permissions



</td>
<td valign="top">

Attempting to access admin API through DevSpace router without admin permissions.

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Access dev space with a user that is not an owner or an admin.



</td>
<td valign="top">

Attempting to login to DevSpace router with user who is not owner of the workspace and not admin

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Access dev space with a user that is not an owner



</td>
<td valign="top">

Attempting to login to DevSpace router with user who is not owner of the workspace

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Access to user dev space by admin with JWT



</td>
<td valign="top">

Access to DevSpace router by admin with jwt authentication

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Access to dev space by admin with cookie authentication



</td>
<td valign="top">

Access to DevSpace router by admin with session cookie authentication

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Dev space - Invalid client ID in JWT



</td>
<td valign="top">

Attempting to login to DevSpace router with wrong client id provided by jwt. jwt client id: \{jwtClientID\}

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Dev space - Invalid tenant ID in JWT



</td>
<td valign="top">

Attempting to login to DevSpace router with wrong tenant id provided by jwt.

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Dev space - Invalid IdP issuer in JWT



</td>
<td valign="top">

Attempting to login to DevSpace router with wrong idp issuer provided by jwt. jwt idp issuer: \{idPOriginIssuer\}

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Access to dev space admin API



</td>
<td valign="top">

Access to DevSpace router admin API. Target URL is: \{targetUrl\}

\{JWT details - user, tenant, scope, ...\)



</td>
</tr>
<tr>
<td valign="top">

Malware detection in dev space



</td>
<td valign="top">

The devspace is infected with malware.



</td>
</tr>
<tr>
<td valign="top">

Extension Deployer



</td>
<td valign="top">

Simple Extension Deployer - Invalid scope



</td>
<td valign="top">

Attempting to log in to Simple Extension Deployer with an Invalid scope \(JWT details - scope, tenant, user, ...\)



</td>
</tr>
<tr>
<td valign="top">

Tenant Termination



</td>
<td valign="top">

Tenant Termination delete event



</td>
<td valign="top">

Role: \{developer/admin\}

Changes field:

Name: workspace \{name\} Tenant \{name\} old:created, new :deleted



</td>
</tr>
<tr>
<td valign="top" rowspan="4">

Workspace Manager



</td>
<td valign="top">

Workspace Manager - Invalid scope



</td>
<td valign="top">

Attempting to log in to WS Manager with an Invalid scope

\(JWT details - scope, tenant, user, ...\)



</td>
</tr>
<tr>
<td valign="top">

Workspace Manager - Expired JWT



</td>
<td valign="top">

Attempting to log in to WS Manager with an expired JWT

\(JWT details - scope, tenant, user, ...\)



</td>
</tr>
<tr>
<td valign="top">

Delete dev space



</td>
<td valign="top">

user: \{userEmail\}

tenant: \{tenantID\}

DataType: "ws-manager"

DataID: \{"ClusterId": \{ClusterId\}, "tenantID": \{tenantID\} \}

Changes: \[\{"Name":\{wsID\} deleted by \{zoneID\}, "Old":"created", New:"deleted"\}\]



</td>
</tr>
<tr>
<td valign="top">

Attempting to access workspace with insufficient scopes



</td>
<td valign="top">

User: \{userEmail\}

Tenant: \{tenantName\}

DataType: "DevSpace"

DataID: \{"ClusterId": \{ClusterId\}, "WorkspaceId": \{wsId\} \}

Role: "\{admin\}"

AccessedData: \[\{targetUrl\}\]



</td>
</tr>
</table>



The following information is described in the table columns:

-   *Event grouping* - Events that are logged with a similar format or are related to the same entities.

-   *What events are logged* - Description of the security or data protection and privacy related event that is logged.

-   *How to identify related log events* - Search criteria or key words, that are specific for a log event that is created along with the logged event.


**Related Information**  


[Audit Logging in the Cloud Foundry Environment](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/f92c86ab11f6474ea5579d839051c334.html)

