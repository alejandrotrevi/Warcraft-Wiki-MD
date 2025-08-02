# API GuildDisband

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Disbands the guild; no warning is given.
 GuildDisband()

==Details==
* Triggers {{api|t=e|PLAYER_GUILD_UPDATE}} if successful.
* Only available to the guild leader.
```