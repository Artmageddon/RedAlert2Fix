# Red Alert 2 Fix

## Intro
This guide is meant to serve as a way to help enable a player to get EA's "Command and Conquer: Red Alert 2" working on newer operating systems such as Windows 10. This may be seen as a duplication of others' efforts to help resolve these issues, but often times these sites are filled with annoying ads, or have broken links to the necessary files - sometimes the download sites themselves can also be extremely sketchy. Reddit has been super helpful in providing direct assistance, but the search can be terrible.

## Disclaimer:
Note that while my goal is to be as specific as possible in this guide, this has not been tested on a variety of systems, (only mine, in fact), so I do *not* and *can not* guarantee that this will work for everyone. In addition, I am not responsible for anything which may happen to your instance of Red Alert 2 or even your system as a result of following the instructions contain herein.

**This guide assumes a clean installation of Red Alert 2 via Origin, not from "C&C: The First Decade" or original copies from Westwood.**

My PC specs are listed below (home-built around 2015), for posterity:

PC Component|What I'm Using
------------|--------------
CPU|Intel i7-4770K
RAM|32GB DDR-3
OS|Windows 10, 64-bit
GPU:|NVidia GTX-970
Display:|Single monitor set to 1920x1200

Red Alert 2 version: v1.006
Yuri's Revenge version: v1.001

## Set the correct compatibility mode for RA2 executables
* Locate the Red Alert 2 folder on your local hard drive
* Right-click on Game.exe, properties, Compatibility Tab
  * Set Reduced Color Mode to True
  * Select 16-bit (65536) color 
  * Set "Run this program as an administrator" to True
* Right-click on GameMd.exe, properties, Compatibility Tab
  * Set Reduced Color Mode to True
  * Select 16-bit (65536) color 
  * Set "Run this program as an administrator" to True

## Download the DirectDraw DLL
Extract the contents of the zip file into your local RA2 folder. Assuming this is your first time attempting this, the DLL and config file should be brand new to the folder, and you should not be prompted about overwriting any other files. *Src.7z* is not necessary (but is included to examine/build the DirectDraw DLL).

[Click here to download the DirectDraw DLL archive](https://github.com/Artmageddon/RedAlert2Fix/raw/master/RA2_Windows_10_64bit.zip)

## Edit the RA2.INI file

Open the RA2.ini file in your favorite text editor. Ensure that the following lines are present within the [Video] section:

    [Video]

    AllowHiResModes=yes

    VideoBackBuffer=no

    ScreenWidth=1920

    ScreenHeight=1080

    StretchMovies=no

The ScreenWidth and ScreenHeight can be adjusted as necessary (assuming your monitor supports it, within reason).

In the Intro section, add "Play=no" to suppress the intro videos and get to the action sooner:

    [Intro]

    Play=no

Feel free to refer to the Sample_RA2.ini contained within this repo as an example.

*Note: Adding "AllowVRAMSidebar=no" in the [Video] section may be an option if the above settings weren't sufficient, but I haven't tested it*

## Configure Origin
* Finally, some of the Origin settings can interfere with the stability of the game. Run Origin, and go to My Games. 
* Right-Click on Red Alert 2, and select Game Properties.
* In the General tab "Disable Origin in Game for this game" to True
* In the "Cloud Saves" tab, find "Enable cloud saves for all supported games" and set it to false / unchecked
* Click Save

Go play!

## Credit where credit is due:

If you're still facing issues, sorry :( but don't give up! Try the links below for more suggestions:

http://patrikkopac.blogspot.com/2015/09/c-red-alert-2-yuris-revenge-windows.html?m=1

https://www.reddit.com/r/redalert2/comments/3lqzf1/resources_for_fixing_compatibility_issues_and_bugs/

https://github.com/CnCNet/ts-ddraw

