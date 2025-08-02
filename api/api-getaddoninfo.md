# API GetAddOnInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Get information about an AddOn.
 name, title, notes, loadable, reason, security, newVersion = GetAddOnInfo(name)

==Arguments==
{{:AddOnInfo}}

==Returns==
:;name:{{apitype|string}} - The name of the AddOn (the folder name).
:;title:{{apitype|string}} - The title of the AddOn as listed in the .toc file (presumably this is the appropriate localized one).
:;notes:{{apitype|string}} - The notes about the AddOn from its .toc file (presumably this is the appropriate localized one).
:;loadable:{{apitype|boolean}} - Indicates if the AddOn is loaded or eligible to be loaded, true if it is, false if it is not.
:;reason:{{apitype|string}} - The reason why the AddOn cannot be loaded. This is nil if the addon is loadable, otherwise it contains a string token indicating the reason that can be localized by prepending "ADDON_". ("BANNED", "CORRUPT", "DEMAND_LOADED", "DISABLED", "INCOMPATIBLE", "INTERFACE_VERSION", "MISSING")
:;security:{{apitype|string}} - Indicates the security status of the AddOn. This is currently "INSECURE" for all user provided addons, "SECURE_PROTECTED" for [[TOC format#Restricted|guarded]] Blizzard addons, and "SECURE" for all other Blizzard AddOns.
:;newVersion:{{apitype|boolean}} - Not currently used.

==Details==
* If the function is passed a string, ''name'' will always be the value passed, so check if ''reason'' equals "MISSING" to find out if an addon exists.
* If the function is passed a number that is out of range, you will get an error message, specifically <code>[<file name>]:<line number> AddOn index must be in the range of 1 to <GetNumAddOns()></code>

==Patch changes==
* {{Patch 10.1.0|note=Added "SECURE_PROTECTED" security level for guarded addons.}}
* {{Patch 6.0.2|note=Removed <code>enabled</code> return. The <code>loadable</code> return was changed from a flag to a boolean. Added <code>newVersion</code> return. The enabled state of an addon can now be queried with {{api|GetAddOnEnableState}}.}}

{{apinavbox|AddOn}}
```