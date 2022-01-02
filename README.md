
# Windows-Theme-Scheduler

## How to set light/dark theme automatically
* Two tasks are needed for both light mode and dark mode. 



#### Open Task Scheduler
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/1.png" width="600">


#### Create a Task
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/2.png" width="600">


#### Name New Task
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/3.png" width="600">


#### Create a Trigger
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/4.png" width="600">


#### Configure New Trigger
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/5.png" width="600">


#### Create an Action
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/6.png" width="600">


#### Add Registry edit
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/8.png" width="600">
* Add the following parameters to edit the theme on the windows registry. This is equivalent to heading to the settings view and adusting your theme via windows GUI.
#### Change Windows UI, Taskbar, File Explorer
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
* Make sure you run the script after a missed schedule. This way when you are on the computer after a schedule run time, the theme change will still be enabled. 
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/9.png" width="600">


#### Test the Script
* Head back to the task scheduler home library, look for the new schedueler, right click and select "run". You should see your windows theme change. Congrats, auto theme is now functional. 
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/10.png" width="600">



