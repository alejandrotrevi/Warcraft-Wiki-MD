# API C PvP.GetSpecialEventDetails

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 info = C_PvP.GetSpecialEventDetails()

==Returns==
:;info:{{apitype|SpecialEventDetails?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| shortDescription || {{apitype|string}} || 
|-
| longDescription || {{apitype|string}} || 
|-
| questID || {{apitype|number?}} || 
|-
| isActive || {{apitype|boolean}} || 
|}

==Patch changes==
* {{Patch 9.1.0|note=Replaced <code>achievementID</code> field with <code>questID</code>}}
* {{Patch 8.2.5|note=Added.}}
```