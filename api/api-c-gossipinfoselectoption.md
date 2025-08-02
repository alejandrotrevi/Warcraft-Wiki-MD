# API C GossipInfo.SelectOption

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Selects a gossip (conversation) option.
 C_GossipInfo.SelectOption(optionID [, text, confirmed])

==Arguments==
:;optionID:{{apitype|number}} - <code>gossipOptionID</code> from {{api|C_GossipInfo.GetOptions}}()
:;text:{{apitype|string?}}
:;confirmed:{{apitype|boolean?}}

==Example==
{{:API_C_GossipInfo.GetOptions#Example}}

==Patch changes==
* {{Patch 10.0.0|note=Changed <code>index</code> param to <code>optionID</code>.}}
* {{Patch 9.0.1|note=Moved to <code>C_GossipInfo.SelectOption()</code>}}
* {{Patch 1.0.0|note=Added as {{api|SelectGossipOption}}()}}

==See also==
* UI [https://github.com/Gethe/wow-ui-source/blob/10.0.0/Interface/FrameXML/GossipFrameShared.lua#L259 SelectGossipOption] - This is an API for players and addon authors to continue to be able to select by index rather than ID
```