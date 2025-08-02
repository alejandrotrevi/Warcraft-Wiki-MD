# API GetMouseFocus

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}}
Returns the frame that currently has mouse focus.
 frame = GetMouseFocus()

==Returns==
:;frame:{{apitype|Frame}} - The frame that currently has the mouse focus.

==Details==
* The frame must have enableMouse="true"

==Example==
You can get the name of the mouse-enabled frame beneath the pointer with this:
<syntaxhighlight lang="lua">
/dump GetMouseFocus():GetName() -- WorldFrame
</syntaxhighlight>
```