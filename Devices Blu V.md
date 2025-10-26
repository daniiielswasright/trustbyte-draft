**Device**: B160V 
**OS**; Android 14 
**Google Play Store Update**: 11/01/2023
**Baseband**: molylr12a.r3-mp.v288.3.pg
**Kernel**: 4.19.191-00317-gc493d54bc2bf
**Build**: up1a.231005.007
**Custom Build** blu_b160v_v14.0.05.05.05.03_fsec 

Primary Compromise Indicator:
Easter 2025 
Unexpected system update notification on EOL/lower-end device accounts. Notable because device shouldn't receive updates due to age/model

**Pre-existing Conditions:**
- Multiple emails  already added to device
- Compromise may have spread through existing accounts?

**System Behavior Anomalies:**
- Android System WebView with multiple sandbox activities (over 30)
- MTP host presence

Weird apps:
- Home (com.google.android.apps.chromecast.app)
    Open links from oauth-redirect.googleusercontent.com, madeby.google.com and .com.google.android.apps.chromecast.app


**Google Play Store** (com.android.vending)  
No battery optimization


Com.android.backupconfim
Data restore tool
**Default print service** 
**DMClient** (com.vzw.otadm)
**My Verizon Services** (com.verizon.mips.services) 
No battery optimization 
Related to my Verizon app
Not a Verizon phone never had Verizon as carrier. Phone locked to one of the Walmart carriers.

Print spooler (com.android.printspooler)
Systemui (com.android.systemui)


**Work Set Up** (com.android.mananagedprovisioning)
This is NOT a work device.

**Verizon Activation** (com.mediatek.ims.pco) 
I don't have Verizon.

**Device Lock Controller**
**Permission Contoller**
Android System 
