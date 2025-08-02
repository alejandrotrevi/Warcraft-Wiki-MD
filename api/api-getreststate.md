# API GetRestState

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns if the character is in a [[Rest|rested]] or normal state.
 exhaustionID, name, factor = GetRestState()

==Returns==
:;exhaustionID:{{apitype|number}} - Rest state index; observed values are '''1''' if the player is "Rested", '''2''' if the player is in a normal state.
:;name:{{apitype|string}} - Name of the current rest state; observed: "Rested" or "Normal".
:;factor:{{apitype|number}} - XP multiplier applied to experience gain from killing monsters in the current rest state.

==Example==
 rested = GetRestState();
 if rested == 1 then
  print("You're rested. Now's the time to maximize experience gain!");
 elseif rested == 2 then
  print("You're not rested. Find an inn and camp for the night?");
 else
  print("You've discovered a hitherto unknown rest state. Would you like some coffee?")
 end
```