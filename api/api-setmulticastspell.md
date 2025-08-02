# API SetMultiCastSpell

**Contributor:** Dark T Zeratul

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the totem spell for a specific totem bar slot.
 SetMultiCastSpell(actionID, spellID)

==Arguments==
:;actionID:{{apitype|number}} - The totem bar slot number.
::{| class="darktable"
  |-
  ! rowspan="2" | Call of the...
  ! colspan="4" | Totem slot
  |-
  ! Fire
  ! Earth
  ! Water
  ! Air
  |-
  | [[Call of the Elements (Wrath Classic)|Elements]]   || 133 || 134 || 135 || 136
  |-
  | [[Call of the Ancestors (Wrath Classic)|Ancestors]] || 137 || 138 || 139 || 140
  |-
  | [[Call of the Spirits|Spirits]]     || 141 || 142 || 143 || 144
  |}

:;spellID:{{apitype|number}} - The global spell number, found on Wowhead or through [[API_COMBAT_LOG_EVENT|COMBAT_LOG_EVENT]].

==Example==
 SetMultiCastSpell(134, 2484)

<big>'''Result'''</big>

Sets [[Earthbind Totem]] on [[Call of the Elements (Wrath Classic)]].
```