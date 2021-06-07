<!-- loio4168f836ff43446c8715de4800fef9ea -->

# Manage Authorizations

As a global account admin, use the terminal for SAP BTP to carry out the following tasks in your global accounts and subaccounts.



<a name="loio4168f836ff43446c8715de4800fef9ea__section_kcc_ctl_whb"/>

## Prerequisites

-   Make sure you are subscribed to the SAP Business Application Studio application. See [Subscribe to SAP Business Application Studio](Subscribe_to_SAP_Business_Application_Studio_b53e261.md).
-   Make sure you have performed the following procedures described the [Account Administration Using the CLI](https://help.sap.com/viewer/824aa13243e849b0a9d33859c1709801/Operator/en-US/7c6df2db6332419ea7a862191525377c.html) topic.
    -   Download the client
    -   Get Started
    -   Login to the subdomain of the subaccount



<a name="loio4168f836ff43446c8715de4800fef9ea__section_g53_41r_whb"/>

## Manage Role Collections

Role collections are user-related authorizations that restrict access to resources and services based on defined user permissions. They consist of individual roles. The roles are based on role templates. For SAP Business Application Studio there are 2 role templates available: Developer role and Administrator role.

1.  Create the `Business_Application_Studio_Developer` role to allow developers to load and develop applications using SAP Business Application Studio.
    1.  Create a Developer role collection.

        ```
        sapcp create security/role-collection "Dev Role Collection Name" --description "Dev role collection" (optional)
        ```

    2.  List all subscribed applications and fetch the SAP Business Application Studio application ID. This will provide the `"appId"` to be used in the request below.

        ```
        sapcp list security/app
        ```

    3.  Add the `Business_Application_Studio_Developer` role to the role collection:

        ```
        sapcp add security/role "Business_Application_Studio_Developer " --of-role-template "Business_Application_Studio_Developer " --of-app "appId" --to-role-collection "Dev Role Collection Name"
        
        ```

2.  Create the `Business_Application_Studio_Administrator` role to manage \(export and delete\) user data.
    1.  Create an Administrator role collection.

        ```
        sapcp create security/role-collection "Admin Role Collection Name" --description "Admin role collection" (optional)
        ```

    2.  List all subscribed applications and fetch the SAP Business Application Studio application ID. This will provide the `"appId"` to be used in the request below.

        ```
        sapcp list security/app
        ```

    3.  Add the `Business_Application_Studio_Administrator` role to the role collection:

        ```
        sapcp add security/role "Business_Application_Studio_Administrator " --of-role-template "Business_Application_Studio_Administrator " --of-app "appId" --to-role-collection "Admin Role Collection Name"
        
        ```




<a name="loio4168f836ff43446c8715de4800fef9ea__section_oyy_3dr_whb"/>

## Assign Role Collections to Users

You can assign and unassign role collections to and from users.

1.  Display a list of all users.

    ```
    sapcp list security/user
    ```

2.  Assign a role collection to a user.

    ```
    sapcp assign security/role-collection "<Dev or Admin> Role Collection Name" --to-user "user_name" --of-idp "ldap" (default "ldap")
    ```

3.  Verify the role collection is assigned to the user.

    ```
    sapcp get security/user "user_name"
    ```


> ### Note:  
> You can unassign a user from a role collection.
> 
> ```
> 
> ```

