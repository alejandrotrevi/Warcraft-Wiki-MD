# API GetGuildLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the level of your guild.
 guildLevel, maxGuildLevel = GetGuildLevel()

==Returns==
:;guildLevel:{{apitype|number}} - Level of the player's current guild.
:;maxGuildLevel:{{apitype|number}} - Maximum possible guild level.

==Patch changes==
* {{Patch 5.0.4|note=Added <code>maxGuildLevel</code> return value, replacing the previously-existing <code>MAX_GUILD_LEVEL</code> FrameXML constant.}}
* {{Patch 4.0.1|note=Added.}}

==See also==
* {{api|GetInspectGuildInfo}}
```