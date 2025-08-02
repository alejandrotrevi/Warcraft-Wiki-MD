# API GetActionLossOfControlCooldown

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a loss-of-control cooldown affecting an action.
 start, duration = GetActionLossOfControlCooldown(slot)

==Arguments==
:;slot:{{apitype|number}} - [[ActionSlot|action slot]] to query information about.

==Returns==
:;start:{{apitype|number}} - time at which the cooldown began, per {{api|GetTime}}.
:;duration:{{apitype|number}} - duration of the cooldown in seconds; 0 if the action is not currently affected by a loss-of-control cooldown.

==Patch changes==
* {{Patch 5.1.0|note=Added.}}

==See also==
* {{api|t=w|Cooldown:SetLossOfControlCooldown}}
* {{api|t=a|C_LossOfControl.GetEventInfo}}
* {{api|t=e|LOSS_OF_CONTROL_UPDATE}}
```