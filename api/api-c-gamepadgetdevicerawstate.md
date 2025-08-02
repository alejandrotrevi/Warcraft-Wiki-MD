# API C GamePad.GetDeviceRawState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GamePad|system=GamePad}}
Needs summary.
 rawState = C_GamePad.GetDeviceRawState(deviceID)

==Arguments==
:;deviceID:{{apitype|number}}

==Returns==
:;rawState:{{apitype|GamePadRawState?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| vendorID || {{apitype|number}} || 
|-
| productID || {{apitype|number}} || 
|-
| rawButtonCount || {{apitype|number}} || 
|-
| rawAxisCount || {{apitype|number}} || 
|-
| rawButtons || {{apitype|boolean[]}} || 
|-
| rawAxes || {{apitype|number[]}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}

{{apinavbox|C_GamePad}}
```