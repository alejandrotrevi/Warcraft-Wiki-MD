# API GetAddOnEnableState

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.0|removed=11.0.2}}
Get the enabled state of an addon for a character
 enabledState = GetAddOnEnableState([character], name)

==Arguments==
:;character:{{apitype|string?}} - The name of the character to check against or nil.
{{:AddOnInfo}}

==Returns==
:;enabledState:{{apitype|number}} - The enabled state of the addon.
:: 0 - disabled
:: 1 - enabled for some
:: 2 - enabled

==Details==
* This is primarily used by the default UI to set the checkbox state in the AddOnList
* A return of 1 is only possible if character is nil

==Patch changes==
* {{Patch 10.2.0|note=Deprecated; function moved to {{api|C_AddOns.GetAddOnEnableState}} with parameter order swapped.}}

{{apinavbox|AddOn}}
```