<!-- loiod90686f9ab524caaaaa4997b29d1e18e -->

# Edit Strings

The i18n Resource Text Customization extension allows you to copy the `i18n` folder of the original application to your extended application. This allows you to edit the UI strings in the extended application without altering the original application.



<a name="loiod90686f9ab524caaaaa4997b29d1e18e__prereq_ssz_qyp_bwb"/>

## Prerequisites

The original application must have an `i18n` folder with at least one `Properties` file that contains the relevant strings.



## Procedure

1.  Right-click on any folder of the extension project to which you want to add the extension and click *Create Extension*.

2.  Make sure that the desired extension project is selected and click *Next*.

3.  Select the *i18n Resource Text Customization* tile and click *Next*.

4.  Click *Finish* to confirm and add the extension.




<a name="loiod90686f9ab524caaaaa4997b29d1e18e__result_mvg_czp_bwb"/>

## Results

The `i18n` folder of the original application is copied to your extended application, including all its `.properties` files. You can change one or more of the strings in the `.properties` file and run your extended application to see them in runtime. The original application remains unchanged.

