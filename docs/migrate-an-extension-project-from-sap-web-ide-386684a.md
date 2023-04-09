<!-- loio386684a2593941a48812cdbf85197eb3 -->

# Migrate an Extension Project from SAP Web IDE

To add new extensions to your extension project, you need to first migrate it from SAP Web IDE.



<a name="loio386684a2593941a48812cdbf85197eb3__section_psd_mtq_bwb"/>

## Prerequisite

Copy the destination from the SAP Web IDE subaccount to the SAP Business Application Studio subaccount:

1.  Find the name of the destination to be copied from the extension project’s `neo-app.json` file.

2.  Export the destination from the Neo subaccount.

    See [Exporting Solutions](https://help.sap.com/docs/BTP/ea72206b834e4ace9cd834feed6c0e09/14a0ff1480494bcd993674061fb4f505.html).

3.  Go to the SAP Business Application Studio subaccount and import the destination.

    See [Import Destinations](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/91ee9db4737d43b798997ab93e7f3d6e.html).

4.  Add the following new property:


    <table>
    <tr>
    <th valign="top">

    Property


    
    </th>
    <th valign="top">

    Value


    
    </th>
    </tr>
    <tr>
    <td valign="top">

    ***HTML5.DynamicDestination***


    
    </td>
    <td valign="top">

    ***true***


    
    </td>
    </tr>
    </table>
    
5.  Make sure that the following properties were added:


    <table>
    <tr>
    <th valign="top">

    Property


    
    </th>
    <th valign="top">

    Value


    
    </th>
    </tr>
    <tr>
    <td valign="top">

    ***WebIDEEnabled***


    
    </td>
    <td valign="top">

    ***true***


    
    </td>
    </tr>
    <tr>
    <td valign="top">

    ***WebIDEUsage***


    
    </td>
    <td valign="top">

    ***odata\_abap,dev\_abap***


    
    </td>
    </tr>
    </table>
    
    See [Connecting to External Systems](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/7e49887e6fd34182bebeca5a6841a0cc.html).

6.  Configure the Cloud Connector to your system.

    See [Cloud Connector](https://help.sap.com/docs/CP_CONNECTIVITY/cca91383641e40ffbe03bdc78f00f681/e6c7616abb5710148cfcf3e75d96d596.html).




<a name="loio386684a2593941a48812cdbf85197eb3__section_s5r_mfr_bwb"/>

## Procedure

1.  Clone your extension project to SAP Business Application Studio from your Git repository or import the project that you exported from the SAP Web IDE workspace.
2.  Make sure that all the resources created in SAP Web IDE are included in this project, including the `.che` folder and the `neo-app.json` file.
3.  If the extension project doesn’t include a `manifest.json` file, create a dummy `manifest.json` file, according to the steps in the [Create a `manifest.json` File](migrate-an-extension-project-from-sap-web-ide-386684a.md#loio386684a2593941a48812cdbf85197eb3__section_f2k_ltq_bwb) section.
4.  In the popup window that appears, click *Start Migration*.

    The *Migration* view opens.

    > ### Note:  
    > You can also open the *Migration* view by entering ***Fiori: Migrate Project for use in Fiori tools*** in the command palette.

5.  In the *Migration* view, perform the following steps:
    1.  Select the destination associated with your original application system \(the destination from the [Prerequisite](migrate-an-extension-project-from-sap-web-ide-386684a.md#loio386684a2593941a48812cdbf85197eb3__section_psd_mtq_bwb) section\).
    2.  Select an SAPUI5 version.

        Currently, the minimum version required is 1.71.0.

    3.  Start the migration.

        See [Migration steps](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/70d41f3ee29d453a90efab3ce025d450.html#migration-steps) for more information.


6.  Add a `createExtconfig.js` file under the project root, with the following content:

    ```
    const fs = require('fs');
    const fileData = fs.readFileSync("./.che/project.json","utf8");
    const parsedFileData = JSON.parse(fileData);
    const settings = parsedFileData.attributes["sap.watt.common.setting"];
    const parsedSettings = JSON.parse(settings);
    fs.writeFileSync("./.extconfig.json", JSON.stringify(parsedSettings.extensibility));
    
    ```

7.  Open the terminal from the extension project's root folder and run the following command:

    ```
    node createExtconfig.js
    ```

8.  Verify that the `.extconfig.json` configuration file was created under the extension project's root folder, which is required for further development of this extension project in SAP Business Application Studio.
9.  Delete the `createExtconfig.js` file from your extension project.



<a name="loio386684a2593941a48812cdbf85197eb3__section_wzg_zsq_bwb"/>

## Development Actions after Migration

You can add extensions, preview, and deploy. See [Extend SAPUI5 Applications](extend-sapui5-applications-47c6ad8.md) for more information.



<a name="loio386684a2593941a48812cdbf85197eb3__section_f2k_ltq_bwb"/>

## Create a `manifest.json` File

If the extension project that you imported doesn't have a `manifest.json` file, create a dummy `manifest.json` file.

1.  Identify the `component-id`.

    From the content of the `webapp/Component.js` file, extract the string marked as `<component-id>`:

    ```
    Component.extend("<component-id>.Component",
    ```

2.  Add a `webapp/manifest.json` file with the following content:

    ```
    {
        "_version": "1.1.0",
        "sap.app": {
            "_version": "1.1.0",
            "id": "<component-id>",
            "type": "application",
            "applicationVersion": {
                "version": "1.0.0"
            },
            "title": ""
        },
        "sap.ui": {
            "_version": "1.1.0",
            "technology": "UI5",
            "icons": {
                "icon": "",
                "favIcon": ""
            },
            "supportedThemes": []
        },
        "sap.ui5": {
            "_version": "1.1.0",
            "dependencies": {
                "minUI5Version": "1.71.0"
            }
        }
    }
    
    ```

3.  In the created `manifest.json` file, replace `<component-id>` with the value that you extracted in step 1.

