# API CreateWindow

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=FrameScript}}
Needs summary.
 window = CreateWindow([popupStyle [, topMost]])

==Arguments==
:;popupStyle:{{apitype|boolean?|default=true}}
:;topMost:{{apitype|boolean?|default=false}}

==Returns==
:;window:{{apitype|SimpleWindow?}}

==Details==
* This function is disabled in public clients and will always return nil.

==Patch changes==
* {{Patch 11.1.0|note=Added <code>topMost</code> argument.}}
```