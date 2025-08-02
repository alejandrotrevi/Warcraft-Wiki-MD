# API GetMultiCastTotemSpells

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns a list of valid spells for a totem bar slot.
 totem1, totem2, totem3, totem4, totem5, totem6, totem7 = GetMultiCastTotemSpells(slot)

==Arguments==
:;slot:{{apitype|number}} - The totem bar slot number:
{| class="darktable" style="margin-left: 3.9em"
|
Call of the Elements
* 133 - Fire
* 134 - Earth
* 135 - Water
* 136 - Air

Call of the Ancestors
* 137 - Fire
* 138 - Earth
* 139 - Water
* 140 - Air

Call of the Spirits
* 141 - Fire
* 142 - Earth
* 143 - Water
* 144 - Air
|}

==Returns==
:;totem1:{{apitype|number}} - The spell Id of the first valid spell for the slot
:;totem2:{{apitype|number}} - The spell Id of the second valid spell for the slot
:;totem3:{{apitype|number}} - The spell Id of the third valid spell for the slot
:;totem4:{{apitype|number}} - The spell Id of the fourth valid spell for the slot
:;totem5:{{apitype|number}} - The spell Id of the fifth valid spell for the slot
:;totem6:{{apitype|number}} - The spell Id of the sixth valid spell for the slot
:;totem7:{{apitype|number}} - The spell Id of the seventh valid spell for the slot

==Example==
 totem1, totem2, totem3, totem4, totem5, totem6, totem7 = GetMultiCastTotemSpells(134)

===Result===
A list of spell ids that can go in totem bar slot number 134.  Slot 134 is the Earth slot for the Call of the Elements spell.
```