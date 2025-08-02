# API C Timer.After

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Schedules a timer.
 C_Timer.After(seconds, callback)

==Arguments==
:;seconds:{{apitype|number}} - Time in seconds before the timer finishes.
:;callback:{{apitype|function,FunctionContainer}} - Callback function to run.
::: <code>function(cb: {{apitype|FunctionContainer}})</code>

==Example==
Prints "Hello" after 2.5 seconds.
<syntaxhighlight lang="lua">
/run C_Timer.After(2.5, function() print("Hello") end)
</syntaxhighlight>
<!-- Repeating timer which calls itself recursively.
<syntaxhighlight lang="lua">
local function bootlegRepeatingTimer()
	print(GetTime())
	C_Timer.After(1, bootlegRepeatingTimer)
end
bootlegRepeatingTimer()
</syntaxhighlight> -->

[https://github.com/Gethe/wow-ui-source/blob/2b92043155e8bd4b66e340b4db99cdca143f1748/Interface/SharedXML/FunctionUtil.lua#L105 RunNextFrame] is a utility function with zero seconds delay.
<syntaxhighlight lang="lua">
-- prints "hello" and then "world"
RunNextFrame(function() print("world") end)
print("hello")
</syntaxhighlight>

==Details==
* With a duration of 0 ms, the earliest the callback will be called is on the next frame.
* Timing accuracy is limited to the frame rate.
* C_Timer.After() is generally more efficient than using an [[Widget_API#Animation|Animation]] or [[UIHANDLER OnUpdate|OnUpdate]] script.
{{Bluepost|poster=Rygarius|date=20140909 16:54|title=[Sticky] 6.0 Add-On Changes|link=https://www.wowhead.com/bluetracker=us.2.1011693?topic=13421662064#136783073307|
body=<p>In most cases, initiating a second C_Timer is still going to be cheaper than using an Animation or OnUpdate. The issue here is that both Animation and OnUpdate calls have overhead that applies every frame while they are active. For OnUpdate, the overhead lies in the extra function call to Lua. For Animations, we’re doing work C-side that allows us to support smoothing, parallel animations, and animation propagation. In contrast, the new C_Timer system uses a standard heap implementation. It’s only doing work when the timer is created or destroyed (and even then, that work is fairly minimal).</p>

<p>The one case where you’re better off not using the new C_Timer system is when you have a ticker with a very short period – something that’s going to fire every couple frames. For example, you have a ticker you want to fire every 0.05 seconds; you’re going to be best served by using an OnUpdate function (where about half the function calls will do something useful and half will just decrement the timer).</p>}}

==Patch changes==
* {{Patch 6.0.2|note=Added.<sup>[https://www.townlong-yak.com/framexml/6.0.2/C_TimerAugment.lua]</sup>}}
```