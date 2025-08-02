# API C AddOns.GetAddOnInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=AddOns}}
Needs summary.
 name, title, notes, loadable, reason, security, updateAvailable = C_AddOns.GetAddOnInfo(name)

==Arguments==
:;name:{{apitype|uiAddon}} - The name of the addon to be queried, or an index from 1 to {{api|C_AddOns.GetNumAddOns}}. The state of Blizzard addons can only be queried by name.

==Returns==
:;name:{{apitype|string}} - The name of the AddOn (the folder name).
:;title:{{apitype|string}} - The localized title of the AddOn as listed in the .toc file.
:;notes:{{apitype|string}} - The localized notes about the AddOn from its .toc file.
:;loadable:{{apitype|boolean}} - Indicates if the AddOn is loaded or eligible to be loaded on this or another character, true if it is, false if it is not.
:;reason:{{apitype|string}} - The reason why the AddOn cannot be loaded. This is nil if the addon is loadable, otherwise it contains a string token indicating the reason that can be localized by prepending "ADDON_".
:;security:{{apitype|string}} - Indicates the security status of the AddOn. This is currently "INSECURE" for all user provided addons, "SECURE_PROTECTED" for guarded Blizzard addons, and "SECURE" for all other Blizzard AddOns.
:;updateAvailable:{{apitype|boolean}} - Not currently used.

==Details==
* A full list of all reason codes can be found below.
{| class="darktable zebra"
! Reason !! Message
|-
| <code>BANNED</code> || Banned
|-
| <code>CORRUPT</code> || Corrupt
|-
| <code>DEMAND_LOADED</code> || Only loadable on demand
|-
| <code>DEP_BANNED</code> || Dependency banned
|-
| <code>DEP_CORRUPT</code> || Dependency corrupt
|-
| <code>DEP_DEMAND_LOADED</code> || Dependency only loadable on demand
|-
| <code>DEP_DISABLED</code> || Dependency disabled
|-
| <code>DEP_EXCLUDED_FROM_BUILD</code> || Dependency excluded from build
|-
| <code>DEP_INCOMPATIBLE</code> || Dependency incompatible
|-
| <code>DEP_INSECURE</code> || Dependency insecure
|-
| <code>DEP_INTERFACE_VERSION</code> || Dependency out of date
|-
| <code>DEP_MISSING</code> || Dependency missing
|-
| <code>DEP_NOT_AVAILABLE</code> || Dependency not available
|-
| <code>DEP_NO_ACTIVE_INTERFACE</code> || Dependency has no active UI
|-
| <code>DEP_USER_ADDONS_DISABLED</code> || Dependency user addons disabled
|-
| <code>DEP_WRONG_ACTIVE_INTERFACE</code> || Dependency has wrong active UI
|-
| <code>DEP_WRONG_GAME_TYPE</code> || Dependency has wrong game type
|-
| <code>DEP_WRONG_LOAD_PHASE</code> || Dependency has wrong load phase
|-
| <code>DISABLED</code> || Disabled
|-
| <code>EXCLUDED_FROM_BUILD</code> || Excluded from build
|-
| <code>INCOMPATIBLE</code> || Incompatible
|-
| <code>INSECURE</code> || Insecure
|-
| <code>INTERFACE_VERSION</code> || Out of date
|-
| <code>MISSING</code> || Missing
|-
| <code>NOT_AVAILABLE</code> || Not Available
|-
| <code>NO_ACTIVE_INTERFACE</code> || No active UI
|-
| <code>UNKNOWN_ERROR</code> || Unknown load problem
|-
| <code>USER_ADDONS_DISABLED</code> || User addons disabled
|-
| <code>WRONG_ACTIVE_INTERFACE</code> || Wrong active UI
|-
| <code>WRONG_GAME_TYPE</code> || Wrong game type
|-
| <code>WRONG_LOAD_PHASE</code> || Wrong load phase
|}
```