# API debuglocals

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a string dump of all local variables and upvalues at a given stack level.
 locals = debuglocals([level])

==Arguments==
:;level:{{apitype|number}} - The stack level to inspect. Defaults to 1 (the calling function).

==Returns==
:;locals:{{apitype|string?}} - A string dump of all local variables, temporaries, and upvalues.

==Details==
* {{wow-inline}} This function will return no values if called outside of the execution of the global error handler function.

==Example==
The following snippet demonstrates example output for a variety of values. Note that this snippet may not work as-is if you have an error handling addon installed, as these typically hijack and replace the ability to change the global error handler.

<syntaxhighlight lang="lua">
local Upvalue = "banana"

seterrorhandler(function()
    local Number = 1.23456
    local String = "foo"
    local NamedFrame = { [0] = ChatFrame1[0] }
    local Table = {
        1,
        2,
        foo = "bar",
        {
            "debuglocals should only inspect at-most one level of tables; this shouldn't be printed",
        },
    }
    local Thread = coroutine.create(function() end)
    local Boolean = true
    local Nil = nil
    local Temp = Upvalue

    print(debuglocals())
end)

error("")
</syntaxhighlight>

<pre>
Number = 1.234560
String = "foo"
NamedFrame = ChatFrame1 {
 0 = &lt;userdata&gt;
}
Table = &lt;table&gt; {
 1 = 1
 2 = 2
 3 = &lt;table&gt; {
 }
 foo = "bar"
}
Thread = &lt;no value&gt;
Boolean = true
Nil = nil
Temp = "banana"
(*temporary) = &lt;function&gt; defined @Interface\FrameXML\UIParent.lua:5234
Upvalue = "banana"
</pre>

==Patch changes==
* {{Patch 10.1.0|note=This function will now return no results when called within a <code>__gc</code> finalizer, and may now be called outside of the [[API geterrorhandler|global error handler]].}}
* {{Patch 3.2.0|note=First usage in FrameXML appears.}}
```