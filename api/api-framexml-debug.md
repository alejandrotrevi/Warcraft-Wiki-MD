# API FrameXML Debug

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{deprecatedapi|patch=10.2.6|removed=11.0.2}}
Queries or sets the FrameXML debug logging flag.
 enabled = FrameXML_Debug([enabled])

==Arguments==
:;enabled:{{apitype|number?}} - <code>0</code> to disable debug logging, or <code>1</code> to enable it. If not specified, the logging flag will not be modified.

==Returns==
:;enabled:{{apitype|number}} - The applied logging flag value.

==Details==
* When FrameXML debugging is enabled extensive information about the load process is written to <code>World of Warcraft/.../Logs/FrameXML.log</code> and <code>GlueXML.log</code>. This information includes addon and file load order, as well as the names of all created frames and templates.

==Patch changes==
* {{Patch 1.0.0|note=Added.}}
```