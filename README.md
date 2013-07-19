To use these files, copy all files into the scripts directory of your deploymentshare.  Please note, if you have made previous modifications to DeployWiz_Definition_ENU.xml then you will want to modify it rather than just copying in this one.  In that case lines 53 and 54 are all that need added.

You will also need to modify customsettings.ini as follows :
 *   Add a Custom Property like this : Properties=SkipAddPrinters
 *   Add this entry to show the wizard page : SkipAddPrinters=NO

You will need to add a custom step in your task sequence to execute the ZTIAddPrinters.wsf script.  Simply add a "Run Command Line" step and set the command line to : cscript.exe %SCRIPTROOT%\ZTIAddPrinters.wsf