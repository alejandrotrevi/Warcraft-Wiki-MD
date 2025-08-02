# API GetText

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns localized text depending on the specified gender.
 text = GetText(token [, gender, ordinal])

==Arguments==
:;token:{{apitype|string}} - Reputation index
:;gender:{{apitype|number}} - [[API_UnitSex|Gender ID]]
:;ordinal:{{apitype|unknown}}

==Returns==
:;text:{{apitype|string}} - The localized text

==Example==
* This should return <code>FACTION_STANDING_LABEL1</code>
<syntaxhighlight lang="lua">
/dump GetText("FACTION_STANDING_LABEL1") -- "Hated"
</syntaxhighlight>

* This should return <code>FACTION_STANDING_LABEL1_FEMALE</code>
<syntaxhighlight lang="lua">
/dump GetText("FACTION_STANDING_LABEL1", 3) -- "Hated"
</syntaxhighlight>

==Patch changes==
* {{Patch 3.1.0|note=Added. Replaced the <code>FrameXML/LocaleProperties.lua</code> implementation.}}

==See also==
* {{api|getglobal}}
```