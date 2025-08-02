# API GetExpertise

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the player's expertise percentage for main hand, offhand and ranged attacks.
 mainhandExpertise, offhandExpertise, rangedExpertise = GetExpertise()

==Returns==
:;mainhandExpertise:{{apitype|number}} - Expertise percentage for swings with your main hand weapon.
:;offhandExpertise:{{apitype|number}} - Expertise percentage for swings with your offhand weapon.
:;rangedExpertise:{{apitype|number}} - Expertise percentage for your ranged weapon. 

==Details==
* Expertise reduces the chance that the player's attacks are dodged or parried by an enemy. This function returns the amount of percentage points Experise reduces the dodge/parry chance by (e.g. a return value of 3.5 means a 3.5% reduction to both dodge and parry probabilities).

==Patch changes==
* {{Patch 5.0.4|note=<code>GetExpertisePercent</code> was merged into this function.}}

==See also==
* {{api|GetCombatRating}}(CR_EXPERTISE)
```