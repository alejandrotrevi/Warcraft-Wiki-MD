# API GetMaxLevelForLatestExpansion

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Expansion}}
Returns the highest reachable character level for the latest expansion.
 maxLevel = GetMaxLevelForLatestExpansion()

==Returns==
:;maxLevel:{{apitype|number}}

==Details==
* This does not update on pre-patch and only when the expansion actually launches; requires a client restart to update, if still in-game.
* Upon initial login, this will return the result of <code>[[API_GetMaxLevelForExpansionLevel|GetMaxLevelForExpansionLevel]](0)</code> (currently <code>30</code>) until sometime between <code>[[PLAYER_ENTERING_WORLD]]</code> and when a <code>[[SHOW_SUBSCRIPTION_INTERSTITIAL]]</code> would fire for a lapsed subscription, but then provides the correct value through subsequent logins and reloads on the same server.

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```