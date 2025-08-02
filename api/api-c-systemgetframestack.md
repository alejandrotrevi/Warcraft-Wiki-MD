# API C System.GetFrameStack

**Contributor:** KethoBot

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|namespace=C_System|system=SystemInfo}}
Returns an array of all UI objects under the mouse cursor, as would be exposed through the frame stack tooltip. The returned table is ordered from highest object level to lowest.
 objects = C_System.GetFrameStack()

==Returns==
:;objects:{{apitype|ScriptRegion[]}}

==Patch changes==
* {{Patch 9.0.1|note=Added.}}
```