# API GetNumGossipOptions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the number of conversation options available with this NPC.
 numOptions = GetNumGossipOptions()

==Returns==
:;numOptions:{{apitype|number}} - Number of conversation options you can select.

==Details==
* This information is available when {{api|t=e|GOSSIP_SHOW}} event fires.

==See also==
* {{api|GetGossipOptions}}
* {{api|SelectGossipOption}}
```