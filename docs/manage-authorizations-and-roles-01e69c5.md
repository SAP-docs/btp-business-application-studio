<!-- loio01e69c53003c4b0a8a64310a3f08867d -->

# Manage Authorizations and Roles

The subaccount administrator can assign the user a role for developing with SAP Business Application Studio or for managing data.

Role collections are user-related authorizations that restrict access to resources and services based on defined user permissions. They consist of individual roles. The roles are based on role templates. For SAP Business Application Studio there are three relevant role templates available: Developer role, Extension Deployer role, and Administrator role:

-   To allow development using SAP Business Application Studio, you must assign the Developer role to the developer.

    The Developer role allows developers to develop applications using SAP Business Application Studio.

-   To allow administrator operations using SAP Business Application Studio, you must assign the Administrator role to the user.

    The Administrator role allows administrators to manage \(export and delete\) user data and to restart a user's dev space. See [Export and Download Personal Data from Specific Users](export-and-download-personal-data-from-specific-users-8091e47.md), [Delete Personal Data](delete-personal-data-03da2fa.md), and [Restart a Dev Space](restart-a-dev-space-1f54583.md).

    > ### Note:  
    > It is recommended to limit the number of administrators with full management permissions.

-   To allow a developer to create an SAP Business Application Studio extension, you must assign the Extension Deployer role to the user.

The Developer and Administrator role collections together with their corresponding role templates are created automatically when you subscribe to SAP Business Application Studio.

> ### Note:  
> If you want to perform both administrator and developer tasks, you must have both roles assigned.



<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_x4s_bsf_xhb"/>

## Prerequisites

-   Your subaccount is subscribed to SAP Business Application Studio. See [Subscribe to SAP Business Application Studio](subscribe-to-sap-business-application-studio-6331319.md).

-   You must be a subaccount administrator to assign roles.
-   You're using a SAML 2.0 standard compliant identity provider. See[Trust and Federation with SAML 2.0 Identity Providers](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/cb1bc8f1bd5c482e891063960d7acd78.html).
-   If you live in the China \(Shanghai\) region, you must create a new role collection before assigning permissions. See [Manage Role Collections](manage-role-collections-7870faf.md).



<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_xmh_h4n_zhb"/>

## Creating Role Collections for the Beta Version of the Business Application

You can create an administrator role collection and a developer role collection that will be assigned to the relevant users.

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Role Collections*.
3.  Select an existing role collection or choose *New Role Collection*.
4.  If you're creating a new role collection, provide a name for the new role.
5.  Select your role collection and choose *Add Role*.
    1.  From the *Application Identifier* dropdown list, select `devxspace-h2o!t<generated-uaa-number>`.
    2.  From the *Role Template* dropdown list, select `Business_Application_Studio_Developer` to create a role collection for developers or `Business_Application_Studio_Administrator` to create a role collection for administrators.
    3.  Save your changes.




<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_mrx_zhd_pdb"/>

## Assigning Permissions

You can assign permissions as follows:

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Role Collections*.
3.  Select an existing role collection:
    -   Select a role collection that was created automatically when you subscribed to SAP Business Application Studio.
    -   If you live in the China \(Shanghai\) region, select a role collection that you created, as described in the [Prerequisites](manage-authorizations-and-roles-01e69c5.md#loio01e69c53003c4b0a8a64310a3f08867d__section_x4s_bsf_xhb).

4.  Click *Edit*.
5.  Enter the email address of the user who you want to give permissions to in the *ID* field.
6.  Select the relevant identity provider, for example, *Default Identity provider*.
7.  Enter the email address of the user who you want to give permissions to in the *E-Mail* field.
8.  Click *Save*.

To assign permissions to groups, follow the instructions in the [Map Role Collections to User Groups](https://help.sap.com/products/BTP/65de2977205c403bbc107264b8eccf4b/51acfc82c0c54db59de0a528f343902c.html) topic.



If you want to create a different set of roles, see [Manage Role Collections](manage-role-collections-7870faf.md).

-   **[Manage Role Collections](manage-role-collections-7870faf.md "You can create a new role collection with a different set of roles or you can update
		an existing role collection.")**  
You can create a new role collection with a different set of roles or you can update an existing role collection.

