<!-- loio03da2fa7b94841aebe756fec24ee9456 -->

# Delete Personal Data

You can delete personal data stored in your workspace.

1.  In your browser, get a list of all workspaces contained in a specific subaccount:

    ```
    https://<sap-business-application-studio-url>/ws-manager/api/v1/workspace?all=true
    ```

2.  Enter your administrator credentials in the login page.
3.  From the list provided, identify the dev space you want to delete \(for example by searching for the username property\).
4.  Copy the `id` property under the `config` section. This ID is the `<ws-id>` parameter used in the request below.
5.  Make sure the dev space you want to delete is in the *Running* state. If not, restart the dev space before exporting the data. See [Restart a Dev Space](Restart_a_Dev_Space_1f54583.md).
6.  Open a new tab in the browser and fetch your JWT token by sending the following request:

    ```
    https://<sap-business-application-studio-url>/jwt
    
    ```

7.  Copy the JWT value from the response.
8.  In the REST API tool, send a DELETE HTTP request to the following API:

    ```
    DELETE https://<sap-business-application-studio-url>/ws-manager/api/v1/workspace/<ws-id>
    
    Request Header:
    X-Approuter-Authorization: Bearer <JWT_Token>
    ```


