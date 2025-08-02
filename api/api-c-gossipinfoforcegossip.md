# API C GossipInfo.ForceGossip

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_GossipInfo|system=GossipInfo}}
Returns true if gossip text must be displayed. For example making this return true shows the Banker gossip.
 forceGossip = C_GossipInfo.ForceGossip()

==Returns==
:;forceGossip:{{apitype|boolean}}

==Details==
* When this is made to return true, gossip text will no longer be skipped if there is only one non-gossip option. For example when speaking to the Banker.

==Patch changes==
* {{Patch 9.0.1|note=Moved to <code>C_GossipInfo.ForceGossip()</code>}}
* {{Patch 3.3.3|note=Added as {{api|ForceGossip}}()}}
```