<!-- loio8091e47403f2469e824e4d6841fea22d -->

# Export and Download Personal Data from Specific Users

You can export and download personal data from the dev spaces of specific users.

1.  In your browser, get a list of all workspaces contained in a specific subaccount:

    ```
    https://<sap-business-application-studio-url>/ws-manager/api/v1/workspace?all=true
    ```

2.  Enter your administrator credentials in the login page.
3.  From the list provided, identify the dev space you want to export \(for example by searching for the username property\).
4.  Copy the `baseUrl` property under the `runtime` section in the dev space you want to export.

    This URL is the `<runtime-url>` parameter used in the request in Step 6.

5.  Make sure the dev space you want to export is in the *Running* state. If not, restart the dev space before exporting the data. See [Restart a Dev Space](restart-a-dev-space-1f54583.md).
6.  Use the following request to export data:

    ```
    https://<sap-business-application-studio-url>/login?e=<runtime-url>/wsmaintain/export
    ```

    > ### Note:  
    > Use the downloaded data with care as it contains unprotected personal data.


