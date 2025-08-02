# API C PlayerInfo.GetSex

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_PlayerInfo|system=PlayerLocationInfo}}
Returns the sex of a player.
 sex = C_PlayerInfo.GetSex(playerLocation)

==Arguments==
:;playerLocation:{{apitype|PlayerLocation}}

==Returns==
:;sex:{{apitype|Enum.UnitSex?}}
{{:Enum.UnitSex|nocaption=1}}

==Example==
Returns the gender of your character.
<syntaxhighlight lang="lua">
/dump C_PlayerInfo.GetSex(PlayerLocation:CreateFromUnit("player")) -- 1 (Female)
</syntaxhighlight>

==Patch changes==
* {{Patch 8.0.1|note=Added.}}

==See also==
* {{api|UnitSex}}()
```