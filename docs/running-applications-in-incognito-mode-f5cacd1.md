<!-- loiof5cacd13e58b4382b86796e315c77bf2 -->

# Running Applications in Incognito Mode

Running an application in Incognito mode allows you to test it with different users.

To run an application in Incognito mode:

1.  Run the application from SAP Business Application Studio. The application opens in a new window.
2.  Copy the URL from the opened application window. For example, `https://port4004-workspaces-ws-ln78g.region10.int.applicationstudio.cloud.sap/`
3.  Open a new window in Incognito mode.
4.  Manually enter a URL using the following format: `<`SAP Business Application Studio`URL with no path>/login?e=<application URL from step 2>`.

    For example, `https://bas-extensions.region10cf.int.applicationstudio.cloud.sap/login?e=https://port4004-workspaces-ws-ln78g.region10.int.applicationstudio.cloud.sap/` 

5.  Login using your SAP Business Application Studio user credentials.
6.  If the application requires authentication, provide the application user you want to use for testing.

