# API UnitClassification

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the classification of the specified unit (e.g., "elite" or "worldboss").
 classification = UnitClassification(unit)

==Arguments==
:;unit:{{apitype|UnitToken}}

==Returns==
:;classification:{{apitype|string}} - the unit's classification: "worldboss", "rareelite", "elite", "rare", "normal", "trivial", or "minus"

Note that "trivial" is for low-level targets that would not reward experience or honor ({{api|UnitIsTrivial}}() would return '1'), whereas "minus" is for mobs that show a miniature version of the v-key health plates.

==Example==
 if ( UnitClassification("target") == "worldboss" ) then
   -- If unit is a world boss show skull regardless of level
   TargetLevelText:Hide();
   TargetHighLevelTexture:Show();
 end

<big>'''Result'''</big>
: If the target is a world boss, then the level isn't shown in the target frame, instead a special high level texture is shown.

==Patch changes==
* {{Patch 5.0.4|note="minus" classification added; used for minion mobs that typically have less health than normal mobs of their level, but engage the player in larger numbers.}}
```