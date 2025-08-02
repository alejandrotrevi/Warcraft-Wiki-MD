# API GetCraftNumReagents

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
This command tells the caller how many reagents are required for said craft.
 numRequiredReagents = GetCraftNumReagents(index)

==Parameters==
===Arguments===
:;index:Numeric. Number from 1 to X, where X is the total number of possible crafts.

===Returns===
:;numRequiredReagents:Integer. This is the number of required reagents for said craft. ie, 4 (for any craft that requires 4 reagents to perform...)

==Patch changes==
* {{Patch 3.0.2|note=Removed.}}
```