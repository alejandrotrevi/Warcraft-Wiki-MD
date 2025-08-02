# API GetProfessions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the spell tab indices of the character's current professions.
 prof1, prof2, archaeology, fishing, cooking = GetProfessions()

==Returns==
:;prof1:{{apitype|number}} - spell tab index for the first primary profession, or nil if not learned.
:;prof2:{{apitype|number}} - spell tab index for the second primary profession, or nil if not learned.
:;archaeology:{{apitype|number}} - spell tab index for Archaeology, or nil if not learned.
:;fishing:{{apitype|number}} - spell tab index for Fishing, or nil if not learned.
:;cooking:{{apitype|number}} - spell tab index for Cooking, or nil if not learned.

==Details==
* The returned indices can be passed to {{api|GetProfessionInfo}} or {{api|GetSpellTabInfo}} functions.
* Indices are not fixed and can change when a character learns or unlearns a profession.
* {{Wow-inline}} Classic uses {{api|GetNumPrimaryProfessions}}() instead.

==Patch changes==
* {{Patch 8.0.1|note=Removed <code>firstAid</code> return.}}
* {{Patch 4.0.1|note=Added}}
```