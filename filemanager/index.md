---
layout: application
appname: OI File Manager
appdescription: OI File Manager for Android is an open file manager that seamlessly cooperates with other applications.
repo: filemanager
appdir: FileManager
appversion: 2.0.7
appvideo1: ZnLiyvCHGrI
appvideo2: x1S2R46cHjI
---

The OpenIntents file manager allows you to browse your SD card, create directories, rename, move, and delete files. It also acts as an extension to other applications to display "Open" and "Save" dialogs.

OI File Manager integrates into
*OI ConvertCSV.
*OI Notepad.

Features:
* Show list of files.
* Icons for home (root) directory and SD card.
* Directory structure displayed through clickable buttons.
* Alternatively, the current path can be displayed in an input field.
* Supports PICK_FILE and PICK_DIRECTORY intents so that other applications can use OI File Manager.
* Support for many file endings and mime types.
* "Back" key works for directories clicked in the list.
* Create directory, rename, delete files.
* Move files.
* Send files by email.
 
<img src="https://raw.githubusercontent.com/openintents/filemanager/master/promotion/OIFM%20site%20screenshots/1.png" width="150px"/>

<img src="https://raw.githubusercontent.com/openintents/filemanager/master/promotion/OIFM%20site%20screenshots/2.png" width="150px"/>

<img src="https://raw.githubusercontent.com/openintents/filemanager/master/promotion/OIFM%20site%20screenshots/3.png" width="150px"/>

<img src="https://raw.githubusercontent.com/openintents/filemanager/master/promotion/OIFM%20site%20screenshots/4.png" width="150px"/>

<img src="https://raw.githubusercontent.com/openintents/filemanager/master/promotion/OIFM%20site%20screenshots/5.png" width="150px"/>

<img src="https://raw.githubusercontent.com/openintents/filemanager/master/promotion/OIFM%20site%20screenshots/6.png" width="150px"/>


### Information for developers
Third party developers can use OI File Manager through simple intents to present an "Open file", "Save file", or "Select folder" activity.

The file manager features PICK_FILE and PICK_DIRECTORY intents:

Intent intent = new Intent("org.openintents.action.PICK_FILE");
startActivityForResult(intent, 1);

You can provide a pre-selected file or folder by setting data through setData() to a file URI, like "file:///sdcard/notepad.csv". The picked file URI can be obtained in onActivityResult() through getData().

With the extras "org.openintents.extra.TITLE" and "org.openintents.extra.BUTTON_TEXT" one can further customize the PICK intent (e.g. display "Open file" or "Save file" in the title bar).

### Sample application TestFileManager
TestFileManager is a small sample application that showcases interaction of third party applications with the OI File Manager.

It shows a (dummy) input field for the file name or folder name, and three buttons to initiate the "open", "save", and "select folder" intents. Once OI File Manager returns, the selected name is put into the input field. No data is actually opened or saved, since this is just a small demo.


This is how the "open" activity can look like:


And this is how you can select a folder:


Note that you can customize the activities by proving extras for the title and the button text.

Details can be found in the sample application TestFileManager. You can download it from the download page, or access the latest version in the public repository.

### Links
Intent registry: OI File Manager, PICK_FILE intent, PICK_DIRECTORY intent.
