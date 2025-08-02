# API GetSheathState

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns which type of weapon the player currently has unsheathed.
 sheathState = GetSheathState()

==Returns==
:;sheathState:{{apitype|number}} - Currently unsheathed weapon type:
{| class="darktable zebra col1-center" style="margin-left: 3.9em"
! Value !! Weapon
|-
| 1 || None || 
|-
| 2 || Melee || 
|-
| 3 || Ranged || 
|}

==Patch changes==
* {{Patch 4.3.0|note=Added.}}

==See also==
* {{api|ToggleSheath}}
```