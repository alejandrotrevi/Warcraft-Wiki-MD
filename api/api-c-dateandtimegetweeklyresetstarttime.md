# API C DateAndTime.GetWeeklyResetStartTime

**Contributor:** LootFever

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DateAndTime|system=DateAndTime}}
Returns the unix timestamp of the last weekly reset.
 seconds = C_DateAndTime.GetWeeklyResetStartTime()

==Returns==
:;seconds:{{apitype|time_t}}

==Example==
  /dump C_DateAndTime.GetWeeklyResetStartTime()
  Dump: value=C_DateAndTime.GetWeeklyResetStartTime() 
  [1]=1723608000 

  1723608000 translates to 2024-08-14 04:00 GMT (last reset on EU as of writing this)
```