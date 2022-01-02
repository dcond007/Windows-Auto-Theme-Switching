
# Windows-Theme-Scheduler

## How to set light/dark theme automatically



#### Open Task Scheduler
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/1.png" width="600">


#### Create a Task
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/2.png" width="600">


#### Name New Task
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/3.png" width="600">


#### Create a Trigger
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/4.png" width="600">


#### New Trigger
* You should trigger the task to run daily on a new schedule. Starting the light theme at 8:00AM and Dark theme at 8:00PM works nicely.
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/5.png" width="600">


#### Create an Action
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/6.png" width="600">


#### Add Registry edit
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/8.png" width="600">
* The following parameters will manually change the windows theme by directliy editing the registry. This is equiveant to heading to the settings menu, and changing the theme. Add the following arguments below as to your preferences. One set of arguments are for changing the windows task bar (windows ui) and the applications themes, such as for web browsers, microsoft word, and other apps. 

* Dark:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 0 /f`
* Light:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 1 /f`

#### Change Apps, Browsers, etc.
* Dark:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 0 /f`
* Light:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 1 /f`


#### Settings
* Run the task as soon as possible after a scheule is missed. Otherwise, if you are not logged into the computer during the runtime, windows will ignore the script. If the task fails, resetart it every minute up to 3 times. Cancel the task if it takes longer than an hour. Do not start a new instance. All of this will run seamless in the background. 
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/9.png" width="600">


#### Test the Script
* Head back to the task scheduler home library, look for the new schedueler, right click and select "run". You should see your windows theme change. Congrats, auto theme is now functional. 
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/10.png" width="600">



