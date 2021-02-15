@Echo off
title Call of Duty Warzone / MW Trace Cleaner AKA Cujo Cleaner
cls
color 0a

echo Welcome to the Call of Duty Warzone / MW Trace Cleanup Utility made by Kevin (Spook#0593) 
echo.
echo discord contact information. Spook#0593
echo.
echo !!! DISCLAIMER !!!
echo PLEASE MAKE SURE BOTH WARZONE AND BLIZZARD ARE BOTH CLOSED - CHECK YOUR SYSTEM TRAY
echo AND MAKE SURE - THIS TOOL WILL NOT WORK PROPERLY IF THEY ARE STILL OPEN. YOU MUST EDIT YOUR GAME LOCATION VIA NOTEPAD!
echo.
echo ********************************************************************************************
echo * !!! WARNING !!! * YOU MUST RUN THIS .BAT TOOL AS WINDOWS ADMINISTRATOR!
echo.
echo * You are about to delete game files and folders that are used by Activision and Blizzard *
echo * to track player progress, including bans on your system. *
echo * *
echo * Once completed, this system will be reset as if the game was freshly installed. *
echo ********************************************************************************************
echo.
echo Close this window to cancel...
PAUSE

echo.
echo Cleaning trace files and folders...
echo.
Ping localhost -n 2 >Nul

echo Phase 1 of 2 - Removing files
echo Removing trace files from the Call of Duty Modern Warfare main folder.
echo.

echo Removing data0.dcache
del /F /Q "E:\Games\Call of Duty Modern Warfare\main\data0.dcache"
Ping localhost -n 2 >Nul

echo Removing data1.dcache
del /F /Q "E:\Games\Call of Duty Modern Warfare\main\data1.dcache"
Ping localhost -n 2 >Nul

echo Removing toc0.dcache
del /F /Q "E:\Games\Call of Duty Modern Warfare\main\toc0.dcache"
Ping localhost -n 2 >Nul

echo Removing toc1.dcache
del /F /Q "E:\Games\Call of Duty Modern Warfare\main\toc1.dcache"
Ping localhost -n 2 >Nul

echo Removing cmr_hist
del /F /Q "E:\Games\Call of Duty Modern Warfare\main\recipes\cmr_hist"
Ping localhost -n 2 >Nul

echo Removing shmem
del /F /Q "E:\Games\Call of Duty Modern Warfare\Data\data\shmem"
Ping localhost -n 4 >Nul

echo. Phase 1 Complete

echo.
echo Phase 2 of 2

echo Removing Warzone and Blizzard Local Application and Program Data Folders
echo Keeping Game Files.
echo.
Ping localhost -n 4 >Nul

echo Removing the Call of Duty Modern Warfare folder from the User Profile
rd /s /q "%USERPROFILE%\Documents\Call of Duty Modern Warfare\"
Ping localhost -n 2 >Nul

echo Removing the Battle.net folder from LocalAppData
rd /s /q "%localappdata%\Battle.net"
Ping localhost -n 2 >Nul

echo Removing the Blizzard Entertainment folder from LocalAppData
rd /s /q "%localappdata%\Blizzard Entertainment"
Ping localhost -n 2 >Nul

echo Removing the Battle.net folder from AppData
rd /s /q "%appdata%\Battle.net"
Ping localhost -n 2 >Nul

echo Removing the Battle.net fodler from ProgramData
rd /s /q "%programdata%\Battle.net"
Ping localhost -n 2 >Nul

echo Removing the Blizzard Entertainment folder from ProgramData
rd /s /q "%programdata%\Blizzard Entertainment"
Ping localhost -n 2 >Nul

echo.
echo.
echo ********************************************************************************************
echo * System Cleanup Complete *
echo * *
echo * The game may reload shaders, because these files were cached and have been removed. *
echo * In rare cases, the game might require a repair before it will launch. *
echo * *
echo ********************************************************************************************
echo.
echo Have a great day!

pause
