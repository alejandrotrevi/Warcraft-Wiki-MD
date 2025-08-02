# API GetActionCooldown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns cooldown info for the specified action slot.
 start, duration, enable, modRate = GetActionCooldown(slot)

==Arguments==
:;slot:{{apitype|number}} - The [[ActionSlot|action slot]] to retrieve data from.

==Returns==
:;start:{{apitype|number}} - The time at which the current cooldown period began (relative to the result of [[API GetTime|GetTime]]), or 0 if the cooldown is not active or not applicable.
:;duration:{{apitype|number}} - The duration of the current cooldown period in seconds, or 0 if the cooldown is not active or not applicable.
:;enable:{{apitype|number}} - Indicate if cooldown is enabled, is greater than 0 if a cooldown ''could be'' active, and 0 if a cooldown cannot be active. This lets you know when a shapeshifting form has ended and the actual countdown has started.
:;modRate:{{apitype|number}} - The rate at which the cooldown widget's animation should be updated.

==Example==
 local start, duration, enable, modRate = GetActionCooldown(slot);
 if ( start == 0 ) then
 	-- do stuff when cooldown is not active
 else
 	-- do stuff when cooldown is under effect
 end

==Patch changes==
* {{Patch 7.1.0|note=The <code>modRate</code> return value was added.}}
* {{Patch 6.2.0|note=The <code>charges</code> and <code>maxCharges</code> return values were removed. They were moved to [[API GetActionCharges|GetActionCharges]].}}
```