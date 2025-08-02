# API CameraOrSelectOrMoveStop

**Contributor:** Ketho

## Content

The following content is in MediaWiki markdown format:

```mediawiki
{{wowapi}} {{restrictedapi|protected}}
Called when you release the "Left-Click" mouse button.
 CameraOrSelectOrMoveStop([stickyFlag])

==Arguments==
:;stickyFlag:{{apitype|boolean?}} - If present and set then any camera offset is 'sticky' and remains until explicitly cancelled.

==Details==
* This function is called when left clicking in the 3-D world.
* When used alone, can cancel a "mouselook" started by a call to [[API CameraOrSelectOrMoveStart|CameraOrSelectOrMoveStart]].
* IMPORTANT: The normal restrictions regarding hardware event initiations still apply to anything this function might do.

==Patch changes==
* {{Patch 2.0.1|note=Protected.}}
* {{Patch 1.10.0|note=Requires a hardware event.}}
```