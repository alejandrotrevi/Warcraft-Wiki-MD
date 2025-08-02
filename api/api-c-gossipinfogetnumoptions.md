# API C GossipInfo.GetNumOptions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Returns the number of conversation options available with this NPC.
 numOptions = C_GossipInfo.GetNumOptions()

==Returns==
:;numOptions:{{apitype|number}}

==Details==
{{i-note|This API is removed in Dragonflight since you can simply iterate over {{api|C_GossipInfo.GetOptions}}}}

Prints options info.
<syntaxhighlight lang="lua">
local options = C_GossipInfo.GetOptions()
for _, info in pairs(options) do
	print(info.name, info.gossipOptionID)
end
</syntaxhighlight>
To e.g. select the first option.
<syntaxhighlight lang="lua">
local options = C_GossipInfo.GetOptions()
C_GossipInfo.SelectOption(options[1].gossipOptionID)
</syntaxhighlight>
To get the amount of options.
<syntaxhighlight lang="lua">
local numOptions = #C_GossipInfo.GetOptions()
</syntaxhighlight>

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_GossipInfo.GetNumOptions()</code>}}
* {{Patch 2.3.0|note=Added as {{api|GetNumGossipOptions}}()}}

==Details==
* This information is available when {{api|t=e|GOSSIP_SHOW}} event fires.
```