# API C DateAndTime.GetServerTimeLocal

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_DateAndTime|system=DateAndTime}}
Returns the server's [[Wikipedia:Unix_time|Unix time]] offset by the server's timezone.
 serverTimeLocal = C_DateAndTime.GetServerTimeLocal()

==Returns==
:;serverTimeLocal:{{apitype|number}} - Time in seconds since the [[Wikipedia:Epoch_(computing)|epoch]], only updates every 60 seconds.

==Comparison==
{{:API_GetServerTime}}

==Patch changes==
* {{Patch 8.1.5|note=Added.}}
```