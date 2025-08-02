# API SetConsoleKey

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Sets the console key (normally ~).
 SetConsoleKey(key)

==Arguments==
:;key:{{apitype|string}} - The character to bind to opening the console overlay, or <code>nil</code> to disable the console binding.

==Details==
* The [[console]] is only accessible when WoW is started with the "-console" parameter. This function does nothing if the parameter wasn't used.
* The console key is not saved by the WoW client, and will revert to the default {{keypress|`}} (backtick) key when WoW is restarted.
* Unlike the {{api|SetBinding}} function, you can ''only'' provide the values of keys that represent standard ASCII characters; no modifiers are allowed.  For instance, <code>SetConsoleKey("CTRL-F")</code> won't work, but <code>SetConsoleKey("F")</code> will.  In addition, non-alphabetic keys that require modifiers to access, such as <code>"!"</code> using {{keypress|Shift|1}}, cannot be used.
* The console key overrides all other key bindings in WoW, regardless of context. This means that if you set it to {{keypress|F}}, you'll be unable to type the F character in chat until you restart WoW.
```