# API C AnimaDiversion.OpenAnimaDiversionUI

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_AnimaDiversion|system=AnimaDiversionInfo}}
Attempts to open the AnimaDiversionFrame.
 C_AnimaDiversion.OpenAnimaDiversionUI()

==Details==
* Triggers {{api|t=e|ANIMA_DIVERSION_OPEN}} only after interacting with an [[Anima Conductor]] at least once since logging on, regardless of subsequent calls to {{api|C_UI.Reload()}}; otherwise, this function silently fails.
* Despite its name, this function is not used by the native UI when interacting with an Anima Conductor.
* Calling this function after walking away from the Anima Conductor results in an incomplete UI because {{api|C_AnimaDiversion.GetOriginPosition()}} returns nil.
* However, it is possible to close and reopen the frame with full functionality if the player has remained within range of the Anima Conductor since interacting with it.

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```