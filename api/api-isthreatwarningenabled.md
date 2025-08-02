# API IsThreatWarningEnabled

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns true if threat warnings are currently enabled.
 enabled = IsThreatWarningEnabled()

==Return values==
:;enabled:{{apitype|boolean}} flag - 1 if the warnings are enabled, nil if they are not.

==Details==
* The warnings are controlled by the {{api|threatWarning|t=c}} CVar, which allows the player to specify in which situations the warnings should be active. This function takes into account the current situation.

==See Also==
* {{api|ShowNumericThreat}}
```