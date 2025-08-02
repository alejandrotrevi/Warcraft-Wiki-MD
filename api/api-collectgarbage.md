# API collectgarbage

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Control the garbage collector and query it for information. As of WoW 2.0, this is the same as the standard collectgarbage() in Lua, but prior to that it was quite different.
 collectgarbage([opt [, arg]])

==Arguments==
:;opt:{{apitype|string}} - This function is a generic interface to the garbage collector. It performs different functions according to its first argument:
:* "collect": performs a full garbage-collection cycle.  This is the default action if '''opt''' is not specified.
:* "stop": stops the garbage collector.
:* "restart": restarts the garbage collector.
:* "count": returns the total memory in use by Lua (in Kbytes).
:* "step": performs a garbage-collection step. The step "size" is controlled by arg (larger values mean more steps) in a non-specified way. If you want to control the step size you must experimentally tune the value of arg. Returns true if the step finished a collection cycle.
:* "setpause": sets arg/100 as the new value for the pause of the collector (see §2.10).
:* "setstepmul": sets arg/100 as the new value for the step multiplier of the collector (see §2.10).
:;arg:{{apitype|number}} - used as an argument for the "step", "setpause" and "setstepmul" calls.

==Example==
The following snippet forces a garbage collection pass and displays how much memory was reclaimed:
 local preGC = collectgarbage("count")
 collectgarbage("collect")
 print("Collected " .. (preGC-collectgarbage("count")) .. " kB of garbage");
```