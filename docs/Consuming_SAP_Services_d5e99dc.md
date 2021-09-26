<!-- loiod5e99dc93434400a9b725537491a650c -->

# Consuming SAP Services

You can consume an SAP service from your application.



<a name="loiod5e99dc93434400a9b725537491a650c__prereq_m21_jgp_23b"/>

## Prerequisites

-   Make sure that your administrator configured the required destination in your Cloud Foundry provider account.
-   Make sure that your workspace contains the project for which you want to consume the service.



<a name="loiod5e99dc93434400a9b725537491a650c__steps_qfn_dlt_3jb"/>

## Procedure

1.  From the menu bar, click *View* \> *Find Command* \> *Consume SAP Services*.

2.  From the dropdown list, select the project type to which you want to bind the service.

3.  Select the project's module.

4.  Select the location of your data source.

    -   If your data source resides within one of your SAP systems:

        1.  From the list of sources \(destinations\) displayed, select the relevant source: *System URL*, *Service URL*, or *Catalog System URL*.

        2.  If you selected *System URL*, enter the path to the specific service.
        3.  If you selected *Catalog System URL*, select the desired service from the list of exposed services displayed.
    -   If your data source resides in the SAP API Business Hub:
        1.  Select the relevant API package \(API Business Hub destination\).
        2.  Select the desired API from the list displayed.

            > ### Note:  
            > You may require to enter credentials for the selected service.




<a name="loiod5e99dc93434400a9b725537491a650c__result_vrf_25t_3jb"/>

## Results

Once you select a data source, the metadata is retrieved and output is created depending on the project type you chose.

-   If you bound a service for a Business Application project, a folder called `external` is created. This folder contains 2 subfolders:
    -   `edmx` - Contains the retrieved data
    -   `csn` - Contains a JSON file representing the CDS version of the `metadata.xml` file.
-   If you bound a service for an SAP Fiori UI application, all the necessary configurations are automatically added to the SAP Fiori app using the service in your UI.

