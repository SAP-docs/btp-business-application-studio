<!-- loio13fcc2a14a73401ebfc7aeabac052d8a -->

# Extend Controllers

You can extend a controller of the original application by replacing it with an empty controller or with a copy of the original controller. You can also implement UI controller hooks if they are provided by the original application. Once one of these controllers is in place, you can customize it as needed.

 <a name="task_xtp_5fp_bwb"/>

<!-- task\_xtp\_5fp\_bwb -->

## Replacing Controllers



<a name="task_xtp_5fp_bwb__steps_axq_xfp_bwb"/>

## Procedure

1.  Right-click on any folder of the extension project to which you want to add the extension and click *Create Extension*.

2.  Make sure that the desired extension project is selected and click *Next*.

3.  Select *Extend Controller* and then click *Next*.

4.  Select the controller that you want to extend.

5.  From the *Replace with*dropdown list, select *Copy of the original controller* to edit the controller based on the original controller, or select *Empty Controller* to replace the controller with an entirely new one and click *Next*.

6.  Click *Finish* to add the extension to the selected extension project.

    > ### Note:  
    > The new controller extends the controller that is provided by SAP. Methods of the custom controller override standard methods with the same name \(except for the controller lifecycle methods that are called in addition to the original controller method implementations\). When overriding a controller method, any functionality that was previously provided by the SAP controller in this method is no longer available. Likewise, any future changes made to the SAP controller method implementation will not be reflected in the custom controller.


 <a name="task_zvj_ggp_bwb"/>

<!-- task\_zvj\_ggp\_bwb -->

## Implementing UI Controller Hooks



<a name="task_zvj_ggp_bwb__steps_cdc_3gp_bwb"/>

## Procedure

1.  Right-click on any folder of the extension project to which you want to add the extension and click *Create Extension*.

2.  Make sure that the desired extension project is selected and click *Next*.

3.  Select *Implement UI Controller Hook* and click *Next*.

4.  Select the controller and the UI controller hook that you want to implement and click *Next*.

5.  Click *Finish* to add the extension to the selected extension project.


