# API C PvP.GetRandomBGRewards

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 honor, experience, itemRewards, currencyRewards, roleShortageBonus = C_PvP.GetRandomBGRewards()

==Returns==
:;honor:{{apitype|number}}
:;experience:{{apitype|number}}
:;itemRewards:{{apitype|BattlefieldItemReward[]?}}
{{:Struct BattlefieldItemReward|nocaption=1}}
:;currencyRewards:{{apitype|BattlefieldCurrencyReward[]?}}
{{:Struct BattlefieldCurrencyReward|nocaption=1}}
:;roleShortageBonus:{{apitype|RoleShortageReward?}}
{{:Struct RoleShortageReward|nocaption=1}}

==Patch changes==
* {{Patch 7.2.0|note=Moved to <code>C_PvP.GetRandomBGRewards()</code>}}
* {{Patch 7.0.3|note=Added as <code>GetRandomBGRewards()</code>}}
```