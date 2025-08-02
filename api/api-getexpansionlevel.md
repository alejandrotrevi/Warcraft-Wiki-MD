# API GetExpansionLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Expansion}}
Returns the expansion level currently accessible by the player.
 expansionLevel = GetExpansionLevel()

==Returns==
:;expansionLevel:{{apitype|number}} - The newest expansion currently accessible by the player.
{{:LE_EXPANSION}}

==Details==
* Trial/Starter accounts are automatically upgraded to the second to last expansion.
* Updated after {{api|t=e|UPDATE_EXPANSION_LEVEL}} fires.

==Example==
Before and after the Shadowlands global launch at November 23 2020 at 3:00 p.m. PST. Requires the player to have pre-ordered/purchased the expansion.
<syntaxhighlight lang="lua">
/dump GetExpansionLevel() -- 7 -> 8
/dump GetAccountExpansionLevel() -- 8
/dump GetServerExpansionLevel() -- 7 -> 8
</syntaxhighlight>
This API is equivalent to
 GetExpansionLevel() == min({{api|GetAccountExpansionLevel}}(), {{api|GetServerExpansionLevel}}())

==Patch changes==
* {{Patch 3.3.0|note=Added.}}

{{apinavbox|Authoring}}
```