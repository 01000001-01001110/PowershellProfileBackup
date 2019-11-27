#Powershell Profile Backup<br>
<br>
If you'd like to show your appreciation you can buy me a tea <a href="buymeacoff.ee/mwWXAyznc">here</a><br><br>

![image](https://user-images.githubusercontent.com/48245017/69575192-bfc41b00-0f97-11ea-9169-751165e026b1.png)

To start You can choose to type in the full UNC path to your from location and your to location. OR You can choose to click the button and browse to the directories you'd like to choose. If you find yourself creating a new directory verify the path is correct after applying. (Sometimes it still has new folder even if you rename. Unless you click on the directory and do not hit enter when renaming.)

Upon starting a backup process you are greeted by the lovely, daring, and overall bad-4$$-Voice that is the "Microsoft Zira Desktop". Who will guide you through a backup expierience you'll not soon forget. On top of the audible queues from the script. The script goes as far as to calculate the overall profile size of the source directory that you are backing up. Just to give you the warm and fuzzies about just how long this backup will take. 

The Backup Process: (The meat of this script)

The script starts and ends by logging the start and end time in the LOG window. Based of what you checked any of the following directories can be backed up.
-Cache Directory<br>
-CD Burning<br>
-Cookies<br>
-Cookies\Low
-CredentialManager<br>
-CryptoKeys<br>
-Device Metadata Store<br>
-dpapiKeys<br>
-NetHood<br>
-PrintHood<br>
-Start Menu Programs<br>
-Quick Launch<br>
-Recent<br>
-SavedGames<br>
-Searches<br>
-Start Menu<br>
-Startup<br>
-SystemCertificates<br>
-Templates<br>
-Desktop<br>
-Documents<br>
-Videos<br>
-Office Quick Parts<br>
-Documents<br>
-Pictures<br>
-Videos<br>
-Browsers (IE, FF, Chrome, Vivaldi, Opera, and Edge)<br>
-OneNote 2016 if in one of two spots.<br>
-Office Ribbon Data<br>
-Office Quick Access Toolbar settings<br>
-Outlook Settings<br>
-Outlook Signature<br>
-Adobe Signature/Security<br>
-Win10 Sticky Notes<br>
-One Drive, if you must spend time backing up a cloud backup....<br>
-OneDrive-Not-Yet-Syncd-Files (Yeah... find this directory in a search online. This was not an easy find for me.)<br>
-Lastly one Custom Directory of your choosing as long as you have the correct UNC path to the location.<br>

This entire backup process is logged thanks to "Robocopy" and the logging available to a temporary text file. This process logs EVERYTHING during the backup as it pertains to the copying of data in the selected directories. Once the log is completed the log file is copied from the temporary location and into the "\LOG" directory appended to the end of your "Browse to Location"

Upon saving information from the browsers the script will check and if it finds a browser open will attempt to close the browser for you so the favorites can be saved. This same method is also done when saving info from outlook. The script will find outlook running and attempt to close it. The script doesn't stop there. If the any of the close-tasks take too long to close it will force close the application. This script also checks the main directories before and after to add another automatic layer to the backup process. In essence what it does is verify the data was moved, and all of the copied data matches the original data. If it finds the source and destination directories do not match after a copy the script will error out and you will need to resolve why this happened. (Very unlikely this would happen.)

When running the script you are immediately provided with the following:
Device name (To verify we are on the right computer) Windows User: Who is logged into the computer right now?<br>
Authenticated User: Who authenticated as admin to run the script?<br>
OS Install Date: Who doesn't want this information? What version of windows and make.<br>

You also have an Inventory Button:
Inventory gathers the following information and outputs it to a "\LOG" directory appended to the end of your "Browse to Location"
Logical Drives<br>
PowerShell Drives<br>
Network Drives<br>
Connected Drives<br>
OS Information<br>
BIOS Settings<br>
IPConfig Information<br>
Local Administrators<br>
Computer Name<br>
Firewall Settings<br>
Application Events - to an .evt file<br>
System Events - to an .evt file<br>
Installed Applications<br>
Processes<br>
Services<br>
The script takes all the non .evt files and combines them into one .XLSX file, then moves it, plus the .evt files into the "\LOG" directory appended to the end of your "Browse to Location"

You are also given a lovely Printers Button:

Printers gathers the printer information in much the same way. Or attempts to. If you run the printer button under the customer you get the correct output. This is due to "Authenticated User/Windows User". Otherwise the script opens the Devices and Printers window for you to catalog the installed printers in case there is anything other than default. The script also opens up an Excel window and provides you with obviously more data than you might need. Maybe not? Not for me! (How many times did finding the same driver version work for local printers? You are welcome!)

You are also given a Programs Button in a newly added tab:

This now resides inside the Computer Information tab. Once clicked it will populate the .csv into the tab control. This part is run during the Inventory Button process, however, it does not pop-up, instead saves to the .XLSX created within the Inventory Button process.
On top of audible queues, popups, and overall awesomeness, there is yet two more important features.
First is the LOG window. This logs every state that the script goes through to the best of my ability. With this the log file now stays with the text so you can always read the text from he log window.
Second is the Copy to Clipboard. This copies the entire contents of the LOG window into the Clipboard so this can be pasted into your notes.

What this script doesn't do?

Steal your soul.<br>
Make you soup.<br>
Hug you, or touch you in any way.<br>
Care about your feelings.<br>
Backup data you or the customer fail to tell it to. Reads minds.<br>
Log the data in the ticket.<br>
Calls someones mom to setup a date.<br>
In fact it will not call anyone.<br>
Know who you or the customer actually are.<br>

Why should you care?

You don't have to. Maybe your process is working for you, if so awesome, I am more than happy it does.<br> Mine did not. So I worked on a better solution. <br>This is the evolution of that initial idea a year later. <br>This is not a single person effort as much as it might seem so. Many people have helped contribute to the functionality and data that the script now backs up. In no way could this have ever been possible without everyone's help.
