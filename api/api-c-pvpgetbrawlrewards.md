# API C PvP.GetBrawlRewards

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PvP|system=PvpInfo}}
Needs summary.
 honor, experience, itemRewards, currencyRewards, roleShortageBonus, hasWon = C_PvP.GetBrawlRewards(brawlType)

==Arguments==
:;brawlType:{{apitype|Enum.BrawlType}}
{{:Enum.BrawlType|nocaption=1}}

==Returns==
:;honor:{{apitype|number}}
:;experience:{{apitype|number}}
:;itemRewards:{{apitype|BattlefieldItemReward[]?}}
{{:Struct BattlefieldItemReward|nocaption=1}}
:;currencyRewards:{{apitype|BattlefieldCurrencyReward[]?}}
{{:Struct BattlefieldCurrencyReward|nocaption=1}}
:;roleShortageBonus:{{apitype|RoleShortageReward?}}
{{:Struct RoleShortageReward|nocaption=1}}
:;hasWon:{{apitype|boolean}}

==Patch changes==
* {{Patch 7.2.0|note=Added.}}
```