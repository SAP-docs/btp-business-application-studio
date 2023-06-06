<!-- loio47c6ad87909b4246a5cbfe42b604207a -->

# Use an Extension Project

You can extend SAPUI5 applications that reside remotely on the on-premise SAPUI5 ABAP repository. If you want to extend a legacy application and you are not able to create an SAPUI5 Adaptation Project, you can create an SAPUI5 extension project.



<a name="loio47c6ad87909b4246a5cbfe42b604207a__prereq_cyq_zn4_yvb"/>

## Prerequisites

-   Activate the `/sap/bc/adt` and the `/sap/bc/ui2/app_index/` services in your back end.
-   Make sure you have configured the connectivity to your ABAP system as described in [Connecting to External Systems](connecting-to-external-systems-7e49887.md).



## Procedure

1.  Migrate your extension project from SAP Web IDE.

    See [Migration](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/70d41f3ee29d453a90efab3ce025d450.html).

2.  \(Optional\) Use source control, such as Git, to maintain your extension project source code.

    You must use the extension project source code to preview the extension project and add more extensions to it.

    See [Git Source Control](git-source-control-9689c07.md).

3.  Add an extension, such as a view or controller extension, to the extension project. See [Create New Extensions](create-new-extensions-06b93dc.md).

4.  Preview your extension project locally in the SAP Business Application Studio workspace.

    See [Preview an Application](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/b962685bdf9246f6bced1d1cc1d9ba1c.html).

5.  Deploy your extension project to the on-premise SAPUI5 ABAP repository.

    See [Deployment to ABAP](https://help.sap.com/docs/SAP_FIORI_tools/17d50220bcd848aa854c9c182d65b699/607014e278d941fda4440f92f4a324a6.html#deployment-to-abap).

    > ### Note:  
    > When extending a project, compatibility issues may arise between the original and the extended project. For more information, see [Caveats Regarding Stability Across Application Upgrades](https://sapui5.hana.ondemand.com/sdk/#/topic/aef3384510724522a07df94ec90d1351).

    > ### Note:  
    > The SAPUI5 ABAP repository is based on the BSP repository of the ABAP Server. The BSP repository is used only as a repository or storage for SAPUI5 application files. However, BSP server-side processing is not used at runtime and therefore the flow logic of ABAP parts cannot be used, since they are not executed at runtime.


-   **[Create New Extensions](create-new-extensions-06b93dc.md "Extensions enable you to change the views or the logic of an extended
		project.")**  
Extensions enable you to change the views or the logic of an extended project.

