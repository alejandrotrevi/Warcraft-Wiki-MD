# API UnitName

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Unit}}
Returns the name and realm of the unit.
 name, realm = UnitName(unit)
             = UnitFullName(unit)
             = UnitNameUnmodified(unit)

==Arguments==
:;unit:{{apitype|string}} : [[UnitId]] - For example <code>"player"</code> or <code>"target"</code>

==Returns==
:;name:{{apitype|string?}} - The name of the unit. Returns <code>nil</code> if the unit doesn't exist, e.g. the player has no target selected.
:;realm:{{apitype|string?}} - The [[API GetNormalizedRealmName|normalized]] realm the unit is from, e.g. <code>"DarkmoonFaire"</code>. Returns <code>nil</code> if the unit is from the same realm.

==Details==
* Will return globalstring <code>UNKNOWNOBJECT</code> "Unknown Entity" if called before the unit in question has been fully loaded into the world.
* The unit name will change if the unit is under the effects of [[Lifegiving Seed]] or a similar effect, but <code>UnitNameUnmodified()</code> is unaffected by this.

==Example==
* Prints your character's name.
<syntaxhighlight lang="lua">
/dump UnitName("player") -- "Leeroy", nil
</syntaxhighlight>

* Prints the name and realm of your target (if different).
<syntaxhighlight lang="lua">
/dump UnitName("target") -- "Thegnome", "DarkmoonFaire"
</syntaxhighlight>

* <code>UnitFullName()</code> is equivalent with <code>UnitName()</code> except it will always return <code>realm</code> if used with the "player" UnitId.
<syntaxhighlight lang="lua">
/dump UnitFullName("player") -- "Leeroy", "MoonGuard"
/dump UnitFullName("target") -- "Leeroy", nil
</syntaxhighlight>

==GetUnitName==
[https://www.townlong-yak.com/framexml/go/GetUnitName GetUnitName]<code>(unit [, showServerName])</code> can return the combined unit and realm name.
* If <code>showServerName</code> is true and the queried unit is from a different server, then the return value will include the unit's name appended by a dash and the normalized realm name.
* If <code>showServerName</code> is false, then <code>FOREIGN_SERVER_LABEL</code> <code>" (*)"</code> will be appended to units from ''coalesced'' realms. Units from the player's own realm or [[Connected Realms]] get no additional suffix.

Unit is from the same realm.
<syntaxhighlight lang="lua">
/dump GetUnitName("target", true)  -- "Nephertiri"
/dump GetUnitName("target", false) -- "Nephertiri"
</syntaxhighlight>

Unit is from a different realm but the same [[Connected Realm]] (LE_REALM_RELATION_VIRTUAL).
<syntaxhighlight lang="lua">
/dump GetUnitName("target", true)  -- "Standron-EarthenRing"
/dump GetUnitName("target", false) -- "Standron"
</syntaxhighlight>

Unit is from a different, non-connected realm ([[API UnitRealmRelationship|LE_REALM_RELATION_COALESCED]]).
<syntaxhighlight lang="lua">
/dump GetUnitName("target", true)  -- "Celturio-Quel'Thalas"
/dump GetUnitName("target", false) -- "Celturio (*)"
</syntaxhighlight>

==Patch changes==
* {{Patch 1.12.0|note=Added <code>realm</code> return value.<sup>[https://www.wowinterface.com/forums/showthread.php?t=5577]</sup>}}

==See also==
* {{api|Ambiguate}}()
```