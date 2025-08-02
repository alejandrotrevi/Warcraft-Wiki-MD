# API C MythicPlus.GetCurrentAffixes

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a table listing the current AffixIDs that are available this week.
 affixIDs = C_MythicPlus.GetCurrentAffixes()

==Returns==
:;affixIDs:{{apitype|MythicPlusKeystoneAffix[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| id || {{apitype|number}} || 
|-
| seasonID || {{apitype|number}} || 
|}

==Details==
* Sample output with Fortified, Afflicted and Raging
<pre>
{
    {   
        id = 10,
        seasonID = 0 
    }, {   
        id = 135,
        seasonID = 0 
    }, {   
        id = 6,
        seasonID = 0 
    } 
}
</pre>

* Use [[API C ChallengeMode.GetAffixInfo|C_ChallengeMode.GetAffixInfo(affixID)]] to see the information about the specified affix.

==Patch changes==
* {{Patch 8.0.1|note=Added.}}
```