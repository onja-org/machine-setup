# configure Wifi network to download windows updates at night

Follow these instructions to automatically switch between metered and unmetered wifi connection. 


1. Download the [batch file and scheduled tasks](./WifiMeteredConnectionSwitcherIndigo.zip)
2. Check that the wifi name in the batch file is correct. Note that it must be done separately for each wifi connection, and redone if the wifi name was to change. 
3. Place the folder “WifiMeteredConnectionSwitcherIndigo” in “C:\Program Files (x86)” If this is not possible put them somewhere they won’t be deleted3.
4. Open “Task Scheduler”. Click “Import task” and navigate to the “WifiMeteredConnectionSwitcherIndigo”. Select the “switch to unmetered task” batch file. 
Click on the “actions” tab of the new popup
Double click the “Start a program” action and click browse for the “Program/script” address. Navigate to the “WifiMeteredConnectionSwitcherIndigo” folder again and select the “switch to unmetered” batch file. 
Click “Ok”
Click “Ok again” - you may have to enter your password. 
5. Repeat the above to create a scheduled task to switch back to metered connection using the relevant files.
6. Go to Settings > System > Power & sleep > Additional power settings > Change when the computer sleeps > Change advanced power settings. 
Then in the sleep drop down set the following: 
Sleep after > Plugged in: “Never”
Allow hybrid sleep > Plugged in: “off”
Hibernate after > Plugged in: “never”
Allow wake timers > Plugged in: “Enable”
Then click save. 

Now you can leave your computer overnight and it will download windows updates starting from 11 pm. 


## In case your want to make your own scheduled task and batch files from scratch then:

1. Create batch file as described [here](https://superuser.com/questions/1015438/configure-windows-for-an-internet-connection-thats-only-metered-during-the-day).  Add a line to the batch file used to switch to unmetered as the system only starts downloading updates once a restart is performed: 
C:\Windows\System32\shutdown.exe /r /t 0

2. Create scheduled tasks to run the batch files at the required time. Make sure to select: 
General tab:
- “run when user is logged on or not
- Run with highest privileges
Conditions tab
- Uncheck “Start the task only if the computer is on AC power”
- Check “Wake the computer to run this task
Settings tab
- For switching back to metered connection check “Run the task as soon as possible after a scheduled restart is missed