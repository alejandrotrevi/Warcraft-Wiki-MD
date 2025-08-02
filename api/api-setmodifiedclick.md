# API SetModifiedClick

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}

Assigns the given modifier key to the given action.

 SetModifiedClick(action, key)

==Arguments==

:;action:{{apitype|string}} - The action to set a key for. Actions defined by Blizzard: 
::AUTOLOOTTOGGLE, CHATLINK, COMPAREITEMS, DRESSUP, FOCUSCAST, OPENALLBAGS, PICKUPACTION, QUESTWATCHTOGGLE, SELFCAST, SHOWITEMFLYOUT, SOCKETITEM, SPLITSTACK, STICKYCAMERA, TOKENWATCHTOGGLE
:;key:{{apitype|string}} - The key to assign. Must be one of:
:: ALT, CTRL, SHIFT, NONE

==Details==
The game only provides user options for changing the AUTOLOOTTOGGLE, FOCUSCAST and SELFCAST modifiers. All other modifiers are set to "SHIFT" by default, except for DRESSUP and SOCKETITEM, which are set to "CTRL".

An additional modifier SHOWMULTICASTFLYOUT exists, but was only used in the shaman totem UI, which was removed from the game in [[Patch 4.0.1]].

==See also==

* {{api|IsModifiedClick}}
* {{api|SetModifiedClick}}
```