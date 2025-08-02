# API BreakUpLargeNumbers

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Divides digits into groups using a localized delimiter character.
 valueString = BreakUpLargeNumbers(value)

==Arguments==
:;value:{{apitype|number}} - The number to convert into a localized string

==Returns==
:;valueString:{{apitype|string}} - The whole-number portion converted into a string if greater than 1000, or truncated to two decimals if less than 1000.

==Details==
* Large numbers are grouped into thousands and millions with a <code>LARGE_NUMBER_SEPERATOR</code>, but no further grouping happens for even larger numbers (billions).
* Small numbers with a decimal portion are separated with a <code>DECIMAL_SEPERATOR</code> and truncated to two decimal places.
* Not intended for use with negative numbers.

==Example==
<syntaxhighlight lang="lua">
BreakUpLargeNumbers(123.456789)   -- 123.45
BreakUpLargeNumbers(1234567.89)   -- 1,234,567
BreakUpLargeNumbers(1234567890)   -- 1234,567,890
</syntaxhighlight>

==Patch changes==
* {{Patch 6.0.2|note=Transferred from [[FrameXML]] to ''userdata'' in the game engine; no impact on functionality.<ref>{{ref FrameXML|UIParent.lua|6.0.2|19033|4131|20141014}}</ref>}}
* {{Patch 5.0.4|note=Added.<ref>{{ref FrameXML|UIParent.lua|5.0.4|16016|4017|20120821}}</ref>}}

==See also==
* {{api|GetLocale}}
* {{api|FillLocalizedClassList}}
* {{api|FormatLargeNumber}}

==References==
{{Reflist}}
```