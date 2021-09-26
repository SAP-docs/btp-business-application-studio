<!-- loio2064b4e1cd2e4eb3b8851d810fabddb6 -->

# Create and Deploy an SAP Business Application Studio Extension

Create an SAP Business Application Studio extension that includes VS Code extensions and Yeoman generators and deploy it to your subaccount.

**Prerequisites**

-   You must have the *Extension deployer* role. See [Manage Authorizations](https://help.sap.com/viewer/9d1db9835307451daa8c930fbd9ab264/Cloud/en-US/01e69c53003c4b0a8a64310a3f08867d.html).

-   You must enable the *SAP Business Application Studio Extension Development* additional extension in your dev space. See [Working in the Dev Space Manager](Working_in_the_Dev_Space_Manager_ad40d52.md).


To create an SAP Business Application Studio extension:

1.  In your workspace, create an extension definition file called `extension.json` with the following content.

    > ### Note:  
    > Make sure to replace the placeholders in the file with the relevant information.

    The extension definition file includes two main parts:

    -   The extension metadata.

    -   The list of components that are part of the extension: VS Code extensions, Yeoman generators, and global NPM packages.

        > ### Note:  
        > You must include at least one of these components in the file.

    > ### Sample Code:  
    > ```
    > {
    >   "apiVersion": "1",
    >   "name": "<technical name>",
    >   "namespace": "ext-<subdomain - where <subdomain> is the subdomain of the subaccount of the relevant BAS instance.>",
    >   "about": {
    >     "description": "<description>",
    >     "author": "<author>",
    >     "tagline": "<the extension name displayed in the dev space manager>",
    >     "thumbnail": "<thumbnail - The thumbnail must be a base64 encoded SVG>"
    >   },
    >   "version": "<version>",
    >   "yeomanPackages": [
    >     {
    >       "name": "<package name>",
    >       "versionRange": "<package version>"
    >     }
    >   ],
    >   "globalNpmPackages": [
    >     {
    >       "name": "<package name>",
    >       "versionRange": "<package version>"
    >     }
    >   ],
    >   "vscodeExtensions": [
    >     {
    >       "source": "url",
    >       "uri": "<the url to the .vsix file>"
    >     }
    >   ]
    >  }
    > ```

2.  Open a terminal and run the following command to deploy the extension to the subaccount:

    ```
    wex deploy
    ```

3.  Go to the Dev Space Manager to verify that the SAP Business Application Studio extension you created is visible as an additional extension. All developers working on the subaccount to which you deployed can enable this extension from their Dev Space Manager.

**To delete the extension:**

1.  Open a terminal and run the following command:

    ```
    wex delete -x <namespace>/<ext-name>
    ```

    > ### Note:  
    > Deletion of an extension is only possible if the extension is not being used by any dev space.


