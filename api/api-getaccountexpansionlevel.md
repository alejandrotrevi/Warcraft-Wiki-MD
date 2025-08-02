# API GetAccountExpansionLevel

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Expansion}}
Returns the expansion level the account has been flagged for.
 expansionLevel = GetAccountExpansionLevel()

==Returns==
:;expansionLevel:{{apitype|number}} - The expansion the player's game license has been flagged for.
{{:LE_EXPANSION}}

==Example==
Before and after pre-ordering the Shadowlands expansion. <s>Requires a client restart to update, if still in-game.</s> No longer requires a client restart to update, if in-game.
 /dump GetAccountExpansionLevel() -- 7 -> 8

==Patch changes==
* {{Patch 2.0.1|note=Added.}}

==See also==
* {{api|GetExpansionLevel}}() - Returns the newest expansion actually available to the player.
```