# API C LFGList.GetSearchResults

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGList|system=LFGList}}
Returns a table of search result IDs.
 totalResultsFound, results = C_LFGList.GetSearchResults()

==Returns==
:;totalResultsFound:{{apitype|number?|default=0}} - Total number of IDs inside <code>results</code>
:;results:{{apitype|number[]}} - Table of resultIDs

==Patch changes==
* {{Patch 6.0.2|note=Added.}}
```