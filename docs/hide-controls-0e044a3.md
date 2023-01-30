<!-- loio0e044a33a430400f81ffc917d38e8468 -->

# Hide Controls

You can hide a specific control of the original application.



## Context

Controls that are configured in a fragment that is loaded dynamically might still appear in the UI. Elements that are set as *visible* manually by the view’s controller will not be hidden.

You can try and hide these controls by replacing the view or extending the controller that hides it and override the method.



## Procedure

1.  Right-click on any folder of the extension project to which you want to add the extension and click *Create Extension*.

2.  Make sure that the desired extension project is selected and click *Next*.

3.  Select *Hide Control* and click *Next*.

4.  Select the view or fragment containing the control that you want to hide.

5.  Select the specific control that you want to hide.

    > ### Note:  
    > Only controls with an ID that is defined in the original application appear in the list.

6.  Click *Next*.

7.  Click *Finish* to add the extension to the selected extension project.

    > ### Note:  
    > You can only hide controls that have their `Visible` property defined as `true`. If the `Visible` property does not exist, you cannot hide the control.

    > ### Note:  
    > If you hide a control and then want to show it again, you must delete the extension from the `component.js/manifest.json` customizing block. Changing the `visible` property from `False` to `True` does not make the control reappear.


