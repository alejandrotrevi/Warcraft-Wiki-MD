# API GetGossipOptions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Get the available gossip items on an NPC (possibly stuff like the BWL and MC orbs too).
 title1, gossip1, ... = GetGossipOptions()

==Returns==
:;title:{{apitype|string}} - The title of the gossip item.
:;gossip:{{apitype|string}} - The gossip type: banker, battlemaster, binder, gossip, healer, petition, tabard, taxi, trainer, unlearn, vendor, workorder

==Details==
* The gossip options are available after {{api|GOSSIP_SHOW|t=e}} has fired.
```