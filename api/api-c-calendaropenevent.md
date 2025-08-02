# API C Calendar.OpenEvent

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Establishes an event for future calendar API calls
 success = C_Calendar.OpenEvent(offsetMonths, monthDay, index)

==Arguments==
:;offsetMonths:{{apitype|number}} - The number of months to offset from today.
:;monthDay:{{apitype|number}} - The day of the month on which the desired event is scheduled (1 - 31).
:;index:{{apitype|number}} - Ranging from 1 through {{api|C_Calendar.GetNumDayEvents}}(offsetMonths, monthDay).

==Returns==
:;success:{{apitype|boolean}}

==Patch changes==
* {{Patch 8.1.5|note=Added <code>success</code> return.}}
* {{Patch 8.0.1|note=Moved to <code>C_Calendar.OpenEvent()</code>}}
* {{Patch 3.0.2|note=Added as <code>CalendarOpenEvent()</code>}}
```