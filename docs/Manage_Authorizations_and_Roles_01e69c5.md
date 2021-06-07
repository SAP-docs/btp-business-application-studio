<!-- loio01e69c53003c4b0a8a64310a3f08867d -->

# Manage Authorizations and Roles

To develop using SAP Business Application Studio or manage data stored by the tool, the relevant role needs to be assigned by the subaccount administrator.

-   To allow development using SAP Business Application Studio, the developer must be assigned the Developer role.
-   To allow administrator operations using SAP Business Application Studio, the relevant user must be assigned the Administrator role.
-   To allow a developer to create an SAP Business Application Studio extension, the relevant user must be assigned the Extension Deployer role.

    The Developer and Administrator role collections together with their corresponding templates are created automatically when you subscribe to SAP Business Application Studio.




<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_x4s_bsf_xhb"/>

## Prerequisites

-   Your subaccount is subscribed to SAP Business Application Studio. See [Subscribe to SAP Business Application Studio](Subscribe_to_SAP_Business_Application_Studio_6331319.md).

-   You must be a subaccount administrator to assign roles.
-   You are using a SAML 2.0 standard compliant identity provider. See[Trust and Federation with SAML 2.0 Identity Providers](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cb1bc8f1bd5c482e891063960d7acd78.html).



<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_xmh_h4n_zhb"/>

## Creating Role Collections for the Beta version of the business application

You can create an administrator role collection and a developer role collection that will be assigned to the relevant users.

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Role Collections*.
3.  Select an existing role collection or choose *New Role Collection*.
4.  If you are creating a new role collection, provide a name for the new role.
5.  Select your role collection and choose *Add Role*.
    1.  From the *Application Identifier* dropdown list, select `devxspace-h2o!t<generated-uaa-number>`.
    2.  From the *Role Template* dropdown list, select `Business_Application_Studio_Developer` to create a role collection for developers or `Business_Application_Studio_Administrator` to create a role collection for administrators .
    3.  Save your changes.



<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_mrx_zhd_pdb"/>

## Assigning Permissions

Role collections are user-related authorizations that restrict access to resources and services based on defined user permissions. They consist of individual roles. The roles are based on role templates. For SAP Business Application Studio there are 3 relevant role templates available: Developer role, Extension Deployer role, and Administrator role:

-   The Developer role allows developers to load and develop applications using SAP Business Application Studio.
-   The Extension Deployer role allows developers to create an SAP Business Application Studio extension.
-   The Administrator role allows administrators to manage \(export and delete\) user data.

You can assign permissions as follows:

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Trust Configuration*.
3.  Select the default IdP by clicking on the name attribute. The name might be *SAP ID Service* or *Default Identity provider*.
4.  Enter the e-mail of the user to whom you want to give permissions.
5.  Choose *Show Assignments*.
6.  Choose *Assign Role Collection*.
7.  From the *Role Collection* dropdown list, select the relevant role collection.

To assign permissions to groups, follow the instructions in the [Map Role Collections to User Groups](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/51acfc82c0c54db59de0a528f343902c.html) topic.



<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_k3m_zhf_gkb"/>

## Manage Role Collections \(Optional\)

You can create a different set of roles as follows:

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Role Collections*.
3.  Select an existing role collection or click ![](images/Create_Role_Collection_icon_09b623b.png) \(Create Role Collection\), provide a name, click *Create*, and select the new role collection.
4.  Click *Edit*.
5.  Open the Role Name dialog box to add a new role.
    1.  From the *Application Identifier* dropdown list, select `<region<IAAS_#>>-app-studio!t<generated-uaa-number>`.

        For example, `jp20-app-studio!t333*`

    2.  From the *Role Template* dropdown list, select the relevant role:
        -   Select `Business_Application_Studio_Developer` to create a role collection for developers.
        -   Select `Business_Application_Studio_Extension_Deployer` to create a role collection for developers who can deploy extensions.
        -   Select `Business_Application_Studio_Administrator` to create a role collection for administrators.
    3.  Select the *Role Name* from the table.
    4.  Click *Add*.
6.  Save your changes.

