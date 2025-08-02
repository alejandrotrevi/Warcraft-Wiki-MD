# API GetRuneCooldown

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=PlayerScript}}
Returns the Death Knight's cooldown info for the specified rune.
 startTime, duration, isRuneReady = GetRuneCooldown(runeIndex)

==Arguments==
:;runeIndex:{{apitype|number}} - The rune index, ranging between 1 and 6.

==Returns==
:;startTime:{{apitype|number}} - The value of GetTime() when the rune's cooldown began (or 0 if the rune is off cooldown).
:;duration:{{apitype|number}} - The duration of the rune's cooldown (regardless of whether or not it's on cooldown).
:;isRuneReady:{{apitype|boolean}} - Whether or not the rune is off cooldown. True if ready, false if not.

==Example==
This will print the number of runes you have ready to cast.
<syntaxhighlight lang="lua">
local amount = 0
for i = 1, 6 do
	local start, duration, runeReady = GetRuneCooldown(i)
	if runeReady then
		amount = amount + 1
	end
end
print("Available Runes: " .. amount)
</syntaxhighlight>
```