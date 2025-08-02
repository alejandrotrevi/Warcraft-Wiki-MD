# API UnitClass

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the class of the unit. 

 className, classFilename, classId = UnitClass(unit)
 classFilename, classId = UnitClassBase(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]]

==Returns==
:;className:{{apitype|string}} - Localized name, e.g. <code>"Warrior"</code> or <code>"Guerrier"</code>.
:;classFilename:{{apitype|string}} - Locale-independent name, e.g. <code>"WARRIOR"</code>.
:;classId:{{apitype|number}} : [[ClassId]]

==Details==
* <code>UnitClass</code> will respect any cosmetic class override the unit may currently have, whereas <code>UnitClassBase</code> will only return the 'real' class of a unit.
** This can be observed when querying NPC party members in [[Follower Dungeons]].

==Example==
<syntaxhighlight lang="lua">
/dump UnitClass("target") -- "Mage", "MAGE", 8
/dump UnitClassBase("target") -- "MAGE", 8
</syntaxhighlight>

==Values==
{{:ClassId}}

==Patch changes==
* {{Patch 5.0.4|note=Added <code>classId</code> return value.}}

{{apinavbox|Class}}
```