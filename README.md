
# Windows-Theme-Scheduler

## How to change windows light/dark theme automatically


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
