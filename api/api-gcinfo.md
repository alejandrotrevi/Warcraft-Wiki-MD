# API gcinfo

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the amount of memory in use by Lua (in kilobytes).
 memoryInUse = gcinfo()

==Returns==
:;memoryInUse:{{apitype|number}} - The amount of memory in use (in kilobytes).

==Details==
* This function is deprecated, use <code>{{api|collectgarbage}}("count")</code> instead.
```