# API C GamePad.GetDeviceMappedState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GamePad|system=GamePad}}
Needs summary.
 state = C_GamePad.GetDeviceMappedState([deviceID])

==Arguments==
:;deviceID:{{apitype|number?}}

==Returns==
:;state:{{apitype|GamePadMappedState?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| name || {{apitype|string}} || 
|-
| labelStyle || {{apitype|string}} || 
|-
| buttonCount || {{apitype|number}} || 
|-
| axisCount || {{apitype|number}} || 
|-
| stickCount || {{apitype|number}} || 
|-
| buttons || {{apitype|boolean[]}} || 
|-
| axes || {{apitype|number[]}} || 
|-
| sticks || {{apitype|GamePadStick[]}} || 
|}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ GamePadStick
! Field !! Type !! Description
|-
| x || {{apitype|number}} || 
|-
| y || {{apitype|number}} || 
|-
| len || {{apitype|number}} || 
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}

{{apinavbox|C_GamePad}}
```