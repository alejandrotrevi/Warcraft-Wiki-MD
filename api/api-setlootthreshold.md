# API SetLootThreshold

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the loot quality threshold for group/master loot.
 SetLootThreshold(threshold)

==Arguments==
:;threshold:{{apitype|number}} - The loot quality to start using the current loot method with.
{| style="margin-left:3em" class="zebra darktable"
! Value !! Description
|- class="qc-uncommon"
| 2 || Uncommon
|- class="qc-rare"
| 3 || Rare
|- class="qc-epic"
| 4 || Epic
|- class="qc-legendary"
| 5 || Legendary
|- class="qc-artifact"
| 6 || Artifact
|}

==Details==
* This function throws an error with <span class="qc-poor">Poor</span> (0) or <span class="qc-common">Common</span> (1) qualities, but it is possible to set these lower thresholds using {{api|SetLootMethod()}} with "master" as the first argment and 0 or 1 and the third.  e.g. <syntaxhighlight inline="true" lang="lua">SetLootMethod("master","player",1)</syntaxhighlight>
* Calling this while the loot method is changing will revert to the original loot method.  To account for this, use {{api|C_Timer.After()}} to delay setting the threshold until a moment later. e.g. <syntaxhighlight inline="true" lang="lua">C_Timer.After(1, function() SetLootMethod(2) end)</syntaxhighlight>

==Example==
If you are the party/raid leader, this script sets the loot threshold to <span class="qc-uncommon">Uncommon</span> items or better and causes everyone to see a chat notice to this effect.
 /run SetLootThreshold(2)

==See also==
* {{api|t=e|PARTY_LOOT_METHOD_CHANGED}}
```