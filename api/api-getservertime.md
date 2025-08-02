# API GetServerTime

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the server's [[Wikipedia:Unix_time|Unix time]].
 timestamp = GetServerTime()

==Returns==
:;timestamp:{{apitype|number}} - Time in seconds since the [[Wikipedia:Epoch_(computing)|epoch]].

==Details==
* The server's Unix timestamp is more preferable over {{api|time}}() since it's guaranteed to be synchronized between clients. The local machine's clock could possibly have been manually changed and might also be off by a few seconds if not recently synced.
* Adjustments to the local system clock while the client is open may result in this function returning incorrect timestamps<ref>https://github.com/Stanzilla/WoWUIBugs/issues/533</ref>.
* Unix time is unrelated to your time zone, making it useful for tracking and sorting timestamps.

==Comparison==
<onlyinclude>When in a EU time zone CEST (UTC+2) and playing on Moon Guard US, CDT (UTC-5). The examples were taken at the same time. Note that <code>time()</code> and <code>date()</code> are tied to your system's clock which can be manually changed.
 -- unix time
 {{api|time}}()                                 -- 1596157547
 {{api|GetServerTime}}()                        -- 1596157549
 
 -- local time, same as `date(nil, time())`
 {{api|date}}()                                 -- "Fri Jul 31 03:05:47 2020"
 
 -- realm time
 {{api|GetGameTime}}()                          -- 20, 4
 {{api|C_DateAndTime.GetCurrentCalendarTime}}() -- hour:20, minute:4
 {{api|C_DateAndTime.GetServerTimeLocal}}()     -- 1596139440 unix time offset by the server's time zone (e.g. UTC minus 5 hours)</onlyinclude>

==Patch changes==
* {{Patch 6.2.0|note=Added.}}

==See also==
* {{api|GetTime}}() - local machine uptime.

==References==
```