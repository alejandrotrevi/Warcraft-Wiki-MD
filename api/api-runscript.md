# API RunScript

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Executes a string of Lua code.
 RunScript(script)

==Arguments==
:;script:{{apitype|string}} - The code which is to be executed.

==Example==
:To define a function dynamically you could do:
<!-- begin code -->
 local retExpr = '"Hello " .. UnitName("target")';
 RunScript("function My_GetGreeting() return " .. retExpr .. ";end");
<!-- end code -->
====Result====
:The My_GetGreeting() function will be defined to return Hello followed by the name of your target.

==Details==
: This function is NOT recommended for general use within addons for a number of reasons:

: 1. It'll do whatever you tell it, that includes calling functions, setting variables, whatever.

: 2. Errors in the script string produce the error popup (at least, they produce the UI_ERROR_MESSAGE event).

: On the other hand, it's invaluable if you need to run code that is input by the player at run-time, or do self-generating code.

==See Also==

* The standard Lua function [[API loadstring]], which can overcome all of the problems of RunScript described above.
```