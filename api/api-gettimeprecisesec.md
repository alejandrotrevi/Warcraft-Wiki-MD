# API GetTimePreciseSec

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} 
Returns a monotonic timestamp in seconds, with millisecond precision.
 seconds = GetTimePreciseSec()

==Returns==
:;seconds:{{apitype|number}} - The number of seconds that have elapsed since this timer was started.

==Details==
* The first call to this function will always return zero. Subsequent calls will return the number of seconds that have elapsed since the first call until the client is restarted.
* Unlike {{api|GetTime}}(), the value returned by this function is not cached once per frame and may change on each call.

==Example==
<syntaxhighlight lang="lua">
print("Start time:", GetTimePreciseSec());

for _ = 1, 2^26 do
    -- Busy loop to make some time pass.
end

print("End time:", GetTimePreciseSec());

> "Start time:", 0
> "End time:", 0.3624231
</syntaxhighlight>

==See also==
* {{api|GetTime()}}
```