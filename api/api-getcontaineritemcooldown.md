# API GetContainerItemCooldown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns cooldown information for an item in your inventory
 startTime, duration, isEnabled = GetContainerItemCooldown(bagID, slot)

==Parameters==
===Arguments===
:(bagID, slot)

:;[[bagID]]:{{apitype|number}} - number of the bag the item is in, 0 is your backpack, 1-4 are the four additional bags
:;slot:{{apitype|number}} - slot number of the bag item you want the info for.

===Returns===
:startTime, duration, isEnabled  <!-- remove this line if it's just one value -->

:;start:the time the cooldown period began
:;duration:the duration of the cooldown period
:;enabled:1 if the item has a cooldown, 0 otherwise
```