<!-- loio01e69c53003c4b0a8a64310a3f08867d -->

# Manage Authorizations

To develop using SAP Business Application Studio or manage data stored by the tool, the relevant role needs to be assigned.

Developers using SAP Business Application Studio must be assigned to developer roles created by the `Business_Application_Studio_Developer` role template.

To allow administrator operations using SAP Business Application Studio, the relevant users must be assigned to administrator roles created by the `Business_Application_Studio_Administrator` role template.

To allow a developer to create an SAP Business Application Studio extension, the relevant user must be assigned to deployer roles created by the `Business_Application_Studio_Extension_Deployer` role template.

You can use any SAML 2.0 standard compliant identity provider. See[Trust and Federation with SAML 2.0 Identity Providers](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/cb1bc8f1bd5c482e891063960d7acd78.html).



<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_x4s_bsf_xhb"/>

## Prerequisites

-   Your subaccount is subscribed to SAP Business Application Studio. See [Subscribe to SAP Business Application Studio](Subscribe_to_SAP_Business_Application_Studio_6331319.md).




<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_k3m_zhf_gkb"/>

## Manage Role Collections

> ### Note:  
> The Developer and Administrator role collections together with their corresponding templates are created automatically when you subscribe to SAP Business Application Studio.
> 
> You can skip this section and go to the **Assigning Permissions** section below.

Role collections are user-related authorizations that restrict access to resources and services based on defined user permissions. They consist of individual roles. The roles are based on role templates. For SAP Business Application Studio there are 3 role templates available: Developer role, Deployer role, and Administrator role.

The Developer role allows developers to load and develop applications using SAP Business Application Studio.

The Deployer role allow developers to create an SAP Business Application Studio extension.

The Administrator role allows administrators to manage \(export and delete\) user data.

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Role Collections*.
3.  Select an existing role collection or choose *New Role Collection*.
4.  If you are creating a new role collection, provide a name for the new role.
5.  Select your role collection and choose *Add Role*.
    1.  From the *Application Identifier* dropdown list, select `<region<IAAS_#>>-app-studio!t<generated-uaa-number>`.

        For example, `jp20-app-studio!t333*`

    2.  From the *Role Template* dropdown list, select the relevant role:
        -   Select `Business_Application_Studio_Developer` to create a role collection for developers.
        -   Select `Business_Application_Studio_Extension_Deployer` to create a role collection for developers who can deploy extensions.
        -   Select `Business_Application_Studio_Administrator` to create a role collection for administrators.
    3.  Save your changes.



<a name="loio01e69c53003c4b0a8a64310a3f08867d__section_xmh_h4n_zhb"/>

## Creating Role Collections for the Beta version of the business application

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

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Trust Configuration*.
3.  Select the default IdP by clicking on the name attribute. The name might be *SAP ID Service* or *Default Identity provider*.
4.  From the Navigation area, choose *Role Collection Assignment*.
5.  Enter the e-mail of the user to whom you want to give permissions.
6.  Choose *Show Assignments*.
7.  Choose *Assign Role Collection*.
8.  From the *Role Collection* dropdown list, select the relevant role collection.

To assign permissions to groups, follow the instructions in the [Map Role Collections to User Groups](https://help.sap.com/viewer/65de2977205c403bbc107264b8eccf4b/Cloud/en-US/51acfc82c0c54db59de0a528f343902c.html) topic.

