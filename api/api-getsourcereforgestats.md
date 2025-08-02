# API GetSourceReforgeStats

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the reforge item's source stats, which can be used to reforge into another (dest) stat.
 name1, statID1, statValue1, ... = GetSourceReforgeStats()

==Returns==
:;name:{{apitype|string}} - Stat Name
:;statID:{{apitype|number}} - Stat ID
:;statValue:{{apitype|number}} - Stat Value. This is the amount that will be subtracted and can be reforged into another stat

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
 /dump GetSourceReforgeStats() => "Spirit", 6, 82, "Haste Rating", 36, 68
{| class="darktable"
!Stat||Old!!Diff!!New
|-
|(6) Spirit||206||<b>- 82</b>||124
|-class="alt"
|(36) Haste Rating||172||<b>- 68</b>||104
|}

This example will print all the reforge item's source stats
<pre>
local stats = {GetSourceReforgeStats()}

for i = 1, #stats, 3 do
	print(stats[i], stats[i+1], stats[i+2])
end
</pre>

==See Also==
* [[API GetReforgeItemStats|GetReforgeItemStats]] for all of the reforge item's stats
* [[API GetDestinationReforgeStats|GetDestinationReforgeStats]] for dest stats
```