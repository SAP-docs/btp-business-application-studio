<!-- loio76db36227d294201a9ac27dd4ade32aa -->

# Restrictions

When using SAP Business Application Studio, there are user restrictions on computing resources and project components to ensure optimal performance.

SAP Business Application Studio computing resources \(CPU, memory, storage\) are limited and optimized for serving standard SAP application development use-cases.

To ensure an optimal performance and developer experience, the following restrictions must be maintained:

-   A user can create up to 10 dev spaces.

-   A user can only have up to two running dev spaces.

-   A user can have disk space of up to 10 GB per dev space.

-   A user can only have up to 50 projects stored on their dev space.

-   A user can only have up to 20 projects or MTA modules open in their workspace.

-   A user can only have up to 1000 Java classes \(comprising up to 27,000 code lines\) on a single project compilation.

-   A user can only have up to 1000 SAP HANA database artifacts on a single project compilation.


If your resource usage is close to any of these restrictions, the system performance may be impacted.

If the restrictions are surpassed, performance can't be assured by the SAP Business Application Studio product license.

> ### Note:  
> We recommend you connect to the data center that is closer to your physical location to ensure best performance. See [SAP Business Application Studio Availability](sap-business-application-studio-availability-8509485.md)

