# API C ClassTalents.LoadConfig

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Needs summary.
 result, changeError, newLearnedNodeIDs = C_ClassTalents.LoadConfig(configID, autoApply)

==Arguments==
:;configID:{{apitype|number}}
:;autoApply:{{apitype|boolean}}

==Returns==
:;result:{{apitype|Enum.LoadConfigResult}}
{{:Enum.LoadConfigResult|nocaption=1}}
:;changeError:{{apitype|string?}}
:;newLearnedNodeIDs:{{apitype|number[]}}

==Patch changes==
* {{Patch 10.0.5|note=Added <code>changeError, newLearnedNodeIDs</code> returns.}}

{{apinavbox|C_Traits}}
```