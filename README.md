#Powershell Profile Backup<br>
<br>


![image](https://user-images.githubusercontent.com/48245017/75276609-78d30500-57d4-11ea-88f1-053f11ca2a5d.png)

<pre>Profile Backup Script:
You can choose to type in the full UNC path to your from location and your to location. OR You can choose to click the button and browse to the directories you'd like to choose.

If creating a new directory verify the path is correct after applying. (Sometimes it still has new folder even if you rename. Unless you click on the directory and do not hit enter when renaming.) Upon starting a backup process you are greeted by the lovely, daring, and overall badA-Voice that is the "Microsoft Zira Desktop" Screams, "WOOOOOOOO", Not really. However, the audible queues from the script help guide you and the customer on a backup journey you will never forget. On top of the audible queues from the script continues to goe as far as to calculate the overall profile size of the source directory that you are backing up. Just to give you the warm and fuzzies about just how long this backup will take. With the audible queues from the script you'd think that would be enough?

The Backup Process: (The meat of this script)
The script starts and ends by logging the start and end time in the LOG window. Based of what you checked any one of the following directories can be backed up.

-Desktop
-Documents
-Videos
-Office Quick Parts
-Documents
-Pictures
-Videos
-Fonts Directory
-Browsers (IE, FF, Chrome, Vivaldi, Opera, and Edge)
-OneNote 2016 if in one of two spots.
-Office Ribbon Data
-Office Quick Access Toolbar settings
-Outlook Settings
-Outlook Signature
-Cache Directory
-CD Burning Directory
-Cookies Directory
-Cookies\Low Directory
-Credential  Manager Directory
-Crypt Keys Directory
-Device Metadata Store Directory
-dpapiKeys Directory
-NetHood Directory
-PrintHood Directory
-Start Menu Programs
-Cache Directory
-CD Burning Directory
-Cookies Directory
-Cookies\Low Directory
-Credential  Manager Directory
-Crypt Keys Directory
-Device Metadata Store Directory
-dpapiKeys Directory
-NetHood Directory
-PrintHood Directory
-Start Menu Programs
-Quick Launch Directory
-Recent Directory
-Saved Games Directory
-Search History Directory
-Start Menu Directory
-Startup Directory
-System Certificates
-Templates
-Quick Launch Directory
-Recent Directory
-Saved Games Directory
-Search History Directory
-Start Menu Directory
-Startup Directory
-System Certificates
-Templates
-Fonts
-Adobe Signature/Security 
-Win10 Sticky Notes
-Group Policy Settings
-One Drive, if you must spend time backing up a cloud backup....
-OneDrive-Not-Yet-Syncd-Files (Yeah... find this directory in a search online. This was not an easy find for me.)
-Lastly one Custom Directory of your choosing as long as you have the correct UNC path to the location. 
This entire backup process is logged thanks to "Robocopy" and the logging available to a temporary text file. This process logs EVERYTHING during the backup as it pertains to the copying of data in the selected directories. Once the log is completed the log file is copied from the temporary location and into the "\LOG" directory appended to the end of your "Browse to Location"

But wait, that's definitely not all. (Like a bad infomercial)
Upon saving information from the browsers the script will check and if it finds a browser open will attempt to close the browser for you so the favorites can be saved. This same method is also done when saving info from outlook. The script will find outlook running and attempt to close it. The script doesn't stop there. If the any of the close-tasks take too long to close it will force close the application. This script also checks the main directories before and after to add another automatic layer to the backup process. In essence what it does is verify the data was moved, and all of the copied data matches the original data. If it finds the source and destination directories do not match after a copy the script will error out and you will need to resolve why this happened. (Very unlikely this would happen.)

When running the script you are immediately provided with the following:
Device name (To verify we are on the right computer) 
Windows User: Who is logged into the computer right now? 
Authenticated User: Who authenticated as admin to run the script?
OS Install Date: Who doesn't want this information? 
What version of windows and make.
You also have an Inventory Button:
Inventory gathers the following information and outputs it to a "\LOG" directory appended to the end of your "Browse to Location"

Logical Drives
PowerShell Drives
Network Drives
Connected Drives
OS Information
BIOS Settings
IPConfig Information
Local Administrators
Computer Name
Firewall Settings
Application Events - to an .evt file
System Events - to an .evt file
Installed Applications
Processes
Services
The script takes all the non .evt files and combines them into one .XLSX file, then moves it, plus the .evt files into the "\LOG" directory appended to the end of your "Browse to Location"

There are a total of three new tabs
The main tab you already know. The Log tab.
The second tab contains the installed programs functions listing all installed programs and giving you the ability to save this information for logging purposes.
The third tab is labeled Tools. In here you are provided with all tools buttons I can think of.
-Control Panel
-Powershell Admin Console
-DOS Admin Console
-Windows 10 Settings Window
-Open CMTrace (If it's installed)
-Method to restart SCCM Locally
-Method to repair SCCM Repository Locally
-Method to reset SCCM Repository Locally
-Keyboard Information
-OS Information
-System Information
-BIOS Information
-CPU Information
-RAM Information
-Motherboard Information
-Physical Drive Information
-Video Information
-Network Information
-Network Setting Information
-Monitor Information
-Mouse Information
-Process Information
-Services Information
-Page File Information
-USB Hub Information
-Logical Drive Information
-Optical Drive Information
-Sound Card Information
-Printer Information
-Fan Information
Tooltip's have been added to most if not all buttons.
You are also given a lovely Printers Button:
Printers gathers the printer information in much the same way. Or attempts to. If you run the printer button under the customer you get the correct output. This is due to "Authenticated User/Windows User". Otherwise the script opens the Devices and Printers window for you to catalog the installed printers in case there is anything other than FOLLOW_ME The script also opens up an Excel window and provides you with obviously more data than you might need. Maybe not? Not for me! (How many times did finding the same driver version work for local printers? You are welcome!)

You are also given a Programs Button:
What? No Way? It's True!

This opens a quick window that shows you all of the applications and versions installed on the computer. This is so you can quickly see what is installed on the old computer and make note as to whether you need to run the Inventory Button process or not. This part is ran during the Inventory Button process, however, it does not popup, and instead saves to the .XLSX created within the Inventory Button process.

No way there's more?
On top of audible queues, popups, and overall awesomeness, there is yet two more important features. First is the LOG window. This logs every state that the script goes through to the best of my ability. Second is the Copy to Clipboard. This copies the entire contents of the LOG window into the Clipboard so this can be pasted into your ticket notes.

What this script doesn't do?
Steal your soul.
Make you soup.
Hug you, or touch you in any way.
Care about your feelings.
Backup data you or the customer fail to tell it to.
Reads minds.
Log the data in the ticket.
Calls someones mom to setup a date.
In fact it will not call anyone.
Know who you or the customer actually are.
Why should you care?
You don't have to. Maybe your process is working for you, if so awesome, I am more than happy it does. Mine did not. The fact that this process is still a manual one still boggles my mind. When I started we were handed a two page document and told to follow the process off this document. No... That's being setup for failure, not success. So I worked on a better solution. This is the evolution of the initial idea. A year later. This is not a single person effort as much as it might seem so. Many people have helped contribute to the functionality and data that the script now backs up. In no way could this have ever been possible without everyone's help.</pre>
