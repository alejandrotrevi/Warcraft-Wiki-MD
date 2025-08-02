# API C LFGList.Search

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_LFGList|system=LFGList}}  {{restrictedapi|hwevent}}
Needs summary.
 C_LFGList.Search(categoryID [, filter [, preferredFilters [, languageFilter [, searchCrossFactionListings [, advancedFilter [, activityIDsFilter]]]]]])

==Arguments==
:;categoryID:{{apitype|number}}
:;filter:{{apitype|Enum.LFGListFilter?|default=0}} - Bitmask of one or more filter enum values.
{{:Enum.LFGListFilter|nocaption=1}}
:;preferredFilters:{{apitype|number?|default=0}}
:;languageFilter:{{apitype|WowLocale?}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| {{apiname|enUS}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|koKR}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|frFR}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|deDE}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|zhCN}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|zhTW}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|esES}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|esMX}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|ruRU}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|ptBR}} || {{apitype|boolean?|default=false}} || 
|-
| {{apiname|itIT}} || {{apitype|boolean?|default=false}} || 
|}
:;searchCrossFactionListings:{{apitype|boolean?|default=false}}
:;advancedFilter:{{apitype|AdvancedFilterOptions?}}
{{:Struct AdvancedFilterOptions|nocaption=1}}
:;activityIDsFilter:{{apitype|number[]?}} - Activity IDs to filter by.

==Patch changes==
* {{Patch 11.0.7|note=Added <code>activityIDsFilter</code> argument.}}
* {{Patch 9.2.5|note=Added <code>searchCrossFactionListings</code> argument.}}
* {{Patch 7.2.0|note=Hardware event protected<ref>https://us.battle.net/forums/en/wow/topic/20754326419</ref>.}}
* {{Patch 6.0.2|note=Added.}}

==References==
```