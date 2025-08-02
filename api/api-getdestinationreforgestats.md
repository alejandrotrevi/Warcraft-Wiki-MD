# API GetDestinationReforgeStats

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the reforge item's dest stats.
 name1, statID1, statValue1, reforgeID1, ... = GetDestinationReforgeStats(stat, value)

==Arguments==
:;stat:{{apitype|number}} - Source Stat ID
:;value:{{apitype|number}} - Source Stat Value
 
==Returns==
:;name:{{apitype|string}} - Stat Name
:;statID:{{apitype|number}} - Dest Stat ID
:;statValue:{{apitype|number}} - Dest Stat Value
:;reforgeID:{{apitype|number}} - <font color="#ff8080">Reforge ID</font>. It behaves more like an index though


{| class="darktable"
!Stat ID!!Stat Name
|-
|<center>3</center>||Agility
|-class="alt"
|<center>4</center>||Strength
|-
|<center>5</center>||Intellect
|-class="alt"
|<center>6</center>||Spirit
|-
|<center>7</center>||Stamina
|-class="alt"
|<center>13</center>||Dodge Rating
|-
|<center>14</center>||Parry Rating
|-class="alt"
|<center>31</center>||Hit Rating
|-
|<center>32</center>||Critical Strike Rating
|-class="alt"
|<center>36</center>||Haste Rating
|-
|<center>37</center>||Expertise Rating
|-class="alt"
|<center>45</center>||Spell Power
|-
|<center>49</center>||Mastery Rating
|}

==Example==
{{item|Handwraps of the Cleansing Flame}}
 /dump GetSourceReforgeStats(6, 82)
 
 => "Dodge Rating", 13, 82, <font color="#ff8080">1</font>, "Parry Rating", 14, 82, <font color="#ff8080">2</font>, "Hit Rating", 31, 82, <font color="#ff8080">3</font>, "Critical Strike Rating", 32, 82, <font color="#ff8080">4</font>, "Expertise Rating", 37, 82, <font color="#ff8080">5</font>, "Mastery Rating", 49, 82, <font color="#ff8080">6</font>

 /dump GetSourceReforgeStats(36, 68)
 
 => "Dodge Rating", 13, 68, 7, "Parry Rating", 14, 68, 8, "Hit Rating", 31, 68, 9, "Critical Strike Rating", 32, 68, 10, "Expertise Rating", 37, 68, 11, "Mastery Rating", 49, 68, 12

This example will print all the reforge item's possible dest stats
<pre>
local sourceStats = {GetSourceReforgeStats()}

for i = 1, #sourceStats, 3 do
	local destStats = {GetDestinationReforgeStats(sourceStats[i+1], sourceStats[i+2])}
	for j = 1, #destStats, 4 do
		print(i, j, destStats[j], destStats[j+1], destStats[j+2], destStats[j+3])
	end
end
</pre>

==See Also==
* [[API GetReforgeItemStats|GetReforgeItemStats]] for all of the reforge item's stats
* [[API GetSourceReforgeStats|GetSourceReforgeStats]] for source stats
```