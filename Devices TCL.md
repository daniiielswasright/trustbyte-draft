Model: T434D 
Kernel: Moly.lr12A.r3.mp.v294.p3
Kernel version: 5.10.209
Suspicious Update Analysis:


**Original phone update version:** v7.06XBA
May 20,2025 forced update version: 6XBG (downgrade)

May 25, 2025 Update version: TCL UI 6XBL (phone says it's currently on TLC UI version v7.06XBL with a build of 6XBL)

  
**Red Flags**:
Version number irregularity (going from 7.06 to 6)
Minor letter change (BA to BG) triggering full system update
Unusual update size (145.9 MB) which is too large for minor patch, too small for legitimate firmware update is consistent with malicious payload or APK injection package.

**Immediate Compromise Indicators:**
- Firebase remote config DNS queries appeared instantly after minimal setup
- Originally only WiFi and Twitter login performed on device and then NextDNS showed immediate suspicious activity including firebase remote configurations, Google remote apis and ton of random apps

**Other wierd things**:
- App not found error briefly for Google Play store 
- Settings has feather suggestions which also gives app not found wrror when first clicked then it brings up smart manager.
- Upon connecting the charger, the bottom edge of the screen lit up with a green glow, accompanied by noticeable visual warping, similar to previous anomalies observed in notifications and overlays.  This is not consistent with the device’s standard charging behavior and suggests a tampered SystemUI or malicious overlay service designed to spoof system-level visuals.

- Weird WiFi calling notification “tap ere to confirm or update emergency location information for WiFi calling. This will allow you to make and receive voice calls when cellular network is not available”  it's a like WiFi calling app? version v14.0.0.0.0005.6 cannot disable it or the notifications.

- Google Docs and GMail app has a “switch to personal drive’ that I can't access 


**October 10, 2025**
TCL v7.0.6XE2
Build 6XE2
Moly.lr12A.r3.mp.v294.p40

---

📞 Telephony & Carrier Control

com.android.calllogbackup
Function: Backs up and restores call logs.  
Red Flags:
- Read voicemails: Accesses sensitive voice message content.
- Query all packages: Can enumerate installed apps—useful for profiling or targeting.
- Broadcast a change message: May trigger other apps or services on call log changes.  
Vector: Call metadata access / app profiling

---

com.android.carrierconfig
Function: Provides carrier-specific configuration (VoLTE, roaming, SMS/MMS).  
Red Flags:
- Read privileged phone state: Elevated access to SIM and network state.
- Bind to carrier services: Can interface with carrier apps for overrides.  
Vector: SIM/network override / privileged access

---

com.android.carrierdefaultapp
Function: Handles out-of-balance (OOB) carrier mitigation and provisioning.  
Red Flags:
- Modify phone state: Can alter network behavior or SIM status.
- Bind job service: Background execution with elevated privileges.  
Vector: Carrier-triggered SIM control / silent provisioning

---

com.android.cellbroadcastreceiver
Function: Delivers emergency and government alerts.  
Red Flags:
- Read cell broadcast messages: Access to sensitive public alert content.
- Dynamic receiver not exported: Hidden broadcast hooks.  
Vector: Alert interception / hidden broadcast triggers

---

🌐 Browser & Web Access

com.android.chrome
Function: Web browser with extensive activity and service footprint.  
Red Flags:
- Access coarse/fine location, Record audio, Bluetooth scan: Enables behavioral tracking.
- Sandboxed process (1–37): Indicates multiple isolated execution environments.
- Mini dump upload, Download broadcast manager: Potential telemetry or crash data exfiltration.  
Vector: User tracking / telemetry / sandboxed execution

---

🧪 System Testing & Shims

com.android.cts.ctsshim / com.android.cts.priv.ctsshim
Function: Compatibility testing and upgrade verification.  
Red Flags:
- Violates W^X policy: May execute writable memory—security risk.
- Post notifications: Can surface alerts despite being dormant.  
Vector: Memory policy violation / stealth notification

---

🔒 Device Lock & Provisioning

com.android.devicelockcontroller
Function: Manages device lock and financing enforcement.  
Red Flags:
- Query all packages, Install existing packages: App enumeration and silent installs.
- Wake lock, Receive boot completed: Persistent background execution.
- Dump: Can extract internal state.  
Vector: Persistent control / silent app manipulation

---

com.android.managedprovisioning
Function: Sets up work profiles and corporate device control.  
Red Flags:
- Manage users, Write settings, Query all packages: Full control over user profiles and system config.
- Dispatch provisioning, Dump: Can trigger device setup and extract state.
- Silent device owner provisioning: Background enterprise control.  
Vector: Enterprise-level device takeover / silent provisioning

---

📧 Messaging & Communication

com.android.emergency
Function: Emergency dialer and alert handler.  
Red Flags:
- Read phone state: Access to SIM and network status.
- Call phone: Can initiate emergency calls—potential abuse vector.  
Vector: Emergency call spoof / SIM state access

---

com.android.mms.service
Function: Handles MMS messaging.  
Red Flags:
- Read SMS, Read phone state: Access to message content and SIM status.  
Vector: Message interception / SIM profiling

---

com.android.imsserviceentitlement
Function: Manages WiFi calling entitlement.  
Red Flags:
- Dump, Broadcast data messages to apps: Can extract internal state and push messages.
- Firebase services + entitlement polling: Persistent background communication.  
Vector: Entitlement spoof / background messaging

---

📂 Storage & Media Access

om.android.externalstorage
Function: Manages access to external storage.  
Red Flags:
- Read external storage: Full access to user files.
- Write external storage: Can modify or inject files.  
Vector: File exfiltration / media manipulation

---

com.android.mmitest
Function: Hardware diagnostics.  
Red Flags:
- Read external storage, Read media video, Read media visual user selected: Deep access to user content.
- Kill background processes: Can terminate other apps.
- Read phone state: SIM/network access.  
Vector: Media surveillance / app disruption

---

📡 Location & Network

com.android.location.fused
Function: Provides fused location data from multiple sources.  
Red Flags:
- Access background/coarse/fine location: Enables persistent location tracking.
- Write secure settings: Can alter system-level location behavior.  
Vector: Stealth location tracking / config override

---

com.android.ons
Function: Opportunistic network service.  
Red Flags:
- Read phone state: Access to SIM and network priority.
- Receive boot completed: Persistent execution.  
Vector: Network manipulation / SIM prioritization

---

com.android.otaprovisioningclient
Function: Handles OTA update provisioning.  
Red Flags:
- Read phone state, Receive SMS, Receive WAP push: Can intercept provisioning messages.
- OTA gateway access: Potential for update manipulation.  
Vector: Provisioning spoof / OTA injection

---

.Here’s a detailed breakdown of read-related permissions across the apps you listed, with why each is concerning from a forensic and threat modeling perspective:

---

📖 Read Flags & Their Implications

com.mediatek.telephonyprovider*
- Read phone state  
  - Grants access to SIM info, network type, roaming status, and call state.  
  - Concern: Enables tracking of SIM activity and potential SIM-based profiling.  
  Vector: SIM surveillance

---

com.mediatek.ims.rcsservice, com.mediatek.ims, com.mediatek.ims.pco
- Read phone state  
  - Same as above, but tied to IMS/RCS stack.  
  - Concern: Could expose VoLTE/RCS session metadata or enable call interception.  
  Vector: VoLTE/RCS metadata access

---

com.android.stk
- No explicit read flags, but SIM Toolkit can indirectly read SIM commands.  
  - Concern: Known SimJacker vector—can execute SIM-based commands that read device state.  
  Vector: SIM command injection

---

com.tcl.browser
- No explicit read flags listed, but browser apps typically request:  
  - Read history/bookmarks, Read external storage, Read network state  
  - Concern: If hidden or unlisted, may read user data silently.  
  Vector: Hidden data exfiltration

---

com.android.shell
- Read accounts  
  - Accesses list of user accounts (Google, email, etc.)  
  - Concern: Can enumerate identities for targeting or spoofing.  
- Access media location  
  - Reads geolocation metadata from media files.  
  - Concern: Enables forensic tracking via photos/videos.  
  Vector: Account enumeration / media geolocation

---

com.android.egg
- Read external storage  
  - Access to user files, photos, downloads.  
  - Concern: Easter eggs are often overlooked; could be a covert data access point.  
  Vector: Hidden file access

---

com.google.android.ext.services
- No explicit read flags, but system services often inherit read access via job services.  
  - Concern: May read cached model data or user preferences.  
  Vector: Model-based profiling

---

com.google.android.setupwizard
- Read contacts  
  - Access to contact list.  
  - Concern: Can be used for social graph mapping or phishing.  
- Read locations from media  
  - Same as Access media location.  
  - Concern: Enables location tracking via user-generated content.  
  Vector: Contact harvesting / location profiling

---

com.google.android.as (System Intelligence)
- Read call log  
  - Access to incoming/outgoing call history.  
  - Concern: Behavioral profiling, call pattern analysis.  
- Read contacts  
  - Same concern as above.  
- Read SMS  
  - Access to text messages.  
  - Concern: High-risk for privacy breach, OTP interception.  
  Vector: Behavioral surveillance / message interception

---

com.android.server.telecom
- Read call log  
- Read contacts  
- Read external data  
- Read phone state  
  - Concern: Full telecom stack access—can reconstruct call behavior, contact networks, and device state.  
  Vector: Telecom surveillance / call manipulation

---

com.google.android.cellbroadcastreceiver
- Read cell broadcasts  
- Read SMS  
  - Concern: Emergency alert interception, SMS monitoring.  
  Vector: Broadcast spoof / SMS surveillance

---

com.android.bluetoothmidiservice
- No read flags, but Bluetooth scan can infer nearby devices.  
  - Concern: Passive device fingerprinting.  
  Vector: Proximity profiling

---

com.android.bluetoothprovider
- No read flags, but bookmark provider could imply legacy read access.  
  - Concern: Compatibility stubs may be exploited for unexpected queries.  
  Vector: Legacy data access

---

🔍 Summary of High-Risk Read Flags

| Permission              | Risk Description                                 | Common Vectors                      |
|------------------------|--------------------------------------------------|-------------------------------------|
| READPHONESTATE     | SIM, network, call status                        | SIM surveillance, VoLTE profiling   |
| READ_CONTACTS        | Access to contact list                          | Social graph mapping, phishing      |
| READCALLLOG        | Call history                                    | Behavioral profiling                |
| READ_SMS             | Text messages                                   | OTP interception, message spoofing  |
| READEXTERNALSTORAGE| User files, media                               | Data exfiltration                   |
| READ_ACCOUNTS        | User identities                                 | Account spoofing, targeting         |
| ACCESSMEDIALOCATION| Geotags from photos/videos                      | Location tracking                   |
| READCELLBROADCASTS | Emergency messages                              | Alert spoofing or suppression       |

---

---

🧠 Suspicious or Ambiguous Functionality

com.mediatek.gbaservice
- No activities/providers/receivers: Suggests passive background operation.
- Permission: bind gba service: Could imply inter-process communication with privileged components.
- "Generic bootstrapping architecture": Vague and potentially misleading—could be a placeholder for multiple Mediatek subsystems.  
Vector: Privileged IPC / passive service injection

com.tcl.fota.system.overlay
- Overlay-only: No code, permissions, or services—yet targets firmware update system.
- Persistence risk: Overlay could enforce update UI or suppress user control.  
Vector: Forced update persistence / UI masking

com.android.settings.overlay
- Settings UI modification: Overlaying system settings can mask or redirect user actions.  
Vector: Configuration spoof / user control obfuscation

com.mediatek.op08.ims
- Uses manage users + read precise phone state: Elevated access to user profiles and SIM/network state.
- No clear IMS activity exposed: Could be carrier-specific or hidden VoLTE hooks.  
Vector: SIM control / user profile manipulation

---

📡 Carrier & Network Manipulation

com.android.carrierdefaultapp
- Captive portal login activities: Suggests network onboarding or SIM provisioning.
- Broadcast receivers for slice purchase: Could tie into dynamic carrier billing or eSIM provisioning.
- Permissions: modify phone state, bind job service: Elevated control over network stack.  
Vector: Carrier provisioning / SIM behavior override

com.android.virtualmachine.res
- No code, AOSP tag: Placeholder or stub for virtualization.
- Permissions: debug/manage VM: Hooks into sandboxed environments—could be used for app isolation or obfuscation.  
Vector: Virtualization / sandbox manipulation

---

🛡️ System Guard / TCL Control Layer

com.tcl.guard
- Large heap + multiple system services: Indicates persistent background operation.
- Constraint proxies: Suggests conditional triggers based on battery/network state.
- Permissions: dump, dynamic receiver, online support AIDL: Potential for remote support or telemetry.
- Ambiguous legitimacy: Could be a security layer or a control mechanism.  
Vector: Telemetry / remote control / conditional execution

---

📢 Broadcast & Emergency Messaging

com.mediatek.cellbroadcastuiresoverlay
- Overlay-only: UI masking for cell broadcast—check if it suppresses or redirects alerts.
- No explicit permissions: Could piggyback on com.google.android.cellbroadcastreceiver.  
Vector: Emergency alert spoof / UI suppression

com.google.android.cellbroadcastreceiver
- Runs at boot + airplane mode exit: Persistent alert delivery.
- Permissions: read SMS, read cell broadcasts, post notifications: Expected, but high-impact.
- No battery optimization: Ensures uninterrupted operation.  
Vector: Emergency alert delivery / persistent broadcast

---

📞 Telecom Core

com.android.server.telecom
- Multiple call-related activities: Emergency, privileged, VZW-specific.
- Receivers for uninstall and broadcast: Could react to app removal or system events.
- Permissions: send SMS, read/write call logs, directly call: Full telecom stack access.  
Vector: Call manipulation / privileged dialer injection

---

🔍 General Observations
- Overlay-only packages (fota, settings, cellbroadcastuiresoverlay) are high-risk if they lack code but target critical UI components.
- Carrier and IMS packages often blur the line between legitimate provisioning and covert control.
- TCL-specific apps like guard may be legitimate but warrant byte-level inspection due to their broad permissions and ambiguous roles.

---

Want to bucket these into threat categories (e.g. Persistence, UI Spoof, SIM Control, Telemetry) or build regex triggers for detection? I can help you weaponize this into audit-ready modules.
