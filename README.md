# Macro-Scanner---Team-SS
JN Macro Scanner

The program scans for known to Team SS mouse macros to save both your and our time. 


ACTIVE ANTIVIRUS - Method 2

If the AntiVirus flags the .exe, it's because the script was written in .bat. Copy paste this code in a notepad & run it as .bat for the same effect. Note that it is absolutely safe to use and doesn't affect anything.

@echo off

title Macro Scanner - By Technostein

color 3 

if not "%1"=="am_admin" (powershell start -verb runas '%0' am_admin & exit /b)

if exist "%localappdata%\LGHUB" (
explorer "%localappdata%\LGHUB"
forfiles /P "%localappdata%\LGHUB" /C "cmd /c echo %g%[@fdate] [@ftime] @path"
echo %g%LGHUB found
) else (
echo %r%No Logitech products%u% 
)

if exist "%programdata%\Razer\Synapse\Accounts" (
explorer "%programdata%\Razer\Synapse\Accounts"
forfiles /P "%programdata%\Razer\Synapse\Accounts" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Razer Synapse detected
) else (
echo %r%No Razer products%u%
)

if exist "C:\ProgramData\Razer\Synapse3\Log" (
explorer "C:\ProgramData\Razer\Synapse3\Log"
forfiles /P "C:\ProgramData\Razer\Synapse3\Log" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Razer Turbo mode logs
) else (
echo %r%No Razer Turbo
)

if exist "%localappdata%\Razer\Synapse3\Settings" (
explorer "%localappdata%\Razer\Synapse3\Settings"
forfiles /P "%localappdata%\Razer\Synapse3\Settings" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Synapse settings
) else (
echo %r%No Razer Synapse
)

if exist "%programdata%\Razer\Razer Central\Accounts" (
explorer "%programdata%\Razer\Razer Central\Accounts"
forfiles /P "%programdata%\Razer\Razer Central\Accounts" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Razer account macros
) else (
echo %r%No Razer products
)

if exist "%appdata%\Corsair\Cue" (
explorer "%appdata%\Corsair\Cue"
forfiles /P "%appdata%\Corsair\Cue" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Corsair softwares
) else (
echo %r%No Corsair products
)

if exist "%localappdata%\BY-COMBO2" (
explorer "%localappdata%\BY-COMBO2"
forfiles /P "%localappdata%\BY-COMBO2" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Glorious found
) else (
echo %r%No Model O
)

if exist "%localappdata%\JM01" (
explorer "%localappdata%\JM01"
forfiles /P "%localappdata%\JM01" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Aukey found
) else (
echo %r%No AUKEY
)

if exist "C:\Program Files (x86)\Bloody7\Bloody7\Data\Mouse" (
explorer "C:\Program Files (x86)\Bloody7\Bloody7\Data\Mouse"
forfiles /P "C:\Program Files (x86)\Bloody7\Bloody7\Data\Mouse" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Bloody7 - method one
) else (
echo %r%No Bloody softwares
)

if exist "C:\Program Files (x86)\Bloody7\Bloody7\UserLog\Mouse\TLcir_9EFF3FF4" (
explorer "C:\Program Files (x86)\Bloody7\Bloody7\UserLog\Mouse\TLcir_9EFF3FF4"
forfiles /P "C:\Program Files (x86)\Bloody7\Bloody7\UserLog\Mouse\TLcir_9EFF3FF4" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Bloody7 - secondary method
) else (
echo %r%No bloody softwares
)

if exist "C:\Users\%username%\AppData\Roaming\REDRAGON\GamingMouse" (
explorer "C:\Users\%username%\AppData\Roaming\REDRAGON\GamingMouse"
forfiles /P "C:\Users\%username%\AppData\Roaming\REDRAGON\GamingMouse" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Redragon products detected
) else (
echo %r%No Reddragon products
)

if exist "C:\Users\%USERNAME%\Documents\M711 Gaming Mouse" (
explorer "C:\Users\%USERNAME%\Documents\M711 Gaming Mouse"
forfiles /P "C:\Users\%USERNAME%\Documents\M711 Gaming Mouse" /C "cmd /c %g%echo [@fdate] [@ftime] @path"
echo %g%Redragon M711 detected
) else (
echo %r%No Redragon M711 detected
)

exit
