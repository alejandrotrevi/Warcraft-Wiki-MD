# API C Calendar.EventGetStatusOptions

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_Calendar|system=Calendar}}
Needs summary.
 options = C_Calendar.EventGetStatusOptions(eventIndex)

==Arguments==
:;eventIndex:{{apitype|number}}

==Returns==
:;options:{{apitype|CalendarEventStatusOption[]}}
{| class="sortable darktable zebra" style="margin-left: 3.9em"
! Field !! Type !! Description
|-
| status || {{apitype|Enum.CalendarStatus}} || 
|-
| statusString || {{apitype|string}} || 
|}

{{:Enum.CalendarStatus}}

==Patch changes==
* {{Patch 9.0.1|note=Added <code>status</code> field.}}
* {{Patch 8.0.1|note=Added.}}
```