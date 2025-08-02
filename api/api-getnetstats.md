# API GetNetStats

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns bandwidth and latency network information.
 bandwidthIn, bandwidthOut, latencyHome, latencyWorld = GetNetStats()

==Returns==
:;bandwidthIn:{{apitype|number}} - Current incoming bandwidth (download) usage, measured in KB/s.
:;bandwidthOut:{{apitype|number}} - Current outgoing bandwidth (upload) usage, measured in KB/s.
:;latencyHome:{{apitype|number}} - Average roundtrip latency to the home realm server (only updated every 30 seconds).
:;latencyWorld:{{apitype|number}} - Average roundtrip latency to the current world server (only updated every 30 seconds).

==Details==
{{Bluepost|poster=Gelmkar|title=Home/World latency (updated) - 4.0.6|date= 02/11/2011 7:54:23 PM UTC|link=http://eu.battle.net/wow/en/forum/topic/1710231176|body=
In essence, <u>Home</u> refers to your connection to your realm server. This connection sends chat data, auction house stuff, guild chat and info, some addon data, and various other data. It is a pretty slim connection in terms of bandwidth requirements.<br/><br/>
<u>World</u> is a reference to the connection to our servers that transmits all the other data... combat, data from the people around you (specs, gear, enchants, etc.), NPCs, mobs, casting, professions, etc. Going into a highly populated zone (like a capital city) will drastically increase the amount of data being sent over this connection and will raise the reported latency.<br/><br/>
Prior to 4.0.6, the in-game latency monitor only showed 'World' latency, which caused a lot of confusion for people who had no lag while chatting, but couldn't cast or interact with NPCs and ended up getting kicked offline. We hoped that including the latency meters for both connections would assist in clarifying this for everyone.<br/><br/>
As is probably obvious based upon this information, the two connections are not used equally. There is a much larger amount of data being sent over the World connection, which is a good reason you may see disparities between the two times. If there is a large chunk of data 'queued' up on the server and waiting to be sent to your client, that 'ping' to the server is going to have to wait its turn in line, and the actual number returned will be much higher than the 'Home' connection.}}

==Patches==
* {{Patch 4.0.6|note=Now returns both home and world latency, instead of just world latency.}}
```