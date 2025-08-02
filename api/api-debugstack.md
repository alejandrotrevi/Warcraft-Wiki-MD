# API debugstack

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns a string representation of the current calling stack.
 description = debugstack([coroutine,] [start [, count1 [, count2]]])

==Arguments==
:;coroutine:{{apitype|thread?}} - The thread with the stack to examine (default - the calling thread)
:;start:{{apitype|number?}} - the stack depth at which to start the stack trace (default 1 - the function calling debugstack, or the top of coroutine's stack)
:;count1:{{apitype|number?}} - the number of functions to output at the top of the stack (default 12)
:;count2:{{apitype|number?}} - the number of functions to output at the bottom of the stack (default 10)

==Returns==
:;description:{{apitype|string}} - a multi-line string showing what the current call stack looks like
::: If there are more than count1+count2 calls in the stack, they are separated by a "..." line.
::: Long lines may become truncated.
::: The string ends with an extra newline character.

==Details==
This is a modified version of [[Lua]]'s [http://www.lua.org/manual/5.1/manual.html#pdf-debug.traceback debug.traceback()] function.

==Example 1==
Assume the following example file, "file.lua":
<syntaxhighlight lang="lua">
function a()
	error("Boom!"); 
end

function b() a(); end

function c() b(); end

function d() c(); end

function e() d(); end

function f() e(); end

function errhandler(msg)
	print (msg .. "\nCall stack: \n" .. debugstack(2, 3, 2));
end

xpcall(f, errhandler);
</syntaxhighlight>

This would output something along the following:

 file.lua:2: Boom!
 Call stack:
 file.lua:2: in function a
 file.lua:5: in function b
 file.lua:7: in function c
 ...
 file.lua:13: in function f
 file.lua:19

==Example 2==
Combining debugstack with a strmatch can enable you to get the current line of a function call.
<syntaxhighlight lang="lua">
function debugprint(msg)
	local line = strmatch(debugstack(2),":(%d):");
	print("Debug Print on Line "..line.." with message: "..msg);
end

function doSomething()
	debugprint("We tried to do something.");
end
</syntaxhighlight>
This would return the following output from print:
 Debug Print on Line 7 with message: We tried to do something.

==Patch changes==
* {{Patch 10.1.0|note=This function will now return no results when called within a <code>__gc</code> finalizer.}}

<!-- luals
---@param coroutine thread
---@param start number
---@param count1 number
---@param count2 number
---@return string description
---@overload fun(start?: number, count1?: number, count2?: number)
function debugstack(coroutine, start, count1, count2) end
-->
```