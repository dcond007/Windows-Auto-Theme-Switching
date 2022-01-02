# Windows-Theme-Scheduler
Change windows app and system theme to light or dark mode using the Task Scheduler

Add a task schedlue script for light mode, and another for dark mode. Script can be set to run at a time, for an automatic effect. <br />

Add the following to the "add" portion to the script editor:<br />


#### Changes the Task Bar, Start Menu, and System UI
##### Dark:
`add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 0 /f`
##### Light:
`add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 1 /f`

#### Changes Apps, Browsers, etc.
##### Dark:
`add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 0 /f`
##### Light:
`add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 1 /f`

# 1
## 2
### 3
#### 4
## Navigation Walkthrough

<img src='' title='Navigation' width='500'  />

