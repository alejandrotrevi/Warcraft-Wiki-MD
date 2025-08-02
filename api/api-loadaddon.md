# API LoadAddOn

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Loads the specified LoadOnDemand addon.
 loaded, reason = LoadAddOn(name)

==Arguments==
{{:AddOnInfo}}

==Returns==
:;loaded:{{apitype|boolean}} - If the AddOn is succesfully loaded or was already loaded.
:;reason:{{apitype|string?}} - Locale-independent reason why the AddOn could not be loaded e.g. <code>"DISABLED"</code>, otherwise returns <code>nil</code> if the addon was loaded.

==Details==
* Requires the addon to have the [[TOC_format#LoadOnDemand|LoadOnDemand]] TOC field specified.
 ## LoadOnDemand: 1
* LoadOnDemand addons are useful for reducing loading screen times by loading only when necessary, like with the different DeadlyBossMods addons/submodules.
{| {{apitable}}
{{apirow | Related Events | {{api|t=e|ADDON_LOADED}} }}
|}

===Reasons===
These have corresponding globalstrings when prefixed with <code>"ADDON_"</code><sup>[https://www.townlong-yak.com/framexml/9.1.0/GlobalStrings.lua#538]</sup>
<syntaxhighlight lang="lua">
ADDON_BANNED = "Banned" -- Addon is banned by the client
ADDON_CORRUPT = "Corrupt" -- The addon's file(s) are corrupt
ADDON_DEMAND_LOADED = "Only loadable on demand"
ADDON_DISABLED = "Disabled" -- Addon is disabled on the character select screen
ADDON_INCOMPATIBLE = "Incompatible" -- The addon is not compatible with the current TOC version
ADDON_INSECURE = "Insecure"
ADDON_INTERFACE_VERSION = "Out of date"
ADDON_MISSING = "Missing" -- The addon is physically not there
ADDON_NOT_AVAILABLE = "Not Available"
ADDON_UNKNOWN_ERROR = "Unknown load problem"

ADDON_DEP_BANNED = "Dependency banned" -- Addon's dependency is banned by the client
ADDON_DEP_CORRUPT = "Dependency corrupt" -- The addon's dependency cannot load because its file(s) are corrupt
ADDON_DEP_DEMAND_LOADED = "Dependency only loadable on demand"
ADDON_DEP_DISABLED = "Dependency disabled" -- The addon cannot load without its dependency enabled
ADDON_DEP_INCOMPATIBLE = "Dependency incompatible" -- The addon cannot load if its dependency cannot load
ADDON_DEP_INSECURE = "Dependency insecure"
ADDON_DEP_INTERFACE_VERSION = "Dependency out of date"
ADDON_DEP_MISSING = "Dependency missing" -- The addon's dependency is physically not there
</syntaxhighlight>

===Example===
* Attempts to load a LoadOnDemand addon. If the addon is disabled, it will try to enable it first.
<syntaxhighlight lang="lua">
local function TryLoadAddOn(name)
	local loaded, reason = LoadAddOn(name)
	if not loaded then
		if reason == "DISABLED" then
			EnableAddOn(name, true) -- enable for all characters on the realm
			LoadAddOn(name)
		else
			local failed_msg = format("%s - %s", reason, _G["ADDON_"..reason])
			error(ADDON_LOAD_FAILED:format(name, failed_msg))
		end
	end
end

TryLoadAddOn("SomeAddOn")
-- Couldn't load SomeAddOn: MISSING - Missing
</syntaxhighlight>

* Manually loads and shows the Blizzard Achievement UI addon.
 /run LoadAddOn("Blizzard_AchievementUI"); AchievementFrame_ToggleAchievementFrame();

==Patch changes==
* {{Patch 1.8.0|note=Prior to the 1.8 patch, this could be used to load addons which were not on-demand if they were disabled at start up and then enabled during the play session. The 1.8 patch restricted this to ONLY addons which are truly marked on demand in their .toc files with <code>## LoadOnDemand: 1</code>}}

==See also==
* {{api|IsAddOnLoaded}}()
* {{api|UIParentLoadAddOn}}()

{{apinavbox|AddOn}}
```