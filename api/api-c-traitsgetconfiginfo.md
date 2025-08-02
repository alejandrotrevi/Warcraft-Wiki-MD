# API C Traits.GetConfigInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Traits|system=SharedTraits}}
Needs summary.
 configInfo = C_Traits.GetConfigInfo(configID)

==Arguments==
:;configID:{{apitype|number}} - For TalentTrees this will often be {{api|C_ClassTalents.GetActiveConfigID}}, this is -1 when inspecting a player. For professions, this will be {{api|C_ProfSpecs.GetConfigIDForSkillLine}}.

==Returns==
:;configInfo:{{apitype|TraitConfigInfo}}
{{:Struct TraitConfigInfo|nocaption=1}}

{{apinavbox|C_Traits}}
```