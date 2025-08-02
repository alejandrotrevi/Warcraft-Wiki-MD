# API GetMastery

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the base mastery percentage.
 mastery = GetMastery()

==Returns==
:;mastery:{{apitype|number}} - sum of player's base and rating bonus mastery.

==Details==
Mastery does not suffer diminishing returns, but the value returns by GetMastery is not, necessarily, your final Mastery value. Different classes, in different forms, can have a multiplier performed against the value returned by GetMastery.

To find your '''true''' Mastery, and the multiplier factor used to calculate it, see {{api|GetMasteryEffect}}.

==See also==
* {{api|GetMasteryEffect}}
```