# API GetNumDisplayChannels

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
 channelCount = GetNumDisplayChannels()

==Returns==
:;channelCount:{{apitype|number}} - the number of channels and headers currently displayed by ChannelFrame. 

==Details==
* This function returns Usually used to loop through all available channels/headers to perfom [[API GetChannelDisplayInfo]] on them.
* Note that this function only retrieves the number of ''visible'' channels/headers! Those subchannels that are hidden by a collapsed header are not counted.
```