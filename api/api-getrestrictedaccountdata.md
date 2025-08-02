# API GetRestrictedAccountData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the cap on trial character level, money and profession skill.
 rLevel, rMoney, profCap = GetRestrictedAccountData()

==Returns==
:;rLevel:{{apitype|number}} - character level cap, currently <code>20</code>
:;rMoney:{{apitype|number}} - max amount of money in copper, currently <code>10000000</code>
:;profCap:{{apitype|number}} - profession level cap, currently <code>0</code>

==Details==
* Only returns proper values while on a [[Starter Edition]] or inactive account.

==Patch changes==
* {{Patch 9.0.1|note=Changed the gold cap to 1000 gold, up from 10.}}
* {{Patch 4.2.0|note=Added.}}
```