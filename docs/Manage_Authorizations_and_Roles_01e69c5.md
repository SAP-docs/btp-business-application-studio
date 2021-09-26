<!-- loio01e69c53003c4b0a8a64310a3f08867d -->

# Manage Authorizations and Roles

The subaccount administrator can assign a role to the user for developing with SAP Business Application Studio or for managing data.

Role collections are user-related authorizations that restrict access to resources and services based on defined user permissions. They consist of individual roles. The roles are based on role templates. For SAP Business Application Studio there are 3 relevant role templates available: Developer role, Extension Deployer role, and Administrator role:

-   To allow development using SAP Business Application Studio, the developer must be assigned the Developer role.

    The Developer role allows developers to develop applications using SAP Business Application Studio.

-   To allow administrator operations using SAP Business Application Studio, the relevant user must be assigned the Administrator role.

    The Administrator role allows administrators to manage \(export and delete\) user data and to restart a user's dev space. See [Export and Download Personal Data from Specific Users](Export_and_Download_Personal_Data_from_Specific_Users_8091e47.md), [Delete Personal Data](Delete_Personal_Data_03da2fa.md), and [Restart a Dev Space](Restart_a_Dev_Space_1f54583.md).

-   To allow a developer to create an SAP Business Application Studio extension, the relevant user must be assigned the Extension Deployer role.

The Developer and Administrator role collections together with their corresponding role templates are created automatically when you subscribe to SAP Business Application Studio.



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

You can assign permissions as follows:

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Trust Configuration*.
3.  Select the default IdP by clicking on the name attribute. The name might be *SAP ID Service* or *Default Identity provider*.
4.  Enter the e-mail of the user to whom you want to give permissions.
5.  Click *Show Assignments*.
6.  Click *Assign Role Collection*.
7.  From the *Assign Role Collection* dropdown list, select the relevant role collection:
    -   Select `Business_Application_Studio_Developer` to assign a role collection to a developer.
    -   Select `Business_Application_Studio_Administrator` to assign a role collection to an administrator.
    -   Select `Business_Application_Studio_Extension_Deployer` to assign a role collection to an extension developer.

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

