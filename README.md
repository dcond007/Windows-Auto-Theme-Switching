# Windows-Theme-Scheduler
Change windows app and system theme to light or dark mode using the Task Scheduler

Add a task schedluer for light mode, and another for dark mode. Script can be set to run at a time, for an automatic effect. <br />

Registry editor commands:<br />

Dark:<br />
add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 0 /f<br />
add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 0 /f<br />

Light:<br />
add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v AppsUseLightTheme /t REG_DWORD /d 1 /f<br />
add HKCU\SOFTWARE\Microsoft\Windows\CurrentVersion\Themes\Personalize /v SystemUsesLightTheme /t REG_DWORD /d 1 /f<br />
