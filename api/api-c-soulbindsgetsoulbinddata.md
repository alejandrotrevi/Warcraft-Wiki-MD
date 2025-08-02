# API C Soulbinds.GetSoulbindData

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Soulbinds|system=Soulbinds}}
Needs summary.
 data = C_Soulbinds.GetSoulbindData(soulbindID)

==Arguments==
:;soulbindID:{{apitype|number}} : {{dbc|soulbind|Soulbind.ID}}

==Returns==
:;data:{{apitype|SoulbindData}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| ID || {{apitype|number}} || 
|-
| covenantID || {{apitype|number}} || [[Enum.CovenantType]]
|-
| name || {{apitype|string}} || 
|-
| description || {{apitype|string}} || 
|-
| textureKit || {{apitype|string}} || 
|-
| unlocked || {{apitype|boolean}} || 
|-
| cvarIndex || {{apitype|number}} || 
|-
| tree || {{apitype|SoulbindTree}} || 
|-
| modelSceneData || {{apitype|SoulbindModelSceneData}} || 
|-
| activationSoundKitID || {{apitype|number}} || 
|-
| playerConditionReason || {{apitype|string?}} || 
|}

{{:Struct SoulbindTree}}

{| class="sortable darktable zebra" style="margin-left: 3.9em"
|+ SoulbindModelSceneData
! Field !! Type !! Description
|-
| creatureDisplayInfoID || {{apitype|number}} || 
|-
| modelSceneActorID || {{apitype|number}} || 
|}

==Example==
Prints soulbind data for [[Niya]].
<syntaxhighlight lang="lua">
/dump C_Soulbinds.GetSoulbindData(5)
</syntaxhighlight>

==Patch changes==
* {{Patch 9.0.5|note=Added <code>playerConditionReason</code> field.}}
* {{Patch 9.0.2|note=Added <code>activationSoundKitID</code> field.}}
* {{Patch 9.0.1|note=Added.}}
```