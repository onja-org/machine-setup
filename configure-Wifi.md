# Configure Wifi network to download windows updates at night

Follow these instructions to automatically switch between metered and unmetered wifi connection. 


1. Download the [batch file and scheduled tasks](./WifiMeteredConnectionSwitcher.zip)
2. Unzip and place the folder “WifiMeteredConnectionSwitcher” in “C:\Program Files”.
3. Open “Task Scheduler”. Click “Import task” and navigate to the “WifiMeteredConnectionSwitcher” folder. Select the “switch to unmetered task” batch file, and click "ok". Click “Ok again” - you will need to enter your windows password - the password you use to log on to your computer. (if you don't have a password you will need to make one - search "change your password" from the windows menu)
4. Repeat the above to create a scheduled task to switch back to metered connections: Again from task scheduler click “Import task” and navigate to the “WifiMeteredConnectionSwitcher” folder. This time select the other batch file “switch to metered task”, and click "ok". Click “Ok again” - again you will need to enter your windows password.
5. The scheduled tasks should now be set up however you need to verify this has been done correctly. In task scheduler click "Task Scheduler Library". Now in the central window you should see the two scheduled tasks "Switch wifi to metered scheduled task" and "Switch wifi to unmetered scheduled task". Double cClick on the "Switch wifi to metered scheduled task" and navigate to the "Actions" tab. Ensure that there is a "start a program" action with a link to the "Switch_to_metered" batch file. If the link is not correct you need to double click the “Start a program” action and click browse for the “Program/script” address. Navigate to the “WifiMeteredConnectionSwitcher” folder  and select the “switch to unmetered” batch file. 
6. Repeat the above step for the "Switch wifi to unmetered scheduled task"
7. Go to Settings > System > Power & sleep > Additional power settings > Change when the computer sleeps > Change advanced power settings. 
Then in the sleep drop down set the following: 
Sleep after > Plugged in: “Never”
Allow hybrid sleep > Plugged in: “off”
Hibernate after > Plugged in: “never”
Allow wake timers > Plugged in: “Enable”
Then click save. 

Now you can leave your computer overnight and it will download windows updates starting from 11 pm. You have finished and do not need to complete the next step. 



### Note for network administrators (everyone else please ignore)

The batch files are configured to automatically change metered/unmetered settings for the following wifi names:
"Router Indigo 2.4Ghz"
"Rainbow access point"
"Router Blue 2.4Ghz"

If these networks are renamed, or new networks added, the networks need to be added to the batch files. 


#### how to make your own scheduled task and batch files from scratch

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