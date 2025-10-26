
## 📚 Glossary  
This glossary defines all core and advanced terms used throughout the investigation.

---

### 1️⃣ Work Profile
A managed environment deployed by Mobile Device Management (MDM) systems to isolate apps and enforce policies. 

**Apple Business Manager** (ABM) — A platform for organizations to manage Apple accounts apps and devices. 

**Behavioral Tracking** — Monitoring user actions like clicks, scrolls, and navigation to build a profile or predict behavior.

**Certificates** – Digital files that prove a secure website or app is trusted and legit.

**Device Admin** — Android system role granting apps elevated control over device security policies. 

**Device Policy Controller (DPC)** — Core app that enforces MDM rules and restrictions.

Device Enrollment Program (DEP)

**Device Owner** — App with full control over the entire device, often set during initial provisioning. 

**EEM (Enterprise Endpoint Management)** – Tools that manage all types of company devices—phones, laptops, desktops—not just mobile.

**Group Policy** (Windows) — Centralized Windows configuration system that enforces restrictions. 

**Hidden Profile** — A user or system profile not visible in standard settings, usually done during device enrollment phase.

**Homoglyph Attack** — using characters that look the same as ASCII characters (but are different code points) to trick readers into misreading text or domains. (e.g. Georgian Characters, Cyrllic, Math, Full Width)

**Invisible characters** — zero-width or non-printing Unicode chars that hide inside text and change how strings are processed or displayed.

**Managed Apple ID** — An Apple account created and controlled by an organization through Apple Business Manager. 

**Microsoft Azure** — Microsoft’s cloud platform for identity, device, and policy management.

**Microsoft Entra** — Microsoft’s identity and access management suite.

**Mobile Device Management** (MDM) — Enterprise-grade control layer that can silently install apps and enforce restrictions. 

**Over-The-Air** (OTA) – Updates or setups done remotely.

**Profile Owner** — App that manages a single work profile.

**Zero-touch deployment** – Enterprise feature that allow the configuration and installation without needing to access the device physically.

---

### 2️⃣ Data Exfiltration
The unauthorized transfer of data from a device to external servers, often through hidden channels or disguised services.  

**Cache** — Temporary storage of images, stylesheets or scripts used to speed up access to websites.  

**Clipboard Access** — Ability to read copied text, including passwords and messages.  

**Cookies** — Small data files stored by websites or apps that help you stay logged in.  

**Exported Components** — App parts exposed to other apps (e.g. a broadcast receiver accessible by delcaring app + other apps).

**Firebase / Analytics SDKs** — Cloud-based channels used for silent data transmission and behavioral tracking.  

**I=** — A URL parameter, typically used to pass identity or session info. (e.g. https://example.com/click?i=abc)

**Keylogging** — Capturing user input before it’s displayed or transmitted.  

**Ports (Router)** — 65,000 logical endpoints for network communication (e.g. when you visit google website, your browser talks to Google’s server over port 443 and Port 445 is used for Windows File Sharing).

**Server Message Block v1 (SMB1)** — Legacy Windows file-sharing protocol.  

**Telemetry** — Automated reporting of device or app usage data.  

**U=** — A URL parameter often used to track or redirect users (e.g. https://website.org/login?i=session_token&u=https://website.org/account_info).

**Virtual Private Network (VPN)** — Encrypted tunnel for network traffic which goes through the VPN server instead of through your device. This hidee your real IP address, makes it look like you’re in another location, and keeps outsiders (like your ISP, Wi-Fi owner, or random peyt5 easily seeing what you doing online.

---

### 3️⃣ Telephony
The system layer that handles SIM cards, mobile networks, and call-related functions across the device. 

**Access Point Name** (APN) — The access point your phone uses to connect to mobile internet. It tells your device how to reach the carrier’s network.

**Baseband** — Low-level firmware that controls cellular radio and SIM behavior.

**Content Delivery Network** (CDN) — A network of servers that deliver content faster by storing copies closer to users. 

**DNS over HTTPS** — Encrypts DNS requests so others can’t see which websites you’re trying to visit. Uses HTTPS to hide the lookup.

**DNS over TLS** — Similar to DNS over HTTPS but uses TLS encryption. Protects DNS traffic from being read or tampered with.

**DNS Rerouting** — Silently redirecting internet traffic.

**eSIM** — Embedded SIM that replaces a physical SIM card.

**International Mobile Equiptment Identiity** (IMEI) – 15 digit,  device identification number, used for network registration and tracking.

**MAC Address Drift** — Multiple or changing MAC addresses on a single device.p

**Man-In-The-Middle (MITM)** — Intercepting and modifying traffic between devices.

**Secret Dialer Codes** – Special number sequences you type into the phone app to open hidden menus or check device info (e.g. #060)

**SIM Serial ID** – Identifier burned into the SIM card. Used by carriers to authenticate and track SIMs.

**SIM Swap** — Replacement or hijacking of a SIM to take over service.

**Spoofed APN** — A fake or altered APN that reroutes your mobile data through a malicious or unauthorized gateway.

---

### 4️⃣ Overlay & UI
Visual elements that draw over or modify the screen—used for accessibility, floating widgets, or system prompts.

**Accessibility Services** — Services designed to help users with disabilities.

**Cloaked Redirects** — Redirects that hide the true destination by masking or layering URLs. 

**Ghost Apps** — Apps that appear briefly, vanish, or run silently in the background.

**Input hijacking** – When an app secretly grabs what you type or tap.

**Overlays** — UI elements layered over real apps.

**Phishing Overlay** – A fake screen that tricks you into typing passwords or private info.

**Switch Control** — Accessibility feature allowing control of a device via external switches or adaptive devices.

**TalkBack** — Android accessibility service that provides spoken feedback.

**UI Hijack** — When an app takes over the screen or input without consent.

**WebView** — In-app browser engine that loads and executes web content.

---

### 5️⃣ Test & Debug
Developer tools and flags that expose internal system behavior, override protections, or simulate runtime conditions.  

**Android Debug Bridge (ADB)** — Tool to control a device from a computer.

**Developer Options** — Hidden settings that allow debugging, mock locations, and system tweaks.

**EduPrint** (Windows) — Windows print service component.

**Hidden Activities** — App screens not visible in the launcher but still active.

**Logcat** — A system tool that displays logs from apps and the operating system, including crash reports and background activity. 

**PowerShell** (Windows) — Command-line and scripting tool with deep system access.

**PowerShell ISE** (Windows) — Integrated Scripting Environment for writing, testing, and debugging PowerShell scripts.

**Runtime** — The environment in which code is executed, including system libraries and permissions.

**Software Development Kit (SDK)** — Collection of tools, libraries, and documentation for building apps.

**Task Scheduler** (Windows) — A Windows tool that runs automated tasks at set times or events such as launching a script at startup. 

---

### 6️⃣ Persistence
Techniques that keep malicious components active across reboots, updates, or app reinstalls.  

**BIOS (Basic Input/Output System)** – The older startup system that wakes up your computer and gets it ready to run. It checks hardware and starts the operating system.

**Deny Only** (Windows) - Account shows in a security group (like Administrators) but its rights are stripped; the group can block access but can’t grant privileges.

**Exported Components** — App parts exposed to other apps; can allow external control.

**Google API** — Tools and services from Google that apps use to access things like maps, login, or cloud storage.

**Intel Management Engine** (Intel ME) — A hidden subsystem in Intel hardware that runs independently and  perform remote management tasks even when the device is powered off.

**Job scheduler abuse** – When apps misuse the job scheduler to keep running in the background or avoid being shut down.

**Kernel** — Core of the operating system that manages hardware and system resources.

**Manifest Drift** — When an app’s declared behavior changes after install (e.g. app that didn’t request location access during install starts accessing GPS after an update).

**Obfuscation** — Technique to hide or disguise code, URLs, or app behavior.

**Payload** — The actual malicious code or exploit delivered to a device. Can be embedded in ads, redirects, or app components.

**Registry** (Windows) = Internal database that stores system, user, and application settings as keys and values, controlling how the OS and software behave.

**Rootkit** – Malware that hides deep in a system to secretly control it without being discovered.

**UEFI (Unified Extensible Firmware Interface)** – The modern startup system that loads before your operating system. It replaces older BIOS and supports faster booting and better security.

**W^X Policy** — Memory must be either writable or executable—never both.

**W^X Violation** — Occurs when memory is both writable and executable, allowing direct code injection and execution, enabling remote access and privilege escalation.

---

### 📱 Android App Anatomy

**Advertisement ID** – User-resettable ID used for ad tracking. 

**Android Manifest** — The app’s blueprint. Declares components, permissions, features, and behavior.

**APK (Android Package)** — The installable app file that contains code, resources, and a manifest.

**Components** — The building blocks of an app: Activities, Services, Broadcast Receivers, and Content Providers.

**Intents** — Signals that apps send to the system or other apps to trigger actions (e.g. opening a file, starting a service, or launching a screen).

**Metadata** — Extra information embedded in an app or manifest, such as version number, SDK target, or analytics tags. Used for configuration, tracking, or system behavior.

**Package Installer** — The system tool that installs, updates, and removes APKs.

**Permissions** — Rules that define what an app is allowed to access (e.g. camera, SIM info, storage).

> **Custom Permissions** — App-defined permissions that grant access to internal features or data.

> **Dangerous Permission** – Grants access to sensitive data or controls (e.g. camera, contacts, location). Requires explicit user approval at runtime.

> **Normal Permission** – Grants access to low-risk features (e.g. internet, vibration). Automatically approved at install time.

> **Signature Permissions** — Permissions that can only be granted to apps signed with the same certificate as the OS or another trusted app.  (e.g. Gboard has a android.permission.BIND_INPUT_METHOD which allows Gboard to act as the virtual keyboard preloaded as its signed with same key as the OS).

> **System Permissions** — High-level permissions reserved for system apps or firmware (e.g. modify system settings).

**Providers (Content Providers)** — Components that manage structured data and allow sharing between apps.

**Queries** — Declarations that let an app find out what other apps are installed (e.g. a launcher querying for apps that support sharing images).

**Services** — Background tasks that run without user interaction (e.g. a music player continuing playback while the app is closed).

**Features** — Hardware or software capabilities declared in the manifest (e.g. camera, Bluetooth, touchscreen).

---

### 🔤 Character Encoding & Visual Spoofing

**ASCII** — Character set with 128 symbols for English letters, digits, punctuation, and control codes (e.g. A, 7, !, /)

**Byte types** - Categories of bytes based on their role or interpretation in data.

> **Single Byte** → 1 byte, represents ASCII chars (e.g., 0x41 → 'A'), 

> **Leading Byte** → first byte in a multi-byte encoding (e.g., 0xC3 in 'é' UTF-8 0xC3 0xA9)

> **Continuation Byte** → follow-up bytes in a multi-byte sequence (e.g., 0xA9 in 'é')

> **Control Byte** → bytes representing control signals, not printable characters (e.g., 0x00 NUL, 0x0A LF)

**Code Point** — A Unicode-assigned number for each character, starting from U+0000 (e.g. U+0042 = B, U+00A9 = ©).

**Confusables** — Characters from different scripts that look nearly identical (e.g. Latin b = U+0062, Cyrillic Ь = U+042C)

**Cyrillic Script** — Used in Russian and other Eastern European languages.  Characters resemble Latin.

**Glyphs** — Visual shape of a character, which may differ across fonts or styles.  

**Latin Script** — Writing system used in English and most Western languages. 

**Lookalikes** — Characters that appear similar but are encoded differently (e.g. B vs Β, I vs I).

**Punycode** – An encoding that converts Unicode domain names containing non-ASCII characters into a format usable by the DNS system, which only supports ASCII. This enables internationalized domain names (IDNs) to resolve correctly and show the encoded version. (e.g. a spoofed domain like “ɡithub.com”, with a small letter 'ɡ') becomes `xn--ithub-vkc.com`, which visually mimics but does not resolve to github.com.

**Unicode** — Universal encoding system for 149,000 characters across all languages (e.g. U+0062 = B, U+3B2 = β).

**UTF-8 (Dec)** — Decimal values of UTF-8 encoded bytes (e.g. B = 66, © = 194 196).

**UTF-8 (Hex)** — Hexadecimal values of UTF-8 encoded bytes.  (e.g. B = 0x42, © = 0xC2 0xA9).

**--vkc** – Encoded suffix generated by the Punycode algorithm to represent specific Unicode characters from the original domain (e.g., 'ɡ' in “ɡithub.com”).

**xn--** – Prefix indicating a domain name has been Punycode-encoded to support non-ASCII Unicode characters in DNS (e.g. **xn**---ithub-**vkc**).

--- 

## 🌐 Networking Concepts

**IP Address** — A number that identifies a device on a network and tells other devices where to send data. There are public IPs and private IPs.  

**Public IP** (72.21.184.64) are assigned by your Internet Provider and used to communicate with devices outside your local network while **Private IP** (192.168.1.0) are assigned by your router for use internally. 

**DNS (Domain Name System)** – The naming system that translates human-readable domain names (like github.com) into IP addresses (like 140.82.112.0) so devices can locate and communicate with each other across the internet.

**DNS Resolver** - The specific server or service that all  domain lookups on your device get routed through (e.g. 1.1.1.1 for Cloudflare).

**Open System Interconnection** (OSI) — Framework that breaks down how data moves across a network (router, modem) into 7 distinct layers. Those layers are:

> **Layer 1 (Physical)** — The literal hardware layer of your network box.

> **Layer 2 (Data Link)** — Moves data between devices on the same local network using MAC addresses.

    **Layer 2 Bleeding** — An issue where data meant for one local segment (like your home Wi-Fi) leaks into another (like a neighbor’s), often due to bad setup or spoofed device IDs.

> **Layer 3 (Network)** — Decides where data should go across different networks using IP addresses.

> **Layer 4 (Transport)** — Makes sure data gets delivered properly, using ports.

> **Layer 5 (Session)** — Starts and manages conversations between devices, keeping track of who’s talking to whom.

> **Layer 6 (Presentation)** — Prepares data so both sides understand it—like translating, encrypting, or compressing files.

> **Layer 7 (Application)** — The layer users interact with directly. Services like websites, email, and messaging live here.

    **Cross-Layer Bleeding** – Unintended exposure or leakage of data, control across OSI layers 3 to 7. Often caused by misconfigured routing, NAT overlap, DPI failure, or protocol tunneling. 

**MAC Address** — A unique hardware ID for a device’s network adapter, used to identify devices on a local network.  

**Modem** — A device that connects your home or office to the internet by translating signals from your provider into usable data.

**Ports** — Logical endpoints used to send and receive data between devices and applications.

**Protocol** — A set of agreed rules that devices follow to exchange data properly.

**Router** — A device that shares your internet connection with multiple devices and directs traffic to the right destination.