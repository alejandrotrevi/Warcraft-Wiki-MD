# API newproxy

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} __NOTOC__

Creates a zero-size "userdata" object, optionally with a sharable empty metatable.
 proxy = newproxy(withmetatable)
       = newproxy(otherproxy)

==Arguments==
:;withmetatable : {{apitype|boolean}} - Whether or not to to create a metatable for the userdata.
:;otherproxy : {{apitype|userdata}} - If an object previously created by newproxy is passed, the new userdata will share that proxy's metatable.

==Returns==

:;proxy : {{apitype|userdata}} - A userdata proxy object.

==Details==
* This function is an undocumented part of the Lua 5.1 standard library<ref>http://lua-users.org/lists/lua-l/2003-01/msg00205.html</ref>.
* This function is used by the [[SecureHandlers|Secure Handlers]] framework as a way of providing handles to frames within the restricted environment.
* Objects created by this function can have a metatable with a <code>__gc</code> method installed to dispatch a function when the object is garbage collected.
** When using finalizers it is strongly recommended to use a protected call barrier as any errors that escape a finalizer may crash the client.

<syntaxhighlight lang="lua">
local function OnObjectCollected_Protected()
    error("Collected!")
end

local function OnObjectCollected()
    -- All errors within 'OnObjectCollected_Protected' will be forwarded
    -- to the global error handler and will avoid crashing the client.
    securecallfunction(OnObjectCollected_Protected)
end

local object = newproxy(true)
getmetatable(object).__gc = OnObjectCollected
</syntaxhighlight>

==Patch changes==
* {{Patch 10.1.0|note=<code>__gc</code> finalizers will no longer spread taint back to any calling code that triggered the collection of an object.}}

==References==
{{Reflist}}
```