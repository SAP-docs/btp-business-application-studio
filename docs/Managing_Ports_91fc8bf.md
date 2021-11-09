<!-- loio91fc8bf6891f42ada98793b8c1c038a8 -->

# Managing Ports

If you want to access an application that is running in your dev space from an external source \(for example a browser or REST client\), you must first expose the port that is listening to the application.



<a name="loio91fc8bf6891f42ada98793b8c1c038a8__section_zhm_qlk_f4b"/>

## Exposing Ports

When running an application that listens to a port, SAP Business Application Studio displays a notification prompting you to expose and open the port.

1.  Click *Expose and Open*.

    The port is exposed and you can preview the service in a new browser tab.

    If you missed the notification, you can do this manually from the command palette by entering the ***Ports: Expose*** command.

2.  Enter a name for the port.



<a name="loio91fc8bf6891f42ada98793b8c1c038a8__section_ff3_5lk_f4b"/>

## Unexposing Ports

If you want to remove the external access, enter the ***Ports: Unexpose*** command in the command palette.

This removes internet access to the applications running on the respective dev space.



<a name="loio91fc8bf6891f42ada98793b8c1c038a8__section_fjk_5lk_f4b"/>

## Previewing Ports

1.  Enter the ***Ports: Preview*** command in the command palette.

    A list of all the exposed applications is displayed.

2.  Click the relevant application.

    The exposed application opens in a new tab.




<a name="loio91fc8bf6891f42ada98793b8c1c038a8__section_zrl_5lk_f4b"/>

## Renaming Ports

1.  Enter the ***Ports: Rename*** command in the command palette.

2.  Select the desired port.

3.  Provide a new name for the port when prompted.


> ### Note:  
> You can have a maximum of 5 ports exposed at a time.



<a name="loio91fc8bf6891f42ada98793b8c1c038a8__section_hcn_5lk_f4b"/>

## Configuring Port Notification Settings

You can define which ports should omit a notification when an application is being run.

1.  In SAP Business Application Studio, open the *Preferences* view.
2.  Search for ***Ports***.
3.  From the list of preferences, select *Ports*.
4.  Under *Exclude Expose Notifications*, click *Edit in settings.json*.
5.  Specify the port or range of ports for which you do not want to show a notification.
6.  Save your changes.

