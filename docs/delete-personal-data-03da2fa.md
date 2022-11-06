<!-- loio03da2fa7b94841aebe756fec24ee9456 -->

# Delete Personal Data

You can delete personal data stored in your workspace.

**Prerequisites**

-   Install a REST API tool such as Postman.


1.  In your browser, get a list of all workspaces in a specific subaccount:

    ```
    https://<sap-business-application-studio-url>/ws-manager/api/v1/workspace?all=true
    ```

2.  Enter your administrator credentials in the login page.
3.  From the list provided, identify the dev space you want to delete \(for example by searching for the username property\).
4.  Copy the `id` property under the `config` section. This ID is the `<ws-id>` parameter used in the request in the last step.
5.  \(Optional\) If you want to export the data before deleting the dev space, the dev space must be in the *Running* state. If the dev space isn’t in the *Running* state, restart the dev space to export the data. See [Restart a Dev Space](restart-a-dev-space-1f54583.md).
6.  Open a new tab in the browser and fetch your JWT token by sending the following request:

    ```
    https://<sap-business-application-studio-url>/jwt
    
    ```

7.  Copy the JWT value from the response.
8.  In the REST API tool, send a DELETE HTTP request to the following API:

    ```
    DELETE https://<sap-business-application-studio-url>/ws-manager/api/v1/workspace/<ws-id>?all=true
    
    Request Header:
    X-Approuter-Authorization: Bearer <JWT_Token>
    ```

    > ### Note:  
    > If you're performing actions on your own workspace, you don't need to include the `?all=true` parameter.


