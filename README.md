# Poly-Phone-Manager

Poly Phone Manager is desiged to work with Poly VVX, CCX and Trio phones connected to Skype for Business and Teams SIP Gateway. This version of the tool has evolved from the Polycom VVX Phone Manager tool, hence that the inital release in this repository is version 4.00. The previous version of this tool is still available over there for the time being: https://github.com/jamescussen/skype-for-business-lync-polycom-vvx-manager.  

![Image](https://github.com/jamescussen/Poly-Phone-Manager/raw/main/PolyPhoneManager4.00sm.png)

**Version: 4.00**
- Teams SIP Gateway / Support for CCX / PowerShell 7
- Now supports Poly phones signed into Teams SIP Gateway
- Now works with Poly CCX Phones!
- You now don't need access to Skype for Business PowerShell to discover devices with the Network Discovery method. From any Windows PC you can discover devices.
- Removed Skype for Business online connectivity because Skype for Business Online has been deprecated.
- Updated to work with PowerShell 7+


**Features:**

**Support Poly phones connected to Skype for Business and Teams SIP Gateway** - Supports Poly VVX, CCX and Trio phones connected to Skype for Business and Teams SIP Gateway.

**Phone discovery** – Phones can be discovered either by automatically querying the Lync/Skype for Business Monitoring database (provided there is a monitoring role deployed in the environment) by pressing the “Discover from Monitoring DB” button. Alternatively, this can be done by entering IP Address ranges and “pinging” contiguous subnet ranges for phones using the “Discover from IP Range” button (format: '192.168.0.1-192.168.0.20' OR '192.168.0.0/24' OR add multiple with comma separation '192.168.0.0/24,192.168.1.0/24'). During the discovery process, phones that are logged in to user accounts will be listed in the users list. If the tool finds a VVX handset that is not signed in, it will be added to the  user list under the name “VVXNot@LoggedIn_<index number>”. This allows you to use the tool to access these devices even though they are not signed into the system.


**Export/Import Phone Info** – This feature outputs a CSV file that contains all the Users, IPs, Firmware Version, Serial Numbers, Lync/Skype for Business Server, and MAC Address (if available) for all phones. If you select the 'More'  checkbox you will also get the additional Lync/Skype for Business policy settings for each user (this is slower).


**Access Web Interface** - Access the web interface of a VVX phone by selecting a user in the user list and clicking the “Web Config” button. This will automatically load the web browser to the phone's web interface.


**Pin control** – The “Pin…” button will load a dialog that will Set, Test, Lock, Unlock a user’s PIN number.


**Send Text Messages** - Send text messages to be displayed on a Polycom VVX phone. An example of this would be to send a message to warn before a system upgrade or a reboot. Messages are displayed on the screen for 30 seconds. (Special configuration is required in the VVXs for this feature. See the blog post for more information)


**Get More Info** – By pressing the “More Info” button you can get extended information about a VVX phone including: Device Info, Call Status, Presence Info, Network Info, Line Info, SIP Status, Network Statistics.


**Reboot/Restart Phones** – You have the choice of Rebooting or Restarting a single, multiple, or All phones.


**Reset Config** – You have the option to Reset the Config or Factory Reset the configuration with one or many phones.


**Get/Set Config** - You can Get or Set any setting in the phone configuration. You simply need to enter the configuration setting name (as you would find in the configuration file eg. log.level.change.hset) and click the Get or Set buttons to view or change the setting's value.


**Dial / End Call** – You can choose to remotely dial a SIP URI (eg. john.smith@domain.com or[+61395551111@domain.com](mailto:+61395551111@domain.com)) on a phone by entering a URI and pressing the “Dial” button. If the phone is on a call you can also choose to end the call using the “End Call” button.


**Test FTP Config Server **- Test your FTP Configuration File server by simply entering the IP address of the FTP server and pressing the “Test FTP” button. The tool will attempt to connect to the FTP server and download information about key files associated with a Polycom configuration server deployment. These include the base configuration file (000000000000.cfg), configuration files in the CONFIG_FILES tag, any MAC address files associated directly with phones, and firmware files
 (*.sip.ld). The tool will give feedback as to the state of the FTP server.


**View Screen** – The “Screen…” button will open a dialog that will show you the user's screen. Before the user's screen can be viewed the user must first manually allow access to the Screen Capture feature (this is a security measure so that the user is aware that someone is viewing their screen). This setting within the Basic->Preferences screen will only be made available while the VVX screen dialog is displayed (the tool automatically makes the setting 'up.screenCapture.enabled'
 in the device to turn on this preference setting). At this point the user will have to enable the following setting in their phone preferences: **Settings -> Basic -> Preferences -> Screen Capture -> Enabled**


**Command Line Settings** – If you would like to load the script with your own specific settings to save time, you can specify these in the command line when loading the script. (See the blog post for more details)


**Settings Dialog** – The “Settings…” button allows you to configure your own passwords, web service port and HTTPS settings for the tool.


