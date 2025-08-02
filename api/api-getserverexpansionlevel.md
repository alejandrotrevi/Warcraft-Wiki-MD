# API GetServerExpansionLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Expansion}}
Returns the expansion level currently active on the server.
 serverExpansionLevel = GetServerExpansionLevel()

==Returns==
:;serverExpansionLevel:{{apitype|number}}
{{:LE_EXPANSION}}

==Details==
* This does not update on pre-patch and only when the expansion actually launches; requires a client restart to update, if still in-game.
* Upon initial login, this will return <code>0</code> until sometime between <code>[[PLAYER_ENTERING_WORLD]]</code> and when a <code>[[SHOW_SUBSCRIPTION_INTERSTITIAL]]</code> would fire for a lapsed subscription, but then provides the correct value through subsequent logins and reloads on the same server.

==Example==
Before and after the Shadowlands global launch at November 23 2020 at 3:00 p.m. PST.
 /dump GetServerExpansionLevel() -- 7 -> 8

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```