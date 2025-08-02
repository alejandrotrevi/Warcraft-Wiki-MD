# API ChangeChatColor

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Updates the color for a type of chat message.
 ChangeChatColor(channelName, red, green, blue)

==Arguments==
:;channelName:{{apitype|string}} - Name of the channel as given in chat-cache.txt files.
:;red:{{apitype|number}} - RGB values (0-1, floats).
:;green:{{apitype|number}}
:;blue:{{apitype|number}}

==Example==
Resets the General channel to the default (255,192,192, slightly off-white) color.
 ChangeChatColor("CHANNEL1", 255/255, 192/255, 192/255);

==See also==
* [[API FontString SetTextColor|FontString:SetTextColor()]].
```