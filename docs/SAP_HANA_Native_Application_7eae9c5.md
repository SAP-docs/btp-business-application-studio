<!-- loio7eae9c5e799e4f70946114f74f413ae9 -->

# SAP HANA Native Application

> ### Note:  
> This feature is not available in the China \(Shanghai\) Region.

Build and deploy native SAP HANA applications or analytical models. This dev space contains a comprehensive set of editors to support the creation of database artifacts \(calculation views, tables, SQLScript procedures, and more\), as well as tools to enable an end-to-end development flow from project creation to the deployment to the SAP BTP.

See [Working with SAP Business Application Studio](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/latest/en-US).

> ### Note:  
> SAP Business Application Studio needs to connect to the SAP HANA Cloud instance where you want to deploy your application’s database artifacts. By default, SAP HANA Cloud accepts all connections from allowed IP addresses in SAP BTP, for example, in the same region and infrastructure where SAP HANA was provisioned.
> 
> If you are working on an Azure account or you are trying to connect an SAP HANA instance from a different region, you must configure SAP HANA Cloud to allow connections from the IP address hosting SAP Business Application Studio for your Cloud region and the underlying platform.
> 
> To learn how to change the SAP HANA Cloud allowed connections, see [Change Allowed Connections](https://help.sap.com/viewer/db19c7071e5f4101837e23f06e576495/latest/en-US/770d34deb86d4eb49dc944ce9921228c.html).
> 
> To find out your SAP Business Application Studio IP address, see [SAP Business Application Studio Availability](SAP_Business_Application_Studio_Availability_8509485.md).

The SAP HANA Native Application scenario contains the following predefined extensions:

-   **SAP HANA Calculation View Editor**

    Allows you to edit and manage SAP HANA calculation views. The extension includes the SAP HANA calculation view editor, the synonym editor, and the analytical privilege editor.

    See [SAP HANA Cloud Modeling Guide for SAP Business Application Studio](https://help.sap.com/viewer/d625b46ef0b445abb2c2fd9ba008c265/latest/en-US/9ed48614318a4831a8a6b3e3222a05f0.html).

-   **SAP HANA Database Explorer**

    Allows you to access and inspect SAP HANA run-time objects. The extension includes a command that opens the SAP HANA Database Explorer in a new browser tab.

    See [SAP HANA Database Explorer](https://help.sap.com/viewer/a2cea64fa3ac4f90a52405d07600047b/cloud/en-US/7fa981c8f1b44196b243faeb4afb5793.html).

-   **SAP HANA Tools**

    Allows you to develop native SAP HANA applications. The extension includes tools such as enhanced graphical and text-based editors, project generators, and productivity tools.

    See [Working with SAP Business Application Studio](https://help.sap.com/viewer/c2b99f19e9264c4d9ae9221b22f6f589/latest/en-US).

-   **SAP HANA Smart Data Integration Tools**

    Allows you to do data federation, replication and transformation in SAP HANA. The extension includes graphical editors such as Flowgraph, Replication Task and File Format editors.

    See [Modeling Guide for SAP Web IDE and SAP Business Application Studio](https://help.sap.com/viewer/cc7ebd3f344a4cdda20966a7617f52d8/latest/en-US/b72a6833d8d54aa2be4c199ac4db6996.html)

-   **MTA Tools**

    Allows you to perform operations such as build, deployment, and validation on multitarget applications. The following tools will be installed as part of the extension:

    -   Cloud Foundry environment CLI

    -   Cloud Foundry environment deployment plugin

    -   Cloud MTA Build Tool

    -   MTA module runner \(VS Code extension\)

    See [MTA Tools](https://help.sap.com/viewer/209802f55bfd47fcaccecf1241df99f8/Cloud/en-US).


