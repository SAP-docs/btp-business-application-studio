<!-- loio2ef2807535a542c3ad107b2d011d21e7 -->

# MTA Editor

The visual MTA editor allows you to edit the MTA descriptor \(the `mta.yaml` file located in the root project folder\) using tables and forms instead of the text-based code editor.

The multitarget application \(MTA\) descriptor contains the metadata of all entities comprising an application or used by it during deployment or runtime, and the dependencies between them.

The MTA descriptor is automatically generated when an application project is created from scratch, and it is updated when the project properties change or when a module is added or removed. However, not all the necessary information can be generated automatically. You need to maintain the descriptor manually to define resources, properties, and dependencies, as well as fill in missing information.

The MTA descriptor is written in the YAML format, which has strict syntax requirements. You can edit the descriptor in the text-based code editor, but we recommend you use the visual MTA editor. The visual MTA editor allows you to easily navigate between the objects in the `mta.yaml` file and helps you avoid dealing with the complex and sensitive syntax of YAML files.

**To open the visual MTA Editor:**

1.  Right-click the desired `mta.yaml` file.
2.  Choose *Open With* \> *MTA Editor*.

> ### Note:  
> The visual MTA editor removes comments and formats the file. If you want to add comments, use the code editor. To open the code editor, double-click on the desired `mta.yaml` file or right-click the file and choose *Open With* \> *Code Editor*.
> 
> If you edit the file with the code editor, it is important to use spaces rather than tabs for indentation.

**Related Information**  


[The Multi-Target Application Model](https://www.sap.com/documents/2016/06/e2f618e4-757c-0010-82c7-eda71af511fa.html)

[SAP Business Application Studio Multitarget Application \(MTA\) development toolkit](https://blogs.sap.com/2020/07/16/sap-business-application-studio-multitarget-application-mta-development-toolkit/)

