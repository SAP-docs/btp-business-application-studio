<!-- loio35e89d82af844b17a22c819c677193b7 -->

# Runtime Capabilities Editor

Add runtime capabilities to your project.

> ### Note:  
> This feature is currently available only in projects of type Full Stack.

The *Runtime Capabilities* editor shows the runtime capabilities available for the project on which you are currently working.

To add a capability:

1.  Open the Storyboard.
2.  From the Storyboard Toolbar, click *Runtime Capabilities*.
3.  Select the capability you want to add from the *Available* section.
4.  Click *Install Capability*.

To remove a capability:

1.  Select the capability you want to remove from the *Installed* section.
2.  Click *Uninstall Capability*.

The following capabilities are available:

-   *Audit Logging \(for Full-Stack Applications\)*

    This enables CAP’s out-of-the-box support for logging personal data-related operations with the SAP Audit Log service using the annotations of respective entities and fields.

    > ### Note:  
    > Installing the Audit Logging feature will add a dependency to the SAP Audit Log Service, premium edition plan.

-   *Change Tracking*

    Provides out-of-the box support for automated capturing, storing, and viewing of the change records of modeled entities.

-   *Attachments*

    Provides out-of-the-box storage and handling of attachments by using the Attachments aspect. By default, the SAP Object Store service and the SAP Malware Scanning service are used in production, and SAP HANA Cloud is used in development without a malware scan. These configurations can be changed manually in the package.json file.

    > ### Note:  
    > Installing the *Attachments* feature will add a dependency to the following services: SAP HANA Cloud \(used locally\), SAP Object Store \(used in production\), and SAP Malware Scan \(used in production\).

-   *Telemetry*

    Provides observability features such as tracing and metrics. After installing this capability, telemetry data will be automatically collected. The data collected can be sent to observability frontends that offer a wide set of capabilities to analyze the current state of an application. On SAP BTP, SAP Cloud Logging is offered as a frontend for these purposes. By default, SAP Cloud Logging will be used as the frontend for telemetry.You can can also manually create a different configuration.

    > ### Note:  
    > Installing the *Telemetry* feature will add a dependency to the SAP Cloud Logging service.


