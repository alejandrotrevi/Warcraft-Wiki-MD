# API GetMouseFoci

**Contributor:** Meorawr

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi|t=a|system=Input}}
Returns the frames that currently have mouse focus.
 regions = GetMouseFoci()

==Returns==
:;regions:{{apitype|ScriptRegion[]}}

==Details==
* For the common case of simply testing if a region has mouse focus, consider using {{api|t=w|ScriptRegion:IsMouseMotionFocus()}}.
* The returned table will contain multiple regions in the case where objects at the top of the stack are configured for mouse input propagation.
* The order of results in the table is such that the topmost region will be at index 1, and the bottommost region will be at the last index in the table.
* This function can return an empty table in cases where the mouse is off-screen, or is over the WorldFrame without first enabling it for mouse motion events.

==Example==
Dumps the top most region under the cursor.
<syntaxhighlight lang="lua">
/dump GetMouseFoci()[1]
</syntaxhighlight>

==See also==
* {{api|t=w|ScriptRegion:SetPropagateMouseClicks}}
* {{api|t=w|ScriptRegion:SetPropagateMouseMotion}}
```