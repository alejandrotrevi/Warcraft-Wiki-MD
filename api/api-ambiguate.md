# API Ambiguate

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a version of a character-realm string suitable for use in a given context.
 name = Ambiguate(fullName, context)

==Arguments==
:;fullName:{{apitype|string}} - character-realm for a character, e.g. "Shion-DieAldor"
:;context:{{apitype|string}} - context the name will be used in, one of: "all", "guild", "mail", "none", or "short".

==Returns==
:;name:{{apitype|string}} - character or character-realm name combination that would be equivalent to <code>fullName</code> in the specified context.

{| class="darktable zebra"
|-
!rowspan="2"|Context!!colspan="2"|Same Realm!!colspan="2"|Different Realm
|-
!Same Guild!!Other Guild!!Same Guild!!Other Guild
|-
|all||character||character||character||character-realm
|-
|guild||character||character||character||character-realm
|-
|craftingorder||character-realm||character-realm||character-realm||character-realm
|-
|mail||character-realm||character-realm||character-realm||character-realm
|-
|none||character||character||character-realm||character-realm
|-
|short||character||character||character||character
|}

==Details==
* If this is used on a character with the "guild" context, and another character in the same guild has the same name but in a different realm, "character-realm" is returned.

==Patch changes==
* {{Patch 5.4.2|note=Added.}}
```