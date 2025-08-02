# API GetAverageItemLevel

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the character's average item level.
 avgItemLevel, avgItemLevelEquipped, avgItemLevelPvp = GetAverageItemLevel()

==Returns==
:;avgItemLevel:{{apitype|number}} - The average item level of the player. This value is not rounded off to any significant digits.
:;avgItemLevelEquipped:{{apitype|number}} - The average equipped item level of the player. This value is not rounded off to any significant digits.
:;avgItemLevelPvp:{{apitype|number}} - The average equipped item level your character is considered to have under PvP situations. Item slots are weighted and gems are taken in account to compute this value. It is likely used to derive [[PvP scaling|PvP Scaling]] coefficient.

==Example==
The following macro prints your average and equipped item levels (to two decimal places) to chat:
 /run print(("Average Item level: %.2f; Equipped item level: %.2f"):format(GetAverageItemLevel()))

==Details==
This function is only used to get the average iLevel of the player. It cannot be used to get the average iLevel of anybody else.

<pre>
Currently Blizzard's formula for equipped average item level is as follows:

 sum of item levels for equipped gear (I)
-----------------------------------------  = Equipped Average Item Level
       number of slots (S)

(I) = in taking the sum, the tabard and shirt always count as zero
      some heirloom items count as zero, other heirlooms count as one

(S) = number of slots depends on the contents of the main and off hand as follows:
      17 with both hands holding items 
      17 with a single one-hand item (or a single two-handed item with Titan's Grip)
      16 with a two-handed item equipped (and no Titan's Grip)
      16 with both hands empty
</pre>
```