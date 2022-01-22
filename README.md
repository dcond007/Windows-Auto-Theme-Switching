
# Windows Automatic Theme Switching
Windows OS does not include automatic theme switching. This guide will show you how to program auto theming via a task schedule. 
* Note: This guide shows the creation of one task. Two are needed for active dark/light mode switching. 


### Open Task Scheduler
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/1.png" width="600">



### Create a Task
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/2.png" width="600">



### Name New Task
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/3.png" width="600">



### Create a Trigger
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/4.png" width="600">



### Configure New Trigger
* Here is where you can set your prefered theme change start time. 
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/5.png" width="600">



### Create an Action
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/6.png" width="600">



### Configure New Action
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/8.png" width="600">

* If you want to change both the applications *and* windows ui theme, you would need two separate actions. Paste the one of the following arguments provided below:
#### Change Windows UI, Taskbar, File Explorer
* Dark:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 0 /f`
* Light:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 1 /f`

#### Change Apps, Browsers, Microsoft Word, etc.
* Dark:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 0 /f`
* Light:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 1 /f`



### Optimize Settings
* Run the script after a missed schedule. This way when you are on the computer after a scheduled run time, the task will still be enabled. 
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/9.png" width="600">



### Test the Script
* Congrats, auto theming is now created. Head back to the task scheduler home library, look for the new schedule, right click and select "run". You should see your windows theme change. Keep in mind another task would need to be created to enable dark mode. 
<img src="https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/10.png" width="600">



