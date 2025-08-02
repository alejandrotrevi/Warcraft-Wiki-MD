# API C AddOns.GetAddOnEnableState

**Contributor:** Ghostopheles

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AddOns|system=System}}
Queries the enabled state of an addon, optionally for a specific character.
 state = C_AddOns.GetAddOnEnableState(name [, character])

==Arguments==
:;name:{{apitype|uiAddon}} - The name of the addon to be queried, or an index from 1 to {{api|C_AddOns.GetNumAddOns}}. The state of Blizzard addons can only be queried by name.
:;character:{{apitype|string?}} - The name or [[GUID]] of the character to check against, or omitted/<code>nil</code> for all characters

==Returns==
:;state:{{apitype|Enum.AddOnEnableState}} - The enabled state of the addon.
{| class="sortable darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Field !! Description
|-
| 0 || None || Disabled
|-
| 1 || Some || Enabled for some characters; this is only possible if <code>character</code> is nil.
|-
| 2 || All || Enabled
|}

==Patch changes==
* {{Patch 10.2.0|note=Added.}}

{{apinavbox|AddOn}}
```