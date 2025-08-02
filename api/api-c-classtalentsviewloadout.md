# API C ClassTalents.ViewLoadout

**Contributor:** Numynum

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Applies loadout information to a previously initialized <code>Constants.TraitConsts.VIEW_TRAIT_CONFIG_ID</code> configID
 success = C_ClassTalents.ViewLoadout(entries)

==Arguments==
:;entries:{{apitype|ImportLoadoutEntryInfo[]}} - should be used with the same data format as {{api|C_ClassTalents.ImportLoadout}}
{{:Struct ImportLoadoutEntryInfo|nocaption=1}}

==Returns==
:;success:{{apitype|boolean}}

==Details==
{{api|C_ClassTalents.InitializeViewLoadout}} should always be called first, to avoid unexpected results.

Can be used in conjunction with {{api|C_ClassTalents.InitializeViewLoadout}} to build a cache of talent information. See that API's page for more details.

{{apinavbox|C_Traits}}
```