# API GetShapeshiftFormCooldown

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns cooldown information for a specified [[Form#Macro form numbers|form]].
 startTime, duration, isActive = GetShapeshiftFormCooldown(index)

==Arguments==
:;index:{{apitype|number}} - Index of the desired form

==Returns==
:;startTime:{{apitype|number}} - Cooldown start time (per {{api|GetTime}}) in seconds.
:;duration:{{apitype|number}} - Cooldown duration in seconds.
:;isActive:{{apitype|number}} - Returns 1 if the cooldown is running, nil if it isn't

==Example==
Displays the seconds remaining on the shapeshift form at index 1 or "Not Active" if there's no cooldown on that form
 local startTime, duration, isActive = GetShapeshiftFormCooldown(1)
 if isActive then
  print("Not Active")
 else
  print(string.format("Form 1 has %f seconds remaining", startTime + duration - GetTime()))
 end
```