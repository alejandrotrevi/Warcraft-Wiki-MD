# API GetNumVoiceSessions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__

Returns the number of voice sessions the client is currently in. Ignores voice channels under the 'World' category. 
 num = GetNumVoiceSessions()

==Returns==

:;num:{{apitype|number}} - Number of voice sessions the client is currently in.



==Details==

: This will only count sessions in which the user can speak. These include custom channels and Party, Battleground and Raid channels.
```