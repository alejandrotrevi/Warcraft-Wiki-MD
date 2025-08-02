# API IsInGuild

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Lets you know whether you are in a guild.
 inGuild = IsInGuild()

==Returns==
:;inGuild:{{apitype|boolean}}

==Example==
 if IsInGuild() then
     SendChatMessage("Hi Guild!", "GUILD")
 end
```