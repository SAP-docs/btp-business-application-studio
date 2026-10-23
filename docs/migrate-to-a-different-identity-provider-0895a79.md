<!-- loio0895a797052441eeb9840390f4f7ae3d -->

# Migrate to a Different Identity Provider

Migrating between Identity Providers \(IdPs\) transitions all SAP Business Application Studio dev spaces that use a given IdP to a new IdP. After the migration, those dev spaces will authenticate against the new provider.

This migration process updates all dev spaces associated with a specific IdP, ensuring they work seamlessly with the new provider once the migration is complete.



## Prerequisites

Before proceeding with the migration, make sure you perform the following steps:

1.  Ensure you have administrator privileges for your SAP Business Application Studio instance. See [Manage Authorizations and Roles](manage-authorizations-and-roles-01e69c5.md).

2.  Identify the issuer URL of the source IdP \(current provider\) and the issuer URL of the target IdP \(destination provider\).

    1.  Open the SAP BTP cockpit.
    2.  Navigate to your subaccount.
    3.  Go to *Security* \> *Trust Configuration*.
    4.  In the table, under the *Origin Key* column, copy the value of your current IdP. This is the value of your `sourceidp`.
    5.  In the table, under the *Origin Key* column, copy the value of your target IdP. This is the value of your `targetidp`.




## Migrate Using the Admin Tool

1.  Open the Admin Tool.

    ```
    https://<landscape-url>/workspace-manager-ui/admin/index.html
    ```

2.  Go to the *Migration* tab.
3.  In the *Migrate Dev Space IdP* section, click *Migrate*.
4.  Provide the source and the target IdPs, and click *Migrate*.



## Migrate Using the API

To migrate dev spaces from one IdP to another:

1.  Make sure you have a REST API tool, such as Postman, to manage API requests.

2.  Open a web browser and send the following request:

    ```
    GET https://<sap-business-application-studio-url>/jwt
    
    ```

3.  Copy the JWT token from the response.

4.  In the browser, send a GET HTTP request to the following API:

    ```
    GET https://<sap-business-application-studio-url>/ws-manager/api/v1/metadata
    
    ```

5.  Copy the `host` property value from the response.

6.  In the REST API tool, send a PUT HTTP request to the following API:

    ```
    PUT https://<host_value>/tenant-manager/api/v1/admin/migrate-idp
    
    ```

    **Request Header:**

    ```
    Authorization: Bearer <JWT_token>
    ```

    **Request Body:**

    ```
    
       {
         "sourceIdp": "old-idp",
         "targetIdp": "new-idp"
       }
    
    ```

    Replace the `sourceIdp` and `targetIdp` values with your actual IdP issuer URLs.


> ### Note:  
> The users' IDs should be the same in both source and target IdPs.

> ### Note:  
> This migration affects all the dev spaces in your subaccount that are currently configured with the source IdP.

