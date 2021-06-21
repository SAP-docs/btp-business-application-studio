<!-- loio1e8ec75c9c784b51a91c7370f269ff98 -->

# Service Center

The Service Center provides a central entry point to explore services from various service providers.

The services can be used as data sources in your application and application development can be triggered from the Service Center.

To explore services, perform the following steps:

1.  From the left side menu, click ![](images/Service_Center-_icon_0ce7c7b.jpg) \(Service Center\) or select *View* \> *Service Center* from the menu bar.

    When the Service Center opens, the SAP Business Application Studio subaccount is displayed. Login occurs automatically, using the SAP Business Application Studio user credentials.

2.  Click the gray arrow to display the SAP Business Application Studio subaccount's destinations \(SAP systems\).
3.  Click the system to see the system properties, including the name, description, URL, authentication type, and status.

    There are different types of systems that can be displayed using the SAP Business Application Studio subaccount's destinations:

    -   ABAP Service Catalog

        The destination points to the ABAP system directly. The system exposes its service catalogs with a list of services \(V2 and V4, for example\). You must click ![](images/Open_System_Details_icon_8f5350a.jpg) \(Open System Details\) and log in with your user credentials to see the list of services.

    -   Service Host

        The destination points to a host. You must add the service path to log in.

    -   Service URL

        The destination points directly to the service.

    If the credentials are maintained in the destination configuration of the account, log in can occur automatically. If a system is available, a green dot is displayed on the icon. \(![](images/green_dot-_system_available_ac1aa72.jpg)\)

    If the credentials aren't maintained in the destination configuration of the account, you need to log in manually to open the system information.

4.  If needed, enter the service path to login or click ![](images/Open_System_Details_icon_8f5350a.jpg) \(Open System Details\) and log in with your user credentials.

    The system properties are displayed.

5.  Click the gray arrow to display the list of services.

    You can click on each service in the list to see the service properties, including the service name, protocol, URL, status, and entity details.

6.  After you're logged in, you can create a project from a service within the system:
    1.  Click *Service Actions* \> *Create a project from a service*.

        The template wizard displays the projects that can be created from a service, for example, an HTML5 project or an SAP Fiori application. See [Create an HTML5 Project](https://help.sap.com/viewer/0e2ec06ee34742fd9054fabe09c12d35/Cloud/en-US/e46be902c7b54f9baaab1870ca553303.html) or [SAP Fiori Elements](https://help.sap.com/viewer/17d50220bcd848aa854c9c182d65b699/Latest/en-US/1488469a315c442fa116ab4449d4ad27.html) for more information.

    2.  Use the template wizard to create the relevant project.
7.  You can add a new system to your SAP Business Application Studio subaccount:

    > ### Note:  
    > If you are using a non-trial account, you must be assigned to the *Business\_Application\_Studio\_Administrator* role in the cockpit. See [Manage Authorizations](https://help.sap.com/viewer/9d1db9835307451daa8c930fbd9ab264/Cloud/en-US/01e69c53003c4b0a8a64310a3f08867d.html).

    1.  Hover over the subaccount and click ![](images/Add_system-_service_center-_plus_icon_3701d6b.jpg) \(Add system\).

        A new tab opens.

    2.  Enter the system name and URL and select the system type, proxy, authentication method, and product.

        > ### Note:  
        > You can select *Basic Authentication* and enter the username and password for your system. This configuration enables you to view the system information without needing to log in each time.

        A system \(destination\) is created on the subaccount level and can be viewed in the cockpit.

8.  You can add a service to an existing CAP Node project:
    1.  Open the desired service page and click *Service Actions* \> *Add a service to a CAP project*.
    2.  Select the target CAP Node project to add the service to and then click *Add*.

        The service is added to the CAP project.

        A metadata file of the service is added to the project.

        A metadata section is added to the `package.json` file of the CAP project, which refers to the *srv* \> *external* \> *metadata.xml* file, containing the metadata of the desired service:

        ```
        "metadata": {
          "kind": "odata",
          "model": "srv/external/metadata"
        ```


