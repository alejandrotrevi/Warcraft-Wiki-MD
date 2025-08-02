# API C LossOfControl.GetEventInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns information about a loss-of-control event.
 locType, spellID, text, iconTexture, startTime, timeRemaining, duration, lockoutSchool, priority, displayType = C_LossOfControl.GetEventInfo(eventIndex)

==Arguments==
:;eventIndex:{{apitype|number}} - index of the loss-of-control effect currently affecting your character to return information about, ascending from 1.

==Returns==
:;locType:{{apitype|string}} - Effect type, e.g. "SCHOOL_INTERRUPT"
:;spellID:{{apitype|number}} - Spell ID causing the effect, e.g. 33786 for Cyclone.
:;text:{{apitype|string}} - Name of the effect, e.g. "Interrupted".
:;iconTexture:{{apitype|string}} - Effect icon texture.
:;startTime:{{apitype|number}} - Time at which this effect began, as per {{api|GetTime}}()
:;timeRemaining:{{apitype|number}} - Number of seconds remaining.
:;duration:{{apitype|number}} - Duration of the effect, in seconds.
:;lockoutSchool:{{apitype|number}} - Locked out spell school identifier; can be used as index into the global <code>SchoolStringTable</code> to retrieve school name.
:;priority:{{apitype|number}} - ?
:;displayType:{{apitype|number}} - An integer specifying how this event should be displayed to the player, per the Interface-configured options:
:* 0: the effect should not be displayed.
:* 1: the effect should be displayed as a brief alert when it occurs.
:* 2: the effect should be displayed for its full duration.

==Patch changes==
* {{Patch 9.0.1|note=Removed. Replaced by {{api|C_LossOfControl.GetActiveLossOfControlData}}.}}
* {{Patch 5.1.0|note=Added.}}

==See also==
* {{api|t=e|LOSS_OF_CONTROL_ADDED}}
* {{api|t=e|LOSS_OF_CONTROL_UPDATE}}
* {{api|C_LossOfControl.GetNumEvents}}
```