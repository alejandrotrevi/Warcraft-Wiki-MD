# API StripHyperlinks

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Strips text of UI escape sequence markup.
 stripped = StripHyperlinks(text [, maintainColor [, maintainBrackets [, stripNewlines [, maintainAtlases]]]])

==Arguments==
:;text:{{apitype|string}} - The text to be stripped of markup.
:;maintainColor:{{apitype|boolean?}} - If true, preserve color escape sequences.
:;maintainBrackets:{{apitype|boolean?}}
:;stripNewlines:{{apitype|boolean?}} - If true, strip all line break sequences.
:;maintainAtlases:{{apitype|boolean?}} - If true, preserve atlas texture escape sequences.

==Returns==
:;stripped:{{apitype|string}} - The stripped text.

==Details==
* If the supplied string contains a protected string sequence (<code>|K</code>) then this function will return an empty string.
* This function is used by the [[Addon compartment]] to strip markup from addon titles prior to sorting.

==Patch changes==
* {{Patch 10.1.0|note=Added.}}
```