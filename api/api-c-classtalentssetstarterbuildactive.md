# API C ClassTalents.SetStarterBuildActive

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ClassTalents|system=ClassTalents}}
Switches your active talent loadout to the Starter Build, which is a Blizzard defined talent build, meant to be good enough for most content.
 result = C_ClassTalents.SetStarterBuildActive(active)

==Arguments==
:;active:{{apitype|boolean}}

==Returns==
:;result:{{apitype|Enum.LoadConfigResult}}
{{:Enum.LoadConfigResult|nocaption=1}}

==Details==
You should call {{api|C_ClassTalents.UpdateLastSelectedSavedConfigID}} with your current [[SpecializationID]] and <code>Constants.TraitConsts.STARTER_BUILD_TRAIT_CONFIG_ID</code> after the Starter Build has successfully been applied.

{{apinavbox|C_Traits}}
```