
# Windows-Theme-Scheduler

## How to set light/dark theme automatically


#### Change the Task Bar, Start Menu, and System UI
* Dark:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 0 /f`
* Light:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 1 /f`

#### Change Apps, Browsers, etc.
* Dark:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 0 /f`
* Light:
	* `add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 1 /f`

![Step 1](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/1.png) width='2'
![Step 2](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/2.png)
![Step 3](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/3.png)
![Step 4](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/4.png)
![Step 5](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/5.png)
![Step 6](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/6.png)
![Step 7](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/7.png)
![Step 8](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/8.png)
![Step 9](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/9.png)
![Step 10](https://github.com/dcond007/Windows-Theme-Scheduler/blob/main/walkthrough/10.png)
