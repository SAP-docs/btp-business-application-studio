<!-- loioed631d4ee2214e9f932b03d40b2c7e41 -->

# What's New for SAP Business Application Studio 






<table>
<tr>
<th valign="top">

Technical Component



</th>
<th valign="top">

Environment



</th>
<th valign="top">

Title



</th>
<th valign="top">

Description



</th>
<th valign="top">

Action



</th>
<th valign="top">

Lifecycle



</th>
<th valign="top">

Type



</th>
<th valign="top">

Line of Business



</th>
<th valign="top">

Modular Business Process



</th>
<th valign="top">

Product



</th>
<th valign="top">

Latest Revision



</th>
<th valign="top">

Available as of



</th>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

VS Code Updates



</td>
<td valign="top">

You can now enjoy the following new features that are available with the release of VS Code 1.80:

-   [More help when editor is readonly](https://code.visualstudio.com/updates/v1_80#_more-help-when-editor-is-readonly)

    With the introduction of [readonly mode](https://code.visualstudio.com/updates/v1_79#_readonly-mode) in VS Code last milestone, editors can be readonly due to workspace configuration.

    This milestone, we enhanced the notification message in the editor when you try to type in a readonly editor and in some cases provide a link to change the `files.readonly` settings.

-   [Editor group split sizing changed to 'auto'](https://code.visualstudio.com/updates/v1_80#_editor-group-split-sizing-changed-to-auto)

    A new value for the `workbench.editor.splitSizing` setting called `auto` is the new default. In this mode, splitting an editor group distributes the available size evenly to all editor groups only if none of the editor groups has been resized. Otherwise, the space of the split editor group is divided in half and placed in the new editor group.

    The intent of this change is to not break layouts that you have created when you split, but still preserve the previous default behavior of distributing the size evenly otherwise.

-   [Resizable content hover](https://code.visualstudio.com/updates/v1_80#_resizable-content-hover)

    It is now possible to resize the content hover control. You can hover over the control borders and drag the sashes to change the size of the hover.

-   [Terminal - Image Support](https://code.visualstudio.com/updates/v1_80#_image-support)

    Images in the terminal, which were previewed last release, are now enabled by default. Images in a terminal typically work by encoding the image pixel data as text, which is written to the terminal via a special escape sequence. The current protocols supported are [sixel](https://en.wikipedia.org/wiki/Sixel) and the inline images protocol pioneered by iTerm.

    To test images manually, you can download and `cat` a `.six` example file from [the libsixel repository](https://github.com/saitoha/libsixel/tree/master/images).

    This feature can be disabled by setting:

    ```
    "terminal.integrated.enableImages": false
    ```

-   [Testing - Terminal output support](https://code.visualstudio.com/updates/v1_80#_terminal-output-support)

    Previously, test output shown in the *Test Results* view would always be shown in an embedded text editor. This stripped it of rich styling such as colors, styles, and symbols it may have had when run in a terminal. In this release, we show output in a real xterm.js terminal.

    Now that the *Test Results* view is fully featured, the commands to *Show Test Output* have been redirected to open the Test Results view instead of creating a temporary terminal.


This list is based on the VS Code [Updates](https://code.visualstudio.com/updates/v1_80) document.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-08-27



</td>
<td valign="top">

2023-08-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development Experience



</td>
<td valign="top">

SAP Business Application Studio now supports \`login.cf.sap.hana.ondemand.com\` as a trusted domain, including the cf endpoint links.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-08-27



</td>
<td valign="top">

2023-08-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In on-premise scenarios, you can now use SAP Business Application Studio for database development with SAP HANA extended application services, advanced model \(XS advanced\). See [SAP HANA Developer Guide for XS Advanced Model \(SAP Business App Studio\)](https://help.sap.com/docs/SAP_HANA_PLATFORM/cf8b4c5847374960a68b55cb86eae013?locale=en-US&version=2.0.07).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-08-25



</td>
<td valign="top">

2023-08-25



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development Experience



</td>
<td valign="top">

JAVA 17 is now the default Java version for SAP Business Application Studio. You can manually change the default version from the command pallete.

Open the command palette and select *JAVA Set Default JDK*.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-08-03



</td>
<td valign="top">

2023-08-03



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

When working in a *Full Stack Cloud Application* or a *Full Stack Cloud Application Using Productivity Tools* dev space, you can now add SAP S/4HANA or SAP S/4HANA Cloud events to your project from the Service Center and then consume them. See [Add SAP S/4HANA or SAP S/4HANA Cloud Events](https://help.sap.com/docs/bas/developing-business-applications-using-productivity-tools/add-sap-s-4hana-cloud-events).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-07-31



</td>
<td valign="top">

2023-07-31



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development Experience



</td>
<td valign="top">

You can now enable the *Python Tools* extension to improve your Python coding experience.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-07-19



</td>
<td valign="top">

2023-07-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

When working in a *Full-Stack Application Using Productivity Tools* dev space, you can now create a multitenant \(SaaS\) application, which you can share among several consumer subaccounts within your SAP BTP global account. See [Enabling Multitenancy](https://help.sap.com/docs/bas/developing-business-applications-using-productivity-tools/enabling-saas?locale=en-US).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-07-19



</td>
<td valign="top">

2023-07-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

MTA



</td>
<td valign="top">

You can now select a specific MTA extension file for deployment. See [Building and Deploying Multitarget Applications](https://help.sap.com/docs/bas/sap-business-application-studio/building-and-deploying-multitarget-applications?version=Cloud#deploying-multitarget-applications).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-07-17



</td>
<td valign="top">

2023-07-17



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Storyboard



</td>
<td valign="top">

When working in an *SAP Fiori* dev space, you can now use the storyboard to trigger the graphical editors and other tools required to develop an SAP Fiori elements application. See [Storyboard](https://help.sap.com/docs/bas/sap-business-application-studio/storyboard-in-sap-fiori-dev-space?version=Cloud).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-07-17



</td>
<td valign="top">

2023-07-17



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now choose which display option is started by Data Preview:

-   Analysis \(default\)

-   Raw Data


See [Configuring Data Preview Behavior](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/92883c2b13c74649b183590c4b5744ae.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now open the SQL Editor from the context menu of the calculation view nodes. See [Preview Calculation View Output](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/903eff885ebd4c5cadb1e0c3e58f681d.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

User-defined functions are now permitted in non-equi-join expressions, data masking expressions, and restricted columns. See [User-Defined Functions](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/150a8dec9cc64aad96bafb452df29a7b.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now specify start and end times for application-time-period tables. See [Add System Time and Application Time](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/7421507f46ef4e64b060b013076d1b8c.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now add objects to calculation views based on associations, and also add objects with join information. See [Add Objects Based on Association](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/c81cdcbe844745ee9a067fc546723503.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

Optimize join columns are now supported for non-equi-joins. See [Optimize Join Execution](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/6100bb67b2e445329605a3b4650f6e46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, it is now possible to filter by name the list of objects displayed in the *CATALOG* pane of the embedded SAP HANA Database Explorer. See [View Database Objects with the Database Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, use the SAP HANA Project Explorer to bind an application to a service managed by the Service Manager. See [Bind an Application to a Service Managed by the Service Manager](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/818a87c6299a43488f80f92fa8453d4b.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now filter by name the list of databases displayed in the embedded SAP HANA Database Explorer. See [View Database Objects with the Database Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now use the embedded SAP HANA Database Explorer to create SQL `CALL` statements. See [View Database Objects with the Database Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, the SAP HANA Project Explorer now displays a warning if an application is using an outdated version of the HDI deployer \(`@sap/hdi-deploy`\). See [Deploy Artifacts with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now use the SAP HANA artifact-creation Wizard to add a job-schedule artifact \(`.hdbschedulerjob`\) to your database application. See [Scheduler Jobs \(.hdbschedulerjob\)](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2cc2e43458d4abda6788049c58143dc/f92e31d2a23f4470829ab300dcce850e.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now use the SAP HANA Project Explorer to bind an application to a database schema service. See [Bind an Application to a Database Schema Service](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4f5add96a6a04d9f81dbaed135bf84ab.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-06-22



</td>
<td valign="top">

2023-06-22



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

When you select a *Full-Stack Application Using Productivity Tools* dev space, the storyboard opens by default as the initial view. See [Get Started](https://help.sap.com/docs/sap-build/developing-business-applications-using-productivity-tools/storyboard).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-05-31



</td>
<td valign="top">

2023-05-31



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

When working in a *Full-Stack Application Using Productivity Tools* dev space, you can now use the context menu in the Project Explorer view to deploy, delete, or view your last deployed project. See [Deploy an Application](https://help.sap.com/docs/sap-build/developing-business-applications-using-productivity-tools/deploying-applications#deploy-an-application).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-05-31



</td>
<td valign="top">

2023-05-31



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Git



</td>
<td valign="top">

You can now select the changes you want to commit or discard in the Simplified Git view. See [Commit Changes in the Simplified Git View](https://help.sap.com/docs/bas/sap-business-application-studio/commit-changes-in-simplified-git-view?version=Cloud) and [Perform Actions in the Pending Changes Section](https://help.sap.com/docs/bas/sap-business-application-studio/perform-actions-from-pending-changes-section?version=Cloud).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-05-21



</td>
<td valign="top">

2023-05-21



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development Experience



</td>
<td valign="top">

You can now enable the *Headless Testing Framework* extension for your dev space.

This extension allows you to run cross-platform end-to-end tests on a UI5 application, with selectors compatible to OPA5.

See [Using BAS with wdi5](https://ui5-community.github.io/wdi5/#/usage?id=using-bas-with-wdi5).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-05-04



</td>
<td valign="top">

2023-05-04



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Storyboard



</td>
<td valign="top">

In the storyboard, you can now create data models and service entities from the column headers or from the toolbar.

In the settings, you can define if you want them created in the default namespace or service or to select the location manually.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-04-23



</td>
<td valign="top">

2023-04-23



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

In the Service Center, you can now search for a service within a package from the SAP Business Accelerator Hub, the API business hub enterprise, or the Unified Customer Landscape service provider. See [SAP Business Accelerator Hub Service Provider](https://help.sap.com/docs/bas/sap-business-application-studio/sap-api-business-hub-service-provider?version=Cloud).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-04-23



</td>
<td valign="top">

2023-04-23



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

You can now edit the data source for an SAP System service from the Storyboard. See [Storyboard and Project Explorer](https://help.sap.com/docs/bas/developing-cap-application-in-sap-business-application-studio/storyboard-and-project-explorer).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-04-09



</td>
<td valign="top">

2023-04-09



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now use the SAP HANA Project Explorer to include trace information in the deployment log displayed in the terminal pane. See [User Preferences for SAP HANA Native Application Development Tools](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/57e2fe608bb042d48b799d41a8d121a7.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-31



</td>
<td valign="top">

2023-03-31



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now use the Database Explorer's SQL console as a custom editor. See [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-31



</td>
<td valign="top">

2023-03-31



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now use the Project Explorer to provide support for SAP Cloud Application Programming \(CAP\) projects and access to tools that help you to maintain native SAP HANA database artifacts. See [Working with the SAP Cloud Application Programming Model](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/166f4fbbcbc64df3bd74220fd75c5b1e.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-31



</td>
<td valign="top">

2023-03-31



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now display syntax suggestions and dependency information in a side panel in the Database Explorer's SQL console. See [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-31



</td>
<td valign="top">

2023-03-31



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

CAP



</td>
<td valign="top">

You can no longer use SAP Business Application Studio run configurations to create and run CAP Java applications based on the classic Java stack. \(The CAP classic Java stack was deprecated in 2021.\) To continue using SAP Business Application Studio run configurations for CAP Java applications, migrate to the new CAP Java stack. See [Java Migration Towards the new CAP Java SDK](https://cap.cloud.sap/docs/java/migration).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

Changed



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-26



</td>
<td valign="top">

2023-03-26



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Java



</td>
<td valign="top">

SAP Business Application Studio now supports JAVA 17. You can select this version from the command palette. Open the command palette and select *JAVA Set Default JDK*.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

Changed



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-26



</td>
<td valign="top">

2023-03-26



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

You can now open a diagram to see the service entities, their properties, and the relationships between the entities from the Service Center. See [SAP System Service Provider](https://help.sap.com/docs/bas/sap-business-application-studio/sap-system-service-provider?version=Cloud).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-26



</td>
<td valign="top">

2023-03-26



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Git



</td>
<td valign="top">

You can now use the Simplified Git view to perform Git operations and manage Git repositories in SAP Business Application Studio. See [Using the Simplified Git View](https://help.sap.com/docs/bas/sap-business-application-studio/using-simplified-git-view?version=Cloud).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-26



</td>
<td valign="top">

2023-03-26



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

In the *Full-Stack Application Using Productivity Tools* dev space, a run configuration is automatically generated when you add an external data model to a service from the SAP System service provider. See [Add an External Data Model](https://help.sap.com/docs/Application%20Development/f9814e8df1cb43e1890e0f8d25374b8f/71817b1ad86d4ca5a27fb5ccfd04cf6f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-03-13



</td>
<td valign="top">

2023-03-13



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

In the *Full-Stack Application Using Productivity Tools* dev space, a run configuration is automatically generated when you add an external data model to a service from the SAP Business Accelerator Hub or the API business hub enterprise. See [Add an External Data Model](https://help.sap.com/docs/Application%20Development/f9814e8df1cb43e1890e0f8d25374b8f/71817b1ad86d4ca5a27fb5ccfd04cf6f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-02-13



</td>
<td valign="top">

2023-02-13



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Extension Project



</td>
<td valign="top">

You can now migrate and extend existing SAPUI5 applications that reside in the SAPUI5 ABAP repository. See [Extend SAPUI5 Applications](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/47c6ad87909b4246a5cbfe42b604207a.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-01-29



</td>
<td valign="top">

2023-01-29



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Adaptation Project



</td>
<td valign="top">

With Adaptation Project, you can now create manifest app descriptor changes using a wizard. The possible types of changes are - Replace OData Service, Add Annotation file, Add OData Service and SAPUI5 Model, and Add Component usage. See [Adding App Descriptor Changes](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/584e0bcbfd4a4aff91c815cefa0bce2d/0d18a12137b84f2ca04bbfea93bbb47b.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-01-20



</td>
<td valign="top">

2023-01-20



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

The Service Center now includes the following additions that make it easier to get started:

-   The *HELP* section provides an overview of the Service Center and links to detailed documentation for each service provider.
-   The SAP System service provider includes a button to add a system for the first time. See [SAP System Service Provider](https://help.sap.com/docs/bas/sap-business-application-studio/sap-system-service-provider?version=Cloud)..



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2023-01-15



</td>
<td valign="top">

2023-01-15



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

Apply filters to both partners of a join. Filters that are applied to one join partner can also be applied to mapped columns of the other join partner. See [Map Filters Between Join Partners](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/997ec7b767794160a373894ee96a365f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-21



</td>
<td valign="top">

2022-12-21



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

The following new options are available for snapshots in a calculation view:

-   Create Snapshot After Deployment Automatically

-   Keep Snapshot During Redeployment

-   Mode of Generated Procedure


See [Create Snapshots](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/d35f768ce50145d2ad0e5916898f004d.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-21



</td>
<td valign="top">

2022-12-21



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

The calculation view editor now lets you undo and redo operations on calculation views. See [Undo and Redo Modeling Operations](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/74d4fa8d18724f3e9ffb09b82c7553b5.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-21



</td>
<td valign="top">

2022-12-21



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, the SAP HANA projects explorer now provides direct access to online help for the specific database artifact type that you are creating. See [Add Database Artifacts to your SAP HANA Cloud Database Application](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/1aa916563bea48c8a880efba306fb7f9.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-21



</td>
<td valign="top">

2022-12-21



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, you can now use the SAP HANA Project Explorer to recover design-time artifacts by binding to a user-provided service. See [Restore Design-time Artifacts from the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/e735ec2bac4541339e9301e8cae7ca0b.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-21



</td>
<td valign="top">

2022-12-21



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, the SAP HANA Project Explorer now supports the multitarget resource type `org.cloudfoundry.managed-service`. See [Configure an SAP CAP Application to Work with Native SAP HANA Artifacts](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/ef0377f5e9d84ce3aeb43a7e4baa5fe4.htm).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-21



</td>
<td valign="top">

2022-12-21



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension for SAP Business Application Studio, the SAP HANA Project Explorer now enables you to set \(in user preferences\) the automatic configuration of the "development mode" feature when deploying migration tables. See [User Preferences for SAP HANA Native Application Development Tools](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/57e2fe608bb042d48b799d41a8d121a7.html#loio57e2fe608bb042d48b799d41a8d121a7__section_n2h_q44_nsb) and [Migration Tables \(SAP HANA Cloud HDI Reference\)](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2cc2e43458d4abda6788049c58143dc/52d1f5acfa754a7887e21226641eb261.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-21



</td>
<td valign="top">

2022-12-21



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development Experience



</td>
<td valign="top">

You can now configure and run continuous integration and delivery \(CI/CD\) pipelines that automatically build, test, and deploy your code changes to speed up your development and delivery cycles. See[Continuous Integration and Delivery](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/b357cfe698f3424cb76c7a3070d9a2b3.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-08



</td>
<td valign="top">

2022-12-08



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

You can now add an SAP Cloud for Customer system to your SAP Business Application Studio subaccount from the Service Center. See [SAP System Service Provider](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/892114ce078b4e17a9ff7e751e6330cc.html).



</td>
<td valign="top">



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-12-04



</td>
<td valign="top">

2022-12-04



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

The Unified Customer Landscape service provider is now integrated in the Service Center. You can use the services from registered SAP S/4HANA Cloud systems as data sources in your application or for application development. See [Unified Customer Landscape Service Provider](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/830adebf4ab3470c9c3278188ceef8a1.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-11-28



</td>
<td valign="top">

2022-11-28



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development Experience



</td>
<td valign="top">

SAP Business Application Studio now uses Code-OSS, the open source used for building Visual Studio Code. This change comes with many user experience improvements that will speed up your productivity.

All business functionality is still available. Some basic IDE capabilities have been updated. Once you are used to the new UI, your development experience will be better and faster.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

Announcement



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-11-06



</td>
<td valign="top">

2022-11-06



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Dev Space Manager



</td>
<td valign="top">

You can now provide feedback regarding your development experience in SAP Business Application Studio by taking our survey.

You can access the survey from the menu bar in the Dev Space Manager.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">

2022-10-03



</td>
<td valign="top">

2022-10-03



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now add temporal information \(system time and application time\) to the definition of a calculation view. See [Add System Time and Application Time](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/7421507f46ef4e64b060b013076d1b8c.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

SAP Business Application Studio



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now apply greedy join pruning to join executions. This can improve the performance of queries in situations in which joins are not required for data correctness. See [Configure Greedy Join Pruning](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/17af2dff9bbc479c9472c693c0ff85c0.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

Window Functions have been enhanced. See [Create Window Function Nodes](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/c8147ba7d406441986483f3a88accf0b.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

Changed



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, you can now use the standard database-artifact creation wizard to add a virtual table to your database application. See [Create Virtual Tables](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/00340d4ede0a43ceb0a67f36bbc46a3a.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, it is now possible to use the Database Explorer's SQL console to select local or SAP HANA database connections. See [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the Database Explorer's SQL console now provides new context menu items that enable you to open SQL files and display the contents directly in the SQL console itself. See [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, new context-menu items in the Database Explorer enable you to generate a `SELECT` or `CALL` statement for supported database artifacts. See [View Database Objects with the Database Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, it is now possible to view the data of supported artifacts in the Database Explorer's SQL console. See [View Database Objects with the Database Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e5ac0b0625b411c8f05346566a3341f.html) and [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application, the Project Explorer now enables you to bind a database module to a user-provided service. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the Project Explorer now displays a warning if services bound to a database modules do not match the current Cloud Foundry space. Users can choose to automatically unbind these services by setting a user preference. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html) and [User Preferences for SAP HANA Native Application Development Tools](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/57e2fe608bb042d48b799d41a8d121a7.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the Project Explorer now displays a warning if services bound to a database modules do not match the database ID defined in the `mta.yaml` file. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, you can now use the Project Explorer to recover design-time artifacts in your workspace from the deployed artifacts in an HDI container. See [Restore Design-time Artifacts from the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/e735ec2bac4541339e9301e8cae7ca0b.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, you can now use the Project Explorer to synchronize the deployment state of a database module with the deployment state from the database. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension,you can now use the Project Explorer to create a procedure grantor when adding a new database connection. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-09-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Guided Answers



</td>
<td valign="top">

You can now open the Guided Answers from the command palette to troubleshoot SAP Business Application Studio.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-08-28



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

In *Low-Code-Based Full-Stack Cloud Application* dev spaces, you can now configure and run continuous integration and delivery \(CI/CD\) pipelines that automatically build, test, and deploy your code changes to speed up your development and delivery cycles. See [Continuous Integration and Delivery](https://help.sap.com/docs/Application%20Development/6a5fc562f6e2402aa84b0416614a05fc/b357cfe698f3424cb76c7a3070d9a2b3.html?version=Cloud).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-08-01



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

In *Low-Code-Based Full-Stack Cloud Application* dev spaces, you can now use the *Get started with SAP Business Application Studio*booster to set up your subaccount for developing low-code business applications. See [Initial Setup](https://help.sap.com/docs/Application%20Development/6a5fc562f6e2402aa84b0416614a05fc/c45ed8eaa3f049f08a0a3f8221ba78bc.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-08-01



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

In *Low-Code-Based Full-Stack Cloud Application* dev spaces, you can now extend an existing service or create an SAP S/4HANA service with additional fields with guided steps from the *Guided Development* tool. See [Creating an SAP S/4HANA Application](https://help.sap.com/docs/Application%20Development/6a5fc562f6e2402aa84b0416614a05fc/113ad607676b405cb2acc3ee4afc60c6.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-08-01



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Development with Productivity Tools



</td>
<td valign="top">

In *Low-Code-Based Full-Stack Cloud Application* dev spaces, you can now extend an existing service or create an SAP S/4HANA service with additional fields with guided steps from the *Guided Development* tool. See [Creating an SAP S/4HANA Application](https://help.sap.com/docs/Application%20Development/6a5fc562f6e2402aa84b0416614a05fc/113ad607676b405cb2acc3ee4afc60c6.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-08-01



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Node.js Version



</td>
<td valign="top">

The Node.js version for Theia was updated to Node.js 16.15.0.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-07-17



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

The API business hub enterprise service provider is now integrated in the Service Center. You can explore OData-based services from the API Business Hub Enterprise. See[API Business Hub Enterprise Service Provider](https://help.sap.com/products/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/328519b3b7c04871b63a41350190d4d5.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-07-17



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now create snapshots based on a specific query in a calculation view. See [Create Query Snapshots](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/d35f768ce50145d2ad0e5916898f004d.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

A new aggregation option MEDIAN is available for:

-   Measures in a calculation view with aggregation or star join

-   Calculated columns with measure type, if client side aggregation is enabled

-   Mapping for a node, if the column is a measure


See [Supported View Nodes for Modeling Calculation Views](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/346dcfd19b3e4fe3a95ac1a1609c9c40.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now map session variables to input parameters. Up to now, it was only possible to map parameters and variables to input parameters. See [Supported View Nodes for Modeling Calculation Views](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/c5a5e12a5cc84196991d40ef0dd2003f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

You can now quickly find out where elements in a calculation view, such as calculated columns, input parameters, restricted columns, or variables, are used. See [Where Used Functionality](https://help.sap.com/docs/HANA_CLOUD_DATABASE/d625b46ef0b445abb2c2fd9ba008c265/d79577f0cda74f4faa1ba5a8b0a6ba45.htm).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

You can now use the SAP HANA Native Application extension to export a package that includes selected objects from an SAP HANA HDI container, for example, if required for testing by support teams. See [Export an SAP HDI Container for Support Purposes](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e4c3403b64d40f093a8a2cb78f9944b.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

You can now create a default "`hdbgrants`" file for the automatic assignment of privileges when adding a new database connection in the *SAP HANA Projects* explorer in the SAP HANA Native Application extension. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, you can now set the user preference "auto-commit" in the SAP HANA *SQL Console* to ensure that any changes to the database required by the code you run in the *SQL Console* are performed immediately, for example, when inserting or updating data in tables. See [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

You can now use the SAP HANA *SQL Console* in the SAP HANA Native Application extension for SAP Business Application to run SQL queries that include parameters. See [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

The *SAP HANA Projects* explorer in the SAP HANA Native Application extension now checks the details of the target schema details when binding to an existing service. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

You can now switch between database connections in the SAP HANA *SQL Console* in the SAP HANA Native Application extension for SAP Business Application. See [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

You can now use context-sensitive menus in the *SAP HANA Databases* explorer's *Catalog Browser* in the SAP HANA Native Application extension to copy the simple or fully qualified name of a database object to the clipboard. See [View Database Objects with the Database Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

You can now use the *SAP HANA Databases* explorer's *Catalog Browser* in the SAP HANA Native Application extension to generate the SQL code that was used to create the selected database object. See [View Database Objects with the Database Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

You can now use the *SAP HANA Projects* explorer in the SAP HANA Native Application extension to bind a user-provided service to a target HDI container. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

You can now use the *SAP HANA Projects* explorer in the SAP HANA Native Application extension to bind to \(or unbind from\) all services displayed in the Database Connections pane. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html) and [View Database Objects with the Database Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-19



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

You can now preview the entity data of an SAP Business Accelerator Hub service before application creation from the Service Center. See [SAP Business Accelerator Hub Service Provider](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/1a2f306c9f9b4628bfa143f8e404ef0a.html?locale=en-US&version=Cloud).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-06-06



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

You can now search for a service in an ABAP service catalog from the Service Center. See [SAP System Service Provider](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/892114ce078b4e17a9ff7e751e6330cc.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-05-23



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Service Center



</td>
<td valign="top">

You can now preview the entity data of a SAP System service before application creation from the Service Center. See [SAP System Service Provider](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/892114ce078b4e17a9ff7e751e6330cc.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-05-23



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Dev Space Manager



</td>
<td valign="top">

You can now select the *Low-Code-Based Full-Stack Cloud Application* dev space type to easily develop, test, build, and deploy applications. See [Low-Code-Based Full-Stack Cloud Application](https://help.sap.com/docs/SAP%20Business%20Application%20Studio/9d1db9835307451daa8c930fbd9ab264/00ad0484344c461caf80a7c695fd38af.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-04-26



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Node.js Version



</td>
<td valign="top">

The Node.js version for Theia was updated to Node.js 14.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

Changed



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-04-26



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

The database-explorer tools can now be used with local database connections on ARM platforms. Note that the limitations of the SAP HANA "hdb" Node.js client apply, for example, SAP HANA User Store connections are not available. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/docs/HANA_CLOUD_DATABASE/c2b99f19e9264c4d9ae9221b22f6f589/4bbbaae1d8694005adcfe1ec06a5cd46.html?version=2022_1_QRC&locale=en-US).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-04-11



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

The SAP HANA Native Application extension now provides access to SAP HANA database development tools from an SAP CAP project. See [Configure an SAP CAP Application to Work with Native SAP HANA Artifacts](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/ef0377f5e9d84ce3aeb43a7e4baa5fe4.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

During the creation of a new application project, the SAP HANA Native Application extension now checks if the project's .gitignore file contains an entry for the SAP HANA native database application .env file. See [Create a New Business Application Project](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/f42acff48e164acbb01b1ee969b1282b.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the list of SAP HANA Database Explorer connections can be hidden using the Show Database Explorer Connections setting in User Preferences. See [User Preferences for SAP HANA Native Application Development Tools](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/57e2fe608bb042d48b799d41a8d121a7.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, local database connections can now be added using credentials stored in the SAP HANA User Store. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the SQL console can open content from \(and save content to\) files. See [Use the SQL Console for SAP HANA to Query the Database](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/7ffe3cc490f04ca997e22326e013e73f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the SAP HANA Database Explorer on SAP Business Technology Platform can now be opened from each SAP HANA Database Explorer connection. See [View Database Objects with the Database Explorer](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the catalog browser now shows the list of database objects. The objects can be filtered by schema. The \(filtered\) list of objects can be also be searched using the standard Visual Studio Code functionality for the tree view. See [View Database Objects with the Database Explorer](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/0e5ac0b0625b411c8f05346566a3341f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

The SAP HANA Native Application extension now provides context-sensitive descriptions of tags and properties in JSON-based HDI artifacts, for example: hdbrole and hdbroleconfig, hdbgrants, hdbsynonym and hdbsynonymconfig. For common scenarios, templates are provided, too. See [Create a Database Role \(Getting Started\)](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/492729c3918c4cb7a645f69a6bdfbc56.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

The SAP HANA Native Application extension now provides JSON syntax validation for the HDI artifacts hdbtabledata and hdblogicalschemaconfig. See [SAP HDI Artifact Types and Build Plug-ins Reference \(SAP HANA Cloud Database\)](https://help.sap.com/viewer/c2cc2e43458d4abda6788049c58143dc/2022_1_QRC/en-US/9789224788a34d93a86080cab993575c.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, you can now use the project explorer to bind a module to the default service. A new option also enables you to bind \(and unbind\) all the services specified in an application's mta.yaml file. When binding a module to an existing service, a new warning is shown. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer.](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/4bbbaae1d8694005adcfe1ec06a5cd46.html) 



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the project explorer now provides a setting for clearing the deployment log when a new deployment is started. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer.](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/4bbbaae1d8694005adcfe1ec06a5cd46.html) 



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, you can now validate connection details when adding a new database connection to a project.

See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, a confirmation dialog is now displayed asking if auto-undeploy should be disabled when binding an application to an existing container. See [Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

SAP HANA Development Tooling



</td>
<td valign="top">

In the SAP HANA Native Application extension, the project explorer now shows HDI configuration files in the application project's file tree. See[Deploy Artifacts and Set up Database Connections with SAP HANA Projects Explorer](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/2022_1_QRC/en-US/4bbbaae1d8694005adcfe1ec06a5cd46.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

Input parameters of a calculation view can now be mapped to the input parameters of a consumed calculation view if this calculation view is consumed via SDA. See [Map Input Parameters](https://help.sap.com/viewer/d625b46ef0b445abb2c2fd9ba008c265/2022_1_QRC/en-US/c5a5e12a5cc84196991d40ef0dd2003f.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

When replacing a node of a calculation view, it is now also possible to map input parameters. See [Replacing Nodes and Data Sources](https://help.sap.com/viewer/d625b46ef0b445abb2c2fd9ba008c265/2022_1_QRC/en-US/a83035bf66b84bf682a3f954580e8220.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

A new configuration option was added to explicitly configure whether a data preview query should be automatically executed. See [Preview Calculation View Output](https://help.sap.com/viewer/d625b46ef0b445abb2c2fd9ba008c265/2022_1_QRC/en-US/903eff885ebd4c5cadb1e0c3e58f681d.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

The data preview allows the preview of hierarchies on SAP HANA Cloud. See [Preview Calculation View Output](https://help.sap.com/viewer/d625b46ef0b445abb2c2fd9ba008c265/2022_1_QRC/en-US/903eff885ebd4c5cadb1e0c3e58f681d.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

In addition to constant mapping and the use of pruning configuration table, column-based pruning is now also supported.

Column-based pruning allows you to prune individual data sources of a union node, based on whether a data source contributes certain columns. See [Create Column-Based Pruning](https://help.sap.com/viewer/d625b46ef0b445abb2c2fd9ba008c265/2022_1_QRC/en-US/04b541d4b9364e00b33575bbc390de66.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Calculation Views



</td>
<td valign="top">

In the Find Data Source dialog, you can now select/unselect ‘Show Services’ to show/hide the Service column in the result table, which contains the service information of each object in the table. See [Create Calculation Views](https://help.sap.com/viewer/d625b46ef0b445abb2c2fd9ba008c265/2022_1_QRC/en-US/5aeb56cba39e4df4ae62b43a0dc2fad4.html).



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

New



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-27



</td>
</tr>
<tr>
<td valign="top">

SAP Business Application Studio 



</td>
<td valign="top">

-   Cloud Foundry



</td>
<td valign="top">

Support for Dynamic Routing



</td>
<td valign="top">

There is no longer a limit on the number of applications \(ports\) running at the same time.



</td>
<td valign="top">

Info only



</td>
<td valign="top">

General Availability



</td>
<td valign="top">

Changed



</td>
<td valign="top">

Technology



</td>
<td valign="top">

Not applicable



</td>
<td valign="top">

 



</td>
<td valign="top">



</td>
<td valign="top">

2022-03-14



</td>
</tr>
</table>

-   **[2021 What's New for SAP Business Application Studio \(Archive\)](2021-what-s-new-for-sap-business-application-studio-archive-d42bd4b.md "")**  

-   **[2020 What's New for SAP Business Application Studio \(Archive\)](2020-what-s-new-for-sap-business-application-studio-archive-431551f.md "")**  


