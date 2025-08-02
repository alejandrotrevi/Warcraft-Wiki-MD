# API GetThreatStatusColor

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns the color for a threat status.
 r, g, b = GetThreatStatusColor(status)

==Arguments==
:;status:{{apitype|number}} - Usually the return of {{api|UnitThreatSituation}}

==Returns==
:;r:{{apitype|number}} - a value between 0 and 1 for the red content of the color
:;g:{{apitype|number}} - a value between 0 and 1 for the green content of the color
:;b:{{apitype|number}} - a value between 0 and 1 for the blue content of the color

==Details==
*Usually returns one of the following:
:: '''1''': <span style="color: #FFFF77">1.00, 1.00, 0.47</span> (yellow)
:: '''2''': <span style="color: #FF9900">1.00, 0.60, 0.00</span> (orange)
:: '''3''': <span style="color: #FF0000">1.00, 0.00, 0.00</span> (red)

* Other values observed in the wild, but these situations do not occur in the default UI:
:: '''0''': <span style="color: #AFAFAF">0.69, 0.69, 0.69</span> (grey)
:: '''4''' to '''4294967294''': <span style="color: #FF00FF">1.00, 0.00, 1.00</span> (magenta)
:: '''4294967295''': <span class="cc-priest">1.00, 1.00, 1.00</span> (white)

==Example==
Prints a description of the player's threat situation to the chat frame, colored appropriately. e.g.
<syntaxhighlight lang="lua">
local statustxts = { "low on threat",  "overnuking", "losing threat", "tanking securely" }

local status = UnitThreatSituation("player", "target") -- returns nil, 0, 1, 2 or 3
if (status) then
	local r, g, b = GetThreatStatusColor(status)
	print(status .. ": You are " .. statustxts[status + 1] .. ".", r, g, b)
else
    print("nil: You are not on their threat table.")
end
</syntaxhighlight>

Results in one of the following.
 <font color="AFAFAF">0: You are low on threat.</font>
 <font color="FFFF77">1: You are overnuking.</font>
 <font color="FF9900">2: You are losing threat.</font>
 <font color="FF0000">3: You are tanking securely.</font>
 nil: You are not on their threat table.

==Patch changes==
* {{Patch 10.2.6|note=Changed <code>status</code> to be in range 0 to 4294967295.}}
* {{Patch 3.0.2|note=Added}}

==See also==
* [[API UnitDetailedThreatSituation]]

[[Category:Interface customization]]
```