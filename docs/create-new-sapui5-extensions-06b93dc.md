<!-- loio06b93dc3bd0d4ee1b3a5da903d3a1daa -->

# Create New SAPUI5 Extensions

You can create SAPUI5 extensions in the SAPUI5 extension project to change the views or the logic of an SAP Fiori application.



## Context

You can create extensions to:

-   Replace an existing view with a new view in an existing project.
-   Add logic to an existing view using an extension point that is defined in the original project.
-   Change control visibility.
-   Extend an existing controller with new logic.
-   Implement a UI controller hook with new logic.
-   Customize the strings of the original application.

Once the extensions have been created, a reference to them is created in the `Component.js/manifest.json` file of the extended project.

> ### Note:  
> If you delete or rename a file that is referenced from the `component.js/manifest.json` file, the application does not work properly. Make sure that you delete the reference or update the file name on the `component.js/manifest.json` file as well.

-   **[Extend Controllers](extend-controllers-13fcc2a.md "You can extend a controller of the original application by replacing it with an empty
		controller or with a copy of the original controller. You can also implement UI controller
		hooks if they are provided by the original application. Once one of these controllers is in
		place, you can customize it as needed.")**  
You can extend a controller of the original application by replacing it with an empty controller or with a copy of the original controller. You can also implement UI controller hooks if they are provided by the original application. Once one of these controllers is in place, you can customize it as needed.
-   **[Extend Views](extend-views-f2f471d.md "You can extend a view using an extension point.")**  
You can extend a view using an extension point.
-   **[Hide Controls](hide-controls-0e044a3.md "You can hide a specific control of the original application.")**  
You can hide a specific control of the original application.
-   **[Edit Strings](edit-strings-d90686f.md "The i18n Resource Text Customization extension allows you to copy the
			i18n folder of the original application to your extended
		application. This allows you to edit the UI strings in the extended application without
		altering the original application.")**  
The i18n Resource Text Customization extension allows you to copy the `i18n` folder of the original application to your extended application. This allows you to edit the UI strings in the extended application without altering the original application.
-   **[Replace Views](replace-views-57beb9e.md "You can replace a specific view in an original application with a new
		view.")**  
You can replace a specific view in an original application with a new view.

