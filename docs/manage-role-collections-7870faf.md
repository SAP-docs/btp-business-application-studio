<!-- loio7870fafa343543829c49a15d0e37c9c0 -->

# Manage Role Collections

You can create a new role collection with a different set of roles or you can update an existing role collection.

To create a different set of roles or update a role collection, perform the following steps:

1.  In the SAP BTP cockpit, navigate to your subaccount.
2.  From the Navigation area, choose *Security* \> *Role Collections*.
3.  Select an existing role collection or click ![](images/Create_Role_Collection_icon_09b623b.png) \(Create Role Collection\), provide a name, click *Create*, and select the new role collection.
4.  Click *Edit*.
5.  Open the *Role Name* dialog box to add a new role.
    1.  From the *Role Template* dropdown list, select the relevant role:
        -   Select `Business_Application_Studio_Developer` to create a role collection for developers.
        -   Select `Business_Application_Studio_Extension_Deployer` to create a role collection for developers who can deploy extensions.
        -   Select `Business_Application_Studio_Administrator` to create a role collection for administrators.

    2.  From the *Application Identifier* dropdown list, select `<region<IAAS_#>>-app-studio!t<generated-uaa-number>`.

        For example, `jp20-app-studio!t333*`

    3.  Select the *Role Name* from the table and click *Add*.

6.  Click *Save*.

