<!-- loiof2b38ec94f5143a6b662fb862c027340 -->

# Auditing and Logging Information

Here you can find a list of the events that are logged by the SAP Business Application Studio service.

These events are critical for security monitoring, compliance, and troubleshooting.

> ### Note:  
> Audit logs are sent to SIEM Splunk where all security logs are stored for 1 year. Security teams can access these logs through the appropriate channels.



## Security Events Written in Audit Logs


<table>
<tr>
<th valign="top">

Event Grouping

</th>
<th valign="top">

Which events are logged

</th>
<th valign="top">

How to identify related log events

</th>
<th valign="top">

Additional information

</th>
</tr>
<tr>
<td valign="top">

Events related to JWT authentication failures.

</td>
<td valign="top">

An attempt was made to log in with an invalid JWT token to various components \(Workspace Manager, Dev Space Router, Tenant Manager, etc.\).

</td>
<td valign="top">

The security event message contains the following text:

-   `Attempting to log in to [Component] with an invalid JWT`
-   Identifier: `AppStudio`



</td>
<td valign="top">

This is a security event.

The reason for the invalid JWT may be:

-   An unparsed JWT
-   A wrong client ID

-   A non-existent tenant




</td>
</tr>
<tr>
<td valign="top">

Events related to expired JWT tokens.

</td>
<td valign="top">

An attempt was made to log in to various components with an expired JWT token.

</td>
<td valign="top">

The security event message contains the following text:

-   `Attempting to log in to [Component] with an expired JWT`



</td>
<td valign="top">

This is a security event.

</td>
</tr>
<tr>
<td valign="top">

Events related to invalid scope authentication.

</td>
<td valign="top">

An attempt was made to access a component without the required scope permissions.

</td>
<td valign="top">

`The security event message contains the following text:`

-   <code><code>Attempting to log in to [Component] with an invalid scope</code></code>
-   `The message inlcudes the JWT details (such as scope, tentant, user, etc.)`



</td>
<td valign="top">

This is a security event.

</td>
</tr>
<tr>
<td valign="top">

Events related to invalid session cookies

</td>
<td valign="top">

An attempt was made to access a componentr with an invalid session cookie.

</td>
<td valign="top">

The security event message contains the following text:

`Attempting to access [component] with an invalid session cookie: (key)`

</td>
<td valign="top">

This is a security event.

</td>
</tr>
<tr>
<td valign="top">

Events related to the workspace lifecycle

</td>
<td valign="top">

A workspace \(dev space\) has been started, stopped, or deleted.

</td>
<td valign="top">

The configuration modification message contains one of the following:

-   `identifier: AppStudio`
-   `workspaceI": {wsID}`

-   `action: {starting/stopping/delete}`




</td>
<td valign="top">

This is a configuration event.

Changes to personal data.

</td>
</tr>
<tr>
<td valign="top">

Events related to admin access to workspaces.

</td>
<td valign="top">

An administrator accessed a workspace they do not own.

</td>
<td valign="top">

The message contains one of the following:

-   `User: {userEmail}`
-   `DataType: DevSpace`

-   `Role: admin`

-   `AccessedData: [{targetUrl}]`




</td>
<td valign="top">

This is a data access event.

Access to sensitive personal data.

</td>
</tr>
<tr>
<td valign="top">

Events related to malware detection.

</td>
<td valign="top">

Malware was detected in a workspace.

</td>
<td valign="top">

The message contains one of the following:

-   `eventType: malware_detection`
-   `workspaceID: {wsId}`

-   `findings: [array of findings]`

-   `infectedFiles: [array of infected files]`




</td>
<td valign="top">

This is a security event.

</td>
</tr>
<tr>
<td valign="top">

Events related to tenant status changes.

</td>
<td valign="top">

The subscription status of a tenant has changed.

</td>
<td valign="top">

The configuration modification message contains:

-   `subscription status changed for tenant {tenantID} from {oldStatus} to {newStatus}`



</td>
<td valign="top">

This is a configuration event.

</td>
</tr>
<tr>
<td valign="top">

Events related to unauthorized access attempts.

</td>
<td valign="top">

A user attempted to access a workspace or admin API without the proper permissions.

</td>
<td valign="top">

The message contains:

-   `Attempting to access [API/workspace] without [permission type] permissions`
-   JWT details \(such as, user, tenant, scope, etc.\)




</td>
<td valign="top">

This is a security event.

Permission types include:

-   Developer permissions

-   Admin permissions

-   Workspace owner permissions




</td>
</tr>
</table>



## Mandatory Fields in Audit Logs

All audit log messages must include the following fields \(where applicable\):


<table>
<tr>
<th valign="top">

Field

</th>
<th valign="top">

Description

</th>
<th valign="top">

When Required

</th>
</tr>
<tr>
<td valign="top">

Workspace ID \(WSID\)

</td>
<td valign="top">

The unique identifier of the workspace.

</td>
<td valign="top">

All containters.

</td>
</tr>
<tr>
<td valign="top">

User Email/Username

</td>
<td valign="top">

The email or username of the user.

</td>
<td valign="top">

Only for components with authentication token.

</td>
</tr>
<tr>
<td valign="top">

Identifier

</td>
<td valign="top">

Always `AppStudio` for all workspace-related audit logs.

</td>
<td valign="top">

All workspace-related events.

</td>
</tr>
</table>



## Kubernetes API Audit Log Events

The following events are logged automatically by Kubernetes API audit policies:


<table>
<tr>
<th valign="top">

Event Grouping

</th>
<th valign="top">

Which Events Are Logged

</th>
<th valign="top">

How to Identify Related Log Events

</th>
</tr>
<tr>
<td valign="top">

Workspace Manager

Kubernetes API calls

</td>
<td valign="top">

The Workspace Manager performed start, stop, or delete operations on workspaces in the working cluster.

</td>
<td valign="top">

-   The `user` field contains:`system:serviceaccount:webide-system:workspace-manager`

-   `category: audit.configuration`

-   The `objectRef` field contains workspace resource details




</td>
</tr>
<tr>
<td valign="top">

Workspace Controller

Kubernetes API calls

</td>
<td valign="top">

The Workspace Controller updated the workspace status or configuration in the working cluster.

</td>
<td valign="top">

-   The `user` field contains: `system:serviceaccount:webide-system:ws-controller`
-   category: audit.configuration




</td>
</tr>
<tr>
<td valign="top">

Kubernetes API authentication failures

</td>
<td valign="top">

An authentication or authorization failure occurred when attempting to access the Kubernetes API.

</td>
<td valign="top">

-   `responseStatus: 401`
-   Request details include the attempted operation



</td>
</tr>
</table>



## Related Information

-   [SAP Audit Log Service for SAP BTP](https://help.sap.com/docs/sap-audit-log)
-   [Audit Log Retrieval API for Cloud Foundry](https://help.sap.com/docs/btp/sap-business-technology-platform/audit-log-retrieval-api-usage-for-subaccounts-in-cloud-foundry-environment)

