# API BuyGuildCharter

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Purchases a [[Guild Charter]].
 BuyGuildCharter(guildName)

==Arguments==
:;guildName:{{apitype|string}} - Name of the guild you wish to purchase a guild charter for.

==Example==
The following purchases a guild charter for "MC Raiders":
<syntaxhighlight lang="lua">
BuyGuildCharter("MC Raiders");
</syntaxhighlight>

==Details==
There are two preconditions to using BuyGuildCharter:
# Must be talking to a ''Guild Master'' NPC.
# Must be on the ''Purchase a Guild Charter'' screen.

==See also==
* {{api|OfferPetition}}
* {{api|TurnInGuildCharter}}
```