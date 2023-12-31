<!-- loio8270e77a1f8445eaad4b433d9d2df0e6 -->

# Runtime Version Management

SAP Business Application Studio uses asdf to allow you to select which runtime versions to install and use for developing your application.

By default, SAP Business Application Studio defines only one Java and Node.js version that is officially supported. The default installed versions, are the Long Term Support \(LTS\) versions for Node.js and Java. You can check the currently installed version in your dev space, using the following command in the terminal:

For Java: `java -version`

For Node.js: `node --version`

You can manually install and select a different version.



<a name="loio8270e77a1f8445eaad4b433d9d2df0e6__section_g21_2fy_dzb"/>

## Install a Runtime Version

1.  From the command palette, select *Runtime: Install*,

2.  Select Node.js or Java as the runtime you want to install.

3.  Select the runtime version you want to install


The new version will be available on your dev space and persisted using your allocated storage. Installing the version does not change the default version used.

> ### Note:  
> -   asdf can be also used from the SAP Business Application Studio terminal to install additional versions. See the *All Commands* topic in the asdf documentation.
> -   If you installed a Java version using the SAP Business Application Studio terminal, it is recommended to run the *Runtime: Add Proxy Certificate to Java* command via the command palette to allow connectivity to on-premise Java repositories during the maven build.



<a name="loio8270e77a1f8445eaad4b433d9d2df0e6__section_ptb_bgy_dzb"/>

## Set a Default Runtime Version

1.  From the command palette, select *Runtime: Set default*.

2.  Select Node.js or Java as the runtime,

3.  Select the runtime version you want to set as default.


Your selection will be persisted on your dev space and applies to all workspaces.

