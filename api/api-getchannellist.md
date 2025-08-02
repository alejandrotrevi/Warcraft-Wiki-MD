# API GetChannelList

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the list of joined chat channels.
 id, name, disabled, ... = GetChannelList()

==Returns==
(Variable returns: <code>id1, name1, disabled1, id2, name2, disabled2, ...</code>)
:;id:{{apitype|number}} - channel number
:;name:{{apitype|string}} - channel name
:;disabled:{{apitype|boolean}}  - If the channel is disabled, e.g. the Trade channel when you're not in a city.

==Example==
Prints the channels the player is currently in.
<syntaxhighlight lang="lua">
local channels = {GetChannelList()}
for i = 1, #channels, 3 do
	local id, name, disabled = channels[i], channels[i+1], channels[i+2]
	print(id, name, disabled)
end
</syntaxhighlight>
<!-- luals
---@return number id
---@return string name
---@return boolean disabled
---@return ...
function GetChannelList() end
-->
```