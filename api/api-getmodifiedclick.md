# API GetModifiedClick

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}

Returns the modifier key assigned to the given action.

 key = GetModifiedClick(action)

==Arguments==

:;action:{{apitype|string}} - The action to query. Actions defined by Blizzard: 
::AUTOLOOTTOGGLE, CHATLINK, COMPAREITEMS, DRESSUP, FOCUSCAST, OPENALLBAGS, PICKUPACTION, QUESTWATCHTOGGLE, SELFCAST, SHOWITEMFLYOUT, SOCKETITEM, SPLITSTACK, STICKYCAMERA, TOKENWATCHTOGGLE

==Returns==

:;key:{{apitype|string}} - The modifier key assigned to this action. May be one of:
:: ALT, CTRL, SHIFT, NONE

==See also==

* {{api|IsModifiedClick}}
* {{api|SetModifiedClick}}
```