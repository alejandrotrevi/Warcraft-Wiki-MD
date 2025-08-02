# API GetLFGRoleUpdateBattlegroundInfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the name of the battleground queue triggering a role check.
 queueName = GetLFGRoleUpdateBattlegroundInfo()

==Returns==
:;queueName:{{apitype|string}} - name of the battleground queue triggering a role check.

==Details==
* While a battleground role check is in progress, {{api|GetLFGRoleUpdate}} returns <code>true</code> for the first and fifth return values.

==Patch changes==
* {{Patch 5.3.0|note=Added.}}

==See also==
* {{api|GetLFGRoleUpdate}}
```