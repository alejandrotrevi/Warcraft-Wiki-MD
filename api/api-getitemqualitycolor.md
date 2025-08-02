# API GetItemQualityColor

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|tentative=1}}
Returns the color for an item quality.
 r, g, b, hex = GetItemQualityColor(quality)

==Arguments==
:;quality:{{apitype|Enum.ItemQuality}}

==Returns==
:;r:{{apitype|number}} - Red component of the color (0 to 1, inclusive).
:;g:{{apitype|number}} - Green component of the color (0 to 1, inclusive).
:;b:{{apitype|number}} - Blue component of the color (0 to 1, inclusive).
:;hex:{{apitype|string}} - [[UI escape sequences|UI escape sequence]] for this color, without the leading "|c".

==Details==
* It is recommended to use the global [https://www.townlong-yak.com/framexml/9.0.1/UIParent.lua#170 ITEM_QUALITY_COLORS] table instead of repeatedly calling this function.

* In particular, <code>ITEM_QUALITY_COLORS[quality].hex</code> already includes the leading "|c" escape sequence whereas the fourth return value of this function does not.

* If an invalid quality index is specified, GetItemQualityColor() returns white (same as index 1):
::r = 1
::g = 1
::b = 1
::hex = |cffffffff

==Example==
<syntaxhighlight lang="lua">
for i = 0, 8 do
   local r, g, b, hex = GetItemQualityColor(i)
   print(i, '|c'..hex, _G["ITEM_QUALITY" .. i .. "_DESC"], string.sub(hex,3))
end
</syntaxhighlight>

===Result===
: Will print all qualities, in their individual colors.
{{Example/Begin}}
0 <span class="qc-poor">Poor 9d9d9d</span><br>
1 <span class="qc-common">Common ffffff</span><br>
2 <span class="qc-uncommon">Uncommon 1eff00</span><br>
3 <span class="qc-rare">Rare 0070dd</span><br>
4 <span class="qc-epic">Epic a335ee</span><br>
5 <span class="qc-legendary">Legendary ff8000</span><br>
6 <span class="qc-artifact">Artifact e6cc80</span><br>
7 <span class="qc-heirloom">Heirloom 00ccff</span><br>
8 <span class="qc-token">WoW Token 00ccff</span>
{{Example/End}}

==Patch changes==
* {{Patch 4.2.0|note=The fourth return value no longer includes the leading <code><nowiki>|c</nowiki></code>.}}
* {{Patch 1.9.1|note=Added.}}
```