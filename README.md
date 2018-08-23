# maya-module-installer
Module template for easy drag-and-drop installation using provided mel script.

## Description
Add the module which is located in the same directory as the .mel file into the first available `MAYA_MODULE_PATH` directory. It doesn't matter where on disk the module lives as the script will make sure the path in the .mod file links to the correct place. There are some basic sanity checks in place to make sure the script doesn't error out. This includes Maya version compatibility with the module. Permissions of the directories files have to be written to and incorrectly formatted module files.

The reason for creating this script is that I have always had trouble finding a good way to distribute scripts. Especially less technical users might have trouble running python/mel code. This method will make it as easy as unpacking the package anywhere on disk and dragging the provided mel file into Maya. The template maya module file can be specific to certain versions of maya, language and operating system. It is also possible to extend the environment variables and adding a userSetup.py. This flexibility will allow you to run code on startup and provide the users with for example a custom shelf that is easily accessible to the user.

## Requires
* Template .mod file ( place `<PATH>` where normally the file path would go )
* Maya module ( scripts/icons/plug-ins directories etc. )

## Usage
Drag and drop the mel file into Maya or run `source <MEL_FILE>;`.

## Maya Module Documentation
* [Maya Documentation: Distributing Multi-File Modules](https://help.autodesk.com/view/MAYAUL/2018/ENU/?guid=__files_GUID_CB76E356_753B_4837_8C5B_3296C14872CA_htm)
* [Maya Documentation: Maya module paths, folders and versions](https://help.autodesk.com/view/MAYAUL/2018/ENU/?guid=__files_GUID_130A3F57_2A5D_4E56_B066_6B86F68EEA22_htm)
