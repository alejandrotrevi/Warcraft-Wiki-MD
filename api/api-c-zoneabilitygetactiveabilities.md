# API C ZoneAbility.GetActiveAbilities

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_ZoneAbility|system=ZoneAbility}}
Returns an array of abilities active within the current zone.
 zoneAbilities = C_ZoneAbility.GetActiveAbilities()

==Returns==
:;zoneAbilities:{{apitype|ZoneAbilityInfo[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| zoneAbilityID || {{apitype|number}} || ID for this zone ability. Likely correlates to the ID column of {{dbc|extraabilityinfo|ExtraAbilityInfo}}
|-
| uiPriority || {{apitype|number}} || Priority used for sorting zone abilities
|-
| spellID || {{apitype|number}} || Spell ID that the ability provides
|-
| textureKit || {{apitype|string}} || Optional name of a texture kit prefix for this ability. Texture kit names map to atlases, potentially suffixed by <code>-<number></code>, where <code>number</code> is the number of abilities with matching texture kit names.
|-
| tutorialText || {{apitype|string?}} || Optional tutorial text to show for the ability. This appears to typically be a hint that the ability can be dragged to a users' action bars.
|}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```