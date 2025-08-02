# API GetNumClasses

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of player classes in the game.
 numClasses = GetNumClasses()

==Returns==
:;numClasses:{{apitype|number}}

==Details==
* {{Wow-inline}} In Classic, this function does ''not'' return the highest class ID, unlike in Retail. This behaviour has changed over time, so it may be unwise to rely on the current behaviour in Classic staying the same.

==Patch changes==
* {{Patch 5.0.4|note=Added.}}

{{apinavbox|Class}}
```