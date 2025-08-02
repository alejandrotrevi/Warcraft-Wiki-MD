# API EnumerateServerChannels

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a list of all available server channels (zone dependent).
 channel1, channel2, ... = EnumerateServerChannels()

==Returns==
:;channel1, channel2, ...:{{apitype|string}} containing all available server channels in this zone

<!-- luals
---@return string ...
function EnumerateServerChannels() end
-->
```