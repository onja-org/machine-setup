# Windows install and configuration

## Starting fresh

We've got several licences of Windows 10 Pro N, and a USB install disk. It should take about 30 minutes to install a new machine, but make sure this is something you want to do, since [we aleady have pre-configured images of previous installs we can restore to our harddrives](./hard-drive-cloning.md).

### Installing windows

1. Make sure the computer is turned off.
1. Plug in the Silver Sandisk USB drive that has Windows 10 on it.
1. As the computer boots up, press `ESC` to load the BIOS Settings
1. Select F9 for Boot Options
1. Select the Mass Storage / USB / Sandisk option from the list.
1. Windows should start the install process

Then you'll be presented with a series of screen:

Option | Value
--- | ---
Language | English (United States)
Currency and Date settings | English (Madagascar)
Keyboard layout | US

Select Windows Pro N (x64) when prompted.

Username: "Student", password: "student".
The Students will change both of these when they configure their new machine.

Switch off diagnostics and unselect all the 'share my data' options

## Windows update

One of the first things you should do after the install finishes is to start Windows Update. This will take about 30 minutes, and will require several restarts.

- Start Windows Update by pressing the `Windows Key`, and type 'update'. Select 'Windows Update'
- Click 'Check for Updates'
- Load money into the router :P

## Uninstall bloatware

In 'Add or remove software', remove whatever you can (but keep Calculator). e.g.

- Xbox
- Office
- OneNote
- OneDrive
- Tips
- Weather
- etc

Uninstall features

- MS Hello Face
- Internet Explorer 11
- Quick Assist
- etc

Uninstall Optional features

- XPS document support
- Print and Fax
- and more?

## Configure Wifi network to download windows updates at night

- First make sure all wifi connections are set to metered. 
- Follow the [configure Wifi network to download windows updates at night file](./configure-Wifi.md)


## Further configuration

Date / Time / TimeZone settings

- Select UTC+3 Nairobi as the Time Zone.
- Make sure the time is correct

Power settings

- Make sure the WiFi adapter uses max performance.

System Preferences

- Press `Windows Key` + `Pause`.
- Under performance, select Best Performance, but check the checkbox for "Smooth edge of screen fonts"
- Remote desktop tab: disable or disallow Remote Desktop

Keyboard settings

- `Windows Key` + `R`
- In the Run Dialog, type 'control' followed by Enter.
- In the top-right, select Small Icons
- Find the Keyboard settings
- Set the keyboard repeat delay to fastest
- Set the keyboard repeat rate to fastest

Disable access keyboard shortcuts

- In settings, look up 'Ease of Access'
- Dsiable all keyboard shortcuts for features such as Sticky Keys, Filter Keys, etc.

## Last steps

Add software our developers use

1. Plug the P-Drive into this new machine.
1. Copy over the 'Onja Software' folder to the C drive.
1. Safely eject the P-Drive

Finally, create a Restore point, so that Windows can roll-back to this point if necessary.

1. `Windows Key` + `Pause`
1. Select the System Restore tab
1. Create a new Restore point, called: "Clean and configured" or such.

Done! Phew! :D

Shut down the machine and pull out the harddrive. [It's time to clone that sucka](./hard-drive-cloning.md)!