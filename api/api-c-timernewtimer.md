# API C Timer.NewTimer

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Schedules a (repeating) timer that can be canceled.
 cbObject = C_Timer.NewTimer (seconds, callback)
          = C_Timer.NewTicker(seconds, callback [, iterations])

==Arguments==
:;seconds:{{apitype|number}} - Time in seconds between each iteration.
:;callback:{{apitype|function,FunctionContainer}} - Callback function to run. It will be supplied a view of the timer handle (<code>cbObject</code>) when invoked. The handle returned from the function and the one supplied to the callback are distinct objects that both reference a shared state.
::: <code>function(cb: {{apitype|FunctionContainer}})</code>
:;iterations:{{apitype|number?}} - Number of times to repeat, or indefinite if omitted.

==Returns==
:;cbObject:{{apitype|FunctionContainer}} - Timer handle with <code>:Cancel()</code>, <code>:IsCancelled()</code> and <code>:Invoke()</code> methods.

==Details==
* '''C_Timer.NewTimer''' has just a single iteration and is essentially the same as <code>C_Timer.NewTicker(duration, callback, 1)</code>
* Errors thrown inside a callback function will not halt the ticker.

==Example==
Schedules a repeating timer which runs 4 times.
<syntaxhighlight lang="lua">
/run C_Timer.NewTicker(2.5, function() print(GetTime()) end, 4)
</syntaxhighlight>

Schedules a timer but cancels it right away.
<syntaxhighlight lang="lua">
local myTimer = C_Timer.NewTimer(3, function() print("Hello") end)
print(myTimer:IsCancelled()) -- false
myTimer:Cancel()
print(myTimer:IsCancelled()) -- true
</syntaxhighlight>

===Detailed examples===
Schedules a timer that prints a value written to a field stored on the timer handle itself. Timer handles all reference the same shared state internally, so user-defined fields written to handles can be used to supply additional data for use by the callback.
<syntaxhighlight lang="lua">
local myTimer = C_Timer.NewTimer(2.5, function(self) print("self.data is:", self.data) end)
myTimer.data = GetTime()
</syntaxhighlight>

Schedules a repeating timer which runs 4 times and prints the timer handle returned from the function and supplied to the callback. Note that each print will result in a different object address being displayed, indicating the timer handles have a distinct identity.
<syntaxhighlight lang="lua">
/run print(C_Timer.NewTicker(0.25, function(self) print(self) end, 4))
</syntaxhighlight>

Another example to illustrate that the handles are distinct objects that both reference a shared state.
<syntaxhighlight lang="lua">
local cb = C_FunctionContainers.CreateCallback(nop)
cb.foo = "bar"
local timer = C_Timer.NewTimer(2, cb)

print(cb)          -- userdata: 000001A9D4C66010
print(timer)       -- userdata: 000001A9D4C66050
print(timer == cb) -- true
print(timer.foo)   -- bar
</syntaxhighlight>

==Patch changes==
* {{Patch 10.0.0|note=Implementation moved to native code. APIs no longer accept non-function callback arguments, and now return userdata handles.}}
<!-- {{Patch 7.3.5|note=Added <code>handle:IsCancelled()</code><sup>[https://www.townlong-yak.com/framexml/25864/C_TimerAugment.lua/diff]</sup>}} 
* {{Patch 6.0.2|note=Added.<sup>[https://www.townlong-yak.com/framexml/6.0.2/C_TimerAugment.lua]</sup>}} -->

==See also==
* [https://www.wowace.com/projects/ace3/pages/api/ace-timer-3-0 AceTimer-3.0]
* [[UIHANDLER_OnUpdate|OnUpdate]]
```