# API GetReforgeItemStats

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__
Returns the reforge item's stats.
 name1, statID1, statValue1, ... = GetReforgeItemStats()

==Returns==
:;name:{{apitype|string}} - Stat Name
:;statID:{{apitype|number}} - Stat ID
:;statValue:{{apitype|number}} - Stat Value

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
 /dump GetReforgeItemStats() => "Stamina", 7, 454, "Intellect", 5, 282, "Spirit", 6, 206, "Haste Rating", 36, 172

This example will print all the reforge item's stats
<pre>
local stats = {GetReforgeItemStats()}

for i = 1, #stats, 3 do
	print(stats[i], stats[i+1], stats[i+2])
end
</pre>

==See Also==
* [[API GetSourceReforgeStats|GetSourceReforgeStats]] for source stats
* [[API GetDestinationReforgeStats|GetDestinationReforgeStats]] for dest stats
```