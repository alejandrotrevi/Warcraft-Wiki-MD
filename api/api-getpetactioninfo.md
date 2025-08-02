# API GetPetActionInfo

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns info for an action on the pet action bar.
 name, texture, isToken, isActive, autoCastAllowed, autoCastEnabled, spellID, checksRange, inRange = GetPetActionInfo(index)

==Arguments==
:;index:{{apitype|number}} - The index of the pet action button you want to query.

==Returns==
:;name:{{apitype|string}} - The name of the action (or its global ID if isToken is true).
:;texture:{{apitype|string}} - The name (or its global ID, if isToken is true) of the texture for the action.
:;isToken:{{apitype|boolean}} - Indicates if the action is a reference to a global action, or not (<small>guess</small>)
:;isActive:{{apitype|boolean}} - Returns true if the ability is currently active.
:;autoCastAllowed:{{apitype|boolean}} - Returns true if this ability can use autocast.
:;autoCastEnabled:{{apitype|boolean}} - Returns true if autocast is currently enabled for this ability.
:;spellID:{{apitype|number}} - Returns the spell ID associated with this ability.
:;checksRange:{{apitype|boolean}} - Returns true if this ability has a numeric range requirement.
:;inRange:{{apitype|boolean}} - Returns true if this ability is currently in range.

==Details==
Information based on a post from Sarf plus some guesswork, so may not be 100% accurate
```