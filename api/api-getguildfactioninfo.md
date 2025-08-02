# API GetGuildFactionInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns the guild name and faction standing of the player.
 guildName, description, standingID, barMin, barMax, barValue = GetGuildFactionInfo()

==Parameters==

===Returns===
:;guildName:{{apitype|string}} - The name of the guild the unit is in or the localized word of "Guild"
:;description:{{apitype|string}} - A localized faction description.
:;standingID:{{apitype|number}} - players faction standing (see [[StandingId]])
:;barMin:{{apitype|number}}
:;barMax:{{apitype|number}}
:;barValue:{{apitype|number}}
```