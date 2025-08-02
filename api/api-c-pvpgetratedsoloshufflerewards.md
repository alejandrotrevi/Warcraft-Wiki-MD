# API C PvP.GetRatedSoloShuffleRewards

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 honor, experience, itemRewards, currencyRewards, roleShortageBonus = C_PvP.GetRatedSoloShuffleRewards()

==Returns==
:;honor:{{apitype|number}}
:;experience:{{apitype|number}}
:;itemRewards:{{apitype|BattlefieldItemReward[]?}}
{{:Struct BattlefieldItemReward|nocaption=1}}
:;currencyRewards:{{apitype|BattlefieldCurrencyReward[]?}}
{{:Struct BattlefieldCurrencyReward|nocaption=1}}
:;roleShortageBonus:{{apitype|RoleShortageReward?}}
{{:Struct RoleShortageReward|nocaption=1}}
```