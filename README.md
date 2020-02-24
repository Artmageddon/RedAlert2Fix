# Red Alert 2 Fix

## Intro + Disclaimer
This guide is meant to serve as a way to help enable a player to get EA's "Command and Conquer: Red Alert 2" working on newer operating systems such as Windows 10. Note that while my goal is to be as specific as possible in this guide, this has not been tested on a variety of systems, (only mine, in fact), so I do *not* and *can not* guarantee that this will work for everyone. In addition, I am not responsible for anything which may happen to your instance of Red Alert 2 or even your system as a result of following the instructions contain herein.

My PC specs are listed below (home-built around 2015), for posterity:

PC Component|What I'm Using
------------|--------------
CPU|Intel i7-4770K
RAM|32GB DDR-3
OS|Windows 10, 64-bit
GPU:|NVidia GTX-970
Display:|Single monitor set to 1920x1200

## Set the correct compatibility mode for RA2
-Locate the Red Alert 2 folder on your local hard drive
-Right-click on RA2.exe
-Set the compatibility mode for Windows XP


## Download the DirectDraw DLL
Extract the contents of the zip file into your local RA2 folder. Assuming this is your first time attempting this, the DLL and config file should be brand new to the folder, and you should not be prompted about overwriting any other files.

## Edit the RA2.INI file
AllowHiResModes=yes
AllowVRAMSidebar=yes
VideoBackBuffer=no
ScreenWidth=1920
ScreenHeight=1080
StretchMovies=no

## Configure Origin
Disable Origin in-game
Disable cloud saves

## Other URLs:
http://patrikkopac.blogspot.com/2015/09/c-red-alert-2-yuris-revenge-windows.html?m=1
