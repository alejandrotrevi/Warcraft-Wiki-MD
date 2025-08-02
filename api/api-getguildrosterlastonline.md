# API GetGuildRosterLastOnline

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns time since the guild member was last online.
 yearsOffline, monthsOffline, daysOffline, hoursOffline = GetGuildRosterLastOnline(index)

==Arguments==
:;index:{{apitype|number}} - index of the guild roster entry you wish to query.

==Returns==
:;yearsOffline:{{apitype|number}} - number of years since the member was last online. May return nil.
:;monthsOffline:{{apitype|number}} - number of months since the member was last online. May return nil.
:;daysOffline:{{apitype|number}} - number of days since the member was last online. May return nil.
:;hoursOffline:{{apitype|number}} - number of hours since the member was last online. May return nil.

==Example==
Displays a message with the name of the person in your guild who has been offline the longest. Note that this requires an updated guild list showing offline members (open Social tab, click "Show offline members").
<syntaxhighlight lang="lua">
local i, tmax, tname, years, months, days, hours, toff = 1, 0, "placeholder";
while (GetGuildRosterInfo(i) ~= nil) do
    years, months, days, hours = GetGuildRosterLastOnline(i);
    years, months, days, hours = years and years or 0, months and months or 0, days and days or 0, hours and hours or 0;
    toff = (((years*12)+months)*30.5+days)*24+hours;
    if (toff > tmax) then
        tname = GetGuildRosterInfo(i);
        tmax = toff;
    end
    i = i + 1;
end

message("Been offline the longest: " .. tname .. " (~" .. tmax .. " hours)");
</syntaxhighlight>
```