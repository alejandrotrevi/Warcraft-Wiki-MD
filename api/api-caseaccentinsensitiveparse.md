# API CaseAccentInsensitiveParse

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Localization}}
Converts a string with accented letters to lowercase.
 lower = CaseAccentInsensitiveParse(name)

==Arguments==
:;name:{{apitype|string}} - The string to be converted to lowercase.

==Returns==
:;lower:{{apitype|string}} - A lowercased equivalent of the input string.

==Details==
This API only supports a limited set of codepoints for conversion and is not suitable as general purpose Unicode-aware case conversion function.

The table below documents support for uppercase characters within defined Unicode codepoint blocks. A block is considered "supported" only if all uppercase class characters within the block will be converted to their lowercase equivalents by this function.

{| class="darktable zebra"
|-
! Block Name !! Supported !! Notes
|-
| [https://codepoints.net/basic_latin Basic Latin] || style="text-align:center" | ✔️ ||
|-
| [https://codepoints.net/latin-1_supplement Latin-1 Supplement] || style="text-align:center" | ✔️ || 
|-
| [https://codepoints.net/latin_extended-a Latin Extended-A] || style="text-align:center" | ❌ || Limited support for Œ (<code>U+0152</code>) and Ÿ (<code>U+0178</code>) only.
|-
|}

==Example==
This example demonstrates the support for the Basic and Supplemental Latin codepoint ranges, outputting a lowercased pair of strings.
<syntaxhighlight lang="lua">
local basic = "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
local supplemental = "ÀÁÂÃÄÅÆÇÈÉÊËÌÍÎÏÐÑÒÓÔÕÖØÙÚÛÜÝÞ"

print(CaseAccentInsensitiveParse(basic))
print(CaseAccentInsensitiveParse(supplemental))

-- Prints:
--    abcdefghijklmnopqrstuvwxyz
--    àáâãäåæçèéêëìíîïðñòóôõöøùúûüýþ
</syntaxhighlight>

==Patch changes==
* {{Patch 6.2.0|note=Added.}}
```