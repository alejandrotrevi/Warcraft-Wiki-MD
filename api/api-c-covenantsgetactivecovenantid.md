# API C Covenants.GetActiveCovenantID

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Covenants|system=Covenant}}
Returns the CovenantID of the chosen covenant.
 covenantID = C_Covenants.GetActiveCovenantID()

==Returns==
:;covenantID:{{apitype|Enum.CovenantType}}
{{:Enum.CovenantType|nocaption=1}}

==Details==
* Only applies to joining a Covenant at maximum level or during [[The Threads of Fate]].
* Returns 0 while [[AddOn loading process|loading addons]] until info is available, before {{api|t=e|PLAYER_LOGIN}} and immediately after /reload.

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```