

> Documentation of multi‑device anomalies, firmware persistence, and unauthorized control patterns observed between May 2024 – Oct 2025.

---

### May 2024 – Pre‑Attack Indicators
### Device: HP Laptop
- Suspicious self‑sent email referencing Pegasus infection
- HP Laptop hardware failure: no HDMI signal or power‑on capability
- Event aligns with Telegram data breach verification (Have I Been Pwned)

### February 2025: Vivobook

- Professor Termux Powershell Script shows Logo and sucess output but nothing happens. Felt something was off so decided to do restart (not sure if this has anything to do with anything). (See Glossary)
- During restart, Microsoft required the Bitlocker code. Accessed aka.ms on mobile one and got an error before accessing code that I was attempting to login to a work account. (See Glossary)
- Downloaded Bitdefender (See Tools)
- While routin3e web browsing, intrusive PowerShell command windows sporadically popped up in the background, demonstrating unauthorized automated scripts interfering with user sessions. 
- **Feb 14**: Factory Reset, deleting all files.
- Downloaded PS 7, edited enviomental variables to push to PS 7, disabled original Powershell programs, changed names and extensions of original Powershell (and ISE).
- Strange **"Status: Shared"** bolded, dark blue text appears at the bottom, left hand corner of File Explorer. Confirmed Network Sharing and other share features were off. No way to turn off or see where its coming from. Multiple folders including **Downloads** and **Documents** show this while others do not.
- Notices items with PHI and PII on them in the Shared folder of One Drive. These files were in the One Drive locked, password protected section.
    - Reported to Microsoft. Changed passwords, changed 2FA methods, changes recovery emails. 
- Attemps to report Bitlocker work error to Microsoft. 
    - Used consumer Live Chat, eventually directed that Microsoft Business. 
    - Attempted to call Microsoft Business with the number provided through Live Chat. Automated prompts with no live support.

## March 2025

- Notices Skype and X Box account while in Windows Account settings i did not create.
- Creates secondary account to make Local Admin Account with password, not connected to Microsoft account for high privleged uses like System Settings. Makes current account basic user. 
- Disables remote features: Lanman and Lanman Workstation, Remote Desktop, Windows Management Instrumentation, SDDP, Work Folders. (See Glossary)
- Powershell Pester module folder appears. 
- Tries to delete folder in multiple ways: right click > delete and clear recycling bin, Bitdefenders Shredder tool worked affer multiple attempts.
- Using PS 7, set excecution policy to restricted. See Glosaary
- **Mar 20**: First Clean Install
- Before completing Clean Install, while in UEFI discovers: Intel Me Management and on UEFI front page, "Memory" in specs is spelled incorrectly, "memroy". Secure Erase does not show in options. Secure Boot is on.
- I used Diskpart, Clean All to completely wipe the drive then deleted the paritions and installed the new Windows 10 from the USB, which went smooth.
- Signed into Windows with a "new" email. 
- Reinstalled Bitdefender (See Tools)

## April 2025
- After finding out about fileless Malware, i used the registry editor to "turn off" Powershell. (See Glossar
- Receieved Bank transaction which shows a transaction being charged from Zoho. I have not accessed that Zoho account since 2024. No charges have came since then.
- Windows 10 22H2 updates fails multiple times with no explanation.
- Upgrades to Windows Pro to get Group Policy.
- Downloads Bitdefender and Malware Bytes (can check for root kits)
- Malware Bytes finds PUM is found in registry editor in Policies along with "do not tell user i'm here" note.
- **April 5**: Second Clean Install
- Forced update in the middle of OS boot up which I end up canceling due to 45 minute stall.
- Disables Intel Management, Camera and Bluetooth in UEFI.
- Unable to use Miracast (keeps cutting off) 
- Services disabled before Clean Install are still disabled.
- Many issues with modifying files and installing programs.
- Pestter appears again
- File Folders in File Explorer labeled as "**My Documents**, "**My Pictures**" "**My Music**", "**My Downloads**" instead of as they have been labeled since Vista (no prefix).
- Bitdefender processes still show up in Task Manager background services.
- Turns Powershell Event Viewer on.
- Redownloaded Malware Bytes and scan shows files it can not access. Not able to view file from in program, attempted to view Scan Log in Malware Bytes folder and I begin seeing file name and extension changes to .bin and .py from .exe and .png etc. etc.
- Discovers many Unknown Devices in Device Manager.
- While disabling Unkown Devices, the screen zoom and tint changes. 
- The mouse disapears and seconds later appears and bgins moving across screen being controlled elsewhere. Not able to control mouse.
- **April** **12**: UEFI Flash and Third Clean Install
- Disabled Intel Management, Camera and Bluetooth.
- Local Account and set up with no network.
- Mouse working again 
- Was not asked to enter a computer name.
- "4688 Event" each time I enter command on Powershell. Successful output but Event Viewer notes a script (same script each time) milliseconds after I send mine which is diffrent than my input.
- Task Scheduler: Multiple tasks with missing author data on Microsoft related systems like Active X, Application Experience, tasks with discrepency authors (Microsoft and Microsoft Corporation) and odd Folders like Enrollment, Edu Print and Work Folders.
- Windows Email App ups up with autofilled username which is email from previous laptop that i can no longer access.
- Discovers Admin Account is Deny Only.
- Discovers Laptop name is same as prior no longer accessible laptop.
- Downloads Malware Bytes on MDuno.

## April: Mobile Device One & Two
- Discovers IP Cam on MDuno in Apps section of Malware Bytes. Phone shuts off moments later. No charge or charging indicator when attached.
- Once reloaded, hours later, phone on reset options screen. Attempt to clear cache and restart phone fail. Factory reset required.
- Realizes MBuno has modded bootloader.
- Mobile Device One (EOLD) gets system update.
- SMBv1 and SMBv2 services (typically disabled on secure setups) were automatically re-enabled on Vivobook.
- Begin migrating files to Mobile Device Two
- MDuno Sim Swapped (first)
- **April 20:** Mobile Device Two (EOL/LE D/ MDdos) shuts down randomly, no charge or charging indicator when attached. Phone cuts back on four hours later.
- MDdos has new System Update completion.

## May 2025
- Logged into WiFi on Mobile Device Three (LE/ MDTres) No other old accounts acceessed. 
- Using Private Browser, Firefox Focus, temporarily logged into prior Gmail. Logged out cleared storage and removed browser on MDTres
- Moments later, Settings App temporarily displays **App Not Found** when clicked but then appeared again, moments later in the app drawer.
- MDtres Update (downgrade  in version number)
- Logged into Wifi on Mobile Device Three at startup.
- Began using NextDNS.
- Moments later while checking DNS Firebase and Sentry conigs hit NextDNS.
- Settings App disappears and reapears on multiple devices.
- Got Device Four
- Sim UI Kit and Auth Kit appear in Screen Time Settings 
- 
- Wikipedia, X, Websheet and Reddt apps appear in Screen Time Restrictions but not seen on device.
- Screenshots end up in the Illustrations photo album
- eSim Swapped
- Hidden Apps section in Settings > Apps but just blurry background when clicked.
- As i was checking Accesaibility features on IPhone, something is attempting to intercept it. They wttempt to shut off screen and use braille features.
- While using Voice Over in Screentime Settings, Wikipedia is pronounced in a strong, Eastern European accent. 
- DFU performed.
- MDtres has an update going from Version **7.06XBA → 6XBG** (downgrade attempt)  
## June 2025
- Unsolicited parental control prompts appear on the smart TV without any related configuration. 
- Sim Swappwd on iPhone for a second time.
- TCL launched an app with the title Device Policy prompting QR or IT code entry.
- Google Drive and Doca has options to switch to personal but are not clickable.
- Google Settings UI on OnePlus shifted from "Your device is not enrolled on a Chromebook" to "Your OnePlus is not enrolled on a Chromebook"
- Protected storage paths like /file/1000000149/ that survive reboots
- Monopoly Go and Whats App folders appear on devices 
