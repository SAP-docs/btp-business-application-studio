<!-- loio1f5458361583460b83eb0e208b89b0ed -->

# Restart a Dev Space

You can change the state of a dev space to *Running*.

1.  In your browser, get a list of all workspaces in a specific subaccount:

    ```
    https://<sap-business-application-studio-url>/ws-manager/api/v1/workspace?all=true
    ```

2.  Enter your administrator credentials in the login page.
3.  From the list provided, identify the dev space you want to wake up \(for example by searching for the username property\).
4.  Copy the `id` property under the `config` section. This ID is the `<ws-id>` parameter used in the request in the last step.
5.  Copy the `displayname` property under the `labels` section. This display name is the `<display-name>` parameter used in the request in the last step.
6.  Open a new tab in the browser and fetch your JWT token by sending the following request:

    ```
    GET https://<sap-business-application-studio-url>/jwt
    
    ```

7.  Copy the JWT value from the response.
8.  In the REST API tool, send a PUT HTTP request to the following API:

    ```
    PUT https://<sap-business-application-studio-url>/ws-manager/api/v1/workspace/<ws-id>?all=true
    
    Request Header:
    X-Approuter-Authorization: Bearer <JWT_Token>
    
    Request Body:
    {"suspended":false, "WorkspaceDisplayName":"<display-name>"}
    ```

    > ### Note:  
    > If you're performing actions on your own workspace, you don't need to include the `?all=true` parameter.


