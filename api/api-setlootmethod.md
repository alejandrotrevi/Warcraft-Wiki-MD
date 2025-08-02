# API SetLootMethod

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Set the current loot method.
 SetLootMethod(method [, playerName, threshold]) 

==Arguments==
:;method:{{apitype|string}} - Any one of the following self-explanatory and case insensitive arguments: 
{| style="margin-left:3em" class="zebra darktable"
! Value
|-
| "group"
|-
| "freeforall"
|-
| "master"
|-
| "needbeforegreed"
|-
| "roundrobin"
|}

:;playerName:{{apitype|string}} - Any valid player name that is in group or raid, only used if first argument is "master"
:;threshold:{{apitype|Enum.ItemQuality}} - The loot quality to start using the current loot method with.

==Details==
* Additionally, if method is "master", the second argument must be a player name, followed by the optional third argument. 
* The third argument is set to 1 if you're promoting a new master looter, as in the case where you right click on a raid member and select "Promote to Master Looter".
* To only change the loot threshold, use [[API_SetLootThreshold|SetLootThreshold]]

==Example==
If you are the party or raid leader, the script will set the loot method to "Master Looter", promote the named char to loot master and the loot threshold to Common Quality. This specific script was often used in AQ40 in Classic to control who got Scarab Key
 /script SetLootMethod("master", "name", 1);
```