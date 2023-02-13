<!-- loioe72930c96b664e3ea4ce5288eb84075f -->

# Accessing On Premise Systems

You can access SAP ABAP or other on-premise systems using a built-in Web Proxy.

Your dev space includes a built-in Web Proxy \(`http://localhost:8887`\) that allows you access to on-premise systems. It is already configured with the HTTP\_PROXY and the HTTPS\_PROXY environment variables.

The proxy requires destination configuration to your on-premise system from your Cloud Foundry subaccount.

For more information, see [Connecting to External Systems](connecting-to-external-systems-7e49887.md).



<a name="loioe72930c96b664e3ea4ce5288eb84075f__section_om3_lzq_dhb"/>

## Defining On Premise Systems for the Web Proxy

1.  Your administrator must create a destination and configure the [Cloud Connector](https://help.sap.com/viewer/cca91383641e40ffbe03bdc78f00f681/Cloud/en-US/e6c7616abb5710148cfcf3e75d96d596.html) so that as a developer, you can access on-premise systems.
2.  To update your dev space with a destination created after your dev space was started, open your dev space terminal and execute the following command:

    ```
    curl http://localhost:8887/reload
    ```

    This will trigger an immediate update of your on-premise destinations used by the dev space Web Proxy.

3.  Use the same URL that's in the destination from your dev space. The proxy will pass your request through the destination.



<a name="loioe72930c96b664e3ea4ce5288eb84075f__section_qhn_nzq_dhb"/>

## Using Git On Premise Repositories

You can work with on-premise Git repositories once an appropriate destination has been created in your subaccount. Make sure to use the exact same host and port as defined in the destination URL property.

For more information, see [Connecting to a Corporate Git Repository](connecting-to-a-corporate-git-repository-d54ddfc.md).



<a name="loioe72930c96b664e3ea4ce5288eb84075f__section_k54_nzq_dhb"/>

## Using NPM Modules from On Premise Repositories

You can use npm modules from an on-premise npm repository or an on-premise Git repository.

Use standard npm registry configurations to set the repository URL.

For example:

```
npm config set @<scope>:registry <URL>
```

Make sure an appropriate destination has been created in your subaccount and that you are using the exact same host and port as defined in the destination URL property.



<a name="loioe72930c96b664e3ea4ce5288eb84075f__section_ocb_3pn_mtb"/>

## Using Java Modules from On Premise Repositories

You can use Java modules as dependencies to your Java projects from an on-premise Maven repository.

Edit the standard Maven settings file \(open file /home/user/.m2/settings.xml\) to add the repository URL.

For example:

```
<repositories>
   . . .
   <repository>
        <id>corporate.repository</id>
        <url>PUT YOUR FULL REPOSITORY URL HERE</url>
   </repository>
   . . .
<\repositories>
```

Make sure an appropriate destination has been created in your subaccount and that you are using the exact same host and port as defined in the destination URL property.

