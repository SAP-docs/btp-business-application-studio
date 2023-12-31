<!-- loio90ba99ae9af64f76a3da593e44ca5b9f -->

# Layout Editor

Display the content of an XML view in the layout editor to see it in a way that closely corresponds to how it will appear in your finished application.

> ### Note:  
> The layout editor is not supported in the Safari browser.



<a name="loio90ba99ae9af64f76a3da593e44ca5b9f__section_itd_gcc_xnb"/>

## Layout Editor Landscape

The layout editor consists of a canvas in the center, and two panes on either side. On one side, you will find the *Controls* and *Outline* tabs, while on the other side, you will find the *Properties* pane.*Events* and *Properties* panes.

![Layout Editor](images/layout_editor-_VS_code_0fbe61b.png)



<a name="loio90ba99ae9af64f76a3da593e44ca5b9f__section_jtd_gcc_xnb"/>

## Toolbar

The layout editor toolbar allows you to:

-   Change the device format of the canvas to smartphone, tablet, or desktop view.

-   Expand and collapse the panes to the sides of the canvas.

    -   One side includes the *Controls* and *Outline* tabs.

    -   The other side includes the *Properties* pane.

        The pane on the right side includes the *Properties* and *Events* panes.


-   Undo and redo actions.


![Buttons in the layout editor toolbar](images/1_19_what_s_new_toolbar_7c8f4b8.jpg)



<a name="loio90ba99ae9af64f76a3da593e44ca5b9f__section_ktd_gcc_xnb"/>

## Controls Tab

You can expand or collapse each section by clicking the arrow on each section header. You can also search for controls by entering the control name in the search field at the top of the *Controls* tab. The relevant sections expand to display the controls that match the search criteria.

> ### Note:  
> Make sure to delete the search criteria if you want to expand other sections.

You can drag and drop controls from the *Controls* tab onto the canvas. For more information, see [Add Controls from the Controls Tab](add-controls-from-the-controls-tab-3a1f27e.md).

![Controls tab in the layout editor](images/BAS_Control_Pane-_cropped_d146acd.jpg)

You can find the list of available controls in [SAPUI5 Controls Supported in the Layout Editor](sapui5-controls-supported-in-the-layout-editor-c5d123e.md).



<a name="loio90ba99ae9af64f76a3da593e44ca5b9f__section_ltd_gcc_xnb"/>

## Outline Tab

Controls that are selected on the *Outline* tab are automatically selected on the canvas and vice versa.

You can use the *Outline* tab to see the hierarchy of controls on the canvas. In addition, you can add and remove controls from the canvas using the *Outline* tab.

For more information, see [Add Controls from the Outline Tab](add-controls-from-the-outline-tab-1cf5a5b.md).

![Outline tab in the layout editor](images/outline_pane-_new_1df47d2.png)



<a name="loio90ba99ae9af64f76a3da593e44ca5b9f__section_mtd_gcc_xnb"/>

## Canvas

The canvas in the middle of the layout editor area provides a graphical display of the selected XML view.

Click a control on the canvas to select it. To select a parent control, hold *Ctrl* and click. You can keep clicking until you reach the highest control in the hierarchy and then the focus will return to the original control. Click outside the canvas to undo the selection.

![Canvas in the layout editor](images/canvas_webide_7b7dfdb.jpg)

**Properties Pane****Events and Properties Pane**

On the side of the canvas is a pane that displays the following:

On the right side of the canvas is a pane that displays the following panes:



<a name="loio90ba99ae9af64f76a3da593e44ca5b9f__section_ntd_gcc_xnb"/>

## Events Pane

The *Events* pane allows you to select an existing event handler from the controller for an event of the selected control. The ![](images/events_icon_91db674.jpg) icon next to each event opens the code editor to display the relevant controller in the XML code.

![](images/events_pane_d0dba3a.jpg)

> ### Note:  
> The *Events* pane is not currently supported.



<a name="loio90ba99ae9af64f76a3da593e44ca5b9f__section_otd_gcc_xnb"/>

## Properties Pane

The *Properties* pane shows the properties of the control that is currently selected in the canvas and allows you to modify its property values. The most commonly used properties for each control are displayed at the top of the list. The ![Data binding](images/data_binding_button_852457c.jpg) icon next to each property opens the *Data Binding* dialog box.

For more information, see [Binding Data](binding-data-c24e9c4.md), [Bind Data to a Simple Control](bind-data-to-a-simple-control-93f40e6.md), and [Bind Data to an Aggregate-Type Control](bind-data-to-an-aggregate-type-control-2d625d5.md).

![Properties pane](images/Properties_Pane_074591c.png)

> ### Note:  
> Deprecated properties or aggregations are marked with the label *deprecated* \(also in the *Outline* tab\). For more information, see *SAP Library for User Interface Add-On 1.0 for SAP NetWeaver* on SAP Help Portal at [http://help.sap.com/nw-uiaddon](http://help.sap.com/nw-uiaddon). Under *Application Help*, open *SAP Library*, and search for *deprecation*.

-   **[Working with the Layout Editor](working-with-the-layout-editor-8fbbaad.md "An overview of the steps required to edit a project using the layout editor.")**  
An overview of the steps required to edit a project using the layout editor.
-   **[SAPUI5 Controls Supported in the Layout Editor](sapui5-controls-supported-in-the-layout-editor-c5d123e.md "Provides a list of SAPUI5 controls that are supported in the layout
		editor.")**  
Provides a list of SAPUI5 controls that are supported in the layout editor.

**Related Information**  


[Working with the Layout Editor](working-with-the-layout-editor-8fbbaad.md "An overview of the steps required to edit a project using the layout editor.")

[SAPUI5 Controls Supported in the Layout Editor](sapui5-controls-supported-in-the-layout-editor-c5d123e.md "Provides a list of SAPUI5 controls that are supported in the layout editor.")

