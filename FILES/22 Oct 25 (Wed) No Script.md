
12:39:59 added Ext settings link moz-extension://b84b89cd-56f0-4f74-92fd-c5cde141733a/ui/options.html#;tab-main-tabs=0 

13:09:42 added code point/dec info about section sign 00A7/167 and yo ying 0E22/3618 


## 411
- NoScript config file very wonky. 

## App

No Script 13.2.2 Browser Extension
**Firefox Beta** 
144.0b9 (Build #2016118122), c836eb5e51e62fd615604606bd50600b5623410b
GV: 144.0-20251003090815
AS: 144.0.1
OS: Android 11


## links involved
1. `moz-extension://b84b89cd-56f0-4f74-92fd-c5cde141733a/ui/options.html#;tab-main-tabs=0`
extension settings page

2. `https://noscript.net/getit/`
no script download page 

3. `https://addons.mozilla.org/en-CA/android/addon/noscript/`
add on page

## category

- [x] u see

---

## notes

I saw many descrepncies in what i had in the No Script extension interface and what was actually happening.

- "Show Full Addresses" (a\https/:website.com) option enabled but domains appearing as "...website.com" in the settings.
- inability to reset the "any page" option which kept auto changing to include "script.

### No Script Configs
NoScript blocks scripts and active content with percision. You csn 

**script** - JavaScript, e.g. `<script>` tags - **can initiate code**

**object** - plugin objects (usually Flash, Java applets, Silverlight, etc) - **oldschool vector**

**media** - HTML5 audio/video

**frame** - subdocuments, e.g. `<frame>` and `<iframe>` - **can track, run overlays**

**font** - remote fonts - **can track you**

**webgl** - WebGL - **fingerprint from multiple sites**

**fetch** - whether other sites can make `XMLHttpRequest` (sometimes abbreviated as "XHR") and Fetch request to this site - **allows bg requests for API (asks server for data)**

**ping** - destination of navigator. sendBeacon and hyperlink ping attribute - **nortifies of clicked links**

**noscript** - whether to show the contents of `<noscript>` elements where NoScript blocks scripts (which can happen either by disabling "script" permission for the site, or having "Any capability blocked in the top document must be blocked in its subdocuments too".

"**lazy load**" - when disabled for a site, NoScript will prevent webpages served by that site from using scriptless lazy loading for any subresources (loading="lazy" attribute will be changed to loading="eager") - **allows wait until all scripts load.**

"**unrestricted CSS**" - when disabled for a site, NoScript mitigates pure-CSS exploits (e.g. CSS PP0) on pages served by that site. 

**LAN** - whether this site is allowed to make requests to resources on your local network, e.g. localhost or private IP addresses, when this site is not itself hosted on your local network.

**Web Assembly** (wasm) - binary code, designed for speed - **cyrptoming, hidden computations. Unreadable** 

#### Trust Levels
There are 4 Trust Levels, Default, Trusted, Untrusted and Custom 

Default - What non configured websites can use.

Trusted - Permamently allows chosen scripts and content you choose.

Trusted Temp - Trusted capabilities for that session. These reset when you close browser.

Untrusted - Websites you choose can be blocked of all capabilites.

Custom - special level which can be tailored specifically for each site by turning on and off individual capabilities, 

Contextual - lets you set different permissions fora site based on where its loaded.

--- 

#### Reset NoScript
I reset NoScript and then exported log.

`moz-extension://b84b89cd-56f0-4f74-92fd-c5cde141733a/ui/options.html#;tab-main-tabs=0`

```

{
"policy":{
"DEFAULT":{
"capabilities":[
"frame",
"fetch",
"noscript",
"other"
],
"temp":false
},
"TRUSTED":{
"capabilities":[
"script",
"object",
"media",
"frame",
"font",
"wasm",
"webgl",
"fetch",
"ping",
"noscript",
"lazy_load",
"unchecked_css",
"lan",
"other"
],
"temp":false
},
"UNTRUSTED":{
"capabilities":[],
"temp":false
},
"sites":{
"trusted":[
"§:addons.mozilla.org",
"§:afx.ms",
"§:ajax.aspnetcdn.com",
"§:ajax.googleapis.com",
"§:bootstrapcdn.com",
"§:code.jquery.com",
"§:firstdata.com",
"§:firstdata.lv",
"§:gfx.ms",
"§:google.com",
"§:googlevideo.com",
"§:gstatic.com",
"§:hotmail.com",
"§:live.com",
"§live.net",
"§:maps.googleapis.com",
"§:mozilla.net",
"§:netflix.com",
"§:nflxext.com",
"§:nflximg.com",
"§:nflxvideo.net",
"§:noscript.net",
"§:outlook.com",
"§:passport.com",
"§:passport.net",
"§:passportimages.com",
"§:paypal.com",
"§:paypalobjects.com",
"§:securecode.com",
"§:securesuite.net",
"§:sfx.ms",
"§:tinymce.cachefly.net",
"§:wlxrs.com",
"§:yahoo.com",
"§:yahooapis.com",
"§:yimg.com",
"§:youtube.com",
"§:ytimg.com"
],
"untrusted":[],
"custom":{}
},
"enforced":true,
"autoAllowTop":false
},
"local":{
"debug":false,
"showCtxMenuItem":true,
"showCountBadge":true,
"showFullAddresses":false,
"showProbePlaceholders":true,
"amnesticUpdates":false
},
"sync":{
"global":false,
"xss":true,
"TabGuardMode":"incognito",
"TabGuardPrompt":"post",
"cascadeRestrictions":false,
"overrideTorBrowserPolicy":false
},
"xssUserChoices":{}
}
```
 
 - Those domains were the defaults shown 
#### "§:" preamble: 
section sign (u+00a7 dec 167)

Drift character.

#### "§:hotmail.com", "§:live.com"
the ":" makes the entire scheme invalid.

#### "showFullAddresses: false"
while UI has this option (show \"https\:website.com" instead of "...website.com") as enabled.

#### TabGuardPrompt:post
shows me popup warning after suspicious post is caught not before.

#### Enforced:true
locks down UI. Cant make changes.

---

### Custom Capabilites
When i entered in a domain with caveots.

```
"custom":{
"ยง:reddit.com":{
"capabilities":[],
"contextual":{
"ยง:reddit.com":{
"capabilities":[
"script",
"fetch",
"lazy_load"
],
"temp":false
}
},
"temp":false
},
"ยง:obsidian.md":{
"capabilities":[
"noscript",
"media",
"font"
],
"contextual":{
"ยง:obsidian.md":{
"capabilities":[
"noscript",
"media",
"font",
"script",
"frame",
"fetch"
],
"temp":false
}
```

in this example, i have obsidian.md as the domain with noscript, media, font, script, frame and fetch.
#### ยง:obsidian.md**
thai chracter yo ying (u+0e22 dec 3618)

At the beginning of both the custom and contextual, that yo ying character pops up. 

now regsters as an unknown namespace or makes new key string that NS wouldnt follow? 

--- 

**Conclsion**: regardless of chosen permissions, both drift characters cause the domain listed to be invalid.